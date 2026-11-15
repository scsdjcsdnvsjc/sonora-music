# Sonora — reproductor musical personal

Aplicación web local-first para reunir archivos propios y catálogos musicales gratuitos con APIs oficiales.

## Incluye
- Importación de archivos de audio al almacenamiento local del navegador (IndexedDB).
- Biblioteca, búsqueda local, vistas por artista y álbum.
- Favoritos, playlists, historial, reproducción aleatoria, repetición y cola básica.
- Búsqueda en Audius e Internet Archive.
- Búsqueda en Jamendo mediante API oficial y Client ID propio.
- Diseño adaptable a escritorio y móvil.

## Ejecutar en macOS
1. Descomprime `sonora-personal.zip`.
2. Abre Terminal y entra en la carpeta:
   ```bash
   cd ruta/a/sonora-personal
   ```
3. Inicia un servidor local:
   ```bash
   python3 -m http.server 8080
   ```
4. Abre `http://localhost:8080` en Chrome, Edge o Safari.

No abras `index.html` directamente con `file://`: las APIs del navegador y el almacenamiento pueden tener restricciones.

## Jamendo
1. Registra una aplicación en https://developer.jamendo.com/
2. Copia el Client ID.
3. En Sonora, abre Ajustes (⚙) e introdúcelo.
4. Ve a Buscar y elige Jamendo o Todo.

## Fuentes y derechos
- Los archivos locales deben ser tuyos o estar autorizados para su uso.
- Jamendo: respeta la licencia de cada canción.
- Audius: respeta los términos y permisos del creador.
- Internet Archive: disponibilidad pública no equivale automáticamente a dominio público. Comprueba los derechos de cada grabación.
- La aplicación no elimina DRM, no descarga catálogos comerciales ni evita anuncios o suscripciones.

## Datos
Las pistas locales se guardan en IndexedDB dentro del navegador. Playlists, favoritos e historial se guardan en localStorage. El botón Ajustes permite exportar los metadatos JSON. La app no sube tu biblioteca a ningún servidor.

## Limitaciones de esta primera versión
- Los metadatos de archivos locales se infieren del nombre del archivo; para etiquetas ID3 completas, organiza primero tu colección con MusicBrainz Picard.
- Para conservar el acceso a archivos locales, importa la música en el mismo navegador y perfil.
- El catálogo externo depende de la disponibilidad y condiciones de las APIs.
- La app es una aplicación web instalable, no un binario nativo firmado de macOS.
