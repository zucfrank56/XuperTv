# XuperTV · Adaptación web para VIDAA

Esta carpeta contiene una reconstrucción web inicial de la interfaz Roku XuperTV v6 para navegadores/entornos web de televisores Hisense VIDAA.

## Publicar en GitHub Pages
1. Crea un repositorio GitHub.
2. Sube **todo el contenido** de esta carpeta a la raíz del repositorio.
3. En GitHub abre **Settings → Pages**.
4. En *Build and deployment*, elige **Deploy from a branch**, selecciona `main` y `/ (root)`.
5. Guarda y abre la URL HTTPS que GitHub Pages genere.

## Compatibilidad y limitaciones que debes conocer
- La interfaz está hecha con HTML/CSS/JavaScript y navegación por teclado/mando (flechas, OK/Enter y Atrás/Escape).
- Implementa el flujo Xtream Codes para categorías, canales en vivo, VOD, series, episodios, búsqueda y reproducción HTML5.
- Se conserva la configuración local, favoritos e historial mediante `localStorage`.
- El protocolo Portal/MAC Stalker requiere una pasarela/proxy HTTPS que gestione CORS, cookies y cabeceras de portal. El navegador VIDAA no permite replicar todas las cabeceras de dispositivo de Roku de forma fiable.
- La fuente privada de cuenta XuperTV del paquete Roku depende de un kit cifrado y operaciones de backend no públicas. No se han publicado claves, tokens ni ese material privado en el código web. Para portarla se necesita una API web autorizada del servicio.
- GitHub Pages solo aloja archivos estáticos: no es un backend/proxy. Si el proveedor bloquea CORS, hará falta un backend propio HTTPS configurado por ti.
- La reproducción depende del navegador VIDAA, del modelo/año del televisor, códecs, contenedor, HLS/DASH y políticas DRM. No se puede garantizar compatibilidad del 100% de streams solo desde el código.
- No incluyas credenciales reales en archivos públicos de GitHub. La app guarda los datos introducidos localmente en el televisor.

## Estructura
- `index.html`: aplicación y pantallas.
- `styles.css`: interfaz y diseño adaptable.
- `app.js`: navegación, almacenamiento, conexión Xtream, catálogo y reproductor.
- `images/`: recursos gráficos originales incluidos en el ZIP de Roku.
