---
name: iads-client-pack
description: "El paso a paso de un cliente de iAds, desde que hay una reunión agendada hasta que renueva o se va. Úsala siempre que se hable de un cliente o de un prospecto que ya tiene reunión: 'me han agendado una reunión con X', 'ha cerrado X', 'me ha pagado X', 'ya ha rellenado el alta', 'ya me ha dado los accesos', 'prepárame la llamada de arranque de X', 'prepárame el plan de vídeos', 'toca la tanda de X', 'acabo de hacer la entrega', 'prepárame la llamada del mes', 'X no contesta', 'X quiere cancelar', 'el cobro de X ha fallado', '¿qué toca hoy?', '¿cuánto deja X?'. Todo lo del cliente se guarda en su carpeta (2-clientes/[escalón]/[marca]/). Para PRODUCIR los vídeos se usa iads-produccion-pack. Para preparar una llamada de venta con alguien que aún no paga, iads-reunion."
---

# iAds · El paso a paso del cliente

Versión 3 · 19/10/2026, reescrita entera con Sami para el modelo nuevo (vídeos + anuncios de Meta). **Sustituye al proceso viejo** (briefing, validación, llamada de resultados), que está en `archivo/`.

Esta skill **conduce**. Sami no se sabe comandos ni tiene por qué: en cada momento se le dice **qué toca, qué se le ha preparado y qué mensaje manda él**, y se espera su respuesta. Si no se ha leído `CLAUDE.md` en este chat, leerlo antes.

---

## Cómo hablar con Sami

- Español sencillo, frases cortas, sin jerga. **Un paso cada vez.**
- **Formato con espacios:** cada punto en su línea, la explicación debajo y una línea en blanco antes del siguiente.
- Lo que vive el cliente y lo que se hace por dentro, **por separado**.
- **Los mensajes al cliente, en plural** ("nos cuentas", "te mandamos"), salvo los que firma Sami en primera persona.
- Cada mensaje que tenga que mandar, **ya relleno** con su nombre, el día y la hora. Nunca un `[nombre]` sin rellenar si el dato se sabe.
- **Opinión, no menú.** Si hay que decidir, se le dice qué haría yo y por qué.

## Las reglas que no se rompen

**0 · Clientes antiguos.** Los que llevan `proceso: antiguo` (todos los de antes del 01/10/2026, en `2-clientes/modelo-videos/`) **no siguen este paso a paso**: vale solo lo que diga su ficha. Su carpeta no se reestructura.

**1 · Todo lo del cliente vive en su carpeta.** Cada llamada, mensaje importante, decisión o número se guarda en el momento en `2-clientes/escalon-[N]/[marca]/`. Nada se queda solo en la conversación.

**2 · Las fechas que se guardan son las reales** (pagó, terminó el alta, lanzó, publicó). Las calculadas las saca `HOY.md`.

**3 · Lo que no esté decidido no se inventa:** se le dice a Sami y se apunta en `IDEAS.md`.

**4 · Al acabar cada paso, commit** con lo que se ha hecho.

**5 · Delante del cliente, "nuestro equipo de media buyers"**, en plural. Por dentro es Marc.

---

# Lo primero: ¿en qué punto está?

| Si Sami dice… | Ve a |
|---|---|
| "me han agendado una reunión con X" | **Antes de que pague → 1** |
| "ha cerrado X" / "me ha pagado X" | **Antes de que pague → 2** |
| "ya ha rellenado el alta" / "ya me ha dado los accesos" | El primer mes de **su escalón** |
| "prepárame la llamada de arranque / el plan de vídeos / la del mes" | **Lo que se prepara** |
| "no contesta" / "quiere cancelar" / "ha fallado el cobro" | **Cuando algo falla** |
| "¿qué toca hoy?" | `python3 sistema/scripts/hoy.py` y se lee `HOY.md` |

---

# ANTES DE QUE PAGUE

## 1 · Hay una reunión agendada

**Quién la agendó decide los mensajes:** si fue **Álvaro**, grupo de WhatsApp de tres; si la agendó **Sami** desde Meta, chat directo. Los dos juegos están en `4-plantillas/clientes/escalon-2/2-RECORDATORIOS.md`.

