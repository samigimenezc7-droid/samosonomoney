# iAds — el mapa (léelo entero al empezar cada chat)

Este archivo es para Claude. Cualquier chat nuevo empieza sin el contexto de las conversaciones anteriores: **todo lo decidido está escrito en esta carpeta**, y este mapa dice dónde. Si algo de aquí choca con un archivo más concreto, manda el archivo concreto (y se corrige este mapa). La skill de clientes `iads-client-pack` (reescrita el 03/10/2026) es **el paso a paso** de un cliente; para producir, `iads-produccion-pack`.

Última actualización: 18/10/2026.

---

## Qué es iAds

Agencia de anuncios hechos con IA (vídeos e imágenes para Meta y TikTok) para tiendas online de producto físico. La lleva **Sami** (16 años; factura su madre, que es autónoma). Desde el 10/10/2026 (modelo nuevo, tras la mentoría) vende **3 escalones mensuales** sin permanencia, todo **+ IVA**:

- **1 · Vídeos:** 10 vídeos + 25 imágenes. 500 €/mes. Solo se ofrece en la llamada, si el cliente ya tiene quien le lleve bien los anuncios.
- **2 · Vídeos + anuncios (el principal):** hasta 15 vídeos + 35 imágenes, y **le llevamos los anuncios de Meta** (Marc). 1.300 €/mes desde el primer cliente (14/10: sin precio de arranque).
- **3 · Todo:** lo del 2 con más contenido, orgánico, email, cara de marca y creadoras. 2.500 €/mes. Borrador.

Los packs de antes (Base, Crecimiento, Escala) están en `archivo/modelo-contenido/`. Detalle en `1-negocio/3-QUE-VENDEMOS.md`. Números (lo que deja cada cliente, solo o delegado) en `1-negocio/6-NUMEROS.md`.

---

## Cómo trabajar con Sami (obligatorio)

1. **Español sencillo, frases cortas, sin jerga.** Nada de "hook", "CTA", "ICP" con él: se dice lo que pasa.
2. **Formato con espacios:** cada punto en su línea, la explicación justo debajo y **una línea en blanco** antes del siguiente. Todo junto le satura.
3. **Proponer en el chat antes de tocar un archivo.** Una pieza cada vez, y esperar su OK. Excepción: cuando dice "hazlo", "cámbialo" o "guárdalo".
4. **Separar lo que vive el cliente de cómo se trabaja por dentro.** Si mezclas los dos en la misma explicación, se lía.
5. **No ir "por encima".** Si pide revisar algo, se entra archivo por archivo y se dice lo que falta de verdad.
6. **"Deberes"** son solo las cosas que hace Sami solo. Lo que se trabaja juntos va a "pendiente".
7. **Enfoque práctico:** lo que sirve ya con 1-5 clientes va antes que la estructura para escalar.
8. **Las afirmaciones de los clientes se apuntan tal cual**, sin suavizarlas por cuenta propia.

9. **Opinión, no menú.** Cuando haya que decidir, dile qué harías tú y por qué, con el porqué pegado a cada cosa. Nada de "lo bueno, lo malo, tú eliges". **Un tema por respuesta**: lo demás que salga se apunta en `IDEAS.md` y se le dice en una línea.

---

## El método de la mentoría (`7-mentoria/`) — desde el 07/10/2026

Es el libro de consejos de InfoCapitals, metido dentro de iAds para tenerlo todo en un sitio.

- **Se mira siempre que haya que decidir algo del negocio:** a quién vendemos y qué le decimos, oferta y precio, conseguir clientes (anuncios, frío, perfil), llamadas de venta y seguimiento, entrega y renovaciones, equipo (productores, setter) y números. Primero `7-mentoria/el-metodo.md` (en qué orden se tocan las cosas) y luego el SOP que toque en `7-mentoria/sops/`, **aplicado a iAds, no en general**.
- **No se mira** para producir vídeos, el papeleo de un cliente (contrato, recordatorios, Drive) ni cosas técnicas (Make, Calendly, calendario): ahí no dice nada.
- **Lo que su carpeta decía del negocio de Sami no se usa** (no se copió su `contexto/` ni `tuyo/`). El negocio es lo que está en iAds. Su bandeja de decisiones pendientes es nuestro `IDEAS.md`.
- **Si su método choca con algo ya decidido en iAds, se le dice a Sami** qué choca y por qué, y decide él.
- **De `7-mentoria/COMO-RESPONDE-LA-IA.md` (su CLAUDE.md, renombrado para que no mande sobre este mapa)** se aplica: diagnóstico y no menú, el porqué pegado, un tema por respuesta, toda cifra con su cuenta, no inventar números, no prometer resultados. **Las normas de cómo trabajar con Sami de arriba siguen mandando** (formato con espacios, español sencillo, proponer antes de tocar archivos).
- **Versiones nuevas:** cuando manden un zip nuevo, se sustituyen dentro de `7-mentoria/` solo `sops/`, `plantillas/`, `el-metodo.md`, `LEEME.md` y `VERSION.md`, y su `CLAUDE.md` nuevo se guarda otra vez como `COMO-RESPONDE-LA-IA.md`. Nada más de iAds se toca. Tenemos la v1 (29/08/2026).
- **Es privado:** no se reparte ni se sube a ningún sitio público (condición suya). Este repo es solo local.

