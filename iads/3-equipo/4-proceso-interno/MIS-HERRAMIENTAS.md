# Mis herramientas

**El manual de las herramientas de Sami: dónde mirar cuando algo no funciona.** Su calendario y Calendly, las grabaciones, los leads de Meta, el CRM y Notion.

*(Se llamaba "Proceso interno" y se renombró el 18/10: ese nombre se confundía con el día a día de un cliente, que es otra cosa y vive en la skill `iads-client-pack` y la skill `iads-client-pack`.)*

Decidido el 03/10/2026; Calendly rehecho el 04/10/2026 y repasado el 18/10/2026.

---

## Las reuniones

**Por Calendly van dos, cada una con su enlace fijo (no cambia nunca):**

- **Closing (venta):** https://calendly.com/sami-iads-agency/closing — la agenda **Álvaro** durante su llamada, o **Sami** cuando el lead entra por los anuncios de Meta, poniendo nombre, email y marca.
- **Arranque:** https://calendly.com/sami-iads-agency/arranque — la reserva el cliente **cuando ya ha dado los accesos**, no antes (el enlace se le abre al final de su alta). *(18/10: Sami ya lo renombró; el enlace del briefing viejo ya no vale.)*

**La llamada del mes (día 25)** se pacta en la llamada anterior y se manda con una **invitación de Google Calendar**. En el escalón 2 no hay más llamadas que esas dos.

**Máximo 2 reuniones de venta al día con Sami.** Si se llenan de forma habitual, se contrata un closer.

---

## Cómo sabe Calendly cuándo está libre Sami

1. **En Calendly**, las dos reuniones usan "Working hours (Default)", un horario amplio y fijo: lunes 7:30-20:00 · martes 8:00-20:00 · miércoles 7:15-19:45 · jueves 7:30-19:45 · viernes 7:30-18:15 · sábado 8:30-20:00 · domingo nada.
2. **Calendly está conectado al Google Calendar grindsociety.es@gmail.com** y quita los huecos ocupados.
3. **En ese calendario solo va como "ocupado" lo que de verdad no se puede mover:**
   - **🏫 Colegio (semana A / semana B):** bloques que se repiten cada 2 semanas hasta el 20/06/2027 (A desde el lunes 05/10, B desde el lunes 12/10). Dejan libres los recreos, la comida y los huecos sin clase.
   - **🏋️ Gym:** todos los días de 20:00 a 22:00.
   - Las reuniones con clientes (las de Calendly se apuntan solas).

**Los huecos libres también están en el calendario, como "🟢 Libre"** (en verde, desde el 05/10), pero marcados como **"Disponible"**: se ven, pero Calendly no los cuenta como ocupados. Si se crea un bloque nuevo que no deba tapar reuniones, se marca también como "Disponible".

**Ya no hay semanas A y B en Calendly** ni enlaces que cambiar cada lunes: el colegio cambia solo en el calendario.

**Si cambia algo** (exámenes, vacaciones, festivos, un día que no puede), se toca en Google Calendar y Calendly se entera solo. Ej.: el 12/10 es festivo; si ese día no hay clase, se borra ese día del colegio ("solo este evento").

**No poner en el calendario como "ocupado"** bloques de venta o de llamadas: taparían justo las horas en las que se quiere que agenden.

**Calendly es de pago** (Standard, 10 €/mes desde el 04/10/2026) para tener las dos reuniones encendidas a la vez.

---

## Grabar las llamadas (desde el 06/10/2026 · repasado el 18/10)

Las graba **Fireflies** (cuenta grindsociety.es@gmail.com, plan gratis). El resumen y la transcripción llegan por email **solo a Sami**. El Notetaker de Calendly va apagado (si no, entran dos bots).

**Para que grabe hacen falta dos cosas, y esto es lo que ha fallado:**

1. **Que la reunión esté en el Google Calendar.** Fireflies solo se une a lo que ve en el calendario. *(18/10: la reunión con Miguel de Venice no se grabó porque el enlace de Meet se mandó por WhatsApp sin crear el evento.)*
2. **Que admitan al bot.** Si la reunión la organiza otro, el anfitrión tiene que dejarlo entrar. *(07/10: el bot no fue admitido en el onboarding de la mentoría.)*

**Las dos soluciones, y las dos están puestas:**

- **Toda reunión va al calendario** (Sami, 18/10). Las de Calendly se apuntan solas; las que se montan sobre la marcha, a mano.
- **La aplicación de escritorio de Fireflies**, descargada el 18/10: graba desde el propio ordenador, sin bot, da igual quién organice y en qué plataforma. Necesita los permisos de **micrófono** y **grabación de pantalla** de macOS.

**Se avisa de palabra** al empezar: *"Grabo las llamadas para revisarlas después con mi equipo, se queda entre nosotros."* Si alguien dice que no, se para.

**Ojo con el plan gratis:** parece limitado a pocas reuniones al mes. Si se queda corto, Fathom es gratis sin límite.

## Los contactos de los anuncios entran solos al CRM (desde el 06/10/2026)