**Qué se hace:**
1. Se le dan a Sami **los recordatorios con su día y su hora ya puestos** (nada más agendar, 48 h, 24 h, 12 h, 1 h y la llamada 5 min antes).
2. Se prepara la llamada con la skill **iads-reunion**: el demo de 5-10 s con su producto, 2-3 ideas y la pantalla del camino (`escalon-2/3-CAMINO-15-DIAS/camino.html?c=[Marca]`).
3. **Si no se presenta:** antes de la hora los mensajes los manda Álvaro; de la hora en adelante, Sami (la llamada y el reagendar).

**La llamada la lleva Sami con su guion de Notion.** Aquí no se improvisa nada.

## 2 · Ha cerrado

**Se le pregunta a Sami, siempre:** qué marca, qué escalón, qué precio, de dónde salió, quién la cerró, si ha pagado y qué día.

**Y se hace, en este orden:**

1. **El enlace de pago** (mensaje 19 de los mensajes de su escalón). Hasta que no paga, no se empieza nada.
2. **El contrato**: se rellenan los huecos de `escalon-[N]/4-CONTRATO.md`, se genera el PDF y se le da a Sami el mensaje para mandárselo por WhatsApp. Se firma a mano y se devuelve; se guarda la captura.
3. **Su carpeta**: se copia `2-clientes/escalon-[N]/_PLANTILLA/` y se le pone su nombre en minúsculas y con guiones.
4. **Su carpeta de Drive**: se duplica `iAds · PLANTILLA cliente — duplicar`, se renombra a `[Marca] — Contenido iAds` y se comparte con él.
5. **El grupo de WhatsApp.**
6. **Su enlace de alta**: `alta.iads-agency.es/?c=[Marca]` para el escalón 2, y `&e=1` para el escalón 1.
7. **La factura:** se le recuerda a Sami que la hace su madre.
8. **Se apunta la llamada de venta** en `3-equipo/3-ventas/LLAMADAS-VENTA.md`, con el tipo de marca y la objeción con sus palabras. *(Sale de la transcripción, no de memoria.)*
9. **Si lo trajo Álvaro:** fila en `3-equipo/3-ventas/alvaro/PAGOS.md`.

---

# EL PRIMER MES · ESCALÓN 2

**Los días cuentan desde que paga.** Todo el detalle de cada pieza está en `4-plantillas/clientes/escalon-2/`.

**Día 0 · Paga.** El contrato, su alta y el grupo. *(Mensaje 1.)* **Y se le crea su panel** (abajo, "Montar el panel de un cliente").

**Días 0-2 · Los accesos.** El cliente los da desde su alta. **Se comprueban entrando nosotros**, no se le pregunta si ha podido. Mientras falte alguno, **el plazo de lanzamiento no empieza a correr** (contrato, cláusula 2). *(Mensajes 1b, 1c, 2, 2b.)*

**Días 1-3 · La llamada de arranque.** La reserva él cuando ya ha dado los accesos. **La hace Sami solo** (Marc no entra). Guion: `6-LLAMADA-ARRANQUE.md`. **De ella sale el presupuesto del mes**, que es la única cifra que tiene que sacar.

**Día 4 · Marc** pasa qué anuncios le han funcionado antes al cliente.

**Día 6 · Tu plan de vídeos.** Documento de Google con `7-PLAN-DE-VIDEOS.md`: las apuestas, cómo van a ser, qué recibe y su web.

**Días 6-12 · Se produce.** Con `iads-produccion-pack`. *(Mensaje 6: el adelanto del día 9.)*

**Día 11 · Marc** pasa **el plan de acción entero**: las campañas, el presupuesto de cada una y los números que espera del mes.

**Día 12 · La tanda y su plan de acción.** La carpeta con el contenido, y el documento aparte con `8-PLAN-DE-ACCION.md`. **24 horas para decir si algo no encaja.**

**Día 13 · Se lanza.** Campaña funcionando con **al menos 5 anuncios**. Es la fecha que promete el contrato (cláusula 2), así que no se mueve. *(Mensaje 6.)* **Y su panel pasa a `enMarcha: true`** con los primeros números.