---

## Las carpetas

```
1-negocio/     quiénes somos, a quién vendemos, qué vendemos, cómo lo entregamos (lo que vive el cliente), metas, números
2-clientes/    modelo-videos/ (activos/ · inactivos/) con el negocio de antes · escalon-1/ · escalon-2/ · escalon-3/ con los nuevos. Cada cliente en la carpeta de su escalón de hoy; si sube o baja, su carpeta se mueve. El panel no mira lo que esté en inactivos/. Detalle en 2-clientes/LEEME.md
3-equipo/      1-EQUIPO (cómo se organiza) · 2-produccion/[productor]/ (FICHA, PAGOS, plantillas) · 3-ventas/ (setter en frío, crm-futuro) · 4-proceso-interno/ (reuniones y enlaces de Calendly, colegio y gym en Google Calendar, Notion, factura) · 5-media-buyer/[persona]/ (FICHA, ACUERDO, PAGOS): quien lleva los anuncios de Meta
4-plantillas/  clientes/ (1-11) · productores/ (1-10) · scripts/ (PDF del contrato, contrato del productor, informe, onboarding) · assets/ (logo)
5-campanas/    servicio aparte de contenido + gestión de campañas con Marc (50/50). NO es iAds, no se mezcla
6-marketing/   conseguir clientes para iAds: anuncios (1-ANUNCIOS.md), provisional hasta la formación de Sami
sistema/       skills/ (clientes, productor, reunion) y scripts/ (hoy.py, copia.sh). Sami no lo abre
HOY.md       lo que toca hoy (lo genera sistema/scripts/hoy.py)
IDEAS.md       pendientes, ideas y el plan acordado
PARA-LA-MENTORIA.md  temas para sacar en las llamadas con la mentoría (InfoCapitals / Guillermo)
PLAN-MODELO-NUEVO.md  el plan para pasar al modelo nuevo (vídeos + anuncios), archivo por archivo
7-mentoria/    el método de InfoCapitals (su "carpeta de información privilegiada"): el-metodo.md, sops/, plantillas/. Es su libro: no se toca
```

---

## Si Sami habla de… ve aquí

**Un cliente nuevo ("tengo un nuevo cliente")**
- Usa la skill **iads-client-pack** (`sistema/skills/clientes/SKILL.md`).
- Pídele la transcripción de la llamada de venta **y además hazle siempre las preguntas por escrito**: pack, precio, marca, web, de dónde salió, quién lo cerró, si ha pagado y qué día, quién lo produce (él o qué productor) y quién hace las llamadas de briefing y validación.
- Después, el paso a paso: contrato (`archivo/modelo-contenido/4-plantillas/scripts/contrato_pdf.py`, plantilla por defecto) + onboarding + el WhatsApp para mandarlos; recordar la factura; crear su carpeta con la estructura nueva; avisar al productor (`archivo/modelo-contenido/4-plantillas/clientes/11-MENSAJES.md`).
- **El paso a paso completo está en la skill** (pasos 1 a 13).

**Una llamada con un cliente**
- La plantilla está en `4-plantillas/clientes/`: 4 briefing · 6 validación · 7 entrega · 8 resultados.
- Dale **siempre**: la plantilla (rellena si es de las que se rellenan), **los recordatorios con día y hora** (48 h, 24 h, 12 h, 1 h y llamada 5 min antes, `10-RECORDATORIOS.md`), quién la hace y qué toca después.
- Después de cada llamada, Sami pega la transcripción: se guarda en `6-llamadas/[tipo]/Transcripción [tipo] — DD-MM-AAAA.md`.

**La ficha de una marca** → `interno/MARCA.md` dentro de la carpeta del cliente (`2-clientes/escalon-2/[marca]/` o la que le toque), con la plantilla `4-plantillas/clientes/comunes/FICHA-MARCA.md`. Es herramienta de Claude.

**El informe del mes** → plantilla `archivo/modelo-contenido/4-plantillas/clientes/9-INFORME-MES.md`; se escribe en Markdown y se saca el PDF con `4-plantillas/scripts/informe_pdf.py`. Se manda el **día 25**. Resumen escrito "desde el corazón", nada de tono de agencia.

**Una venta / un prospecto / una reunión de closing** → skill **iads-reunion** (`sistema/skills/reunion/SKILL.md`) y `archivo/modelo-contenido/4-plantillas/clientes/1-LLAMADA-VENTA.md` (incluye los recordatorios anti no-show).

**Un productor nuevo ("he encontrado a un productor / creador")** — paso a paso

Ve paso a paso con Sami: en cada uno, dile **qué toca, qué le preparas tú y qué mensaje manda él**. No pases al siguiente hasta que el anterior esté hecho. Plantillas en `4-plantillas/productores/`.

