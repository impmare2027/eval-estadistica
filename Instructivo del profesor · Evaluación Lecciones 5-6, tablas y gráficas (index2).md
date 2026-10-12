# Instructivo del profesor · Evaluación Lecciones 5-6, tablas y gráficas (index2)

Oct 11, 2026 · @Mike Rivers

## Qué evalúa y cuánto vale

Son 15 actividades y 93 reactivos en cuatro bloques. Las tablas y las gráficas valen 7 de los 10 puntos, y los dos mapas conceptuales solo 0.5, como diagnóstico. Calcule alrededor de una hora; los alumnos necesitan calculadora.

| Actividad | Tipo de reactivo | Reactivos | Valor |
| --- | --- | --- | --- |
| A1 · Mapa de técnicas de recolección | Mapa conceptual | 6 | 0.25 |
| A2 · Técnica que usa cada proyecto | Clasificación | 6 | 0.50 |
| A3 · Estudios observacionales y experimentales | Opción múltiple | 5 | 0.75 |
| **Bloque A · Lección 5** |  | **17** | **1.5** |
| B1 · Mapa de tipos de variable y escalas | Mapa conceptual | 6 | 0.25 |
| B2 · Escala de medición de cada variable | Clasificación | 8 | 0.75 |
| B3 · Identificar variables y su tipo | Opción múltiple | 4 | 0.50 |
| **Bloque B · Lección 6** |  | **18** | **1.5** |
| C1 · Tabla de datos no agrupados (desayuno) | Completar casillas | 6 | 1.00 |
| C2 · Interpretar la tabla | Opción múltiple | 4 | 0.60 |
| C3 · Ordenar los pasos para agrupar datos | Ordenar | 6 | 0.40 |
| C4 · Tabla agrupada paso a paso (traslado) | Cálculo guiado | 10 | 1.40 |
| C5 · Completar la tabla agrupada | Completar casillas | 4 | 0.60 |
| **Bloque C · Tablas** |  | **30** | **4.0** |
| D1 · Qué gráfica conviene | Clasificación | 6 | 0.40 |
| D2 · Leer e interpretar gráficas | Opción múltiple con gráfica | 10 | 1.20 |
| D3 · Encontrar el error y emparejar | Opción múltiple con gráfica | 5 | 0.60 |
| D4 · Construir el histograma (estaturas) | Construir gráfica | 7 | 0.80 |
| **Bloque D · Gráficas** |  | **28** | **3.0** |
| **Total** |  | **93** | **10.0** |

Cómo se califica:

- **Primer intento.** Un reactivo suma su valor solo si se acierta al primer intento. El alumno debe corregir para avanzar, así que siempre termina viendo la respuesta correcta y su explicación.
- **Cálculos.** En las casillas numéricas, después de dos intentos fallidos se muestra el valor correcto (0 puntos) para que el alumno pueda seguir. Si presiona Revisar sin cambiar un valor que ya estaba mal, no pierde la segunda oportunidad.
- **Errores que no se arrastran.** En el cálculo guiado (C4), si un paso se falla, el siguiente parte del valor correcto. Un error en el rango no cuesta también la amplitud.
- **Tolerancias.** Las frecuencias relativas se califican con 3 decimales (±0.001), los porcentajes con 1 decimal (±0.05), y Sturges y la amplitud con ±0.01. Se acepta punto o coma decimal.
- **Orden aleatorio.** En cada intento se barajan las tarjetas, las preguntas y las opciones. El orden de las 15 actividades y de los pasos de C4 es fijo.
- **Ojiva.** Se dibuja con los vértices en los **límites superiores** de las clases, empezando en el eje horizontal. Así, el punto sobre 48 se lee como «estudiantes que tardan menos de 48 minutos». El material de clase usa las marcas de clase; conviene comentarlo con el grupo antes del examen.

## Antes de aplicar

Hay que hacer tres cosas una sola vez: publicar el archivo, conectar un formulario nuevo de Forms y probar el envío. Mientras `FORMS_PREFILL_URL` esté vacío, los alumnos solo verán el botón de descarga del CSV.

