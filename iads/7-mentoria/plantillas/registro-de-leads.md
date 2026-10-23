# Registro de leads

> **Rellena esto en `tuyo/`, no aquí.** Esta carpeta se sustituye entera cuando
> te mandamos versión nueva, así que lo que escribas aquí dentro se pierde.

El mínimo viable para no perder un lead. Sirve igual en una hoja de cálculo que
en una base de datos: lo que importa son las columnas, los estados y la regla de
la próxima acción. Móntalo donde quieras, pero móntalo hoy, aunque sea feo.

Esto resuelve dos problemas distintos y conviene tenerlos separados en la
cabeza. El primero es que se te olvidan leads: usar la bandeja de mensajes como
registro significa que existe el que recuerdas y desaparece el resto. El
segundo, más caro, es que sin estos números no sabes dónde está tu cuello de
botella, y entonces optimizas el cierre cuando lo que está roto es que no llega
nadie a la llamada.

El criterio de qué hacer con cada ratio está en `sops/setting.md` y en
`sops/metricas.md`.

## 1 · Las columnas

| Columna | Qué se escribe | Por qué está |
|---|---|---|
| Fecha de entrada |  | Sin ella no puedes medir cuánto tarda un lead en cerrar |
| Nombre o identificador |  |  |
| Canal de origen |  | Decide dónde metes esfuerzo el mes que viene |
| Qué vende y a quién |  | Es la cualificación mínima: sin esto no sabes si puede pagar |
| Volumen o tamaño de su negocio |  | Separa al que tiene un problema caro del que tiene un problema barato |
| Estado |  | Ver la lista de abajo, cerrada |
| Temperatura |  | Frío, templado, caliente. Decide el orden de contacto del día |
| Follow ups hechos |  | Un contador, no una sensación |
| Fecha de la próxima acción |  | La columna que sostiene todo el registro |
| Cuál es esa acción |  | En una frase y en infinitivo |
| Notas |  | Lo que dijo él, con sus palabras |
| Quién llevó la llamada |  | Solo si hay más de una persona vendiendo. Sin ella no se puede saber nunca si el que cierra poco tiene un problema suyo o le pasas otros leads |
| Motivo del no |  | Con las palabras del lead. Es el dato que decide antes que ningún ratio, y el único que no se puede rellenar hacia atrás |

*El fallo de siempre:* montar veinte columnas el primer día. Un registro de doce
columnas que se rellena todos los días vale infinitamente más que uno de treinta
que se abandona en la segunda semana. Las columnas se añaden cuando has echado
de menos una tres veces, no antes.

*El segundo fallo:* escribir las notas ya interpretadas. Si apuntas "le preocupa
el precio" pierdes la frase con la que él lo dijo, y esa frase es lo que le vas
a devolver en la llamada. Se copia literal.

## 2 · Los estados

Cerrados. Un lead está en uno y solo en uno.

1. **Contactado**: le has escrito, no ha contestado nada todavía.
2. **En conversación**: hay ida y vuelta real, no un emoji de respuesta.
3. **Cualificado**: sabes qué vende, a quién y de dónde saldría el dinero.
4. **Agendado**: tiene hora reservada.
5. **Show**: se presentó.
6. **Oferta presentada**: ha visto precio y condiciones.
7. **Cerrado**: ha pagado o ha firmado con fecha de pago.
8. **No cerrado**: dijo que no o no decidió. No desaparece, pasa a repesca.
9. **Descartado**: no encaja y no va a encajar. Con el motivo escrito al lado.

*Por qué los estados están cerrados:* si cada uno inventa el suyo, los ratios
dejan de compararse entre semanas y el registro pierde su única función. Añadir
un estado es una decisión que se toma una vez y se aplica hacia atrás.

*El fallo de siempre:* no distinguir el 8 del 9. Un "no cerrado" es dinero
guardado que vuelves a tocar dentro de unas semanas; un "descartado" es alguien
al que no vas a escribir nunca más. Meterlos en el mismo cajón hace que dejes de
repescar, y la repesca es la parte del registro que más cash produce, porque son
personas que ya saben quién eres y ya te dedicaron una hora.

## 3 · La regla de la próxima acción

**Ningún lead vivo puede tener la casilla de próxima acción en blanco.**

Se aplica así:

- Toda fila en estado 1 a 8 lleva fecha y acción. Si no sabes qué hacer con él,
  la acción es "decidir qué hacer con él" y la fecha es mañana.
- La fecha es un día concreto, nunca "esta semana" ni "pronto". Una fecha difusa
  no aparece nunca en la lista de hoy, y lo que no aparece no se hace.
