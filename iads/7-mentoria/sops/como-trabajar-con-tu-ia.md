# Cómo trabajar con tu IA

Este es el SOP de la propia carpeta: cómo se usa el día a día, cómo se le
pregunta para que conteste bien, cómo se alimenta con tu material y cómo se
actualiza cuando te mandamos versión nueva.

Léelo entero una vez. Son diez minutos y es la diferencia entre tener un
consultor dentro del ordenador y tener un buscador con modales.

## Cuándo toca esto y cuándo no

Toca el primer día, antes que ningún otro SOP.

Antes de abrirlo necesitas dos cosas hechas: la carpeta descargada y abierta con
Claude Code dentro (el paso a paso está en la guía de instalación), y
`contexto/tu-negocio.md` rellenado. Si el segundo está en blanco, para y
rellénalo. Todo lo que viene aquí abajo funciona a medias sin eso.

## Qué es esto y qué no es

**Es** el criterio con el que trabajamos, en un formato que una IA puede leer.
Cómo se decide un precio, cómo se estructura una llamada, qué se mira cuando el
contenido no trae leads, en qué orden se tocan las cosas.

**No es** un curso, no lleva vídeos y no hay nada que "completar". Tampoco es
una base de datos de resultados: no lleva números nuestros ni casos de otros
clientes con nombre, y si se lo preguntas te va a decir que no los tiene. No se
lo está inventando, te está diciendo la verdad.

Y no es un chat de soporte. Para lo que necesite una persona, tu canal.

## La primera sesión

**1. Comprueba que ha leído lo suyo.** Lo primero que hace Claude al arrancar
dentro de la carpeta es leer `CLAUDE.md`. Si no ves que lo lee, es que has
arrancado fuera. Cierra y vuelve a entrar desde dentro de la carpeta, porque
todo lo demás depende de eso.

**2. Haz la pregunta de calibración.** Esta, literal:

> Lee el-metodo.md y contexto/tu-negocio.md y dime en qué escalón está mi
> problema principal, con el porqué.

Es la primera que hacemos nosotros con cualquier negocio, y sirve para dos cosas
a la vez: te dice por dónde empezar, y te enseña si la carpeta está bien
instalada. Una respuesta buena nombra un escalón concreto, dice por qué ese y no
otro, y usa números tuyos. Una respuesta genérica que podría valerle a cualquiera
significa que algo falla arriba.

**3. Discútele la respuesta.** No la aceptes a la primera. Si crees que se
equivoca, dile por qué. Está preparada para defender su diagnóstico o cambiarlo,
y en las dos direcciones aprendes tú algo.

## Cómo se le pregunta

La calidad de lo que sale depende casi entera de esto.

**Dale el contexto de la situación, no solo la pregunta.** "¿Subo el precio?" da
una respuesta de manual. "Llevo cuatro meses al mismo precio, cierro más de la
mitad de las llamadas que hago y voy justo de tiempo, ¿subo el precio?" da una
respuesta que puedes ejecutar, porque esos tres datos son justo los que deciden.

**Pídele el porqué siempre que no venga.** Una instrucción sin mecanismo no se
puede adaptar el día que tu caso cambie un poco. Si te da un paso sin explicar
qué pasa si no lo haces, pídeselo.

**Cuando te dé una recomendación, pregúntale qué la invalidaría.** Es la mejor
pregunta de control que existe: "¿en qué caso esto que me acabas de decir sería
un error?". Si no sabe contestarla, la recomendación era floja.

**Enséñale material de verdad.** Pégale el guion de tu VSL, la conversación de
setting que se cayó, el título del vídeo que no funcionó. Trabaja mucho mejor
sobre algo concreto que sobre una descripción de algo concreto.

**Una cosa por conversación.** Si le metes ocho temas te devuelve un muro que no
se ejecuta. Es la misma regla que aplicamos nosotros contigo.

### Preguntas que funcionan bien al empezar

- "Léete mi oferta en contexto/tu-negocio.md y dime qué le sobra."
- "Aquí está mi última conversación de setting que no acabó en agenda. ¿Dónde la
  perdí y qué debería haber escrito en su lugar?"
- "Con mis números, ¿qué salto del embudo me está costando más dinero?"
- "Voy a subir el precio. Hazme la cuenta de cuánto close rate puedo permitirme
  perder y dime si me la juego."