1. **Preguntas a Sami:** nombre, cómo lo ha encontrado y si ya le ha contado algo de iAds.
2. **Mensaje inicial** (`1-MENSAJE-INICIAL.md`): se lo das relleno con su nombre. Explica qué es iAds, que cobra 65/125 € por pack Base y que necesita Claude de pago. Lleva el enlace al formulario.
3. **Formulario** (`2-FORMULARIO-FILTRO.md`): cuando Sami diga que lo ha rellenado, lees la hoja "iAds — Filtro Productores (Responses)" por el conector de Drive y das el veredicto: pasa / no pasa / dudoso, con el motivo en una línea, para qué clientes encaja y si podría hacer llamadas. Se guarda en su ficha.
4. **Si pasa → contrato** (`3-CONTRATO-PRODUCTOR.md`): preguntas a Sami cuándo prefiere cobrar el productor (al entregar o a final de mes) y si hará llamadas con clientes. Generas el PDF con `4-plantillas/scripts/contrato_productor_pdf.py` y le das el mensaje para mandarlo. Hasta que responda "de acuerdo", no recibe nada más.
5. **Crear su carpeta** `3-equipo/2-produccion/[clave]/`: `FICHA.md` (de `9-FICHA-PRODUCTOR.md`, con los datos del formulario; la nota la pone Sami), `PAGOS.md` vacío (con la cabecera de la tabla) y `plantillas/` con su contrato en PDF.
6. **Kit de bienvenida** (`4-KIT-BIENVENIDA.md`): los Looms y la skill del productor (zip de la última versión). **Ojo:** el kit está aparcado hasta que Sami grabe los Looms; si aún no están, avísale.
7. **Prueba** (`5-PRUEBA.md`): montas en Drive la carpeta con el kit de un cliente antiguo (p. ej. Wondernastic) y le das el mensaje. 3 días. Sin pago (iAds pone los créditos). Cuando entregue, Sami la revisa solo; tú le ayudas con la lista de qué mirar. Resultado: pasa / casi (segunda ronda) / no pasa.
8. **Si pasa:** queda listo para su primer cliente. Sus 2-3 primeros packs, Sami revisa cada vídeo de cerca (nivel "nuevo" en su ficha).
9. **Con cada cliente** (`6-ENCARGO-AL-PRODUCTOR.md`): carpeta del encargo en Drive + fila en su `PAGOS.md` + aviso (`archivo/modelo-contenido/4-plantillas/clientes/11-MENSAJES.md`). Revisión con Sami el día 6 (`7-LLAMADA-REVISION.md`). Pago (`8-PAGO.md`). Ficha al día.
10. **Si se va** (`10-SALIDA.md`): cerrar lo pendiente, pagarle, quitarle los accesos, recordarle el contrato y poner su ficha en `estado: inactivo`.

**Revisar candidatos sueltos:** "revisa los candidatos" → leer la hoja por el conector de Drive, veredicto por persona y guardarlo.

**Su skill** es `iads-produccion-pack` (`sistema/skills/productor/`), con versiones en `CAMBIOS.md`. **También la usa Sami cuando produce él**, aquí en Claude Code ("tira de iads-produccion-pack"): el proceso es el mismo, saltando los pasos de avisar y revisar con Sami. Al cambiarla, en **tres sitios**: el repo, la copia de Claude Code (`~/.claude/skills/iads-produccion-pack/`) y el zip `~/Downloads/iads-produccion-pack-vN.zip` (borrando el anterior) para que Sami la suba a su Claude.

**Durante un pack: situaciones que ya tienen respuesta** (detalle completo, en la skill del paso a paso cuando se haga)

- **"El cliente ha reservado el briefing"** → darle a Sami los recordatorios rellenos con su día y hora (que traiga los 4 anuncios: 2 ganadores, 1 que no soporte, 1 de la competencia que le guste), y prepararle su web, sus colores y su tipografía para la fase 5 del briefing.
- **"Acabo de hacer el briefing"** → Sami pega la transcripción (+ lo que entendió y un resumen); se hace la ficha de la marca, se monta la carpeta del encargo en Drive y se le da el mensaje para el productor.
- **"El productor me ha pasado los guiones"** → ayudar a Sami a revisarlos antes de la validación: ideas distintas de verdad, que suenen a la marca, que respeten lo que no se puede decir.
- **"Ya hemos hecho la validación"** → la transcripción va al productor; si rechazó más de 4-5, el mensaje de guiones rehechos para antes de las 20:00 (`11-MENSAJES.md`).
- **"Tengo el vídeo muestra"** → el mensaje para mandarlo (`11-MENSAJES.md`) y avisar cuando pasen las 24 horas.
- **"Voy a entregar"** → comprobar la carpeta y el documento "Cómo usar tus anuncios", darle la plantilla de la entrega rellena y recordarle **pedir el acceso de analista en esa misma llamada**: los datos se miran **como mínimo 3 días antes** de la llamada de resultados, para analizarlos con calma.

**Productores: situaciones que ya tienen respuesta**

- **"Revisa los candidatos"** → leer la hoja "iAds — Filtro Productores (Responses)" por el conector de Drive y decir quién pasa, quién no y por qué.
- **"Hay que cambiar algo de la skill del productor"** → cambiarla en `sistema/skills/productor/SKILL.md`, subir la versión (arriba del archivo y en `CAMBIOS.md`), rehacer el zip `~/Downloads/iads-produccion-pack-vN.zip` (borrando el anterior) y mandárselo a Sami.

**Ventas: situaciones que ya tienen respuesta**

- **"Tengo una llamada con Álvaro"** → darle a Sami la lista de `3-equipo/3-ventas/alvaro/QUE-DECIRLE.md` (lo pendiente de decirle). Después de la llamada, pasar lo dicho a "Ya hablado" con la fecha. **Cada vez que se decida algo que afecte a Álvaro, apuntarlo ahí** (Sami no le escribe fuera de las llamadas).

