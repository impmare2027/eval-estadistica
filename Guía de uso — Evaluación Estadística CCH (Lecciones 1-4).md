# Guía de uso — Evaluación Estadística CCH (Lecciones 1-4)

Oct 11, 2026 · @Mike Rivers

## Qué es y cómo la recorre el alumno

`index.html` es una sola página autocontenida (HTML + CSS + JavaScript nativo) para evaluar las Lecciones 1 a 4 de Estadística y Probabilidad I. Se abre con doble clic en cualquier navegador, sin internet ni servidor.

Flujo del alumno:

1. **Registro** — nombre completo, número de cuenta y grupo (validados antes de poder avanzar).
2. **Bloque 1 (Lecciones 1-2)** — mapa mental de 11 definiciones (arrastrar y soltar), clasificación de 8 variables de una encuesta escolar, 6 casos prácticos de opción múltiple sobre el caso de transporte.
3. **Bloque 2 (Lecciones 3-4)** — mapa mental de 13 definiciones, clasificación de 8 propuestas de muestreo, 8 casos prácticos (rectángulos, censo vs. muestreo, Literary Digest, etc.).
4. **Resultados** — calificación de 0 a 10, desglose por bloque y por cada una de las 6 actividades, botón de descarga del reporte en CSV y, si se configura, botón de envío a Microsoft Forms.

Cada pestaña se desbloquea solo al terminar la anterior, y tanto el orden de las preguntas como el de sus opciones se revuelve de nuevo cada vez que se carga o reinicia la actividad.

## Cómo personalizar preguntas y bancos de reactivos

Todo el contenido editable vive en el `<script>`, en arreglos de JavaScript con comentarios que indican a qué bloque pertenecen:

| Reactivo | Bloque 1 | Bloque 2 |
| --- | --- | --- |
| Mapa mental | `B1_MAPA_ITEMS` / `B1_MAPA_LABELS` | `B2_MAPA_ITEMS` / `B2_MAPA_LABELS` |
| Clasificación | `B1_CLASIF_ITEMS` / `B1_CLASIF_LABELS` | `B2_CLASIF_ITEMS` / `B2_CLASIF_LABELS` |
| Casos prácticos | `B1_CASOS` | `B2_CASOS` |

- **Mapa mental**: cada objeto es `{ key, def }`. `key` debe coincidir exactamente con el `data-key` de su casilla (`<div class="dropzone" data-key="...">`) en el HTML. Si agregas o quitas una definición, agrega o quita también su casilla.
- **Clasificación**: cada objeto es `{ id, texto, cat }`. `cat` debe coincidir con el `data-key` de su "bin" (`<div class="bin" data-key="...">`).
- **Casos prácticos**: cada pregunta tiene `texto`, `pista` y un arreglo `opciones` de 5 objetos `{ texto, correcta, feedback }` (exactamente una con `correcta: true`).
- La tabla de transporte y la figura SVG de los 12 rectángulos son estáticas en el HTML; edítalas directamente si cambian los datos.

## Recoger resultados en Excel (CSV)

En la pantalla de Resultados, el botón **"⬇ Descargar Reporte de Resultados en Excel (CSV)"** genera un archivo `resultado_[NÚMERODECUENTA].csv` con codificación UTF-8 y BOM (los acentos se ven correctamente al abrirlo en Excel).

El archivo incluye:

- Metadatos del alumno (nombre, cuenta, grupo, fecha y hora).
- Calificación final (0-10), aciertos y errores totales, y desglose por bloque y por cada una de las 6 actividades.
- Un detalle reactivo por reactivo: ítem, respuesta correcta, respuestas dadas en orden, número de intentos y resultado.
- Un **código de verificación** (hash) calculado a partir de los datos del alumno, útil para detectar si el archivo fue editado manualmente antes de entregarlo.

Forma de recolección sugerida: que el alumno suba el CSV a una carpeta compartida (Classroom/Drive) o lo envíe por correo/chat del grupo.

## Activar el envío automático a Microsoft Forms

Por defecto `FORMS_PREFILL_URL` está vacío y la actividad solo ofrece el CSV. Para activar el botón de envío directo:

1. En Microsoft Forms, crea una pregunta (texto corto o largo) por cada dato que quieras capturar: Nombre, Cuenta, Grupo, Fecha, Calificación, Resumen y Detalle.
2. Contesta el formulario tú mismo una vez, escribiendo literalmente como respuesta de cada pregunta el marcador correspondiente: `TOK_NOMBRE`, `TOK_CUENTA`, `TOK_GRUPO`, `TOK_FECHA`, `TOK_CALIF`, `TOK_RESUMEN`, `TOK_DETALLE` (uno por campo).
3. En el menú "···" de esa respuesta, elige **"Obtener vínculo con datos ya completados"** ("Get prefill link") y cópialo.
4. Pega ese vínculo entre las comillas de `FORMS_PREFILL_URL`, cerca del inicio del `<script>` de `index.html`.

Con eso, al terminar la actividad aparece el botón **"📤 Enviar mi resultado a mi profesor"**: se abre tu formulario en una pestaña nueva con los datos del alumno ya escritos (nombre, cuenta, grupo, calificación, resumen por bloque y detalle reactivo por reactivo); el alumno solo presiona "Enviar". Si el navegador bloquea la ventana emergente, se muestra un enlace para abrirlo manualmente. El botón "Copiar mi resultado" y la descarga del CSV siguen disponibles como respaldo.

## Notas técnicas y solución de problemas

- Requiere JavaScript activado; funciona sin conexión a internet (salvo el envío a Forms, que sí la necesita).
- Compatible con cualquier navegador moderno de escritorio o móvil (Chrome, Edge, Safari, Firefox); el arrastrar-y-soltar funciona con mouse y con pantalla táctil.
- Si el CSV se ve con caracteres extraños al abrirlo, confirma que el programa detecte UTF-8 (el BOM ya está incluido; normalmente Excel lo abre bien de forma automática).
- Si el envío a Forms no llega: revisa que el vínculo copiado sea el de **"datos ya completados"** (no el vínculo normal del formulario) y que las preguntas usadas como `TOK_*` sean de respuesta de texto, no de opción múltiple.
- Para reiniciar la actividad, usa el botón "Reiniciar actividad" o recarga la página; no hay forma de recuperar un intento a medias.
