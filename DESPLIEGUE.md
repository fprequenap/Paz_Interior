# Despliegue en GitHub Pages — Guía Paso a Paso

## Tiempo estimado: 10 minutos

### Paso 1 — Crear repositorio en GitHub
1. Entra en https://github.com/new
2. Nombre: `paz-interior` (o el que prefieras)
3. Público (necesario para GitHub Pages gratuito)
4. Clic en "Create repository"

### Paso 2 — Subir archivos
1. En la página del repositorio vacío, clic en "uploading an existing file"
2. Arrastra TODO el contenido de la carpeta `pwa/`:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `apple-touch-icon.png`
   - Carpeta `icons/` (con los 8 archivos .png)
3. Clic en "Commit changes"

### Paso 3 — Activar GitHub Pages
1. Settings → Pages (menú lateral izquierdo)
2. Source: "Deploy from a branch"
3. Branch: `main` / `/ (root)`
4. Clic en "Save"
5. Espera 1-2 minutos

### Paso 4 — Tu URL
Tu app estará en:
```
https://TU-USUARIO.github.io/paz-interior/
```

## Resultado

Los usuarios:
1. Abren la URL en su navegador móvil
2. El navegador les sugiere "Añadir a pantalla de inicio"
3. La app aparece con el icono del guerrero (2 Tim 4:7)
4. Funciona offline tras la primera carga
5. Se abre a pantalla completa, como una app nativa

## Datos almacenados localmente

- Idioma seleccionado
- Plataforma musical (Spotify/Apple)
- Resultados del test
- Entradas del diario

Todo en localStorage del navegador. Sin servidor, sin cookies, sin rastreo.

## Actualización

Para actualizar la app, simplemente sube los archivos modificados al repositorio.
GitHub Pages los despliega automáticamente en 1-2 minutos.
Cambia la versión en `sw.js` (línea 1: `paz-interior-v3`) para forzar
que los usuarios reciban la nueva versión.