> 💤 **Dormido hasta que haya campañas** (Sami, 18/10). No hay anuncios en marcha, así que no entra ningún lead. **Y cuando se enciendan, hay que rehacerlo:** el formulario actual es del modelo viejo (clientes de packs de vídeos), así que hay que **crear un formulario nuevo** con las preguntas del modelo nuevo y **volver a conectarlo en Make**. Lo de abajo describe el montaje de hoy, que sirve de guía para rehacerlo.

Cuando alguien rellena el formulario de Meta ("iAds - Demo gratis v2", página IAds-Agency), **Make** lo manda al CRM de InfoCapitals (pestaña Leads) con origen **"Ads"**: nombre, teléfono, web (en el campo de Instagram) y una nota con *qué vende · cuánto invierte · web*.

- Escenario de Make: "Integration Facebook Lead Ads" (Facebook Lead Ads "New Lead" → HTTP POST a `/api/crm/entrada`). Tiene que estar **activo** (interruptor arriba a la derecha).
- La llave del CRM va solo en Make (cabecera `Authorization: Bearer …`). Si se rehace la llave en el CRM, hay que pegarla otra vez en Make o deja de entrar todo.
- Entran **todos** los contactos, también los no cualificados; Sami mira la nota antes de llamar: **el mínimo son 1.000 €/mes de inversión** (18/10; antes ponía 300 €, que era del modelo viejo).
- Para probarlo: Herramienta de prueba de anuncios para clientes potenciales de Meta (developers.facebook.com/tools/lead-ads-testing).

## El CRM ✅ CERRADO el 22/10 · dos bases en Notion

**La frontera, y no se cruza:** **Notion llega hasta que el cliente firma. Desde que firma, todo vive en esta carpeta** — su contrato, su alta, su panel, sus informes. *(Sami, 22/10.)* Por eso en Notion no hay nada de cobros, facturación ni duración del cliente: eso es la vida del cliente y ya tiene su sitio.

### 1 · Leads · https://app.notion.com/p/8b178452f0674668bdc8c34dbf6b0d7b

Todo lo de **antes de la reunión**. Diez campos y se acaba ahí (Sami: *"se tiene que acabar ahí"*):

**Marca · Canal · Filtro 1 · Filtro 2 · Filtro 3 · Estado · Siguiente paso · Qué día · Teléfono · Quién lo lleva**

**Los tres filtros son huecos a propósito:** todavía no está decidido qué se pregunta. Cuando se decida, se les cambia el nombre — **y son las mismas tres preguntas que irán en el formulario de Meta**.

**Los siete estados:** 1. Nuevo · 2. No contesta · 3. Seguimiento · 4. Nurture · 5. Agendada · 6. Descartado · 7. Perdido.
**Descartado y Perdido están separados a propósito** (idea de Sami): uno lo tiramos nosotros, al otro nos tira él. Si se llena uno u otro, el problema que tienes es distinto.

**Los canales no incluyen el frío:** Meta · Lead antiguo/cliente · Conocido · Recomendación. **El frío entero vive en el Notion de llamadas en frío.**

**Tres vistas:** *Todos* · *Hoy* (filtrada a **Qué día ≤ hoy**, sin los cerrados, ordenada por fecha: los atrasados salen arriba) · *Por canal* (tablero).

### 2 · Reuniones · https://app.notion.com/p/6d41efec9e7b438d9f030188412ffa09

Todo lo de **después de agendar**. En la tabla, nueve columnas: **Marca · Día y hora · Estado · Quién la agendó · Qué se le ofreció · Por qué no cerró · Siguiente paso · Qué día · Lead**.

**Y dentro de cada ficha, las 16 preguntas del informe**, en cuatro bloques (la marca · cómo están ahora · lo que quieren · cómo fue la llamada). **Son las mismas del manual de Álvaro.** En la tabla no salen a propósito: serían 25 columnas ilegibles. Se leen abriendo la ficha, justo antes de la llamada.

**Los cinco estados:** 1. Agendada · 2. Se presentó · 3. No show · 4. Cliente · 5. No cerró. **No show y No cerró separados:** una es que no vino (falla el recordatorio), la otra que vino y dijo que no (falla la llamada).

**Dos gráficos que se calculan solos:** *Cómo van* (donut por estado: show rate y cierre) y *Cuántas por semana*.

**Enlazada con Leads** por la propiedad *Lead*: desde la reunión ves de qué canal salió.

### 3 · Lo de Álvaro · https://app.notion.com/p/3fda44732c3d81a88b69d9106342c948

**No se toca.** Es un circuito paralelo y completo: su base de frío y sus reuniones. **Las reuniones de Álvaro viven ahí, las de Sami en la suya** (Sami, 22/10).

**Por qué separado y no todo junto:** por acceso, no por organización. En Notion, quien entra en una base ve todas las filas, y Álvaro es alguien de fuera que cobra por reunión. **El día que entre un setter de dentro, va en la base de Sami con "Quién lo lleva": no se crea una base nueva por persona, nunca.**

### Lo que se descartó por el camino

**El CRM de InfoCapitals** — montado y conectado a Meta, pero Sami lo probó y no le entró (*"no lo estoy entendiendo nada"*). **Se queda dormido, no se borra.**

