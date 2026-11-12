# Aura Music Signature — GitHub Pages

PWA de reproductor musical personal. Preparada para publicarse en un repositorio GitHub Pages bajo `https://USUARIO.github.io/REPOSITORIO/`.

## Publicar desde Android o computadora

1. Crea un repositorio público llamado `aura-music`.
2. Sube **el contenido de esta carpeta directamente a la raíz** del repositorio. `index.html` debe quedar en la raíz, no dentro de otra carpeta.
3. En GitHub abre **Settings → Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/ (root)`, luego pulsa **Save**.
6. Espera a que GitHub Pages publique el sitio. La URL tendrá la forma `https://TU-USUARIO.github.io/aura-music/`.
7. Abre esa URL en Chrome Android, carga la página una vez y usa el menú ⋮ → **Instalar aplicación** o **Añadir a pantalla de inicio**.

## Actualizaciones

Sube los archivos nuevos a la misma raíz y confirma los cambios. El service worker usa una versión de caché nueva para reemplazar los archivos anteriores. Si ves una versión vieja, cierra la PWA y vuelve a abrirla con conexión.

## Datos y biblioteca

La biblioteca se guarda en IndexedDB del navegador y queda asociada al origen. Cambiar de Netlify a GitHub Pages significa cambiar de origen: exporta un respaldo en Aura Music antes de migrar. No borres los datos del sitio antiguo hasta verificar que la copia se restauró en el nuevo.

## Limitaciones conocidas

- La lectura automática de etiquetas ID3 se implementa para MP3; la compatibilidad de portadas depende de los metadatos y del formato del archivo.
- El navegador puede bloquear el inicio automático del audio tras una recarga; la app puede restaurar la canción y el punto de reproducción, pero quizá debas pulsar Play.
- La API de ecualización depende del soporte del navegador.
- GitHub Pages aloja archivos estáticos; no convierte por sí solo la PWA en APK.