**1. Publicar.** Suba `index2.html` al repositorio [impmare2027/eval-estadistica](https://github.com/impmare2027/eval-estadistica) con **Add file → Upload files → Commit changes**. No reemplaza a `index.html`: los dos exámenes conviven. La liga para el grupo será `https://impmare2027.github.io/eval-estadistica/index2.html`. GitHub tarda un par de minutos en publicar.

**2. Crear el formulario.** En [forms.office.com](https://forms.office.com) haga un formulario nuevo para este examen, con siete preguntas de texto en este orden. Así sus respuestas no se mezclan con las de la Unidad 1. Puede duplicar el formulario anterior y cambiarle el título.

| Pregunta | Tipo de respuesta | Marcador |
| --- | --- | --- |
| Nombre completo | Corta | `TOK_NOMBRE` |
| Número de cuenta | Corta | `TOK_CUENTA` |
| Grupo | Corta | `TOK_GRUPO` |
| Fecha y hora | Corta | `TOK_FECHA` |
| Calificación | Corta | `TOK_CALIF` |
| Resumen | Larga | `TOK_RESUMEN` |
| Detalle | Larga | `TOK_DETALLE` |

**3. Obtener el vínculo.** En el menú **…** del formulario elija la URL rellenada previamente (*Get Pre-filled URL*), active las respuestas rellenadas y escriba en cada pregunta su marcador, tal cual. Copie el vínculo generado.

**4. Pegarlo en el archivo.** Abra `index2.html` con un editor de texto, busque `FORMS_PREFILL_URL` (está al inicio del bloque `<script>`) y pegue el vínculo entre las comillas:

```js
const FORMS_PREFILL_URL = 'https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=...';
```

Vuelva a subir el archivo a GitHub.

**5. Probar.** Abra `https://impmare2027.github.io/eval-estadistica/index2.html?profesor=1`. El panel debe decir que encontró los 7 marcadores. Presione **Ver resultados con datos de ejemplo** y después **Enviar mi resultado a mi profesor**: el formulario debe abrir con las siete respuestas escritas. Envíe esa respuesta de prueba; aparecerá como «ALUMNO DE PRUEBA» y puede borrarla después.

Si no tiene tiempo de crear otro formulario, puede pegar el vínculo del formulario de la Unidad 1. Las respuestas de este examen se distinguen porque su Detalle empieza con `u1b-v1`.

## El día del examen

Comparta la liga y lea al grupo estas indicaciones; caben en un mensaje de Teams o en el pizarrón.

1. Abre `impmare2027.github.io/eval-estadistica/index2.html` en tu teléfono o computadora. Ten a la mano **calculadora, lápiz y papel**.
2. Escribe tu nombre completo, tu número de cuenta (8 a 10 dígitos, sin guiones) y tu grupo, y presiona **Comenzar actividad**.
3. Resuelve las 15 actividades en orden: A (Lección 5), B (Lección 6), C (tablas) y D (gráficas).
4. **Tarjetas:** arrástralas a su casilla, o tócala y luego toca la casilla. Soltarla fuera de las casillas no cuenta como error.
5. **Cálculos:** escribe el número y presiona **Comprobar** o **Revisar**. Las frecuencias relativas van con 3 decimales y los porcentajes con 1 decimal. Tienes dos oportunidades por casilla; después se muestra el valor correcto.
6. **Histograma:** arrastra cada barra hacia arriba o abajo, o usa los botones − y +.
7. **Solo suma lo que aciertas al primer intento.** El valor de cada reactivo aparece en pantalla.
8. Al final presiona **Enviar mi resultado a mi profesor**, revisa tus datos en el formulario y presiona **Enviar**. Si te pide iniciar sesión, usa tu cuenta institucional.
9. Si el formulario no abre, presiona **Descargar Reporte de Resultados en Excel (CSV)** y envía el archivo por el medio que te indique tu profesor. No lo modifiques.
10. Si la página se cierra, vuelve a abrir la liga y elige **Continuar donde me quedé**. No uses **Reiniciar actividad**: borra tu avance y el nuevo intento queda registrado como intento 2.

## Revisar los resultados

Cada respuesta llega con la calificación, un resumen y una cadena de detalle reactivo por reactivo. Desde la pestaña **Respuestas** de Forms se abre todo en Excel.

**Resumen.** Trae los puntos de cada bloque (A, B, C, D), los puntos por tipo de reactivo (mapas, clasificación, opción múltiple, cálculo y construcción), los aciertos al primer intento, los intentos fallidos, la duración en minutos y el número de intento.

**Detalle.** Ejemplo de un recorrido de prueba con 7.8:

```text
u1b-v1;418123456;7.8;A1=111112;A2=111211;A3=11121;B1=211111;B2=21111111;B3=1121;C1=221111;C2=1121;C3=221111;C4=1112111112;C5=2211;D1=111211;D2=2111111111;D3=11121;D4=2111111;#5979F849
```

Cada dígito es el número de intentos de un reactivo: 1 es acierto al primer intento. En las casillas numéricas, un 2 puede significar que acertó al segundo intento o que se le mostró la respuesta; el CSV distingue los dos casos. Los dígitos siguen el orden en que los reactivos están escritos en el archivo, no el orden aleatorio que vio el alumno.

La clave C4 es la más útil para diagnosticar, porque cada dígito es un paso del cálculo:

| Dígito de C4 | Paso |
| --- | --- |
| 1 a 3 | Dato mínimo, dato máximo y rango |
| 4 y 5 | Sturges sin redondear y número de clases |
| 6 y 7 | Amplitud sugerida y amplitud redondeada |
| 8 | En qué clase se cuenta un dato frontera (28) |
| 9 | Marca de clase |
| 10 | Contar la frecuencia de una clase en los datos |

En el ejemplo, `C4=1112111112` indica que falló Sturges (paso 4) y el conteo de la frecuencia (paso 10).

**Verificar que nadie editó su resultado.** Abra la actividad con `?profesor=1`, copie de Excel la columna Detalle (una o varias celdas) y péguela en el verificador. Recalcula la calificación a partir de los dígitos y revisa el código final. Los dictámenes son: Válido, Código no coincide (texto modificado), Calificación alterada, Detalle incompleto y Es un intento de PRUEBA. Un detalle del examen de la Unidad 1 aparece como «formato no reconocido», así que no se confunden.

**Respaldo en CSV.** El archivo `resultado_CUENTA.csv` abre en Excel con acentos correctos. Trae el renglón de resumen, la ponderación de las 15 actividades y los 93 reactivos con la respuesta correcta, lo que escribió o eligió el alumno en cada intento y los puntos obtenidos. Es la única vía para ver qué valor equivocado escribió cada alumno.

## Clave de respuestas y datos verificados

Todos los datos son inventados con contexto del CCH Oriente. Cada cifra se recalculó con un programa independiente y coincide con la que califica el examen. Las tablas y las gráficas se generan de los mismos datos, así que no pueden contradecirse.

**Tiempo de traslado (min), 50 estudiantes** (C4, C5 y gráficas de D2 y D3):

```text
32 34 63  8 53 32 12  8 65 21 62 71 18 30 30 28 18 46 18 35 18 53 53 49 40
15 76 25 33 39 42 33 55 27 31 43 25 28 31 31 23 37 20 38 45 13 26 41 23 13
```

| Paso de C4 | Respuesta |
| --- | --- |
| Dato mínimo / máximo | 8 / 76 min |
| Rango | 76 − 8 = 68 min |
| Sturges sin redondear | 1 + 3.322 × log 50 = 1 + 3.322 × 1.699 ≈ 6.64 |
| Número de clases | 7 |
| Amplitud sugerida | 68 ÷ 7 ≈ 9.71 |
| Amplitud redondeada hacia arriba | 10 (7 × 10 = 70 ≥ 68) |
| Clase del dato 28 | \[28, 38) |
| Marca de la tercera clase | (28 + 38) ÷ 2 = 33 |
| Frecuencia de \[18, 28) | 12 (18, 18, 18, 18, 20, 21, 23, 23, 25, 25, 26, 27) |

| Clase (min) | Marca | fi | fr | Fa | Fr acum. |
| --- | --- | --- | --- | --- | --- |
| \[8, 18) | 13 | 6 | 0.12 | 6 | 0.12 |
| \[18, 28) | 23 | 12 | 0.24 | 18 | 0.36 |
| \[28, 38) | 33 | 14 | **0.28** | 32 | 0.64 |
| \[38, 48) | 43 | 8 | 0.16 | **40** | 0.80 |
| \[48, 58) | **53** | 5 | 0.10 | 45 | 0.90 |
| \[58, 68) | 63 | 3 | 0.06 | 48 | **0.96** |
| \[68, 78\] | 73 | 2 | 0.04 | 50 | 1 |

En negritas, las casillas que completa el alumno en C5.

**Días a la semana que desayunan, 40 estudiantes** (C1, C2 y la gráfica de barras de D2):

| Días | fi | fr | % | Fa | Fr acum. |
| --- | --- | --- | --- | --- | --- |
| 0 | 2 | 0.05 | 5 | 2 | 0.05 |
| 1 | 3 | 0.075 | **7.5** | 5 | 0.125 |
| 2 | 4 | 0.1 | 10 | 9 | 0.225 |
| 3 | **6** | 0.15 | 15 | 15 | **0.375** |
| 4 | 7 | 0.175 | 17.5 | **22** | 0.55 |
| 5 | 9 | **0.225** | 22.5 | 31 | 0.775 |
| 6 | 5 | 0.125 | 12.5 | **36** | 0.9 |
| 7 | 4 | 0.1 | 10 | 40 | 1 |

En C1 la frecuencia de 3 días se obtiene del total: 40 − 34 = 6. Respuestas de C2: Fa(4) = 22 significa «22 desayunan a lo más 4 días»; 5 días o más = 18 ÷ 40 = 45 %; menos de 3 días = 9; moda = 5 días, con fr = 0.225.

**Gráficas de D2 y D3:**

| Gráfica | Pregunta | Respuesta |
| --- | --- | --- |
| Barras (desayuno) | 6 días o más | 5 + 4 = 9 |
| Circular: Deporte 14, Música 8, Danza 6, Ajedrez 4, Ninguna 8 | Cuántos eligieron danza | 15 % de 40 = 6 |
| La misma circular | Ángulo de deporte | 0.35 × 360° = 126° (los cinco suman 360°) |
| Histograma (traslado) | Al menos 28 y menos de 38 min | 14 |
| Histograma (traslado) | Por qué las barras van pegadas | Variable continua, clases contiguas |
| Polígono (traslado) | Por qué empieza en 3 y termina en 83 | Marcas de dos clases ficticias con frecuencia 0 |
| Ojiva (traslado) | Menos de 48 min | 40 |
| Ojiva (traslado) | 58 min o más | (50 − 45) ÷ 50 = 10 % |
| Puntos (hermanos de 20 estudiantes) | 3 hermanos o más | 6 ÷ 20 = 30 % |
| Líneas (préstamos: 420, 610, 580, 640, 230) | Mayor aumento | Agosto a septiembre (+190) |
| Histograma con barras separadas | Error | Las barras deben ir pegadas |
| Polígono sin cerrar | Error | Debe cerrarse en 3 y 83 |
| Ojiva que baja en 58 (marca 35) | Error | Una frecuencia acumulada nunca disminuye; debe ser 45 |
| Circular con 40, 25, 20 y 20 % | Error | Suma 105 %; debe sumar 100 % |
| Circular numerada (45, 25, 15, 15 %) | Tabla que le corresponde | Tabla 2 (lectura) |

**Estaturas de 40 estudiantes (D4):** clases de 5 cm de \[150, 155) a \[180, 185\], con frecuencias 2, 5, 9, 11, 7, 4 y 2. Son las alturas que debe tener cada barra.

Las respuestas de los bloques A y B (técnicas, escalas y casos de las lecturas de la Lección 5) están en el CSV de cualquier alumno, en la columna «Respuesta correcta». La forma más rápida de verlas todas es el CSV del intento de ejemplo del modo profesor.

## Ajustes y límites conocidos

Todo lo configurable está al inicio del bloque `<script>` de `index2.html`, con comentarios en español.

- **Cambiar la ponderación.** Edite los números de `VALORES` (uno por actividad, de `a1` a `d4`). Si la suma deja de ser 10, la calificación se reescala sola y la pantalla muestra los valores ya reescalados.
- **Cambiar los datos.** Los conjuntos están en `TRASLADO`, `DESAYUNO`, `EXTRA`, `ESTATURA`, `HERMANOS` y `BIBLIO`. Las tablas, las gráficas y las respuestas de las casillas se recalculan solas; las cifras escritas en el texto de las preguntas y en sus opciones (por ejemplo, 126° o 45 %) hay que actualizarlas a mano.
- **Cambiar reactivos.** Están en la lista `ACTS`. Cada pregunta de opción múltiple necesita exactamente una opción con `correcta:true`.
- **Modo profesor.** Con `?profesor=1` al final de la dirección se ven el estado del vínculo de Forms, el intento de ejemplo y el verificador. Los alumnos no lo ven si no escriben esa dirección.

Límites:

- **El envío no es de un solo clic.** La página abre el formulario ya lleno, pero el alumno debe presionar Enviar dentro de Forms, y puede editar lo que llega escrito. El código de la columna Detalle disuade esas ediciones, aunque no es infalible: el archivo es público.
- **Reintentos.** Un alumno puede reiniciar y volver a resolver conociendo las respuestas. El reporte lo delata con el número de intento, pero solo dentro del mismo dispositivo.
- **Dispositivos compartidos.** El avance guardado caduca a las 12 horas. Antes de eso, el siguiente alumno verá el nombre del anterior y debe elegir Empezar de nuevo.
- **Contar 50 datos en el teléfono.** En el paso 10 de C4 los datos quedan arriba de la pregunta; en pantallas pequeñas hay que desplazarse para verlos. Conviene sugerir papel para ir anotando.
- **Pruebas realizadas.** Recorrido automatizado completo en Chromium simulando un teléfono táctil de 390 px (con errores deliberados en cada tipo de reactivo), en escritorio con ratón y teclado, en 360 × 640 px y con el teléfono acostado. No se probó en un iPhone físico con Safari ni contra un formulario real; hágalo una vez antes de aplicar el examen.
