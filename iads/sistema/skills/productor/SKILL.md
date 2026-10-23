---
name: iads-produccion-pack
description: "Producción de un pack de vídeo de iAds para una marca que ya es cliente, paso a paso: lee la carpeta del encargo (encargo, ficha de la marca, transcripción del briefing, material), propone ángulos y guiones en el formato de iAds, y cuando están aprobados convierte cada guion en prompts de Seedance 2.5 (Higgsfield) con el método de iAds, vídeo a vídeo, hasta la edición en CapCut y la entrega. Úsala siempre que alguien de iAds (un productor o el propio Sami) empiece o continúe la producción de un pack: 'empiezo el pack de [marca]', 'aquí tienes el encargo', 'aquí tienes la carpeta', 'toca hacer los guiones', 'ya están validados los guiones', 'hazme el prompt del vídeo 3', 'el vídeo muestra', 'voy a entregar'. Material confidencial de iAds."
---

# iAds — Producción de un pack

**Versión 7** (02/10/2026)

Esta skill es el método de producción de iAds. Te lleva desde la carpeta del encargo de una marca hasta
el pack entregado, en el orden en que se trabaja. **Es material confidencial de iAds**
(contrato de colaboración, cláusula 5): solo se usa para encargos de iAds.

Cada conversación es **un pack de una marca**. No mezcles marcas en la misma conversación.

**Cómo hablar con el productor:** en español, claro y corto. Un paso cada vez. Al
terminar cada paso, dile qué toca después y espera a que conteste.

**Si quien produce es Sami** (por ejemplo, desde Claude Code): el proceso es exactamente
el mismo. Lo único que cambia es que los pasos de "pásaselo a Sami", "avisa a Sami" y la
llamada de revisión con Sami del día 6 se saltan: Sami es quien revisa. Todo lo demás
(esperar el OK del cliente, avatar primero, vídeo muestra, un vídeo cada vez, estáticos,
"Cómo usar tus anuncios") se hace igual.

---

## Las 5 reglas que nunca se rompen