- **"El setter me ha agendado una reunión con [marca]"** → el informe del setter (las 16 respuestas) está en Notion, base "Reuniones agendadas" de la página "📞 iAds — Llamadas en frío" (se lee por el conector de Notion, nunca por el Chrome de Sami); úsalo. Skill `iads-reunion`: preparar la llamada (demo de 5-10 s con su producto, 2-3 ideas, pack recomendado) y recordar a Sami los recordatorios del grupo de WhatsApp (nada más agendar, 48 h, 24 h, 12 h, 1 h y llamada 5 min antes), con sus textos de `archivo/modelo-contenido/4-plantillas/clientes/1-LLAMADA-VENTA.md` (fase 0) ya rellenos con día y hora.
- **"No se ha presentado a la llamada de venta"** → los 3 pasos de rescate de `1-LLAMADA-VENTA.md` ("Si no se presenta"): llamada y mensaje a los 5 min; ese mismo día, mensaje con **dos opciones concretas** de día y hora; si no contesta, un último mensaje al día siguiente y se marca "no se presentó" en el CRM.
- **"Me ha dicho que se lo piensa"** → lo que hay en `1-LLAMADA-VENTA.md` (cierre, B y C): preguntar qué parte le hace dudar y no colgar nunca sin un siguiente paso con fecha. Si ese paso ya está fijado, recordárselo a Sami ese día con un mensaje listo. *(La cadencia de seguimiento más allá de eso no está decidida: preguntar a Sami.)*

**Clientes: situaciones que ya tienen respuesta**

- **"El cliente ha pagado pero no reserva el briefing"** → los pasos de `archivo/modelo-contenido/4-plantillas/clientes/11-MENSAJES.md`: mensaje a las 12 h, llamada a las 24 h, mensaje con dos opciones concretas a las 48 h y aviso a los 4 días (a los 7 sin respuesta, pausa por contrato). Dar a Sami cada mensaje relleno el día que toca.
- **"El cliente quiere cancelar"** → `archivo/modelo-contenido/4-plantillas/clientes/11-MENSAJES.md`: primero preguntar el motivo (en plural, "nos"); si tiene arreglo, una solución concreta una sola vez; si cancela, el mensaje de despedida, cancelar en Stripe, motivo a la ficha y moverlo a `antiguos/`. Si avisa tarde, por defecto se le perdona (lo decide Sami).
- **"El cobro ha fallado"** → `11-MENSAJES.md`: mensaje el mismo día con el enlace para actualizar la tarjeta, no se produce nada mientras no pague, aviso a los 3 días y, a los 7 sin pagar ni contestar, se da por cancelado.
- **"El cliente quiere cambiar de pack"** → `11-MENSAJES.md`: siempre desde la siguiente renovación; contrato nuevo, cambio en Stripe y, si sube, dos tandas y el productor cobra el doble; si baja, Base a 500 € (el 350 € es solo para clientes nuevos).
- **"Un cliente antiguo quiere volver"** → `11-MENSAJES.md`: entra con el proceso nuevo entero, al precio de ahora sin el primer mes a 350 €, briefing más corto, y por dentro sale de `antiguos/` y su ficha pasa a `proceso: nuevo`.
- **"El cliente ha movido / no se ha presentado a una llamada"** → contrato, cláusulas 4a y 10: si mueve o falta, **la entrega se mueve lo mismo**; si pasa **7 días seguidos** sin responder ni presentarse, el pack queda **en pausa** (el cobro no se para). Dar a Sami el mensaje para reagendar y apuntar en la ficha (`esperando_hasta` / `esperando_por`).
- **"El cliente no ha publicado los vídeos"** → contrato, cláusula 4c (se compromete a publicar en la fecha de la entrega). En la llamada de resultados, el plan B de `8-LLAMADA-RESULTADOS.md` (fase 5): decirlo claro, entender qué le frena, fecha nueva y ayuda si hace falta. *(Qué hacer antes de la llamada de resultados no está decidido: preguntar a Sami.)*

**Marc, el media buyer, o algo de los anuncios de Meta de un cliente** → `3-equipo/5-media-buyer/marc/FICHA.md`: qué hace con cada cliente, plazos, quién decide qué, cuánto cobra (400 € escalón 2 · 800 € escalón 3) y qué pasa si lo deja. Sus pagos, en `PAGOS.md`. Hasta que se rehaga la skill de clientes (bloque B), un cliente de los escalones 2 o 3 se lleva mirando esta ficha.

**Cada persona del equipo tiene su carpeta** con su ficha (lo que lee cualquier chat), su acuerdo y sus pagos. Se hace igual con cada uno: definir lo que hace con Sami, hablar con él y que diga que sí por escrito, y guardarlo aquí.

**Equipo: situaciones que ya tienen respuesta**

- **"Toca pagar al equipo"** → mirar el `PAGOS.md` de cada productor (lo `entregado` sin pagar), y las comisiones: closer 60 € + 10 %, setter (Álvaro) 150 € + 5 % (ver abajo y su ficha). Marc: `3-equipo/5-media-buyer/marc/PAGOS.md`. Dar a Sami la lista de quién, cuánto y por qué, y el mensaje de "¡Pagado!" (`4-plantillas/productores/8-PAGO.md`). Al pagar, marcar `pagado` con la fecha.