- "Revísame estos cinco títulos de vídeo y dime cuál atrae al cliente que quiero
  y cuál me trae gente sin dinero."

### Señales de que te está contestando mal

Cuatro, y todas tienen el mismo arreglo:

1. **La respuesta serviría para cualquier negocio.** No ha leído tu contexto, o
   tu contexto está vacío.
2. **Te da cinco opciones para que elijas.** Está incumpliendo su propia
   instrucción. Dile "elige una y dime por qué".
3. **Te suelta un número que tú no le has dado.** Páralo. Que te diga de dónde
   sale. Si no sale de tu contexto, no vale.
4. **Te motiva.** Si aparece un "tú puedes con esto", algo se ha torcido.
   Recuérdale el CLAUDE.md.

## Cómo se alimenta con tu material

Aquí es donde la carpeta pasa de ser buena a ser tuya. Tienes una carpeta
`tuyo/`, que es solo tuya y que nosotros no tocamos nunca.

- `tuyo/llamadas/`: transcripciones de tus llamadas. Las de venta enseñan por qué
  te compran y por qué no. Las de cliente enseñan qué está roto en tu entrega.
- `tuyo/conversaciones/`: exportaciones de tus DMs y de tu Discord o WhatsApp con
  clientes y leads.
- `tuyo/procedimientos/`: lo tuyo. Cómo haces tú las cosas, incluido lo que no se
  parece a lo que decimos nosotros.
- `tuyo/material/`: guiones, ofertas, contratos, lo que tengas escrito.

### La regla que decide si esto ayuda o estorba

**Curar, no volcar.** Es el error que cometemos nosotros primero y el que más
caro sale.

Una carpeta con doscientas transcripciones en bruto no es una carpeta más lista,
es una más lenta y más confusa. El modelo tiene un espacio limitado de atención,
y cada documento que no aporta compite con los que sí. Diez ficheros buenos
rinden más que doscientos regulares, y no es una diferencia pequeña.

Lo que funciona, en este orden:

1. **Métele la llamada en bruto** cuando la acabes, en `tuyo/llamadas/`.
2. **Pídele que la destile**: "guárdame lo que sirva de esta llamada". Ella sola
   escribe la ficha en `tuyo/llamadas/`, con el formato de
   `plantillas/ficha-de-llamada.md` y la fecha delante en el nombre. Lo
   importante es el porqué, no el resumen: "hace seguimiento a los tres días" no
   sirve; "hace seguimiento a los tres días porque el lead se enfría después del
   pico de dolor de la llamada" sí.
3. **El bruto se aparta solo**, a `tuyo/llamadas/bruto/`. No se borra sin que tú
   lo digas, pero tampoco se vuelve a leer. Cuando se acumulen, vacíala.

**Ojo con la diferencia entre `llamadas/` y `procedimientos/`.** Una ficha de una
llamada concreta va a `tuyo/llamadas/`. Un procedimiento es otra cosa: es cómo
haces tú algo, y **solo se escribe cuando algo ha pasado dos veces**. Si metes
cada llamada en `procedimientos/`, en tres meses esa carpeta tiene quince fichas
de lead y ningún procedimiento, y lo que de verdad vale queda enterrado.

### Lo que rellenes, rellénalo en `tuyo/`

`plantillas/` son formularios en blanco y esa carpeta **se sustituye entera** cada
vez que te mandamos versión nueva. Si rellenas una plantilla ahí dentro, la
pierdes en la siguiente actualización.

Rellénalas siempre en `tuyo/`. Tu registro de leads es `tuyo/registro-de-leads.md`,
tu check de la semana es `tuyo/checks/AAAA-MM-DD.md`, y tu documento de oferta es
`tuyo/material/oferta.md`. La plantilla se queda en blanco donde está, de
referencia.

Y ponle la fecha delante en el nombre a todo lo que sea de un día concreto:
`AAAA-MM-DD-descripcion.md`. Con veinte ficheros dentro, sin eso no encuentras
ninguno.

### Ponle fecha a todo

Cualquier cosa que describa el estado de tu negocio lleva la fecha dentro. Sin
fecha, un documento se lee siempre como si fuera de hoy, y así es como una
herramienta que dejaste de usar en febrero acaba presentada como parte de tu
sistema actual. Nos ha pasado y por eso está escrito aquí.

### Lo que NO metes dentro

- Datos personales de tus clientes que no necesites para decidir nada.
- Contraseñas, claves de API o tokens. Nunca, en ningún fichero.
- Material de programas de pago de terceros que no sea tuyo para repartir.

