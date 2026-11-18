# Agenda del día — versión PWA

## Archivos
- `index.html`: aplicación web adaptada para PWA.
- `manifest.webmanifest`: nombre, apariencia e iconos de instalación.
- `sw.js`: caché básica para abrir la aplicación cuando no haya conexión.
- `icons/`: iconos para Android y iPhone.
- `Agenda del día - original.html`: respaldo intacto del HTML recibido.

## Publicar con GitHub Pages
1. Crea un repositorio en GitHub.
2. Sube todos los archivos y la carpeta `icons` manteniendo esta estructura.
3. En Settings → Pages, elige Deploy from a branch, rama `main`, carpeta `/ (root)`.
4. Abre la URL HTTPS que te proporcione GitHub Pages.
5. En Android, abre la URL con Chrome y usa Instalar aplicación / Añadir a pantalla de inicio.
6. En iPhone, abre la URL con Safari → Compartir → Añadir a pantalla de inicio.

## Notas importantes
- Los datos existentes se guardan en el almacenamiento local del navegador (`localStorage` e IndexedDB). Eso significa que cada dispositivo/navegador tendrá sus propios datos: no se sincronizan automáticamente entre computadora, Android y iPhone.
- El modo sin conexión permite abrir la aplicación después de la primera carga, pero las funciones que dependen de recursos externos pueden necesitar internet.
- La generación de PDF carga jsPDF desde una CDN, por lo que requiere conexión a internet.
- La aplicación original utiliza almacenamiento local; antes de usarla como sistema de producción conviene configurar copias de seguridad y sincronización en la nube si necesitas compartir los mismos pacientes/citas entre varios dispositivos.