**"Un amigo / una marca quiere unos pocos vídeos sueltos"** → encargo puntual, `4-plantillas/clientes/comunes/ENCARGO-PUNTUAL.md`: 25-40 €/vídeo amigos, 70-90 €/vídeo desconocidos; mismo proceso adaptado; contrato corto `2b-CONTRATO-PUNTUAL.md`; ficha con `estado: puntual` (cuenta como cliente, sin renovación); productor 12,50 €/vídeo; setter 10 %.

**Situaciones que todavía NO tienen respuesta decidida** (no inventarla: decírselo a Sami y apuntarlo; ver `IDEAS.md`): cierre de semana o de mes (aparcado hasta ~noviembre).

**"Empiezo un chat nuevo" / "¿dónde nos quedamos?"** → leer este mapa entero y la sección "Dónde estamos", y decírselo a Sami en 3-4 líneas.

**Si algo falla con un productor** (va tarde, entrega algo malo, no contesta) → `4-plantillas/productores/11-SI-ALGO-FALLA.md`. El cliente nunca tiene que notarlo; solo se le avisa si cambia su fecha.

**Pagos al equipo**
- **Productor (aparcado: produce Sami):** 125 € (escalón 1), 150 € (escalón 2) y 300 € (escalón 3) al mes por cliente, desde el primer mes (`1-negocio/6-NUMEROS.md`). Los créditos los pone iAds. Se apunta en su `PAGOS.md`. *(El paso a paso de "un productor nuevo" de arriba es del modelo viejo: se repasa cuando se desaparquen.)*
- **Closer:** 60 € el primer mes del cliente y el 10 % los meses 2 y 3.
- **Setter en frío (Álvaro), desde el 13/10:** 150 € al cerrar + 5 % los meses 2 y 3 en los escalones 2 y 3; 75 € + 5 % en el escalón 1. Su ficha: `3-equipo/3-ventas/alvaro/FICHA.md`. Lo de Álvaro lo lleva Sami directamente.

**Qué toca hoy / a quién escribir** → `HOY.md` (se regenera con `python3 sistema/scripts/hoy.py`). En cada update, decir a quién le toca escribir hoy y con qué mensaje.

**"Tengo llamada con la mentoría" / "apúntalo para la mentoría"** → `PARA-LA-MENTORIA.md`: darle a Sami la lista; añadir ahí lo que haya que preguntarles; después de la llamada, pasar lo hablado a "Ya hablado" con lo que dijeron.

**Metas** → `1-negocio/5-METAS.md` es la del mes en curso (la lee el panel). Las de meses pasados, en `1-negocio/metas-pasadas/[AAAA-MM-mes]/`. Al cambiar de mes, se mueve allí la anterior.

**El servicio de campañas con Marc** → solo `5-campanas/`. No cuenta para las metas de iAds.

---

## Reglas que no se olvidan

- **Clientes antiguos:** todos los de antes del 01/10/2026 llevan `proceso: antiguo` en su ficha. **No tienen el proceso nuevo** (onboarding, contrato, 4 llamadas, "Cómo usar tus anuncios"…) **ni el precio de catálogo**: vale solo lo que dice su ficha (p. ej. CoolCrab pagó 200 €). No se les cambia la estructura de carpetas.
- **Clientes nuevos:** estructura `0-RESUMEN · 1-contrato · 2-onboarding · 3-material-cliente · 4-entrega (copia del Drive) · 5-informes · 6-llamadas/[tipo] · interno`.
- **El proceso del cliente** (lo que vive él): `1-negocio/4-COMO-LO-ENTREGAMOS.md`. El mes 1 es para **encontrar ganadores**; el mes 2, para **explotarlos**.
- **Renovación:** cobro automático cada 30 días desde el pago. Se cancela avisando **como mínimo 5 días antes** (15/10, con el contrato nuevo). Informe el día 25.
- **El panel tiene un fallo de base conocido:** da por hecho que todos renuevan cada 30 días (por eso dice cosas raras de Romero o Wondernastic). Se revisa a fondo en la fase del panel; mientras, fíate de lo que diga Sami y de la ficha.
- **Estilo de producción:** vídeos en Seedance 2.5 con la voz de Higgsfield (no Marketing Studio); en la voz, solo la frase y el acento de Madrid castizo, sin fonética. Estáticos con GPT Image 2. Créditos de Higgsfield: no son techo, Sami compra más si hace falta.
- **El cambio de modelo (desde el 07/10/2026):** tras la mentoría se rehace la oferta (vídeos + gestión de Meta, ~1.200 €/mes). **Nada se borra:** la foto de cómo estaba todo es la etiqueta de git `modelo-contenido-2026-10-07` (y el zip `~/Documents/iads-modelo-contenido-2026-10-07.zip`). Cada pieza que se sustituya, su versión vieja se **mueve** a `archivo/modelo-contenido/` (misma ruta que tenía), no se borra. Lo que no cambia se queda donde está.
- **Lo único que Sami lleva en Notion es la llamada de closing** (es la que hace en caliente y es siempre igual): *ESTRUCTURA LLAMADA DE CLOSING CLIENTES*, copiada en `4-plantillas/clientes/escalon-2/1-LLAMADA-VENTA.md`. **El resto de llamadas no se duplican:** se le preparan rellenas antes de cada una ("prepárame la llamada del mes de [marca]"). Si se duplican, un día lee la vieja.
- **Delante del cliente, "nuestro equipo de media buyers"**, en plural (Sami, 18/10). Por dentro es Marc. Cuando él da la cara (la llamada del día 25), se presenta como **el jefe del equipo**, no como quien gestiona la cuenta. Vale para todo lo que el cliente lee u oye: la pantalla del camino, los mensajes, las llamadas y los informes.
- **Al cambiar algo de un sitio, cámbialo en todos** (texto + script del PDF, skill del repo + copia instalada en `~/.claude/skills/`, plantilla + índice). Y commit con lo que se ha hecho.