**Días 13-30 · Corriendo.** Su panel al día · **informe cada lunes** (`9-INFORME-DEL-LUNES.md`, con los números que pasa Marc el domingo) · hacia el día 19-23, **la segunda tanda** con versiones de lo que va mejor.

**Día 22 · Marc** pasa sus conclusiones del mes.

**Día 25 · La llamada del mes** (`10-LLAMADA-DEL-MES.md`) y, **después**, su informe (`11-INFORME-DEL-MES.md`).

**Día 30 · Renueva.** Stripe cobra solo.

---

# EL PRIMER MES · ESCALÓN 1

**Los días cuentan desde que TERMINA el alta**, no desde que paga (contrato, cláusula 2). El cobro sí cuenta desde el pago: **son dos relojes distintos.**

**Día 0 · Paga.** Contrato, su alta (más larga: no hay llamada de arranque) y el grupo. *(Mensaje 1.)*

**Días 1-3 · Conocer su marca, sin llamada.** Se comprueba que el **acceso de analista** funciona entrando. Se lee su alta, se miran sus referencias, sus anuncios y su competencia, y se eligen los ángulos.

**Día 4 · Los guiones.** Documento con `6-GUIONES.md`: primero el mapa de ángulos, después los guiones. **Tiene 24 horas**; si no dice nada, se produce. *(Mensaje 5.)*

**Días 5-9 · Se produce.** Con `iads-produccion-pack`. **Día 6: el vídeo muestra** (`7-VIDEO-MUESTRA.md`), 24 horas.

**Día 10 · La llamada de entrega** (`8-LLAMADA-ENTREGA.md`). Se le enseñan los vídeos compartiendo pantalla, **se cierra el día en que publica** y después se le manda **"Cómo usar tus anuncios"** (`9-COMO-USAR-TUS-ANUNCIOS.md`) completado con lo que se habló.

**Día ~15 · ¿Están publicados?** Se entra en su Meta a mirar. *(Mensaje 9: uno si están y otro si no.)* **Es el aviso temprano del problema clásico de este escalón.**

**Día ~22 · Sus números.** Con el acceso de analista, se mira qué vídeos han funcionado y se reparten en funciona / regular / no tira / sin datos.

**Día 25 · La llamada del mes** (`10-LLAMADA-DEL-MES.md`) y, después, su informe (`11-INFORME-DEL-MES.md`). **Si sus anuncios no sacan partido a los vídeos, ahí se le propone el escalón 2**, con las reglas de cuándo sí y cuándo no.

**Día 30 · Renueva.**

---

# DEL SEGUNDO MES EN ADELANTE

**Escalón 2:** empieza con el plan de la llamada del 25 · **anuncios nuevos cuando hacen falta** (en 5 días como mucho desde que uno se cansa), mínimo una tanda al mes · panel al día e informe cada lunes · día 25, llamada e informe · día 30, renueva. **Sin llamada de arranque ni plan de vídeos: ya le conocemos.**

**Escalón 1:** lo mismo desde los guiones, sin alta. **El vídeo muestra solo si hay un estilo nuevo.** **La entrega, sin llamada** (mensaje 8): su carpeta y un mensaje. La única llamada es la del 25.

---

# MONTAR EL PANEL DE UN CLIENTE

**El panel es uno solo para todos**, en `panel.iads-agency.es`. No se duplica ni se copia nada: lo que cambia es **una fila en una hoja**. Todo lo demás (diseño, contraseña, dominio) ya está hecho.

**La hoja es `iAds · Panel`**, en el Drive de Sami. Tres columnas y una fila por cliente:

| marca | clave | datos |
|---|---|---|
| `nordik` | `nordik-7421` | `{"marca":"Nordik", …}` |

**marca** · lo que va en el enlace. **Minúsculas, sin acentos, sin espacios**: así es como lo busca el script.

**clave** · su contraseña. **Se inventa una por cliente** (su marca y cuatro números vale). Nunca se repite entre clientes.

**datos** · el bloque de números en JSON. Lo escribe Claude.

