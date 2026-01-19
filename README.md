# Devolveme Landing Page

Esta carpeta contiene el sitio web estático para el sistema de recuperación de objetos "Devolveme".

## Estructura

- `index.html`: El código fuente completo (HTML, CSS, JS).
- `_redirects`: Archivo de configuración para Cloudflare Pages (Manejo de rutas `/f/*`).
- `logo.png`: (Debe ser agregado) El logo de la marca.

## Despliegue en Cloudflare Pages

1.  **Subir al Repositorio**: Asegúrate de que esta carpeta (`landing-page`) esté en tu repositorio de GitHub/GitLab.
2.  **Crear Proyecto en Cloudflare**:
    *   Ve al Dashboard de Cloudflare -> Pages.
    *   "Connect to Git".
    *   Selecciona el repositorio.
3.  **Configuración de Build**:
    *   **Project Name**: devolveme-landing (o el que gustes).
    *   **Production Branch**: main.
    *   **Framework Preset**: None (Es HTML estático).
    *   **Build Command**: (Dejar vacío).
    *   **Build Output Directory**: `landing-page` (IMPORTANTE: Indica la carpeta donde están estos archivos).
4.  **Deploy**: Haz clic en "Save and Deploy".

## Funcionamiento

El sitio detecta automáticamente URLs con el formato `https://devolveme.lat/f/{CODIGO}`.
- Extrae el `{CODIGO}`.
- Genera enlaces dinámicos a WhatsApp, Telegram y Email incluyendo ese código.

## Personalización

Para cambiar textos, colores o números de teléfono, edita directamente el archivo `index.html`.
