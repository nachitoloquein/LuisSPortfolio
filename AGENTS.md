# FolioOne

## Descripción

FolioOne es un portfolio personal estático para Luis Sallorenzo, docente de conducción. El sitio presenta su perfil, trayectoria, servicios de formación vial y material relacionado con simulación y conducción profesional.

## Estructura

- `index.html`: portada y presentación principal.
- `about.html`: perfil, enfoque pedagógico y áreas de formación.
- `resume.html`: trayectoria profesional.
- `services.html`: servicios de docencia y acompañamiento, si se incorpora nuevamente al sitio.
- `portfolio.html`: experiencias y recursos.
- `assets/css/main.css`: estilos principales.
- `assets/js/main.js`: comportamiento e interacciones del sitio.
- `assets/img/`: imágenes del perfil, portfolio y recursos visuales.
- `files/CV/`: documentos descargables, como el currículum.

## Convenciones de contenido

- El idioma visible del sitio es español; conservar `lang="es"` en las páginas.
- Usar una voz cercana, profesional y concreta, vinculada a la seguridad vial y la formación de conductores.
- No inventar años de experiencia, cifras de alumnos, certificaciones, testimonios ni instituciones. Si falta un dato, dejar un texto general o solicitarlo.
- Evitar texto de plantilla, Lorem ipsum, nombres de ejemplo y etiquetas de tecnología que no correspondan al trabajo de Luis.
- Mantener navegación, enlaces a documentos y rutas de imágenes existentes salvo que el cambio lo requiera.

## Desarrollo y validación

No hay framework ni dependencias de build: es un sitio HTML/CSS/JavaScript estático. Para revisarlo localmente, servir la carpeta raíz con cualquier servidor HTTP estático y abrir `index.html`; no usar `file://` si se necesitan rutas o scripts.

Antes de entregar cambios:

1. Verificar que los enlaces internos y las rutas de imágenes funcionen.
2. Buscar texto de relleno (`Lorem`, `ipsum`, nombres de ejemplo) en los HTML.
3. Comprobar que la portada y las páginas modificadas sean legibles en móvil y escritorio.
4. Ejecutar `git diff --check`.

## Despliegue

El destino de producción es Vercel. El proyecto no requiere comando de build: la raíz del repositorio es el directorio público. La configuración está en `vercel.json` y el despliegue automático se ejecuta mediante `.github/workflows/vercel.yml` cuando hay cambios en `main`.

El workflow necesita los secretos de GitHub `VERCEL_TOKEN`, `VERCEL_ORG_ID` y `VERCEL_PROJECT_ID`. Nunca guardar esos valores en el repositorio ni dentro de `vercel.json`.