---

## Dónde estamos (actualizar al cerrar cada sesión)

- **Contexto:** se está montando "la base de la casa" para lanzar anuncios en octubre de 2026. Cuando Sami empiece la mentoría, **se volverá a tocar el producto** (packs, precios, oferta): mucho de lo de ahora cambiará, y es normal. Esto es la base, no la versión final.
- **Hecho (24/09-02/10/2026):** negocio, clientes, equipo, plantillas (cliente 1-12, productor 1-11), el mapa, el manual del setter v2, la skill del productor v7 y las situaciones de "qué pasa si…".
- ✅ **03-05/10:** skill de clientes v2; proceso interno (`3-equipo/4-proceso-interno/`: Calendly de pago con enlaces fijos /closing y /briefing, colegio + gym + huecos libres en Google Calendar); tracker de setters en Notion; meta de octubre; revisión de clientes (Romero y RaceUp cerrados). Marketing: con la formación de Guillermo (desde el 05/10), anuncios hacia el 15/10. **Siguiente: grabar los 10 Looms del productor** (estructura en `4-plantillas/productores/4-KIT-BIENVENIDA.md`; puntos del Loom 1 ya preparados en el chat del 05/10 — si no están, rehacerlos con esa estructura). Factura: la lleva la madre de Sami. Detalle en `IDEAS.md`.
- ✅ **06/10:** CRM de InfoCapitals configurado; formulario de Meta → CRM con Make (activo); Fireflies probado (graba solo lo que está en el calendario de grindsociety). **07/10:** onboarding de la mentoría (lo hablado y el roadmap, en `PARA-LA-MENTORIA.md`). **Cambio de modelo:** vídeos + gestión de Meta como oferta principal. Foto de lo de antes guardada (etiqueta `modelo-contenido-2026-10-07`). Método de InfoCapitals metido en `7-mentoria/`. Oferta nueva a medias en `1-negocio/OFERTA-NUEVA.md` (mercado, a quién, 3 escalones y extras del 2). Álvaro y Looms, en pausa hasta tener la oferta.
- **08/10:** en el cuaderno de la oferta nueva (hoy en `archivo/modelo-contenido/1-negocio/OFERTA-NUEVA.md`): en público solo el escalón 2; base (crear anuncios y llevarlos), promesa y extras; **Marc llevará los anuncios como freelance (400-500 €/cliente), pendiente de hablarlo con él**; garantía sin cerrar (Sami no quiere jugarse dinero). Sami ha preguntado a la mentoría si rehacer toda la base antes de lanzar (su propuesta, archivo por archivo).
- ✅ **08-10/10 · Bloque A (el negocio) rehecho** en `1-negocio/` (1 a 6; los números, en borrador hasta el equipo). Lo viejo, en `archivo/modelo-contenido/`. Meta de octubre nueva: bases antes del 20/10 y 1-2 clientes del escalón 2 del 20 al 31.
- ✅ **11/10 · Repaso del bloque A hecho**, con las clases del curso (posicionamiento, producto MVP). Nuevo: el problema concreto (las tiendas lanzan 3-4 anuncios al mes), garantía de rapidez (15 días, campaña funcionando con al menos 5 anuncios —antes 10, cambiado el 13/10— o se devuelve), extras (plan de acción suelto, cuota que sube con la inversión, recomendaciones), escalón 1 sin llamada de arranque, escalón 3 "gana por tres lados", y la entrega contada como camino de A a B. Documentos en el Drive de grindsociety para la mentoría: "iAds · Oferta nueva (para revisar)", "iAds · Cómo lo entregamos (camino de A a B)" y "iAds · Preguntas para la grupal" (enlaces en `PARA-LA-MENTORIA.md`). Sami manda la oferta por el chat; la entrega, cuando la hayan visto.
- ✅ **12-13/10 · Bloque B (el equipo), casi entero.** Base: Marc lleva Meta, Álvaro llama en frío, Sami cierra, produce y es la cara ante el cliente, la madre factura. **Marc:** carpeta `3-equipo/5-media-buyer/marc/` (FICHA, ACUERDO mandado el 13/10, falta su "sí" y 7 puntos que decirle, al final de `la skill `iads-client-pack``). **Álvaro:** carpeta `3-equipo/3-ventas/alvaro/`, manual v3 con guion y PDF, 16 preguntas en Notion, portada de Notion rehecha; llamada con él el 14/10 (`3-equipo/3-ventas/alvaro/QUE-DECIRLE.md`). **Productores:** aparcados (produce Sami). **Garantía:** campaña funcionando con al menos 5 anuncios (antes 10). **Proceso interno del escalón 2:** el primer mes hecho en `la skill `iads-client-pack``; el segundo mes, propuesta pendiente del OK de Sami.
- ✅ **14/10 · Bloque B (el equipo) cerrado.** Proceso interno de los escalones 2 y 1 (`la skill `iads-client-pack`` y la skill `iads-client-pack`; el 3, aparcado) · quién es quién (`3-equipo/1-EQUIPO.md` y su página visual) · números v4 (`1-negocio/6-NUMEROS.md` y la hoja de Google Sheets "iAds · Números") · sin precio de arranque (todos a 1.300 €) · cambios mandados a Marc (`3-equipo/5-media-buyer/marc/mensajes/`; su CRM de Notion es su herramienta, en su espacio) · Álvaro: manual v3, Notion rehecho, llamada el 14/10.
- **14/10 · Bloque C empezado: el contrato del escalón 2**, en `4-plantillas/clientes/escalon-2/4-CONTRATO.md` (cabecera y cláusulas 1-3 escritas; la forma, de la plantilla de un colega; sin domicilio; falta saber quién sale como Prestador). La lista del bloque C, en orden: contrato · onboarding (Sami le pide a Guillermo cómo tienen montado su formulario) · llamada de venta (después de que Sami vea las clases "Closing", "Presentación de ventas" y "SOPs llamadas de venta") · guía de la llamada de arranque · plan de acción · "Tu plan de acción" · panel · informe del lunes · llamada e informe del mes · escalón 1 (adaptar) · mensajes de cada situación · skill de clientes e índice. Prototipo del panel de Sami, aparcado en `IDEAS.md`.
- ✅ **15/10 · El contrato del escalón 2, entero menos la garantía.** Las 12 cláusulas escritas y con el OK de Sami en `4-plantillas/clientes/escalon-2/4-CONTRATO.md`, con las decisiones de cada una apuntadas arriba del archivo. **La 3 (garantía) se aparca** hasta después de las plantillas (Sami: cambiarla son dos minutos). **Sale Sami como Prestador**, pendiente de confirmarlo con la gestora. **PDF nuevo:** `4-plantillas/scripts/contrato_escalon2_pdf.py`, 6 páginas, con la forma copiada del contrato de un colega de Sami (márgenes de una pulgada, 11 pt con aire, cabecera y pie en todas las páginas, firmas sobre línea). **Si cambia el texto, se cambia en los dos sitios.** Pendientes que deja: la **firma digital** (con qué se firma) y pasar `11-MENSAJES.md` de 7 a **5 días** en el cobro fallido. **El contrato no se toca cliente a cliente:** lo que cambia son los huecos, y lo distinto va en un anexo aparte.
- ✅ **15-16/10 · El onboarding del escalón 2, entero**, en `4-plantillas/clientes/escalon-2/5-ALTA.md`: el recorrido (contrato con **firma electrónica dentro** → cuestionario → accesos → la agenda, que **se abre solo cuando están los accesos**), el **formulario de 30 preguntas** (se escribieron 41 y Sami las repasó una a una; al final del archivo está qué se quitó y por qué), el **documento de bienvenida** en 6 secciones (ya no es un deck por cliente: es el texto de las pantallas) y la **guía de accesos** en 2 pasos (todo Meta en la pantalla del acceso de socio, sin contraseñas). La mecánica se copió de la guía del onboarding de InfoCapitals. **Pendientes:** el OK de Marc a la guía de accesos y el ID del portfolio, lo que diga Guillermo de su herramienta, y el campo de audio de la pregunta 14. **Decidido también para qué sirve la llamada de arranque:** no para repetir el formulario (apretar respuestas flojas, lo que Marc vio en su cuenta, cerrar el presupuesto y que le vea la cara).
- ✅ **16/10 · El alta del cliente, funcionando.** `https://alta.iads-agency.es/?c=[marca]`: la página es de iAds (dominio propio, sin rastro de Google) y las respuestas caen solas en un documento por cliente en la carpeta *iAds · Altas* del Drive. Montaje: DonDominio → Netlify → Apps Script. Todo explicado en `4-plantillas/clientes/escalon-2/5-ALTA-web/apps-script/LEEME.md`, incluido cómo cambiar la página (arrastrar la carpeta `web-alta` a Netlify). **El contrato NO va dentro del alta:** se manda por WhatsApp y se firma a mano sobre el PDF.
- ✅ **16/10 · Bloque C, seis piezas más.** En `4-plantillas/clientes/borradores/`: la **guía de la llamada de arranque** (5 puntos; los 30 min son el techo), **Tu plan de vídeos** del día 6 (seis bloques, con la revisión de su web que promete el contrato y los tres niveles de franqueza según lo mala que sea), **Cómo lanzamos** del día 12 (la carpeta solo con contenido; el documento, aparte) y **el informe del lunes** (mensaje de WhatsApp, cuatro bloques, cerrando con "tienes el detalle en tu panel"). **Decidido:** los informes los escribe iAds, no Marc (él pasa números y su lectura cada domingo) · falta decírselo. **Pendiente del onboarding:** aplicar lo que contestó Marc de los accesos (a los dos correos, acceso total, y los clics son *Personas → Añadir*), para lo que hacen falta **los dos correos exactos**; y añadir un bloque "tus herramientas" cuando estén todas.
- ✅ **17/10 · Bloque C, cinco piezas más.** **La llamada del mes** (día 25, 6 puntos, con Marc entrando cuando Sami se lo pida y el bloque de si el mes ha ido mal) · **el informe del mes** (el acta de esa llamada, **después** de ella) · **el panel del cliente** diseñado entero y público en `creative-baklava-859ee2.netlify.app` (4 secciones; los datos irán a mano, decidido con Marc: la API de Meta pide verificación de empresa) · **el inventario de todo lo que necesita un cliente** (`3-equipo/4-proceso-interno/ESTADO-DE-LAS-PIEZAS.md`), que sacó dos cosas que no estaban en ninguna lista: **la suscripción de Stripe a 1.300 €** y el resumen de salida · y **la llamada de venta del escalón 2**, con el método del SOP de la mentoría dentro (el destino en números, el "¿por qué ahora?" y el diagnóstico antes del pitch). La llamada de venta vive también como documento de Google, que es donde la toca Sami: **iAds · Llamada de venta (escalón 2) · v2**.
- ✅ **18/10 · Los 25 mensajes de cada situación y la pantalla del camino.** Los mensajes, en `4-plantillas/clientes/escalon-2/12-MENSAJES.md` (del alta a la salida; pausar un mes se lleva a llamada igual que cancelar; el mes 2 en adelante, aparcado). **La pantalla del camino** (`4-plantillas/clientes/escalon-2/3-CAMINO-15-DIAS/`), que es el único apoyo del bloque 5 de la llamada de venta: cuatro paradas (arrancamos · plan de acción · la tanda · lanzamos, con la garantía) y la banda del "cada mes". **No se sube a internet:** se comparte pantalla, con `camino.html?c=Marca`. Dos frases se quedan fuera a propósito porque las dice Sami hablando (que Marc entra en su cuenta, y las 24 horas para verlo antes de que salga). **Abierto:** Sami no está cómodo con *Tu plan de acción* del día 6 — *"el plan de verdad viene el día 13"* — y se habla al volver al recorrido del cliente.
- ✅ **18/10 · Los 25 mensajes, la pantalla del camino y la casa ordenada entera.** Por la mañana: los mensajes de cada situación (`escalon-2/12-MENSAJES.md`), **la pantalla del camino** (`escalon-2/3-CAMINO-15-DIAS/`, se comparte en la venta con `?c=Marca`) y los **recordatorios anti no-show** en dos versiones. Después, **ordenar la carpeta entera por fases** (`PLAN-ORDEN.md`, etiqueta de git `antes-de-ordenar-2026-10-18`): el negocio (los seis repasados uno a uno; **la meta de octubre pasa a ser llamadas agendadas**, 3 y 5) · los clientes (por modelo y escalón, con la carpeta de un cliente nuevo montada) · el equipo (Marc en cuatro archivos, Matt en pendiente, todo lo de Álvaro junto, **su Notion rehecho de cero** y `PANEL.md` renombrado a **`HOY.md`**, que ahora cuenta las ventas del mes) · y **las plantillas** (las trece del escalón 2 numeradas en `4-plantillas/clientes/escalon-2/`, fuera "borradores" y el índice, lo viejo al archivo). **Repasadas una a una de la 1 a la 11** (faltan la 12 y la 13, que van mañana), de donde sale el cambio del día: **el plan de acción pasa al día 12 y el día 6 es "Tu plan de vídeos"** (Marc deja de pasar su parte el día 5). **Delante del cliente se habla de "nuestro equipo de media buyers"**, en plural.
- **Mañana (19/10), en orden:** la lista está arriba del todo en `IDEAS.md`. Primero la **llamada con Marc** (sus dos correos y las métricas del panel), su madre (Prestador e impuestos) y **Stripe**; después, con Claude: el onboarding, el panel y el **escalón 1**, que no tiene ni una plantilla. **El martes:** la skill de clientes y este mapa.
- **Siguiente:** la **segunda llamada con Marc** (enseñarle el panel y cerrar las métricas de "El detalle", la ventana de atribución y sus dos correos) · **Stripe**, la suscripción de 1.300 € + IVA, sin la que no se puede cobrar · los **recordatorios anti no-show**, que aún hablan del briefing del modelo viejo · **el bloque "tus herramientas"** del onboarding · y el tema abierto del **plan de acción del día 6**.
- **Siguiente: el panel del cliente.** Lo pensado y las cinco decisiones, en `4-plantillas/clientes/escalon-2/13-PANEL/NOTAS.md`. Después: el informe y la llamada del mes, el escalón 1, la llamada de venta (tras las clases de closing) y los mensajes de cada situación.
- **Siguiente: bloque C (las plantillas del cliente).** La lista exacta de lo que falta está al final de la skill `iads-client-pack` y la skill `iads-client-pack` (las 📄). Pendientes sueltos: el "de acuerdo" de Álvaro y de Marc, preguntarle a Marc cuántos clientes caben, y hablar con la madre de Sami de impuestos y de cómo pagar a Marc. Después de las plantillas: volver al equipo y los márgenes y preguntarlos a la mentoría; luego pasarles el contrato, el onboarding y el closing por el Discord de la formación (`PARA-LA-MENTORIA.md`). Fecha máxima de las bases: 20/10.
