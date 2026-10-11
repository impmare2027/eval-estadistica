# Guía de configuración — envío de resultados a Microsoft Forms

**Cómo funciona:** el alumno abre la liga, resuelve la actividad y, al final, presiona **"Enviar mi resultado a mi profesor"**. Se abre tu formulario de Microsoft Forms con sus datos y resultados ya escritos; solo presiona **Enviar**. Las respuestas se acumulan en tu cuenta y las bajas a Excel cuando quieras. El alumno ya no te manda ningún archivo.

Tiempo estimado de configuración: 15 a 20 minutos, una sola vez.

---

## Parte 1 — Crear el formulario

1. Entra a **forms.office.com** con tu cuenta Microsoft (institucional o personal).
2. **Nuevo formulario** → título: *Resultados Unidad 1 — Estadística y Probabilidad I*.
3. Agrega **7 preguntas de tipo "Texto"** con estos títulos (el orden no importa):

   | Pregunta | Nota |
   |---|---|
   | Nombre completo | |
   | Número de cuenta | Déjala como texto, sin validación numérica |
   | Grupo | |
   | Fecha y hora | |
   | Calificación | Déjala como texto |
   | Resumen | |
   | Detalle | Activa **"Respuesta larga"** |

4. **Quién puede responder** (⋯ → Configuración). Como tus alumnos tienen cuenta institucional:
   - Elige **"Solo las personas de mi organización pueden responder"**. Esto exige que el formulario esté creado con **tu cuenta institucional del mismo dominio** que la de los alumnos. Si lo creas con una cuenta personal o de otra organización, ellos no podrán entrar.
   - Activa **"Registrar nombre"**: Forms guardará automáticamente el nombre y el correo con el que cada alumno inició sesión, y ese dato no lo puede editar el alumno.
   - Activa **"Limitar a una respuesta"** si no quieres envíos repetidos.
   - Si quieres limitarlo solo a tu grupo, usa **"Personas específicas de mi organización"** y agrega a tus grupos o alumnos.
5. **Vínculo de rellenado previo:**
   1. En el menú **⋯** (más opciones del formulario) elige **"Obtener vínculo de rellenado previo"**.
   2. En cada pregunta escribe **exactamente** este marcador:

      | Pregunta | Escribe |
      |---|---|
      | Nombre completo | `TOK_NOMBRE` |
      | Número de cuenta | `TOK_CUENTA` |
      | Grupo | `TOK_GRUPO` |
      | Fecha y hora | `TOK_FECHA` |
      | Calificación | `TOK_CALIF` |
      | Resumen | `TOK_RESUMEN` |
      | Detalle | `TOK_DETALLE` |

   3. Presiona **"Obtener vínculo de rellenado previo"** y luego **"Copiar vínculo"**.

> Si no ves la opción de rellenado previo (depende de la versión o de la configuración de tu institución), avísame: hay una variante en la que el alumno copia su resultado y lo pega en el formulario.

## Parte 2 — Poner el vínculo en la actividad

**Opción A (la más fácil):** pégame el vínculo en el chat y te devuelvo `index.html` listo.

**Opción B:** abre `index.html` con el Bloc de notas, busca esta línea y pega el vínculo **entre las comillas**:

```js
const FORMS_PREFILL_URL = '';
```

## Parte 3 — Probar antes de dárselo a los alumnos (5 minutos)

1. Abre `index.html`, regístrate con datos de prueba y resuelve la actividad.
2. En *Resultados*, presiona **"Enviar mi resultado a mi profesor"**.
3. Se abre Forms con **los 7 campos llenos**. Presiona **Enviar**.
4. En Forms → pestaña **Respuestas** debe aparecer tu envío.
5. **Repite la prueba con una cuenta de alumno** (o pídele a un alumno de confianza que lo haga). Con el formulario restringido a la organización, Forms pedirá iniciar sesión, y hay que confirmar que **los datos siguen rellenados después de iniciar sesión**. Si salen vacíos, avísame y cambiamos al método de "Copiar mi resultado".

Si algún campo sale vacío, el marcador de esa pregunta se escribió distinto en el paso 5 de la Parte 1. Repite ese paso y vuelve a copiar el vínculo.

## Parte 4 — Darles la liga a los alumnos

OneDrive y SharePoint **no muestran archivos HTML como página web**, así que necesitas una de estas opciones:

- **Sin liga (la más sencilla):** envía `index.html` por Classroom, Teams, correo o USB. El alumno lo abre desde su equipo o celular. Solo necesita internet al final, para abrir el formulario.
- **GitHub Pages (liga gratuita):**
  1. Crea cuenta en github.com → **New repository** (público), por ejemplo `eval-estadistica`.
  2. **Add file → Upload files** y sube `index.html`.
  3. **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
  4. En 1 o 2 minutos tendrás la liga `https://TU-USUARIO.github.io/eval-estadistica/`. Esa es la que compartes.
- **Netlify Drop:** en app.netlify.com/drop arrastra una carpeta que contenga `index.html`; crea una cuenta gratis para que la liga no caduque.

## Parte 5 — Recibir y usar los resultados

- En Forms → **Respuestas** ves cada envío. Con **Abrir en Excel** descargas todas las respuestas hasta ese momento; repite cuando quieras actualizar.
- Verás una fila por alumno: nombre, cuenta, grupo, fecha, calificación, resumen y detalle.
- **Cómo leer "Detalle":** `A1.4=2[Nominal];` significa que el reactivo 4 de la Actividad 1 se resolvió en 2 intentos y el primer error fue colocarlo en "Nominal". `=1;` es acierto al primer intento. Las preguntas de la Actividad 3 solo muestran el número de intentos.

### Revisar que nadie haya cambiado sus datos o su calificación
Los campos del formulario se pueden editar antes de enviar. Con "Registrar nombre" activado, tu hoja trae además las columnas de **nombre y correo de la cuenta institucional**, que sí son confiables: compáralas con el nombre y la cuenta que el alumno escribió. Para la calificación, el número de aciertos se puede recalcular desde "Detalle". Si Detalle quedó en la columna **G**, esta fórmula cuenta los aciertos al primer intento:

```
=(LEN(G2)-LEN(SUBSTITUTE(G2,"=1;","")))/3
```

La calificación correcta es esa cifra ÷ 23 × 10. Ajusta la letra de columna según tu hoja.

## Límites que conviene saber
- **El envío no es 100 % automático:** el alumno debe presionar *Enviar* en Forms. Quien no lo haga no aparecerá en tus respuestas, así que conviene recordárselo en clase.
- **Los datos viajan en el vínculo y se pueden editar** antes de enviar (por eso la fórmula de revisión y el registro de nombre/correo). Evitarlo del todo requiere un servicio que califique en un servidor, y eso no se puede con Forms solo.
- **Privacidad:** nombres y números de cuenta quedan guardados en tu cuenta. Avisa a los alumnos.
- **Respaldo:** el botón de descargar CSV sigue disponible si algún alumno no puede abrir el formulario.