**Una hoja de Google** (`iAds · Leads`, https://docs.google.com/spreadsheets/d/1KhxUMdBW10pTRjm4ndLrQYF6AAAWYKtKBRK6m2pCLIc/edit) — se montó como alternativa y se descartó el mismo día: **manda la costumbre, y Sami entra en Notion todos los días.**

### La única regla

**Ningún lead vivo sin fecha en "Qué día".** Lo demás se puede rellenar flojo; esto no. Un lead sin fecha no aparece en *Hoy* y se muere sin que nadie se entere — y eso ya pasó con tres del CRM viejo.

### Lo que queda

- **Los tres filtros**, que son huecos hasta que se decidan las preguntas.
- **Make → Notion** el viernes, con el formulario de Meta nuevo: los leads caen solos en la base de Leads con Canal = Meta.
- Borrar la hoja de Google y la reunión de ejemplo.

### El CRM de InfoCapitals · ⏸️ dormido (22/10)

**No se toca nada del CRM hasta que empiece a haber llamadas agendadas de verdad.** Ahora no hay campañas, ni leads de Meta, ni reuniones, así que decidirlo hoy es hablar en abstracto.

**Lo que hay que decidir ese día, todo junto:**

1. **Si el CRM es el de InfoCapitals o se coge otro.**
2. **Cómo llegan ahí las reuniones de Álvaro.** Él trabaja en su Notion —es su herramienta y no se toca— pero **lo que agenda tiene que acabar en el CRM de Sami**: o lo pasa Sami a mano cuando Álvaro avisa, o se automatiza.
3. **Qué se guarda de cada llamada.** En el CRM van **todos los leads**, no solo los que se agendan: también los que no cierran. Y hace falta que quede **de dónde salió cada uno**.
4. **Qué pasa con `3-equipo/3-ventas/LLAMADAS-VENTA.md`**, la tabla del 18/10 para decidir el nicho (tipo de marca, objeción con sus palabras, si se trabajaría a gusto). O eso son campos del CRM y la tabla se borra, o la tabla se queda solo con eso.
5. **Y actualizar lo de abajo**, que es la configuración de hoy y está vieja.

### La configuración de hoy (06/10/2026, sin tocar)

Pestaña Config. Provisional hasta la llamada de onboarding con la mentoría (dudas en `PARA-LA-MENTORIA.md`).

- **Closers:** Sami. **Setters:** Álvaro (entró el 12-14/10).
- **Sources:** Ads (tiene que llamarse así: lo manda Make) · Llamadas en frío · Contactos calientes · Recomendaciones · Calendario · Otro.
- **Avatares:** los 5 nichos (Ropa, Cosmética, Joyería, Accesorios, Suplementación).
- **Programas:** ⚠️ **siguen siendo los del modelo viejo** (Pack Base 350/500, Crecimiento 850, Escala 1200). **Tienen que ser:** Escalón 1 = 500 · Escalón 2 = 1.300 · Escalón 3 = 2.500 (+ IVA). **Lo cambia Sami en el CRM**: hasta entonces, los números de cada venta salen mal.
- **Formas de cierre:** Suscripción mensual · Pago único (encargo suelto).
- **Objetivos:** ⚠️ los que hay son de la meta vieja (1.750 €/mes con 5 clientes a 350 €). **La meta de octubre son llamadas agendadas**, 3 de suelo y 5 de objetivo (`1-negocio/5-METAS.md`). Cierre 20-35 % · se presentan el 75 % · contestar en 60 min.

## Notion · rehecho el 18/10/2026

**La página es `iAds · Llamadas en frío`:** https://app.notion.com/p/3fda44732c3d81a88b69d9106342c948

**Por qué se rehízo:** la vieja tenía seis vistas por base ("todo con fecha", "mis marcas", "embudo", "fase 5", "objeciones"…) y ni Sami se aclaraba. **Tres cosas y una vista buena cada una.**

- **A quién llamo** — las marcas. Siete columnas y ordenadas por fase, así que las de "por llamar" salen arriba. Es lo único que Álvaro toca a mano.
- **Reuniones** — una ficha por reunión agendada. Se rellena con el formulario **"He agendado una reunión"** (la marca, la fecha y las preguntas del informe). La pestaña **"Próximas"** enseña las pendientes con lo que decide si encaja: cuánto invierte y quién le lleva los anuncios.
- **Mi día** — su parte diario, con el formulario **"Cómo me ha ido hoy"**.

**Lo que aprendimos montándolo:** los formularios **no se pueden rellenar de preguntas desde Claude** (solo acepta la primera). Si hay que montar otro, las preguntas se añaden a mano con el **+**, eligiendo campos que ya existan. Y la pregunta del nombre tiene que ser de tipo **Title**, o las fichas salen sin nombre.

**La página vieja** (`📞 iAds — Llamadas en frío`) sigue existiendo con los datos de prueba. Se borra cuando Álvaro esté trabajando en la nueva.

## La factura

La lleva la madre de Sami (decidido el 06/10/2026).
