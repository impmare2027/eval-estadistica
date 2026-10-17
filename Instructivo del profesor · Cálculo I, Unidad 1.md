# Instructivo del profesor · Cálculo I, Unidad 1: Procesos infinitos (index3)

Oct 12, 2026 · @Mike Rivers

## Qué evalúa y cuánto vale

Son 20 reactivos con 47 partes calificables, en cuatro secciones que siempre van en orden (I → IV). Hay 5 reactivos básicos (0.35 c/u), 10 intermedios (0.50 c/u) y 5 avanzados (0.65 c/u), que suman 10. Calcule unos 70 minutos de una sesión de 90; los alumnos necesitan calculadora científica.

| Reactivo | Tipo | Nivel | Aprendizaje | Valor |
| --- | --- | --- | --- | --- |
| R01 · Término general de una PA | Opción múltiple | Básico | A2 | 0.35 |
| R02 · Sucesión ↔ término general | Emparejar (4 tarjetas) | Intermedio | A1 | 0.50 |
| R03 · Patrón de puntos y diferencias finitas | Cálculo guiado (3 partes) | Intermedio | A2 | 0.50 |
| R04 · ¿Hacia dónde tiende la sucesión? | Recta numérica + opción | Básico | A5 | 0.35 |
| R05 · Verdadero o falso, y por qué | Dos niveles | Avanzado | A5 | 0.65 |
| **Sección I · Sucesiones** |  |  |  | **2.35** |
| R06 · Suma con notación Σ | Respuesta numérica | Básico | A1 | 0.35 |
| R07 · Progresión aritmética: n y Sₙ | Respuesta numérica (2 partes) | Intermedio | A4 | 0.50 |
| R08 · Suma de Gauss | Ordenar 5 pasos | Intermedio | A2 | 0.50 |
| R09 · Progresión geométrica: n y Sₙ | Respuesta numérica (2 partes) | Intermedio | A4 | 0.50 |
| R10 · Encuentra el error | Opción múltiple con solución resuelta | Avanzado | A1 | 0.65 |
| **Sección II · Sumas finitas** |  |  |  | **2.50** |
| R11 · Serie geométrica infinita | Opción múltiple | Básico | A7 | 0.35 |
| R12 · ¿Cuáles series convergen? | Selección múltiple (todo o nada) | Intermedio | A5 | 0.50 |
| R13 · Decimal periódico como serie | Opción + fracción | Intermedio | A1 | 0.50 |
| R14 · La pelota que rebota | Cálculo guiado (3 partes) | Avanzado | A4 | 0.65 |
| R15 · Serie telescópica | Opción múltiple | Avanzado | A7 | 0.65 |
| **Sección III · Series** |  |  |  | **2.65** |
| R16 · Exploración con deslizador | Deslizador + 2 respuestas | Básico | A7 | 0.35 |
| R17 · Tabla de etapas de un fractal | Completar 5 casillas | Intermedio | A2 | 0.50 |
| R18 · Clasifica procesos | Clasificar 6 tarjetas | Intermedio | A3 | 0.50 |
| R19 · Paradoja de un proceso infinito | Dos niveles | Avanzado | A5 | 0.65 |
| R20 · Gráfica de S(n) y notación de límite | Opción múltiple con gráfica | Intermedio | A6 | 0.50 |
| **Sección IV · Procesos infinitos** |  |  |  | **2.50** |
| **Total** |  |  |  | **10.0** |

Aprendizajes del programa: A1 transita entre registros · A2 identifica el patrón · A3 distingue un proceso infinito · A4 resuelve problemas en contexto · A5 distingue si hay límite · A6 expresa el límite simbólicamente · A7 establece el valor límite.

Cómo se califica:

- **Primer intento.** Una parte suma su valor solo si se acierta al primer intento. El alumno debe corregir para avanzar, así que siempre termina viendo la respuesta y su explicación.
- **Respuestas numéricas.** Se acepta entero, decimal (punto o coma) o fracción. En R13 se exige fracción; si escriben un decimal se les pide la fracción sin gastar intento. Después de dos fallos se muestra el valor correcto (0 puntos).
- **Selección múltiple (R12).** Todo o nada: la selección debe coincidir exactamente con las tres series convergentes.
- **Convenciones.** La etapa 0 es la figura inicial; «lim» solo se usa con n → +∞.

## Formas A-D y barajado

Cada reactivo existe en cuatro versiones paralelas, con el mismo aprendizaje, tipo, nivel y número de pasos, pero con datos distintos. Además, dentro de cada sección se baraja el orden de los cinco reactivos y, en cada reactivo, el de las opciones y tarjetas. Hay 207 360 000 órdenes posibles de reactivos por forma, sin contar el barajado de opciones.

**Cómo se asigna la forma** (elija una de tres maneras):

| Modo | Liga que comparte | Cuándo conviene |
| --- | --- | --- |
| Por número de cuenta (predeterminado) | `…/index3.html` | Siempre. Cada alumno recibe siempre la misma forma, aunque recargue o cambie de dispositivo. Con 1000 cuentas de prueba el reparto fue de 235 a 273 por forma. |
| Fija por fila | `…/index3.html?forma=A` (B, C, D) | Cuando quiera garantizar que alumnos contiguos tengan formas distintas: comparta una liga distinta a cada fila. |
| Al azar | `…/index3.html?forma=azar` | Para práctica; la forma cambia en cada intento nuevo. |

No se baraja lo que tiene un orden natural: las secciones, las partes de un mismo reactivo (por ejemplo, n antes que Sₙ), las filas de la tabla de etapas y las opciones Verdadera/Falsa.

La forma no aparece en la pantalla de registro. Se muestra en el reporte final, en el CSV, al inicio del resumen que llega al formulario y como segundo campo del Detalle.

## Antes de aplicar

Haga tres cosas una sola vez: publicar el archivo, conectar un formulario nuevo y probar el envío con las cuatro formas. Mientras `FORMS_PREFILL_URL` esté vacío, los alumnos solo verán la descarga del CSV.