### El día que paga (día 0)

1. **Se le crea la fila** con `enMarcha: false`, su fecha de lanzamiento y lo que se sepa de él. El panel le dirá *"Tus anuncios se lanzan el [día]"* y nada más: **sin ceros ni gráficos vacíos.**
2. **Se le manda el enlace con la contraseña**, dentro del mensaje de bienvenida:
   > Aquí vas a ver tus resultados: panel.iads-agency.es/?c=[marca] · tu contraseña es [clave]

### El día que se lanza (día 13)

Se pone **`enMarcha: true`** y entran los primeros números. La próxima vez que abra verá la bienvenida y, detrás, su panel. **Va dentro de los números del lanzamiento, no es un paso aparte.**

### Cada lunes

Se actualiza la columna `datos` con lo que pasó Marc el domingo. **El cliente no tiene que hacer nada**, ni volver a meter la contraseña: su navegador se acuerda.

### Si se va

Se deja su fila **congelada** con el último mes, no se borra. Si vuelve, su panel sigue ahí.

**El detalle técnico, en `4-plantillas/clientes/escalon-2/13-PANEL/LEEME.md`**: los dos modos, cómo se cambia la página y cómo se vuelve a subir.

---

# CUANDO ALGO FALLA

Los textos están en `escalon-[N]/12-MENSAJES.md`. **Se le da a Sami el mensaje relleno, no el archivo.**

| Qué pasa | Qué se hace |
|---|---|
| No empieza el alta | Mensaje a las 24 h · a los 4 días, aviso |
| No da los accesos | A las 48 h · **el plazo de lanzamiento no corre mientras falten** |
| No reserva la llamada de arranque | Mensaje, llamada a las 24 h y dos opciones concretas a las 48 h |
| No contesta en 5 días | Mensaje · **a los 5 seguidos, el servicio queda en pausa y el cobro no se para** |
| El cobro falla | Mismo día con el enlace · a los 3 días otro aviso · **a los 5, cancelado** |
| Quiere cancelar | **Siempre a llamada.** Nunca por WhatsApp |
| Quiere pausar un mes | **También a llamada** |
| Mueve o no se presenta a una llamada | Se reagenda y **las fechas se mueven lo mismo** |
| Habla de dinero o "no veo ventas" | **Se le llama esa misma semana, con números** |
| Pide algo que no entra | Se dice que no **con el porqué en la misma frase** |
| Meta le rechaza anuncios | Se le cuenta antes de que lo vea él |
| Quiere cambiar de escalón | **Desde la siguiente renovación**, con contrato nuevo |
| Se va | Mensaje de despedida · cancelar en Stripe · motivo a su ficha · carpeta a `inactivos/` |

---

# LO QUE SE PREPARA

Cuando Sami lo pide, se lee lo que haga falta y se le deja hecho en la carpeta del cliente.

| Sami dice | Se lee | Se devuelve |
|---|---|---|
| "prepárame la llamada de arranque de X" | su alta (carpeta *iAds · Altas* del Drive) y lo que haya visto Marc | las 2-3 respuestas flojas con su pregunta, lo visto en su cuenta y una hipótesis de ángulos |
| "prepárame el plan de vídeos" | su alta y la transcripción del arranque | el documento relleno en su carpeta |
| "prepárame los guiones" *(escalón 1)* | su alta y sus referencias | el mapa de ángulos y los guiones |
| "prepárame el plan de acción" | lo que pasó Marc el día 11 | el documento relleno |
| "el informe del lunes de X" | los números que pasó Marc el domingo | el mensaje de WhatsApp, listo, **y su panel actualizado** |
| "prepárame la llamada del mes" | el panel, lo que pasó Marc el 22 y su alta | sus números con la lectura escrita y las preguntas que va a hacer con su respuesta |
| "el informe del mes" | la transcripción de esa llamada | el documento, **después** de la llamada |

---

# ESCALÓN 3

**No existe todavía.** Si alguien lo pide, se le dice a Sami y se para: su proceso no está escrito y no se improvisa (`1-negocio/3-QUE-VENDEMOS.md`).
