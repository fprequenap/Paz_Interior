# Guía para la Paz Interior

**Programa anual de restauración de la armonía entre alma y cuerpo**

*Francisco de Paula Requena Paredes · AMDG*

---

## Qué es

Aplicación web progresiva (PWA) basada en la teoría de las 7 fatigas emocionales: soberbia, envidia, ira, pereza, avaricia, gula y lujuria. Cada fatiga es un anhelo legítimo del alma que se ha desvirtuado. La app proporciona un programa diario de 365 días que combina contemplación, acción concreta y música clásica para restaurar el equilibrio interior.

## Funcionalidades

- **Contenido diario** — Contemplación + 3 acciones + pieza musical asignada por fatiga
- **Test de 70 preguntas** — 10 por fatiga, escala 1-5, resultados inmediatos
- **Panel de instrumentos** — 7 tacómetros SVG estilo aviación con 4 zonas (virtud, leve, moderada, alta)
- **Rosa de los vientos** — Visualización vectorial de la deriva emocional combinada
- **Calendario anual** — 12 meses navegables con indicador de entradas de diario
- **Repertorio musical** — 56 piezas de música clásica (8 por fatiga) con enlace directo a Spotify y Apple Music
- **Alarma diaria** — Recordatorio configurable con vista previa de notificación
- **Diario personal** — Reflexión diaria con almacenamiento local
- **Teoría** — Explicación de las 7 fatigas, anhelos, virtudes y sistema de medición

## Idiomas

Español · English · Français · Português · Italiano · Deutsch

Detección automática del idioma del dispositivo. Selector manual con banderas en la pantalla principal. La preferencia se guarda localmente.

## Instalación en el móvil

1. Abre la URL en el navegador del móvil
2. **Android (Chrome):** Menú ⋮ → "Añadir a pantalla de inicio"
3. **iPhone (Safari):** Compartir ↑ → "Añadir a pantalla de inicio"
4. La app aparece como icono independiente y funciona offline

## Despliegue en GitHub Pages

**Tiempo: 10 minutos. Coste: 0 €.**

### 1. Crear repositorio
- https://github.com/new
- Nombre: `paz-interior`
- Visibilidad: Público

### 2. Subir archivos
- Clic en "uploading an existing file"
- Arrastrar todo el contenido de esta carpeta:
  - `index.html`
  - `manifest.json`
  - `sw.js`
  - `apple-touch-icon.png`
  - `README.md`
  - Carpeta `icons/` (8 archivos PNG)
- Commit changes

### 3. Activar Pages
- Settings → Pages
- Source: Deploy from a branch
- Branch: `main` / `/ (root)`
- Save

### 4. URL resultante
```
https://TU-USUARIO.github.io/paz-interior/
```

Operativa en 1-2 minutos tras activar Pages.

## Arquitectura técnica

| Componente | Detalle |
|---|---|
| Tipo | PWA (Progressive Web App) |
| Código | HTML + CSS + JavaScript vanilla, un solo archivo |
| Dependencias externas | Ninguna |
| Tamaño total | ~850 KB (incluidos 8 tamaños de icono) |
| Almacenamiento | localStorage del navegador |
| Servidor | Ninguno (estático) |
| Telemetría | Ninguna |
| Modo oscuro | Automático vía `prefers-color-scheme` |
| Service Worker | Cache-first, offline completo tras primera carga |

## Privacidad

La aplicación no recoge, transmite ni almacena datos en ningún servidor. Todos los datos del usuario (idioma, resultados del test, diario, preferencia musical) se guardan exclusivamente en el `localStorage` del navegador del dispositivo. No hay cookies, analytics, ni conexiones a terceros. Los enlaces a Spotify y Apple Music se abren en una nueva pestaña sin enviar datos del usuario.

## Actualización

1. Modificar los archivos necesarios
2. Subir al repositorio de GitHub
3. Cambiar la versión del cache en `sw.js` (línea 1: `'paz-interior-v3'`)
4. GitHub Pages despliega automáticamente en 1-2 minutos
5. Los usuarios reciben la actualización en su siguiente visita

## Estructura de archivos

```
├── index.html              App completa (62 KB)
├── manifest.json           Configuración PWA
├── sw.js                   Service Worker (offline)
├── apple-touch-icon.png    Icono iOS (192×192)
├── README.md               Este archivo
└── icons/
    ├── icon-72.png
    ├── icon-96.png
    ├── icon-128.png
    ├── icon-144.png
    ├── icon-152.png
    ├── icon-192.png
    ├── icon-384.png
    └── icon-512.png
```

## Licencia

© Francisco de Paula Requena Paredes. Todos los derechos reservados.

El contenido textual (contemplaciones, acciones, preguntas del test, teoría de las 7 fatigas) es propiedad intelectual del autor. El código fuente de la aplicación puede reutilizarse con atribución.