1. **Publicar.** Suba `index3.html` a [impmare2027/eval-estadistica](https://github.com/impmare2027/eval-estadistica) con **Add file → Upload files → Commit changes**. Convive con `index.html` e `index2.html`. La liga será `https://impmare2027.github.io/eval-estadistica/index3.html`.
2. **Crear el formulario.** En [forms.office.com](https://forms.office.com) haga uno nuevo para este examen (puede duplicar el anterior y cambiarle el título) con siete preguntas de texto en este orden: Nombre completo, Número de cuenta, Grupo, Fecha y hora, Calificación (respuestas cortas), Resumen y Detalle (respuestas largas).
3. **Obtener el vínculo.** En el menú **…** elija la URL rellenada previamente (*Get Pre-filled URL*), active las respuestas rellenadas y escriba en cada pregunta su marcador: `TOK_NOMBRE`, `TOK_CUENTA`, `TOK_GRUPO`, `TOK_FECHA`, `TOK_CALIF`, `TOK_RESUMEN`, `TOK_DETALLE`. Copie el vínculo.
4. **Pegarlo.** Abra `index3.html` en un editor de texto, busque `FORMS_PREFILL_URL` (al inicio del bloque `<script>`), pegue el vínculo entre las comillas y vuelva a subir el archivo.
5. **Probar.** Abra `…/index3.html?profesor=1`. El panel debe decir que encontró los 7 marcadores. Para cada forma, elija **Forma A** (B, C, D), presione **Ver resultados de ejemplo** y después **Enviar mi resultado a mi profesor**: el formulario debe abrir con las siete respuestas escritas y el resumen debe empezar con «Forma A». Las respuestas de prueba llegan como «ALUMNO DE PRUEBA»; bórrelas después.
6. **Revisar la clave.** En el mismo panel, abra **Clave de respuestas de la forma …** para ver las respuestas de cada forma en orden R01-R20. También están en la sección de claves de este documento.

## Indicaciones para el alumno

Para leer al grupo o pegar en Teams:

1. Abre la liga que te dio tu profesor en tu teléfono o computadora. Ten a la mano **calculadora científica, lápiz y papel**.
2. Escribe tu nombre completo, tu número de cuenta (8 a 10 dígitos, sin guiones) y tu grupo, y presiona **Comenzar actividad**.
3. Resuelve los 20 reactivos en orden. Tus compañeros tienen otra versión y otro orden: copiar no sirve.
4. **Opción múltiple:** elige una opción. En «marca todas las correctas» selecciona varias y presiona **Comprobar**.
5. **Números:** escribe un entero, un decimal o una fracción con diagonal (por ejemplo 5/11) y presiona **Comprobar**. Tienes dos oportunidades; después se muestra el valor correcto.
6. **Recta numérica, tarjetas y deslizador:** arrastra con el dedo; también puedes tocar una tarjeta y luego su casilla.
7. **Solo suma lo que aciertas al primer intento.** El valor de cada reactivo aparece en pantalla.
8. Al final presiona **Enviar mi resultado a mi profesor**, revisa tus datos en el formulario y presiona **Enviar**. Si te pide iniciar sesión, usa tu cuenta institucional.
9. Si el formulario no abre, presiona **Descargar Reporte de Resultados en Excel (CSV)** y envía el archivo sin modificarlo.
10. Si la página se cierra, vuelve a abrir la liga y elige **Continuar donde me quedé**. No uses **Reiniciar actividad**: borra tu avance y el nuevo intento queda registrado como intento 2.

## Revisar los resultados

Cada respuesta llega a Forms con la calificación, un resumen que empieza con la forma, y una cadena de detalle por reactivo. Desde **Respuestas** se abre todo en Excel.

**Detalle.** Ejemplo de un recorrido de prueba de la forma A con errores deliberados:

```text
cdi1-u1-v1;A;418123456;8.0;R01=2;R02=1111;R03=111;R04=21;R05=11;R06=1;R07=21;R08=22111;R09=11;R10=1;R11=1;R12=1;R13=11;R14=111;R15=2;R16=11;R17=11111;R18=111112;R19=21;R20=1;#40DCBE60
```

Se lee así: examen, **forma**, cuenta, calificación, un grupo de dígitos por reactivo y el código de verificación. Cada dígito es el número de intentos de una parte: 1 significa acierto al primer intento. Los reactivos van siempre en orden fijo R01-R20, aunque el alumno los haya visto barajados; así puede comparar a todo el grupo reactivo por reactivo, sin importar la forma. En el ejemplo, `R04=21` indica que falló la ubicación del límite en la recta, pero acertó cómo se acercan los términos.

**Diagnóstico por aprendizaje.** Cada reactivo evalúa un aprendizaje del programa (tabla de la primera sección). Para ver qué aprendizaje cuesta más al grupo, cuente en Excel cuántos alumnos tienen un dígito distinto de 1 en los reactivos de cada aprendizaje; por ejemplo, A5 corresponde a R04, R05, R12 y R19.

**Verificar que nadie editó su resultado.** Abra `?profesor=1`, copie de Excel la columna Detalle (una o varias celdas) y péguela en el verificador. Reconoce la forma de cada alumno, recalcula la calificación con la clave de esa forma y revisa el código. Los dictámenes son: Válido, Código no coincide (texto modificado), Calificación alterada, Detalle incompleto y Es un intento de PRUEBA. Los detalles de los exámenes anteriores (`index.html` e `index2.html`) aparecen como «formato no reconocido».

**Respaldo en CSV.** El archivo `resultado_CUENTA.csv` trae la forma, la ponderación de los 20 reactivos (con la posición en que el alumno vio cada uno) y las 47 partes, con la respuesta correcta y lo que escribió o eligió el alumno en cada intento.

## Claves de las formas A, B, C y D

Las 47 partes de cada forma (188 en total) se recalcularon con un programa independiente que usa fracciones exactas, y coinciden con las que califica el examen. Las partes de un reactivo se separan con «·».

| Reactivo | Forma A | Forma B | Forma C | Forma D |
| --- | --- | --- | --- | --- |
| R01 (datos) | 13, 17, 21, … | 8, 15, 22, … | 293, 287, 281, … | 41, 36, 31, … |
| R01 aₙ | 4n + 9 | 7n + 1 | −6n + 299 | −5n + 46 |
| R02 | 4n − 1 · 2·3ⁿ⁻¹ · n² · (−1)ⁿ⁺¹ | 3n + 2 · 3·2ⁿ⁻¹ · n² + 1 · (−1)ⁿ | 12 − 2n · (1/2)ⁿ⁻¹ · n(n + 1) · n/(n + 1) | 5n + 2 · 4·3ⁿ⁻¹ · n² − 1 · 1/n |
| R03 (t₆ · Δ² · tₙ) | 42 · 2 · n(n + 1) | 21 · 1 · n(n + 1)/2 | 48 · 2 · n(n + 2) | 37 · 2 · n² + 1 |
| R04 (límite · cómo) | 2 · por arriba | 3 · por abajo | 1 · alternando | 1/2 · por arriba |
| R05 | Falsa · oscila entre 1 y 2 | Verdadera · la diferencia 1/10ⁿ → 0 | Falsa · n/(n + 1) crece y tiende a 1 | Verdadera · \|r\| = 2/3 < 1 |
| R06 | 35 | 57 | 70 | 42 |
| R07 (n · Sₙ) | 20 · 860 | 19 · 646 | 19 · 893 | 21 · 1449 |
| R08 (resultado) | 5050 | 1275 | 3240 | 1830 |
| R09 (n · Sₙ) | 8 · 9840 | 10 · 2046 | 8 · 1275 | 7 · 4372 |
| R10 (paso con error · suma) | Paso 4: signo · 1023 | Paso 2: n = 8 · 765 | Paso 4: aritmética · 728 | Paso 3: rⁿ, no rⁿ⁻¹ · 1275 |
| R11 | 3 | 10 | 9 | 16/3 |
| R12 (convergen) | (1/5)ⁿ, (−1/2)ⁿ, (0.99)ⁿ | (3/4)ⁿ, (1/10)ⁿ, (−0.9)ⁿ | (2/7)ⁿ, (−1/3)ⁿ, (0.8)ⁿ | (5/6)ⁿ, (−0.5)ⁿ, (1/9)ⁿ |
| R13 (serie · fracción) | 45/100 + 45/100² + … · 5/11 | 36/100 + … · 4/11 | 27/100 + … · 3/11 | 81/100 + … · 9/11 |
| R14 (1.er rebote · rebotes · total, m) | 1 · 2 · 6 | 1 · 3/2 · 6 | 2 · 3 · 12 | 3 · 12 · 28 |
| R15 | 1/3 | 1/2 | 1/4 | 1/5 |
| R16 (S(2) · límite) | 3/4 · 1 | 5/16 · 1/3 | 4/9 · 1/2 | 6/25 · 1/4 |
| R17 (figura) | Conjunto de Cantor | Triángulo de Sierpinski | Alfombra de Sierpinski | Segmento en quintos |
| R17 (casillas) | 4 · 1/9 · 4/9 · 8 · 8/27 | 9 · 1/16 · 9/16 · 27 · 27/64 | 64 · 1/81 · 64/81 · 512 · 512/729 | 9 · 1/25 · 9/25 · 27 · 27/125 |
| R19 | Falsa · la longitud sigue siendo √2 | Falsa · el perímetro crece ×4/3 | Falsa · 0.999… = 1 | Verdadera · (3/4)ⁿ > 0, pero su límite es 0 |
| R20 | lim S(n) = 4 | lim S(n) = 3 | lim S(n) = 5 | lim S(n) = 2 |

En R02 las sucesiones van en el orden de la tabla: aritmética, geométrica, cuadrática y alternante o racional. Las casillas de R17 son: piezas, medida de cada pieza y medida total en la etapa 2; después, piezas y medida total en la etapa 3.

**R18 (clasificar procesos).** Cada forma tiene 2 procesos que convergen, 2 que divergen, 1 que oscila y 1 que no es infinito:

- **A:** convergen el área de Sierpinski y la distancia de la pelota; divergen los segmentos de Cantor y el perímetro de Koch; oscila (−1)ⁿ; no es infinito sumar 40 calificaciones.
- **B:** convergen 1/2 + 1/4 + … y la longitud de Cantor; divergen 1 + 2 + 3 + … y 2ⁿ; oscila 1 − 1 + 1 − …; no es infinito repartir 12 dulces.
- **C:** convergen (n + 1)/n y el área de Sierpinski; divergen los segmentos de Cantor y el perímetro de Koch; oscila 0, 1, 0, 1, …; no es infinito contar 20 escalones.
- **D:** convergen la distancia de la pelota y 1/2 + 1/4 + …; divergen 1 + 2 + 3 + … y 2ⁿ; oscila (−1)ⁿ·3; no es infinito calcular S₁₀ de una progresión aritmética.

La clave completa, con los textos exactos de cada opción, se ve en el modo profesor (`?profesor=1`, **Clave de respuestas de la forma …**).

## Correcciones al material, ajustes y límites

**Correcciones respecto a la «Propuesta de Evaluación» adjunta.** Ninguno de estos problemas pasó al examen:

- El reactivo de 0.4545… tenía dos opciones correctas (5/11 y 45/99). Ahora ninguna opción es equivalente a la respuesta.
- El reactivo de 1.777… no tenía opción correcta (vale 16/9).
- La pendiente de la tangente y la velocidad de la moneda son de la Unidad 2 y quedaron fuera.
- «lim n→6» se sustituyó por f(6); «lim» solo se usa con n → +∞.
- La etapa 0 es siempre la figura inicial, porque las soluciones 1.1.4 y 1.1.5 numeraban las etapas de forma distinta.

**Ajustes.** Todo está al inicio del bloque `<script>` de `index3.html`, con comentarios:

- `VALORES_NIVEL` define el valor de los reactivos básicos, intermedios y avanzados. Si la suma deja de ser 10, la calificación se reescala sola.
- Los datos de cada forma están dentro de cada reactivo, en tablas `{A:…, B:…, C:…, D:…}`. Los distractores y las figuras se calculan a partir de esos datos. Si cambia un dato, conviene revisar en el modo profesor que la clave tenga sentido.
- `?profesor=1` muestra el estado de Forms, la clave por forma, el resultado de ejemplo de cada forma y el verificador.

**Límites:**

- **El envío no es de un solo clic.** La página abre el formulario lleno, pero el alumno debe presionar Enviar en Forms y puede editar lo que llega. El código del Detalle disuade las ediciones, aunque no es infalible porque el archivo es público.
- **La forma por cuenta no garantiza que los vecinos sean distintos.** Dos alumnos contiguos tienen 1 en 4 probabilidades de tener la misma forma, aunque vean otro orden y otras opciones. Si quiere evitarlo del todo, use una liga `?forma=` por fila.
- **Reintentos.** Reiniciar permite volver a resolver; el reporte marca el número de intento, pero solo dentro del mismo dispositivo. Con `?forma=azar` el alumno podría cambiar de forma al reiniciar.
- **MathML.** Las fórmulas con Σ usan MathML nativo (Chrome 109+, Safari y Firefox). En navegadores muy antiguos se verían como texto plano.
- **Pruebas realizadas.** Recorrido automatizado completo de las 4 formas en un teléfono táctil simulado de 390 px (con errores deliberados en cada tipo de reactivo) y en escritorio (todo bien → 10.0 en las cuatro). También en 360 × 640 px y con el teléfono acostado, sin desbordes. No se probó en un iPhone físico ni contra un formulario real; hágalo una vez antes de aplicar.