## Lo que tu IA hace sola, para que sepas que puedes contar con ello

No hace falta que se lo pidas cada vez. Está instruida para:

- **Guardar sin que le digas dónde.** Tú le dices "guárdame esto" y ella decide
  la carpeta, el nombre con la fecha delante y el formato, y te lo dice en una
  línea al final.
- **Apuntar lo que queda abierto** en `tuyo/decisiones-pendientes.md`. Cuando le
  traigas ocho temas te resuelve los que se resuelven solos, deja una pregunta
  abierta y apunta el resto ahí con lo que desbloquea cada uno. No se pierden:
  están en un sitio y los puedes ver todos juntos cuando quieras.
- **Proponerte guardar cosas que tú no ves.** Una decisión que ya has tomado dos
  veces igual, una objeción repetida, o un resultado tuyo con su cifra y su
  fecha. Ese último es el que más se pierde y el que hace falta el día que montes
  un caso de éxito.
- **Avisarte de que la carpeta necesita limpieza** cuando se acumulen brutos sin
  destilar o haya dos fichas del mismo tema.
- **Comprobar tu contexto** la primera vez que lo lee, buscando descuadres entre
  tus propios números. De ahí suele salir algo que no sabías.

Si algo de esto no lo hace, recuérdaselo. Está escrito en su `CLAUDE.md`.

## Cómo se actualiza cuando te mandamos versión nueva

La carpeta se actualiza cada cierto tiempo. Cuando eso pase, te avisamos por tu
canal y en la plataforma. El fichero `VERSION.md` te dice qué versión tienes y
qué cambió en cada una.

Actualizar es descargar el zip nuevo y **sustituir solo lo nuestro**:

- **Se sustituye**: `CLAUDE.md`, `el-metodo.md`, `LEEME.md`, `VERSION.md`, y las
  carpetas `sops/` y `plantillas/` enteras.
- **No se toca nunca**: `contexto/` y `tuyo/`. Ahí está tu trabajo.

En la práctica: borras `sops/` y `plantillas/`, descomprimes el zip nuevo encima,
y ya está. Si prefieres no pensarlo, díselo a tu propia IA con la carpeta abierta
y que lo haga ella, que para eso está.

**Y si has escrito procedimientos propios, no los guardes en `sops/`.** Van en
`tuyo/procedimientos/`, precisamente para que una actualización nuestra no se los
lleve por delante. Es la única forma de perder trabajo aquí, y se evita con eso.

## Los errores que más se ven

**Arrancar fuera de la carpeta.** El más común con diferencia. Todo parece
funcionar, las respuestas suenan bien, y son genéricas porque no está leyendo
nada de lo que te dimos. Compruébalo mirando si lee `CLAUDE.md` al arrancar.

**Dejar `contexto/tu-negocio.md` a medias.** El segundo más común. Sin tus
números, la mitad de los SOPs no puede aplicarse a tu caso y te va a dar la
versión de manual.

**Poner un número a ojo para no dejar el hueco vacío.** Escribe "no lo sé". Es
información y sabe qué hacer con ella. Un número inventado se lee a las tres
semanas como si estuviera medido.

**Volcar todo el Drive dentro.** Ya está arriba, pero es el error que más
degrada la carpeta con el tiempo y no se nota de golpe, se nota como que "cada
vez contesta peor".

**Pedirle táctica antes que diagnóstico.** "Dame diez ideas de reels" tiene
respuesta siempre, y no sirve de nada si tu problema está dos escalones más
abajo. Empieza por dónde está el problema.

**Tratarla como buscador.** Si le preguntas cosas que responde cualquier chat,
te contesta como cualquier chat. Lo que tiene de distinto es el criterio, y el
criterio sale cuando le traes una decisión de verdad.

## Qué no tocar todavía

**No reescribas los SOPs nuestros** para adaptarlos a tu caso. Si algo no encaja,
escribe tu versión en `tuyo/procedimientos/` y díselo: se queda con las dos y usa
la tuya, que es lo correcto porque es tu negocio. Tocar los nuestros solo
consigue que la próxima actualización te los pise.

**No montes automatismos con esto** hasta que lleves unas semanas usándolo a
mano. Primero hay que saber qué le pides y qué te contesta bien; automatizar
antes es fijar en piedra un flujo que todavía no sabes si es el bueno.