- El día empieza filtrando por fecha de próxima acción igual a hoy o anterior.
  Eso es tu lista. Lo que no está ahí no se toca, aunque te apetezca.
- Cuando ejecutas la acción, escribes la siguiente en el mismo momento. No al
  final del día: en el momento, porque al final del día ya no te acuerdas del
  matiz que te hizo elegirla.
- Si un lead ha llegado al límite de follow ups que te hayas puesto y sigue sin
  responder, no se borra: se pasa a repesca con fecha lejana. Los leads perdidos
  no se descartan, se pescan más tarde.

*Por qué esta regla y no una más elaborada:* es la única que convierte el
registro en una lista de trabajo. Sin ella tienes un archivo bonito que se
consulta cuando te acuerdas, y acordarse es exactamente la capacidad que estás
intentando sustituir.

*El fallo de siempre:* poner la próxima acción solo a los leads calientes. El
caliente no se te olvida nunca. La regla existe para el templado, que es donde
está la mayor parte del dinero que hoy se te escapa.

## 4 · Los cinco números de la semana

Se cuentan del propio registro, sin herramienta extra. Una fila por semana.

| Semana | Contactados | Conversaciones | Agendas | Shows | Cierres |
|---|---|---|---|---|---|
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

Los ratios que salen de ahí, y a dónde apunta cada uno cuando cae:

| Ratio | Se calcula | Si está bajo, se interviene en |
|---|---|---|
| De contactado a conversación |  | El primer mensaje: a quién escribes y cómo abres |
| De conversación a agenda |  | El momento y la forma de proponer la llamada |
| De agenda a show |  | El recordatorio, la antelación y qué pasa entre reserva y llamada |
| De show a cierre |  | La llamada y la oferta |

*Cómo se usa:* se mira el ratio más alto del embudo que esté roto y se arregla
solo ese. Un arreglo arriba multiplica hacia abajo, y por eso no tiene sentido
pelearse con el cierre cuando lo que falla es que casi nadie pasa de la primera
conversación.

*El fallo de siempre:* medir cinco cosas más porque se pueden medir. Estos cinco
números dan casi todo el embudo, y añadir métricas antes de estar usando estas a
diario solo produce un panel que se mira una vez.

## 5 · La revisión de cinco minutos

Todos los días, al terminar:

- [ ] Todos los leads de hoy tienen su próxima acción con fecha.
- [ ] Los estados están actualizados, incluidos los que han empeorado.
- [ ] Los cinco números del día están anotados.
- [ ] Hay al menos un lead en repesca al que le toca esta semana.

*El fallo de siempre:* actualizar solo lo que ha ido bien. Un registro donde
nadie retrocede de estado es un registro que miente, y a las tres semanas
tomas una decisión de precio o de canal encima de números inventados.

## Si hay alguien más haciendo llamadas

Dos columnas más, y sin ellas no se puede contestar la pregunta que llega
siempre, que es si el que cierra poco tiene un problema suyo o le estás pasando
otros leads.

- **Quién llevó la llamada.** Se puede rellenar hacia atrás mirando el
  calendario, porque es un evento que quedó registrado.
- **Motivo del no, en palabras del lead.** Esta no se rellena hacia atrás nunca.
  Un motivo reconstruido tres semanas después es un dato inventado de buena fe, y
  dentro de dos meses sostiene una decisión de precio.

Y una regla de reparto que va antes que cualquier medición: **las llamadas de
venta se asignan por orden de entrada, no por criterio**. (Ojo, no confundir con
el reparto de la cartera de entrega, que sí va por criterio y está en
`sops/equipo.md`: son dos cosas distintas y la regla es la contraria en cada
una. Las llamadas se reparten a ciegas para poder comparar a las personas; los
clientes se reparten con cabeza porque no se trata de comparar a nadie.) Si el
dueño se queda los
referidos calientes y le pasa lo demás al closer, no estás comparando a dos
personas, estás comparando dos embudos, y esa comparación no se puede arreglar
después.

El dato que decide antes que el ratio, y que no necesita volumen, es el motivo
del no. Si en las llamadas de uno se repite siempre el mismo, el problema está
antes de la llamada y es del dueño. Si están repartidos, es conducción y se
corrige con la grabación delante.

## Parte diario, si hay equipo

Una línea por persona y día. Se rellena el mismo día, nunca el domingo de
memoria, porque lo que se reconstruye se redondea siempre hacia arriba.

| Fecha | Quién | Conversaciones nuevas | Agendas | Celebradas | Cierres | Nota de una línea |
|---|---|---|---|---|---|---|
| | | | | | | |

La nota de una línea es la parte que más vale con el tiempo: es donde queda por
qué ese día fue raro.
