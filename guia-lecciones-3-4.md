# Guía — Evaluación interactiva Lecciones 3 y 4

**Archivo:** `lecciones-3-4.html` (una sola página, sin instalación). Evalúa ramas de la estadística (descriptiva e inferencial), población, muestra y tipos de muestreo.

## Estructura (29 reactivos; calificación = aciertos al primer intento ÷ 29 × 10)
| Actividad | Reactivos | Qué hace el alumno |
|---|---|---|
| 1 · Mapa mental | 13 | Arrastra definiciones a dos esquemas: ramas de la estadística (6) y tipos de muestreo (7) |
| 2 · Muestreo | 8 | Clasifica 8 propuestas de proyecto en los 5 tipos de muestreo |
| 3 · Casos | 8 | Preguntas de 5 opciones con retroalimentación por opción: censo/muestreo, noticias, rectángulos, sesgo, *Literary Digest*, parámetro/estadístico |

## Publicarlo (misma forma que el anterior)
1. En tu repositorio `eval-estadistica`: **Add file → Upload files** y sube `lecciones-3-4.html`.
2. La liga para los alumnos será:
   `https://impmare2027.github.io/eval-estadistica/lecciones-3-4.html`
   (el nombre del archivo va al final de la liga).

## Recibir resultados en Forms
El archivo sale **sin formulario configurado**: de momento ofrece solo el CSV de respaldo. Para el envío automático:
1. En Forms abre tu formulario de la Unidad 1 → **⋯ → Duplicar**. Duplícalo; **no reutilices el mismo**, porque “Limitar a una respuesta” impediría a los alumnos enviar un segundo resultado.
2. Renombra el duplicado, por ejemplo *Resultados Lecciones 3 y 4*, y revisa que esté aceptando respuestas.
3. **⋯ → Obtener vínculo de rellenado previo**, escribe los marcadores (`TOK_NOMBRE`, `TOK_CUENTA`, `TOK_GRUPO`, `TOK_FECHA`, `TOK_CALIF`, `TOK_RESUMEN`, `TOK_DETALLE`) y copia el vínculo.
4. Pégamelo en el chat y te devuelvo el archivo ya configurado, o pégalo tú entre las comillas de `const FORMS_PREFILL_URL = '';`.

El campo *Resumen* empieza con “Lecciones 3-4”, así que aunque algún día mezcles formularios podrás distinguirlos.

## Clave de respuestas
**Actividad 1.** Esquema 1: Descriptiva (resume y presenta datos; sus métodos son gráficas y resúmenes numéricos); Inferencial (generaliza a la población; sus métodos son estimación y contraste de hipótesis). Esquema 2: Probabilístico (aleatorio, estratificado, sistemático); No probabilístico (voluntarios, conveniencia).

**Actividad 2.** Beso en la explanada → conveniencia · Lista numerada con S + kN → sistemático · Tarjetas en una caja → aleatorio · Correo a todos y se usan las respuestas → voluntarios · Mismo número por grupo → estratificado · Enlace en el chat → voluntarios · 60 números aleatorios de 600 → aleatorio · Muestra por turno en proporción → estratificado.

**Actividad 3.** 1) Se observa toda la población vs. una muestra · 2) (i) descriptiva, (ii) inferencial · 3) Población: todos los pacientes con cáncer de próstata; muestra: los 185 pacientes · 4) 256 u² · 5) Estimación 252 u², error 4 u² · 6) Muestra sesgada (subestima) · 7) Muestra sesgada (listas no representativas y respuesta voluntaria) · 8) 21.3 es parámetro; 21 es estadístico.

## Revisar calificaciones
En Excel, si *Detalle* está en la columna G, los aciertos al primer intento son:
`=(LEN(G2)-LEN(SUBSTITUTE(G2,"=1;","")))/3`
y la calificación es ese número ÷ 29 × 10.