1. **Sin la carpeta del encargo no se empieza.** Nada de inventarse la marca.
2. **Nada se produce sin el OK del cliente a los guiones.** Después de entregar los
   guiones, **esperas**. No se planifica ni se escribe ningún prompt hasta que el
   productor te diga que el cliente ha dado el OK (algo como *"el cliente da el OK, vamos
   a producir el primer vídeo"*).
3. **Cada vídeo empieza por su avatar.** Antes de planificar o escribir nada de un vídeo,
   se crea su avatar (hoja de personaje con 4 vistas, ver PASO 4).
4. **Primero el vídeo muestra.** El resto no se produce hasta que el cliente da el OK a
   la muestra (o pasan 24 horas sin respuesta: entonces se sigue con ese estilo).
5. **Un vídeo cada vez.** Nunca prompts de varios vídeos de golpe: se hace uno, se
   revisa, y luego el siguiente.

---

## Los formatos de vídeo

No hay una lista cerrada de formatos. Cada vídeo puede tener el suyo: alguien hablando a
cámara con el móvil (UGC), una campaña cinematográfica, un antes/después, una
demostración, un sketch… y cualquier otro que encaje con la marca y con la idea. **Se
buscan formatos nuevos**, no repetir siempre los mismos.

El formato cambia casi todo (cómo se escribe, cómo se genera y cómo se monta), así que se
decide en los guiones (punto 5 del documento) y se aprueba en la validación. Más abajo
tienes cómo se producen los dos más habituales (UGC y cinematográfico) como ejemplo; para
cualquier otro formato se usa el mismo formato de prompt.

---

## PASO 1 — Leer la carpeta del encargo

Pide la carpeta del encargo si no está en la conversación:

> Para empezar necesito la carpeta del encargo: el enlace de Drive (o los archivos):
> el **Encargo**, la **Ficha de la marca**, la **Transcripción del briefing** y el
> **Material del cliente** (logo, fotos del producto, anuncios de referencia).

Cuando lo tengas, léelo **entero** y devuelve un resumen corto para confirmar que lo has
entendido:

```
[Marca] — lo que he entendido
Qué vende: …
Producto que empujamos: …
A quién le vende (y qué le pasa): …
Qué le frena a comprar: …
Tono: …
Lo que NO se puede decir: …
Pack: [N] vídeos + [N] estáticos · Fechas: guiones [día], validación [día], entrega a Sami [día]
¿Falta algo o lo he entendido mal?
```

Si en el material falta algo importante (fotos del producto de frente, por ejemplo), dilo
ya: no se descubre el día de producir.

---

## PASO 2 — Ángulos y guiones (día 1)

Objetivo: **un documento por vídeo**, con el formato de iAds, listo para pegar en la
carpeta "Ángulos y guiones" → "Vídeo N". Sami lo usa para presentarlo al cliente sin
contexto, así que **tiene que entenderse solo**.

### Cómo se piensan los ángulos

- **Ángulos distintos de verdad**, no diez versiones del mismo vídeo. Cada vídeo ataca un
  motivo de compra diferente (un problema, una objeción, un deseo, una identidad…).
- **Una idea por vídeo.** Un gancho, una idea, un resultado.
- **Se apoyan en el briefing** cuando se puede (lo que dijo el cliente, lo que le repiten
  sus clientes), pero también valen ideas propias que creas que pueden funcionar.
- **Tipo de producto** (decide la estructura):
  - **Problema → solución** (suplementos, cosmética, salud, gadgets): gancho con el
    problema en primera persona → lo que ya probó y no funcionó → el producto lo
    resuelve → un resultado creíble → cierre.
  - **Deseo / identidad** (moda, decoración, lifestyle): gancho con la sensación o una
    imagen potente → el cambio → antes/después visual → "ahora sí es mío" → cierre. Aquí
    **no se fuerza un dolor**.
  - **Utilidad** (herramientas, servicios): la molestia → cómo era antes → el producto
    lo hace fácil → el tiempo o esfuerzo ahorrado → cierre.

### El documento de cada vídeo (formato obligatorio)

```
Vídeo [N] — [nombre corto]

1. La idea, en una frase:
2. De dónde sale: (algo que dijo el cliente, algo que se ha visto que funciona, o una idea propia; cuál y por qué)
3. A quién va dirigido y qué le pasa:
4. Qué pasa en el vídeo, parte a parte:
   - Gancho (0-3 s): qué pasa y por qué engancha.
   - Desarrollo:
   - Cierre:
5. Qué se ve: formato (UGC, cinematográfico u otro), quién sale (edad, aspecto), dónde, cómo aparece el producto, duración.
6. Por qué creemos que funciona:
7. Cómo contárselo al cliente (listo para decir):
8. Guion completo:
9. Estado: Propuesto
```

Escríbelo sin jerga: nada de "hook", "ángulo de objeción", "formato UGC" en lo que va a
leer el cliente. Se describe lo que pasa ("una chica en su baño se mira al espejo…").

Entrega **todos los documentos del pack a la vez** (es lo que se presenta en la
validación), revisa con el productor y ajusta.

### La hoja de la llamada de validación

Con los documentos cerrados, prepara **la hoja para la llamada de validación** de este
cliente. La abre quien haga la llamada (normalmente el productor) y va leyendo y
explicando: aunque sea su primera llamada, no se queda en blanco. Las partes fijas van
tal cual; lo de entre corchetes lo rellenas tú con este cliente.

```
LLAMADA DE VALIDACIÓN — [Marca]

0. ANTES DE LA LLAMADA
- Leerse esta hoja la noche antes. Si algo no se sabría explicar, se cambia antes.
- Confirmar que viene quien aprueba los guiones: [nombre]. Si no viene, mejor moverla.
- Recordatorios (48 h, 24 h, 12 h, 1 h y llamada 5 min antes).
- Carpeta "Ángulos y guiones" abierta para compartir pantalla: [enlace]

1. APERTURA
- Romper el hielo.
- Pasos: lo que entendí de tu marca · los vídeos, uno a uno · lo que pasa después.
- "La idea es que salgamos de aquí con todos los guiones cerrados. Así mañana ya
  empezamos a producir y llegamos a tiempo."
- "Si algo no te encaja, dímelo sin miedo. Ahora cambiar un guion es gratis; cuando
  el vídeo esté hecho, ya no."

2. LO QUE ENTENDÍ DE TU MARCA (1 minuto, listo para leer)
- A quién le vendemos: [ ]
- Lo que le frena: [ ]
- El tono: [ ]
- El formato que te gustó: [ ]
- La oferta que metemos: [ ]
"¿Es así o se me escapa algo?"
Confirmar lo que no quedó claro: [cada supuesto de la ficha, como pregunta]

3. LOS VÍDEOS, UNO A UNO (del más fuerte al más flojo)
Nunca todos y preguntar al final. No defender de más un guion. Cada cambio, en voz
alta para que quede en la transcripción.

Vídeo [N] — [nombre corto]
La idea: [una frase, sin jerga]
De dónde sale: ["Esto sale de lo que me dijiste de…"]
Cómo se ve: [quién sale, dónde, formato, producto, duración]
Guion: [completo, para leer en voz alta]
"¿Qué te parece? ¿Lo dejamos así, cambiamos algo o lo quitamos?"
Si pone pegas: [una alternativa ya pensada]
Estado: ☐ aprobado ☐ con cambios: ____ ☐ quitar

4. SI RECHAZA VARIOS
- 1-3: se rehacen en la llamada, con él (usar las alternativas).
- Más de 4-5: "Estos los rehago con todo lo que me has dicho y te los mando hoy por
  WhatsApp antes de las 20:00."
- Si no le convence nada: volver al punto 2 y entender qué no encaja de fondo.

5. CIERRE
- Resumen de lo aprobado, con cambios y lo que se manda esta tarde.
- "El [fecha] te llega el primer vídeo, la muestra. Si en 24 horas no me dices nada,
  seguimos con ese estilo."
- Agendar ya la llamada de entrega: [fecha, día 7 desde el briefing]. Que venga
  quien sube los vídeos: [nombre].
- A partir de aquí los guiones ya no se cambian.
```

Después: *"Súbelos a la carpeta junto con la hoja de la llamada y pásale el aviso a Sami.
Cuando pase la llamada de validación, pégame aquí la transcripción."*

**Y aquí te paras.** No propongas empezar a producir ni adelantes ningún prompt. Hasta
que el productor no te pase la transcripción de la validación y te diga que el cliente
ha dado el OK, no se produce nada.

---

## PASO 3 — Después de la validación

La llamada de validación siempre se transcribe, y el productor **pega la transcripción
aquí**. Léela entera y saca **todos los cambios**, también los pequeños que se deciden
sobre la marcha (por ejemplo: "que se toque la oreja en vez del pelo", "que la chica sea
más joven", "cambia la última frase").

Devuelve una lista por vídeo para que el productor la confirme:

```
Vídeo 1 — Aprobado tal cual
Vídeo 2 — Aprobado con cambios: se toca la oreja en vez del pelo; cierre nuevo: "…"
Vídeo 3 — Rechazado: el cliente quiere [lo que dijo]
¿Me falta algo?
```

Cuando lo confirme, actualiza cada documento (punto 8 con el guion final, punto 9 con
**Aprobado** o **Cambios que pidió el cliente: …**) y dáselos para subir.

**Si se rechazaron muchos vídeos** (más de 4 o 5) y no se cerraron en la llamada: se
reescriben aquí mismo a partir de lo que dijo el cliente en la transcripción, y se le
mandan al cliente por WhatsApp **ese mismo día, antes de las 20:00**, para que dé el OK.

A partir de aquí, **el guion aprobado es la ley**: no se cambia en producción.

Y antes de empezar el primer vídeo, **espera a que el productor te diga que el cliente
ha dado el OK** a todos los guiones.

---

## PASO 4 — Planificar la producción de un vídeo

### Primero, pregunta

Antes de proponer nada del vídeo, pregunta al productor:

> Antes de empezar con el vídeo [N]: ¿tienes alguna idea del avatar que quieres crear o
> del formato del vídeo? Si no, te propongo yo.

Si tiene idea, se parte de la suya. Si no, propón tú a partir del guion aprobado.

### Después, el avatar (siempre lo primero)

**Cada vídeo tiene su avatar, y se crea antes de hacer nada más.** Normalmente es nuevo
en cada vídeo; alguno puede repetirse (por ejemplo, 3 de 10 vídeos con la misma
persona), pero lo habitual es uno distinto por vídeo.

El avatar se crea siempre como **hoja de personaje con 4 vistas en una sola imagen**:
de frente, tres cuartos izquierda, tres cuartos derecha y perfil. Esa imagen es la que
luego se usa como Element del personaje. Escribe el prompt siguiendo este de referencia
(cambiando la persona según el vídeo, y dejando igual la estructura, la luz y el fondo):

```
Character reference sheet of the same man, 27 years old, Southern European. Four views
on one image: front facing, three-quarter left, three-quarter right, profile. Neutral
expression, mouth closed, eyes to camera on the front view.

Handsome but believable, not a fashion model. Strong jaw with light stubble, straight
nose, deep-set brown eyes, thick eyebrows. Sun-tanned skin with visible texture: open
pores, faint sun lines at the corners of the eyes, a small scar through one eyebrow,
natural shine on the forehead. Slightly sun-bleached tips. No retouching, no airbrushed
skin.

Dark brown hair, medium length, pushed straight back off the forehead, slightly damp, a
few strands out of place. Surf-lifestyle look.

Athletic build: lean and defined, broad shoulders, visible chest and stomach definition
but not bulky, not a bodybuilder. Shown shirtless from the waist up so the build reads
clearly in all four views.

Flat even neutral lighting, no shadows, plain mid-grey seamless background. Shot on
85mm, f/5.6, everything in focus, all four views identical in scale and lighting.
Photorealistic, natural film grain, casting reference photo.
```

Lo que no cambia nunca: las 4 vistas, expresión neutra con la boca cerrada, piel con
textura real (poros, marcas, asimetrías: "guapo" a secas sale con cara de render),
**atractivo pero creíble**, luz plana, fondo gris liso y fotorrealista. Si la ropa del
cliente tiene que salir en el vídeo, en la hoja va con **ropa lisa sin estampado** (o sin
camiseta, como en el ejemplo), para que la prenda entre limpia.

Cuando el productor tenga el avatar, se sigue con el plan.

### El plan del vídeo

Antes de escribir el prompt, **se planifica qué pasa en el vídeo, tramo a tramo**, y se
confirma con el productor. Lo que sigue es el **formato UGC** (el habitual). Para el
cinematográfico, ver más abajo "Formato cinematográfico".

```
Vídeo [N] — plan
0-3 s — Gancho: [plano + qué pasa] · dice: "…"
3-8 s — [corte a …] · sigue hablando (en off sobre el plano)
8-15 s — [...]
15-20 s — Cierre: [plano] · dice: "…"
Duración total: … · Créditos aprox.: [segundos × 6,5]
```

- **Por defecto, el vídeo va entero en una sola generación** de Seedance 2.5 (hasta
  30 s). Solo se trocea si el guion pasa de 30 s, cortando por puntos naturales y
  manteniendo el mismo avatar, sitio y luz.
- **El avatar habla casi todo el vídeo.** La voz es **una sola pista continua** de
  principio a fin: cuando se le ve, habla a cámara; cuando corta al producto o a un
  detalle, **sigue hablando en off por encima**. Nunca un plano mudo, nunca se para la
  voz.
- **Nunca una cabeza hablando fija 15 segundos.** Mínimo: 1 plano hablando + 2-3 planos
  de producto o de uso, con las manos gesticulando. Ejemplo en cosmética: habla → corta
  a la crema → toca la textura → se la aplica → antes/después.
- **Voz y gesto a la vez:** al nombrar el producto lo levanta y lo gira para que se vea;
  en el antes/después señala a dos lados (ahí van los textos en CapCut); cierra mirando
  a cámara.

### Los personajes y el producto (Reference Elements)

- **Avatar:** su Element (categoría character) es la hoja de personaje de 4 vistas que
  se ha creado al principio del vídeo.
- **Producto:** su propio Element (categoría prop). Si hay varios productos, **un Element
  por producto** y nómbralos en cada plano.
- **Imagen de estilo** (opcional): una foto que marque la luz y el ambiente, indicando
  que **NO copie su encuadre**.
- Si salen varias personas, **diferéncialas por pelo, color de ropa y silueta**, no solo
  por la cara.

---

## PASO 5 — El prompt (formato obligatorio)

Todo prompt sale en estos bloques, en este orden. Está comprobado en render: los cortes
caen donde marca el tiempo.

```
[GOAL]
[Qué tipo de vídeo es y qué pasa de principio a fin, en 1-2 líneas.]
Duration: [N] seconds.

[REFERENCES]
<<<id del Element avatar>>> — Avatar: cara, pelo y complexión de esta persona. IGNORA la
          ropa y el fondo de la foto.
<<<id del Element producto>>> — Producto: [descripción visual exacta: forma, color,
          material, etiqueta, texto impreso]. Forma y texto exactos. Es el producto
          protagonista: tiene que leerse nítido.
<<<image_1>>> — SOLO referencia de estilo: [luz, materiales, ambiente]. NO copies su
          encuadre, su composición ni su ángulo de cámara.   [si la hay]
Do not use any of the backgrounds from the photos.

[CONTINUITY]
Character A — [quién es + qué lleva puesto de principio a fin, detalle a detalle.]
[Secundarios — cómo van y que nunca miran a cámara.]   [si los hay, máximo 1-2]
The scene — [una localización, una luz, la misma del primer al último frame.]

[STAGES]
STAGE 1 — 0-[n]s — [nombre] — [plano: escala y ángulo + qué pasa + dónde está el
          producto]. [Boca cerrada, NO habla.] — CORTE DURO al final.
          End state: [cómo queda todo al acabar].

STAGE 2 — [n]-[n]s — [nombre] — [...]
          Español de España: {[frase exacta]} — [qué hace después] — CORTE DURO al final.
          End state: [...]

LAST STAGE — [n]-[n]s — [nombre] — [...] — SIN CORTE, plano continuo hasta el final.
          End state: [...]

[VOICE]
Acento: Español de Madrid, castizo, [masculino/femenino]. NADA de locutor neutro. NADA
de acento latinoamericano. Distinción c/z = theta, nunca seseo. La 's' siempre limpia,
nunca cecear. Habla continua y fluida, sin silencios muertos. Cada frase termina en
punto = bajada de tono real y pausa corta. Ninguna frase al mismo nivel que la anterior.
Dialogue: [el guion tal cual, limpio]
Total: [N] palabras.

[LOOK]
[Tipo de pieza (UGC con móvil / campaña cinematográfica…). Cámara en mano con
micro-movimiento. Objetivos (35mm general, 50mm personaje). Apertura (f/2.0 caras, f/4
producto para que se lea). Grano, halación, dominantes de color. Fotorrealista.]

[CAMERA AND PERFORMANCE]
Cutting — [ritmo]. Sin transiciones ni fundidos. Cada corte cae exactamente en el
segundo indicado, nunca antes, aunque la acción o la frase se queden a mitad. Cada stage
ocupa su ventana completa de tiempo hasta el último frame.
Cada stage desde una posición de cámara CLARAMENTE distinta: altura, ángulo y distancia.
En todos hay movimiento de cámara: nunca un plano quieto.
[Movimientos que NO se quieren: raíl, dron, estabilizador…]
LA ESCENA SIGUE VIVA: [la tela se mueve, respira, parpadea, la luz baila, la cámara hace
una deriva mínima y continua en mano] — nunca se queda congelada.

[AUDIO]
[Sin música / música.] <[sonido ambiente]>
[Murmullo: "voces humanas reales pero completamente ininteligibles, sin ninguna palabra
reconocible en ningún idioma".] Sin subtítulos.

[EXCLUSIONS]
Nada de texto en pantalla ni subtítulos — se montan en post. Ningún producto inventado:
solo el de la referencia, con su texto exacto. Ningún rótulo ni texto legible en el
decorado. Ninguna pantalla visible. NINGÚN PLANO ESTÁTICO NI CONGELADO. Nada que parezca
una foto fija. Ninguna palabra reconocible fuera de las frases entre llaves: nunca idioma
inventado, nunca inglés, nunca acento latinoamericano. Ningún personaje con la boca en
movimiento sin frase asignada.
```

**Cierre obligatorio de cada prompt** (la línea de ajustes para la web de Higgsfield):

```
AJUSTES → Vídeo · Seedance 2.5 · 720p · 9:16 · [N]s · Audio: Activado · 1 generación
Referencias: [qué Elements y qué imagen de estilo, en qué orden subirlas]
```

- Siempre **720p** (1080p cuesta el doble y no compensa). Coste: **6,5 créditos por
  segundo** (8 s ≈ 52 créditos).
- El diálogo va siempre **entre llaves**, dentro del stage donde se dice.

### Formato cinematográfico

Campaña de moda o belleza, casi sin hablar (como mucho una palabra o la frase final), voz
en off y música en CapCut, montado a partir de **bloques de 5-9 s**, cada uno su propia
generación. Se planifica en bloques:

```
Vídeo [N] — plan de bloques (cinematográfico)
Bloque 1 (0-6 s) — Apertura: … · dice: "…" / no habla
Bloque 2 (6-14 s) — Montaje rápido: … · no habla
Bloque 3 (14-20 s) — Detalles / producto: … · no habla
Bloque 4 (20-26 s) — Cierre: … · dice: "…"
Voz en off y música (en CapCut): "…"
```

Mismo formato de prompt, con estos cambios:
- En [GOAL], si no es el primer bloque: *"Escena NUEVA, no continúa el encuadre de ningún
  plano anterior."* Si nadie habla: *"Nadie habla: la voz en off se monta en post."*
- En [VOICE], si nadie habla: *"Ningún personaje habla ni mueve los labios."* Si dice una
  palabra o una frase, solo esa, en el Dialogue.
- En [LOOK]: *"Campaña cinematográfica de [moda/belleza]. Cámara en mano con
  micro-movimiento constante. 35mm en los generales, 50mm en los planos del personaje.
  f/2.0 en las caras, f/4 en el plano del producto para que se lea. Grano fino de
  película, halación en las luces. Fotorrealista."*
- En [CAMERA AND PERFORMANCE]: cada plano desde una posición de cámara **claramente
  distinta** (altura, ángulo y distancia) y movimiento en todos.
- Recursos que funcionan: un corte de "detrás de cámaras" (equipo de rodaje de espaldas o
  de perfil), zooms bruscos a detalles (labios, ojos, pelo, tela), el producto leyéndose
  nítido en un plano propio, una sola palabra mirando a cámara.

**Ejemplo real (bloque de moda en un yate, 8 s):**

```
[GOAL]
Montaje rápido de una sesión de moda en un yate: el mismo hombre en cinco momentos
distintos del barco, incluido un corte de detrás de cámaras. Cortes secos entre ellos. En
uno de los cortes mira a cámara y dice UNA sola palabra; en el resto no habla. Escena
NUEVA, no continúa el encuadre de ningún plano anterior.
Duration: 8 seconds.

[REFERENCES]
<<<avatar>>> — Avatar: cara, pelo y complexión de este hombre. IGNORA el fondo de la foto.
<<<producto>>> — Producto: camisa de manga corta oversize, algodón azul aciano con finas
          rayas verticales blancas, cuello clásico, botones blancos, y un gran texto
          caligráfico azul marino impreso en vertical en el panel izquierdo. Forma,
          tejido, rayas y tipografía exactas. Tiene que leerse entera y nítida.
<<<image_1>>> — SOLO referencia de estilo: madera de caoba, herrajes dorados, tapicería
          clara y luz de un yate clásico. NO copies su encuadre ni su ángulo de cámara.
Do not use any of the backgrounds from the photos.

[CONTINUITY]
Character A — el hombre del avatar. Lleva la camisa ABROCHADA salvo en el primer stage,
donde se la está abrochando. Pantalón de lino claro. Pelo hacia atrás. Sin gafas.
Crew — dos técnicos con ropa oscura lisa, de espaldas o de perfil, nunca mirando a cámara.
The scene — el mismo yate clásico fondeado en una cala, de principio a fin. Sol alto de
mediodía, duro. Reflejos del agua en la madera. Sombras cortas, contraste alto.

[STAGES]
STAGE 1 — 0-1.5s — Abrochándose — Plano medio frontal, se abrocha la camisa botón a botón,
          mirando lo que hace. Boca cerrada, NO habla. — CORTE DURO al final.
STAGE 2 — 1.5-3s — Backstage — Plano general de la cubierta como set: cámara de cine en
          trípode, un técnico con un reflector. Él en el centro colocándose el cuello. La
          cámara cruza el set. Nadie mira a cámara, nadie habla. — CORTE DURO al final.
STAGE 3 — 3-4.5s — La palabra — Primer plano cerrado de su cara en el comedor de caoba.
          Levanta la mirada a cámara y dice una única palabra.
          Español de España: {Hoy} — cierra la boca y aguanta la mirada medio segundo.
          — CORTE DURO al final.
STAGE 4 — 4.5-6s — La prenda — De cintura para arriba, la camisa bien extendida, el texto
          perfectamente legible. Gira despacio el torso hacia la luz. NO habla.
          — CORTE DURO al final.
LAST STAGE — 6-8s — Babor — Plano medio lateral, apoyado en la barandilla mirando al
          horizonte, el viento le mueve la camisa. NO habla. — SIN CORTE hasta el final.

[VOICE]
Una sola palabra en todo el vídeo, en el STAGE 3. En el resto nadie habla ni mueve los
labios. Acento: Español de Madrid, castizo, masculino. NADA de acento latinoamericano.
Voz grave, tono medio-bajo, casi confidencial. Sin énfasis publicitario. Dialogue: Hoy.

[LOOK]
Campaña cinematográfica de moda masculina. Cámara en mano con micro-movimiento. 50mm en
los planos de él, 35mm en el backstage. f/2.0 en caras, f/4 en la prenda. Grano fino,
halación en los reflejos del agua. Contraste alto. Fotorrealista.

[CAMERA AND PERFORMANCE]
Cinco cortes secos, cada uno en su segundo exacto aunque la acción quede a mitad. Cada
stage desde una posición de cámara claramente distinta. Movimiento en todos. Nada de
raíl, dron ni estabilizador. LA ESCENA SIGUE VIVA: la camisa ondea, el agua se mueve, él
respira y parpadea.

[AUDIO]
Sin música. <agua contra el casco, viento, murmullo lejano ininteligible>

[EXCLUSIONS]
Nada de texto en pantalla. Ninguna prenda inventada. El texto de la camisa exacto.
Ningún rótulo legible. NINGÚN PLANO ESTÁTICO NI CONGELADO. Ninguna palabra fuera de la
palabra entre llaves.
```

Para bloques de detalle con zooms bruscos funciona un prompt más corto con
**coreografía de cámara por tiempos**:

```
Vertical 9:16, [N] seconds. [Personaje] [dónde está y qué hace]. She never speaks —
mouth closed and relaxed throughout, no lip movement.

Camera choreography, handheld with subtle micro-movement:
— 0-1s: [plano general, qué hace]
— 1-2.5s: whip zoom in to an extreme close-up of [detalle], hold one beat, snap back out.
— [...]
— [n]-[N]s: slow push in that ends framed on [producto].

Each zoom abrupt, no easing. Each extreme close-up must show real skin detail: [poros,
pestañas, pecas…]. f/2.0, shallow depth of field, fine film grain, photorealistic. No
dialogue.
```

### Continuidad entre bloques (formato cinematográfico)

Para que dos bloques parezcan del mismo rodaje: usa un **frame del bloque anterior** como
imagen de referencia y escribe: *"Match the reference frame's lighting, colour grade,
grain and location only. Do NOT reuse its camera angle or framing: this is a different
shot from a new position."* Y describe la nueva posición de cámara.

---

## Las reglas del motor (Seedance 2.5) — se aplican en todos los prompts

Todas están comprobadas en render. Un prompt que las rompe sale mal aunque el guion sea
perfecto.

**Acción y plano**
- **Acción = intención + resultado**, nunca biomecánica: "abre el tapón y deja el bote en
  la encimera", no "la mano derecha gira el tapón en sentido antihorario…".
- **Solo lo que se ve o se oye.** Nada de olores, sabores ni pensamientos.
- **Emociones como gestos visibles:** "se le abren los ojos, la comisura del labio sube",
  nunca "parece feliz".
- **Máximo 2 personas en plano** (protagonista + como mucho una secundaria).
- **Si alguien sale de plano, no vuelve** en ese plano. Lo que pasa fuera de plano no
  existe.
- **El producto siempre ubicado**: en la mano a la altura del pecho, en la encimera,
  girando hacia cámara… nunca flotando.
- **Una localización por generación.**
- **Nada de reflejos**: espejos, cristales, charcos. Excepción: un probador donde el
  espejo es el plano a propósito.

**Que no se congele**
- **Nunca pidas "plano fijo", "estable" ni "quieto"**: el motor devuelve una foto fija.
  Pide siempre que la escena siga viva (respira, parpadea, la tela se mueve, deriva
  mínima de cámara).
- **No prohíbas el movimiento de cámara Y congeles al actor a la vez.**

**Que no aburra**
- **Escalada:** cada plano más fuerte que el anterior.
- **Salta de escala, no solo de ángulo:** mete un general de verdad y un detalle extremo.
- **Algo se mueve en cada plano.**
- **Cortes desiguales** (seis cortes de 2 s exactos adormecen).

**Voz**
- **Tildes siempre bien puestas** (el motor acentúa por la tilde), frases cortas acabadas
  en punto, la palabra de énfasis en MAYÚSCULAS, números escritos en letra.
- **Nada de pronunciación.** En el prompt va solo la frase en el Dialogue y el acento
  (Madrid castizo, con z y con c). No se añade fonética ni sílabas: lo empeora.
- **La regla de la boca:** todo personaje con la boca visible o lleva su frase entre
  llaves, o se le dice explícitamente que no habla (boca cerrada, de espaldas, de perfil,
  lejos). Si no, se inventa un idioma. Incluye a los secundarios.
- **En los planos con voz en off**, di que no mueve los labios.
- **Pausas teatrales con un gesto** que las acompañe (sin gesto lo dice de corrido).
- **Prohíbe el acento latinoamericano** en VOICE y en EXCLUSIONS.

**Pantallas y texto**
- **Nunca enfoques una pantalla** (móvil, ordenador, tele): salen palabras que no existen.
  Portátil de espaldas a cámara o móvil pegado a la oreja.
- **Prohíbe todo texto del decorado:** carteles, pizarras, notas, rótulos.
- **El texto del anuncio nunca va en el prompt**: se pone en CapCut.

**Producto**
- **Fidelidad exacta**: mismo envase, color, logo y proporciones. Nunca "mejorarlo".
- **Prendas colgando = estampado deformado.** Si sale mal: prenda extendida sobre una
  mesa con la cámara bajando.
- **El producto se intuye desde el segundo 0.** Si se tapa, que sea parcial y por algo
  natural (el encuadre, las manos), nunca con desenfoque.

---

## PASO 6 — El vídeo muestra

El primer vídeo que se produce es **la muestra**: el que mejor enseña el estilo del pack.
Se produce, se edita y se manda a Sami para que se la envíe al cliente.

**Mientras el cliente la mira, haz los estáticos** (ver abajo): no dependen del estilo
del vídeo y así no se pierde el día.

Cuando llegue el OK del cliente (o pasen 24 horas sin respuesta), se sigue con el resto
de vídeos, **uno a uno**.

### Los estáticos

Cuántos: los que diga el Encargo (25, 35 o 50 según el pack).

**1. El reparto, primero.** Antes de generar nada, propón al productor cómo se reparten
**por ángulos, en bloques**: por ejemplo, con 25, cinco bloques de 5, cada uno atacando
un ángulo del pack. Cada estático sabe a qué ángulo va y para quién. Esto es lo que Sami
explica en la llamada de entrega, así que tiene que quedar claro:

```
Bloque 1 — [ángulo] (5): [tipo de cada uno: testimonio, antes/después, oferta…]
Bloque 2 — [ángulo] (5): …
```

**2. Las personas: máxima variedad.** Se usan **todos los avatares de los vídeos** del
pack, más **3 o 4 nuevos** (con la misma hoja de 4 vistas), y se van intercalando. Nunca
el mismo avatar en muchos estáticos seguidos.

**3. Los tipos.** Dentro de cada bloque, mezcla: avatar con el producto, testimonio o
reseña, problema/solución, antes/después, oferta, producto con una frase potente… y
cualquier otro que ataque bien ese ángulo.

**4. Cómo se generan:**
- **Modelo: GPT Image 2** en Higgsfield (6,5 créditos por imagen).
- **Cada estático en un tamaño:** se mezclan **9:16, 1:1 y 4:5** a lo largo del pack.
  No se hace cada uno en los tres.
- **El texto lo pone la IA** en la imagen, dentro del prompt. No se revisa uno a uno.
- El producto va como imagen de referencia, para que salga igual que el real.

**5. Cómo se escribe el prompt**, en inglés y en este orden:
1. **Las referencias primero.** El producto como Element: que sea igual de forma,
   colores, proporciones y logo, y describe lo que tiene de especial (lo que la IA
   suele fallar). La persona como Element: igual de cara y pelo.
2. **"Create:"** y el tipo de anuncio en una frase (paso a paso, oferta, testimonio…).
3. **Los colores de la marca en código** (#3A2A30), fondo incluido.
4. **La composición por zonas:** arriba, en medio, abajo. Qué va en cada sitio.
5. **Todo el texto exacto, entre comillas y en español**, con su tamaño (grande,
   pequeño, tachado…).
6. **Los detalles que evitan fallos:** "nada tapa la mano", "uñas cortas sin esmalte"…
7. **Cierre fijo:** logo abajo a la derecha, *"Photorealistic, real skin texture"* y el
   tamaño (4:5, 9:16 o 1:1).

**Dos ejemplos que funcionan muy bien** (calidad y estructura). No son los únicos
formatos que valen: son la referencia de cómo se escribe.

Ejemplo 1 — paso a paso (4:5):
```
Use the attached references. Element @producto-uñas is the product: match its exact
shape, colors, proportions and logo precisely. It is a white matte round device with a
black flat top that has FIVE round holes arranged like an open hand. Element @alejandra
is the model: match her exact face and hair.

Create: a step-by-step instructional ad on a warm off-white (#F7F1EC) background. Top:
bold all-caps "CÓMO SE USA NAILYX" in deep plum (#3A2A30).

Below: three equally spaced horizontal rows. Each row has a large deep plum circled
number (1, 2, 3) on the left, a small square photo in the middle, and a bold
instruction line on the right with a lighter one-line description below.
Row 1 photo: close-up of @alejandra's hand, each fingertip wrapped in a white cotton pad
soaked in acetone, covering the nail. Text: "ALGODÓN EN CADA UÑA" / "Con un poco de
acetona."
Row 2 photo: @alejandra's hand resting on top of the device, all FIVE fingertips
inserted into the five holes at the same time, the back of the hand fully visible,
light steam around the fingers. Nothing covers the hand. Text: "LOS 5 DEDOS DENTRO" /
"El vapor lo ablanda en 8-10 minutos."
Row 3 photo: close-up of an orange wood stick gently lifting the gel off a nail. Text:
"SALE CON EL PALITO" / "Sin rascar tu uña."

Bottom: the @producto-uñas device centered, studio-lit. "NAILYX" logo text bottom
right. Clean, editorial, instructional. Photorealistic. 4:5 aspect ratio.
```

Ejemplo 2 — oferta con persona (9:16):
```
Use the attached references. Element @producto-uñas is the product: match its exact
shape, colors, proportions and logo precisely. Element @sara is the model: match her
exact face and hair.

Create: a promotional ad with a split background. Top 60% is deep plum (#3A2A30) and
bottom 40% is warm cream (#F7F1EC). @sara, from the waist up, stands centered where the
colors meet, smiling confidently, holding the @producto-uñas device with both hands at
chest height, soft studio lighting. Her nails are short, natural, bare and matte, with
no polish.

Upper area: large cream sans-serif text reading "-36% HOY". Below it, smaller: "Quítate
el gel en casa por 44,90 €". A small line with "69,90 €" struck through.

Lower section: small deep plum text: "Devolución en 30 días · Pago seguro". "NAILYX"
logo text bottom right. Photorealistic, real skin texture. 9:16 aspect ratio.
```

**6. Entrega:** en la carpeta "Entrega", una subcarpeta por bloque con el nombre del
ángulo.

---

## PASO 7 — Edición en CapCut

- Si un vídeo se generó en varias partes, júntalas en orden. Cortes secos.
- **Voz en off** sobre los planos, sin cortes.
- **Textos y subtítulos** aquí, nunca en el prompt. Revisa la ortografía.
- Música si el vídeo lo pide (bajo la voz).
- Exporta en **vertical 9:16, 1080×1920**.

---

## PASO 8 — Revisión propia antes de entregar

Antes de mandarle nada a Sami, repasa cada vídeo:

- [ ] ¿Es el **guion aprobado**, palabra por palabra?
- [ ] ¿El **producto se ve bien** y es exacto (envase, color, texto)?
- [ ] ¿Alguien habla en **otro idioma, con acento raro** o mueve los labios sin frase?
- [ ] ¿Hay **manos, caras o dedos deformes**?
- [ ] ¿Algún **plano congelado** o que parezca una foto?
- [ ] ¿Algún **texto raro** en el decorado o en pantalla?
- [ ] ¿Los **subtítulos** están bien escritos?
- [ ] ¿El **cierre (CTA)** se oye bien y tiene sentido?

Lo que falle, se rehace antes de entregar.

---

## PASO 9 — Entregar

- **Nombre de cada archivo:** `[marca]-[nº]-[idea corta].mp4` (el número es el del
  documento del vídeo). Ejemplo: `lumea-03-por-fin-funciona.mp4`.
- Súbelo todo a la carpeta **Entrega** del encargo **el día 6 por la mañana**: vídeos en
  "Vídeos 01", imágenes en "Estáticos/Bloque N — [ángulo]".
- **Cada vídeo en su carpeta** dentro de "Vídeos 01" (`[marca]-01 — [idea corta]/`), con el vídeo y un documento "Texto y titular para Meta": para quién es, el texto de arriba y el titular (con la oferta activa si la hay).
- **Prepara "Cómo usar tus anuncios"** (el documento que el cliente lee sin Sami; es lo que se dirá en la llamada de entrega, por escrito). Tiene que **sonar a Sami**: cercano, frases cortas, nada de tono de agencia. Lleva: hola; lo que hay en la carpeta y para quién es cada vídeo; que cada anuncio en Meta se llame igual que su carpeta; por dónde empezar (semana 1, 2 y 3, y por qué), cuánto dejar cada anuncio (mínimo 3-4 días) y qué mirar (ventas y cuánto cuesta cada una); la oferta y hasta cuándo; y "qué pasa ahora". Deja en blanco lo que se decide en la llamada (qué día empiezan, retoques, fecha de resultados): se completa después.
- **Llamada de revisión con Sami** (20-30 min, día 6): presentas cada vídeo diciendo
  **para quién es y por qué lo planteaste así** (es lo que Sami contará al cliente). Los
  cambios que salgan se arreglan **ese mismo día**.
- Si en algún momento ves que no llegas a una fecha, **avisa en cuanto lo sepas**, no el
  día de la entrega.
