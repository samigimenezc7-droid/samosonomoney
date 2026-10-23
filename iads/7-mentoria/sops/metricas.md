# Métricas · qué se mide, desde dónde y cada cuánto

Este SOP existe para una sola cosa: saber dónde está tu cuello de botella. Si no
lo sabes, cualquier mejora que hagas puede estar atacando el sitio equivocado, y
entonces no es que no mejores, es que empeoras, porque metes dinero y horas donde
no toca y se los quitas al punto que sí lo resolvía. Aquí va qué se mide, de
dónde tiene que salir el dato, cuándo un ratio ya se puede leer y cuándo todavía
es ruido, y con qué frecuencia se mira cada cosa. Aquí se declara además **el
umbral de volumen a partir del cual un ratio se puede leer**, que manda sobre
cualquier mínimo que aparezca en otro sitio de la carpeta.

Dos palabras que se usan juntas y no son lo mismo. Las **métricas** son cómo
bajas los datos a tierra. El **tracking** es el proceso que va desde que alguien
ve tu contenido hasta que queda registrado en esas métricas. Casi todos los
problemas que vas a tener son de tracking, no de métricas.

> **Plantilla de este SOP**: `plantillas/registro-de-leads.md`, el registro
> mínimo viable, con sus columnas y sus estados.

## Cuándo toca esto y cuándo no

Toca en cuanto tengas conversaciones. No hace falta que vendas todavía: si hay
gente entrando, ya hay embudo que medir, aunque el final sea cero.

Y toca de forma obligatoria, no opcional, en cuanto haya otra persona en el
proceso comercial. Si tienes a alguien abriendo conversaciones o cerrando y no
mides lo que hace, para y monta esto primero, porque sin datos suyos vas a
discutir a ciegas: no vas a poder distinguir un mal mes del mercado de un mal mes
de la persona, y vas a acabar decidiendo por quién te cae mejor.

No toca antes de tener con quién hablar. Si tu problema hoy es que no hay leads,
montar el registro completo es construir un panel para medir ceros, y encima te
sirve de coartada para no hacer lo que sí toca, que es `sops/contenido.md` y
`sops/setting.md`. En ese caso apunta cuatro números en una libreta y sigue.

## La métrica sale de eventos, nunca de memoria

Esta es la regla de origen y es la que sostiene todo lo demás.

Un evento es algo que pasó y quedó registrado en el momento en que pasó: una
conversación abierta, una llamada agendada, una llamada celebrada, un cobro. Se
registra cuando ocurre, no cuando te acuerdas.

Qué pasa mecánicamente cuando reconstruyes a mano, al final de la semana o del
mes:

- **Se pierde lo que no cerró.** Te acuerdas de los cierres y de las broncas, no
  de las doce conversaciones que murieron en el segundo mensaje. Y esas doce son
  justamente el dato que buscabas, porque el numerador lo tienes y lo que te falta
  siempre es el denominador.
- **El número se redondea hacia arriba.** No por mentir: porque reconstruir es
  estimar, y nadie estima a la baja su propio trabajo. Dos personas del mismo
  equipo pueden reportar dos cifras distintas del mismo mes y las dos estarán
  convencidas.
- **Se pierde la fecha.** Y sin fecha no puedes comparar dos periodos, que es
  para lo único que sirve medir.
- **Se pierde la causa.** El motivo por el que alguien no compró se recuerda mal
  a las tres semanas, y es la información más rentable de todo el sistema.

Corolario que se aplica sin excepción: **si el dato no se registró el día que
pasó, no existe**. No se rellena de memoria, porque un hueco es información y un
hueco rellenado a ojo es un error que a los dos meses sostiene una decisión de
precio. Se deja vacío y se marca.

Y de aquí sale el criterio para conectar herramientas cuando llegues a eso: **una
integración no es funcionalidad, es validación**. Conectar el calendario o la
pasarela de cobro no te da un número que no tuvieras: te lo da sin depender de
que alguien lo teclee bien. Eso es todo lo que hace, y por eso vale la pena.

## El embudo completo, salto a salto

El embudo son personas moviéndose entre estados. Lo que se mide no son los
estados, son **los saltos**, porque cada salto tiene una intervención distinta y
si los agregas pierdes exactamente la información que necesitabas.

Los estados, en orden:

1. **Impacto:** alguien ve una pieza tuya.
2. **Visita:** entra a tu perfil o a tu web.
3. **Contacto:** te escribe, rellena un formulario o le escribes tú.
4. **Conversación:** hay ida y vuelta real, no un mensaje suelto.
5. **Agenda:** hay una llamada reservada con fecha.
6. **Show:** se presenta a esa llamada.
7. **Cierre:** dice que sí.
8. **Cobro:** el dinero está en la cuenta.

Y estos son los saltos, con qué acusa cada uno cuando está bajo:

| Salto | Qué está fallando si es bajo |
|---|---|
| Impacto a visita | El contenido llega a gente a la que no le interesas, o no das motivo para mirar quién eres |
| Visita a contacto | Tu perfil o tu web no dicen en cinco segundos qué problema quitas, o no hay una acción obvia |
| Contacto a conversación | El primer mensaje, tuyo o automático. Muchos contactos y pocas conversaciones es siempre el arranque |
| Conversación a agenda | El agendamiento: no estás pidiendo la llamada, o la pides tarde, o pones fricción donde no toca |
| Agenda a show | Lo que pasa entre la reserva y la llamada: recordatorio, confirmación, y qué le mandas mientras |
| Show a cierre | La llamada, el precio, y lo que vio antes de ti |
| Cierre a cobro | Tu proceso de cobro, no tu producto |

Dos lecturas que casi nadie hace y que cambian decisiones:

**Recorre la cadena entera antes de concluir.** Si tienes pocos leads, la
conclusión fácil es que la web convierte mal, y suele ser mentira. Cuando bajas
salto a salto con la analítica nativa de cada sitio, la mayoría de las veces el
agujero está mucho antes: hay visitas al perfil pero casi nadie pincha el enlace,
lo que acusa a la cuenta y al contenido, no a la página. Si tu conversión de
página a formulario es alta, la página no es el problema por muy fea que te
parezca. Cambiar la bio cada semana no mueve la rueda.

**Los costes se gastan antes de la agenda.** Todo lo que mejores después de ese
punto entra casi limpio, porque el gasto de traer a esa persona ya está hecho.
Por eso una mejora pequeña en show up o en cierre pesa más de lo que parece: haz
la cuenta con tus números, coge tu facturación del último mes, sube un salto de
la mitad del embudo un tercio y mira cuánto sale, sin tocar ninguna otra variable.
Ese es el orden en el que hay que atacar cuando el volumen ya existe.

## El volumen mínimo antes de leer un ratio

**Este apartado manda sobre cualquier umbral de volumen de la carpeta.** Donde
otro SOP dé un mínimo para leer algo (piezas por formato en
`sops/check-semanal.md`, llamadas para saber si tu cuello es la oferta en
`sops/oferta.md`, llamadas por tier en `sops/precio.md`), el número está puesto
para esa decisión concreta. Si alguna vez chocan, se decide con la cuenta de aquí
y gana este fichero.

El error más común de todo este SOP es sacar conclusiones de un ratio que todavía
no dice nada, y es peligroso porque no se siente como un error: se siente como
tener datos.

La cuenta que hay que hacer, con tus números y no con los de nadie:

**Cuánto mueve el ratio un solo evento más.** Se calcula dividiendo 1 entre el
denominador. Si llevas 5 llamadas y 1 cierre, tu close rate no es del 20%: si la
sexta cierra, pasas al 33%. Un solo evento te mueve 13 puntos. Ningún cambio que
hagas en el proceso va a producir un efecto mayor que el ruido, así que no puedes
atribuir nada.

**El umbral práctico:** si un evento más mueve el ratio más de 5 puntos, no lo
leas. Eso pasa por debajo de 20 eventos en el denominador. Entre 20 y 30 lo miras
como tendencia y no tomas decisiones caras. Por encima de 30 ya decides. Y cuidado
con el denominador correcto: para juzgar a quien cierra, el denominador son
llamadas celebradas, no leads.

Consecuencia práctica que salva mucho dinero: **la mayoría de las decisiones que
tomas en los primeros meses no se pueden apoyar en un ratio**, y está bien. Se
apoyan en criterio y en volumen. Meter mensajes durante quince días y no cerrar
nada no significa que el mensaje esté roto, significa que el juego de números
todavía no ha llegado a donde se puede leer. Antes de cambiar el proceso,
comprueba que has hecho suficientes repeticiones para saber que el proceso es el
problema.

**La regla general, la que se aplica a cualquier umbral de la carpeta:** el
mínimo no es un número de la casa, sale de cuánto mueve la aguja un solo evento.
Divides 1 entre el denominador que vas a usar, miras cuánto se desplaza el ratio
con un evento más, y lo comparas con la diferencia que esperas encontrar. Si el
ruido es mayor que la diferencia, todavía no puedes leerlo. Por eso el umbral
cambia con la decisión y no con el tema.

**Y por eso los números de la carpeta no coinciden entre sí, que es lo que
despista:** no es lo mismo un ratio del que cuelga una decisión de precio que una
señal para elegir qué mirar primero. Equivocarte en el primero te deja el precio
mal puesto durante meses y con contratos firmados encima; equivocarte en el
segundo te cuesta una semana mirando el sitio que no era, y eso se corrige el
lunes siguiente. Puesto en concreto: para decidir si subes el precio quieres los
treinta eventos; para decidir si esta semana miras los títulos o los ganchos, con
diez o quince piezas del mismo formato ya tienes señal suficiente, porque con esa
lectura no vas a cambiar nada irreversible.

**Así que cuando un umbral de otro SOP te parezca bajo, no lo subas por tu
cuenta: mira qué decisión cuelga de él.** Si de ese número salen un precio, un
contrato, una garantía o una contratación, aplica el de aquí. Si sale una
prioridad de la semana, el del otro SOP es suficiente y esperar a tener más
volumen te cuesta más de lo que te ahorra.

## Las métricas que mienten

No todas mienten igual. Estas son las que hay que mirar con desconfianza y por
qué:

- **El close rate cuando el denominador lo eliges tú.** Si descartas antes de la
  llamada a todo el que dudas, tu porcentaje sube y tu facturación no. Se mira
  siempre pegado al número absoluto de cierres.
- **Un close rate muy alto.** Es la métrica que más se celebra y casi siempre
  significa lo contrario de lo que parece: **si cierras a casi todo el mundo, tu
  precio está bajo**. Haz la cuenta: coge tu ratio actual y tu precio, sube el
  precio y calcula qué ratio necesitarías para ganar lo mismo. Casi siempre queda
  margen enorme. La señal de que el precio está bien puesto es que un porcentaje
  claro de gente no pueda entrar por precio, y que el precio pueda ser la única
  objeción. Eso se decide en `sops/precio.md`.
- **La facturación, cuando lo que necesitas es caja.** Facturado y cobrado no son
  lo mismo, y con pagos fraccionados la diferencia es tu supervivencia. La
  métrica de la que dependes para pagar mañana es el dinero que entró, no el que
  se comprometió.
- **El coste por lead sin la etapa siguiente.** Un canal barato que trae gente que
  no puede pagarte es más caro que uno caro que trae gente que sí. El coste solo
  se lee junto a la conversión posterior.
- **Cualquier ratio calculado sobre un estado que no se actualiza.** Si las
  llamadas se quedan marcadas como pendientes después de hacerse, tu close rate
  está mal y el resumen entero miente sin avisar. Un panel con datos viejos es
  peor que no tener panel, porque le das crédito.
- **Los picos de una sola pieza.** Una pieza que se sale de la media de tu propio
  canal es un dato interesante y no una tendencia. Se mira qué la hizo funcionar,
  no se rehace el plan entero.

## Vanidad y decisión

El test es de una frase: **si el número sube, ¿qué cambia mañana en lo que haces?**
Si no cambia nada, es vanidad y no se mide.

- Seguidores, visualizaciones y "me gusta" son vanidad mientras no los cruces con
  el salto siguiente. Views con contactos al lado ya es una métrica de decisión,
  porque te dice qué tipo de pieza trae a alguien que habla contigo.
- La métrica de decisión más infravalorada es **el motivo por el que alguien no
  compró**, registrado en el momento y con sus palabras. Cuando el mismo motivo
  aparece en varias llamadas seguidas, el problema no está en la llamada: está en
  lo que la gente ve antes de llegar. La solución no es entrenar más a quien
  cierra, es crear el contenido que responda a esa duda antes de que se agende.
  Ese es el hallazgo que convierte un registro en dinero.
- El objetivo se pone al revés que la métrica: partes de lo que quieres facturar,
  divides por tu precio para saber cuántos cierres, divides por tu ratio de
  cierre para saber cuántas llamadas, y divides por tu ratio de agenda para saber
  cuántas conversaciones al día. Ese último número es tu tarea. Si al hacer la
  cuenta te sale un número de llamadas que no cabe en tu semana, el problema no es
  de esfuerzo: es de precio o de capacidad de entrega, y lo has descubierto antes
  de estrellarte contra él.

## La cadencia

Lo que se mira a diario, a la semana y al mes es distinto, y mezclarlo es lo que
hace que se deje de mirar.

**A diario, y solo esto:** los eventos del día. Conversaciones nuevas,
seguimientos hechos, llamadas agendadas, llamadas celebradas, cobros entrados. Es
registro, no análisis. La pregunta diaria es una sola: **¿cuántas conversaciones
o agendas nuevas hay hoy?** Varios días seguidos a cero es la única alarma diaria
que necesitas, y no requiere ningún panel.

Lo que no se mira a diario: ningún ratio. A un día de distancia todos los ratios
son ruido y mirarlos produce cambios de rumbo semanales que no dejan que nada
llegue a volumen suficiente.

**A la semana:** los ratios del embudo y la comparación con la semana anterior.
Una hora, siempre el mismo día, con la pregunta de qué salto ha caído y qué se
toca la semana que viene. Uno, no tres. Cómo se estructura esa sesión está en
`sops/check-semanal.md`.

**Al mes:** lo que solo tiene sentido con más volumen. Facturado contra cobrado,
coste de adquisición por canal, precio medio, y de dónde vinieron de verdad los
que compraron. Y una revisión de la propia lista: qué métricas has mirado este mes
y cuáles no ha mirado nadie.

## El registro mínimo viable

No hace falta herramienta cara, y montarla pronto es el error clásico. El criterio
de cuándo pasar a algo más serio **no es tu facturación, es tu carga operativa**:
cuando registrar a mano te ocupe tiempo real o cuando haya varias personas
metiendo datos y pisándose.

El fallo que hay que evitar es intentar montar el sistema complejo desde el
principio: se rompe, cansa, y acabas sin trackear absolutamente nada por haber
querido hacer algo que no tocaba. **Primero trackea de algún modo. Ya lo
mejorarás.**

El modelo de datos mínimo son tres tablas, y con eso tienes casi todo el embudo:

**Tabla de contactos.** Una fila por persona, y se crea el día que aparece. Campos:
fecha de primer contacto, de dónde vino, enlace a su perfil, estado actual, número
de seguimientos hechos, fecha del próximo. El estado es el campo que hay que
disciplinarse en actualizar, porque de ahí salen todos los ratios.

**Tabla de llamadas.** Una fila por llamada, y se rellena el mismo día. Campos:
fecha, si se presentó, qué se ofreció, resultado, motivo si es un no, y qué duda
traía sin resolver. Con eso ya puedes leer show up, cierre, y el patrón de
objeciones.

**Tabla de cobros.** Una fila por pago comprometido, no por pago recibido. Campos:
importe, fecha pactada, fecha real, y qué queda pendiente. Esta tabla existe por
un motivo muy concreto: **si no registras lo que te tienen que pagar, con pagos
fraccionados se te olvida cobrar**, y eso es dinero que ya habías ganado y pierdes
por administración.

Añade después una tabla de partes diarios si hay más de una persona. Y no añadas
nada más hasta que eches en falta un número dos veces.

Dos avisos de construcción, valgan para una hoja de cálculo o para algo hecho a
medida:

- **La nomenclatura tiene que ser estable.** Si cada uno nombra las cosas a su
  manera, en dos meses no se puede agrupar nada y el registro deja de servir. Se
  fija el día uno y no se cambia.
- **El sistema es una cadena.** Si una sola pieza no se rellena, se cae la
  trazabilidad de todo el recorrido, no solo de ese campo.

## El tracking de contenido con atribución

Esta es la parte que casi nadie tiene y la que más decisiones de contenido
desbloquea, porque sin ella publicas a ciegas y decides por sensación.

**Se carga pieza a pieza, nunca por plataforma agregada.** Una fila por pieza
publicada, con fecha, enlace directo, un nombre estable, a qué avatar apunta, qué
dolor toca, y los números nativos de la plataforma. La agregación mensual te dice
si el mes fue bien y no te dice qué repetir, que es para lo único que sirve esto.

**Cómo se sabe de dónde vino un lead de verdad.** Hay tres vías y solo la primera
es fiable:

1. **Que quede registrado por el propio sistema:** un enlace distinto por sitio de
   publicación, o un formulario distinto por canal. Es la única atribución que no
   depende de que nadie se acuerde de nada. Cuesta media hora montarla y es lo
   primero que se hace.
2. **Preguntar en el primer contacto y registrarlo entonces:** "¿por dónde me has
   visto?" en el primer mensaje o en el formulario de entrada. Funciona bastante
   bien y tiene un sesgo conocido: la gente nombra lo último que vio, no lo que la
   convenció.
3. **Registrar la primera pieza que consumió**, si puedes saberlo. Es el campo más
   valioso de todos, porque cruzado con la fecha de compra te dice cuánto tarda
   alguien en decidirse contigo y qué tipo de pieza empieza esa cuenta atrás. Con
   eso ya sabes qué producir más.

Y el diagnóstico más útil de este bloque, que evita una injusticia que se comete
mucho: **si la persona que abre conversaciones no encuentra la pieza en el
desplegable cuando va a registrar de dónde vino un lead, es que la pieza no se
cargó**. Eso no es un fallo suyo, es un fallo del proceso previo, que es tuyo. Se
le suele echar la culpa a quien rellena, cuando el error viene de la arquitectura.

Un aviso de orden: si arrancas el registro hoy, mete también una tabla con lo
publicado antes, aunque sea solo enlace y fecha. Un lead que llega hoy pudo haber
consumido algo de hace seis meses, y sin esa lista esa atribución se pierde.

## El tracking de setting

Si hay alguien abriendo conversaciones por ti, este es el único tracking que es
obligatorio, y el porqué es de diagnóstico por capas.

Cuando una semana caen las llamadas, tienes varias capas posibles: el volumen de
apertura, a quién estás atrayendo, o cómo lo estás nutriendo antes de la llamada.
No puedes atacarlas todas a la vez. **El parte diario existe para descartar la
primera**, que además es la más barata de arreglar. Si el volumen está donde tiene
que estar y aun así no hay llamadas, ya sabes que el problema es de a quién estás
atrayendo, y eso te ahorra una semana de discusión.

Qué se registra cada día, al terminar la jornada y siempre: fecha, mensajes
nuevos enviados, seguimientos hechos, conversaciones abiertas, llamadas agendadas.
Cinco campos. Si tarda más de un minuto en rellenarlo, deja de rellenarse la
segunda semana.

Dos criterios de lectura:

- **Los seguimientos se miran aparte de los mensajes nuevos.** Son cosas
  distintas con coste distinto: abrir en frío gasta reputación de cuenta, y volver
  sobre alguien con quien ya hablaste es barato. Si están en el mismo número, no
  puedes ver que alguien está inflando su parte a base de mensajes fríos.
- **Los primeros días de alguien nuevo no se leen como rendimiento.** Se leen como
  línea base para saber contra qué comparar.

Y el aviso que hace que esto no funcione: **si la reconstrucción automática tapa
el hueco, nadie rellena su parte**. Si el sistema adivina los datos que faltan, el
parte deja de rellenarse en dos semanas. Sirve como red de seguridad, no como
sustituto, y quien no lo rellena tiene que notar que no lo ha rellenado.

## Coste de entrega por cliente y margen por cliente

**Cuándo toca, y es antes de lo que dice la regla general de posponer márgenes:**
en cuanto haya alguien cobrando por vender o por entregar. Mientras estás solo,
la caja te sirve de aproximación porque casi todo lo que entra es tuyo. Con un
sueldo y una comisión dentro deja de servir, y esperar a tener un año de
histórico es decidir a ciegas justo cuando las decisiones ya cuestan dinero:
puedes estar subiendo la facturación y perdiendo margen con cada cliente nuevo, y
la caja tarda meses en enseñártelo porque los cobros van por delante de los
costes. Esto no necesita recorrido, necesita un mes cerrado. No lo confundas con
el valor de vida de cliente, que sí se pospone porque depende de renovaciones que
todavía no han pasado.

**Qué se suma. Cuatro bloques, y el primero es el que se salta todo el mundo:**

1. **Las horas del dueño, valoradas.** Las tuyas cuestan aunque no te las pagues.
   Se valoran a un precio y solo uno, elegido una vez y no cambiado: o lo que te
   costaría pagarle a alguien por hacer eso, o lo que produce esa misma hora
   dedicada a vender. La segunda sale más alta y es la más honesta cuando tu
   cuello de botella es tu tiempo. Si no las metes, el número te va a decir que
   todo tiene un margen estupendo y vas a concluir que puedes coger más clientes,
   que es exactamente el error que este cálculo existe para evitar.
2. **Los sueldos de quien entrega**, con las cargas que pagues por esa persona. Lo
   que cuesta alguien no es lo que le ingresas.
3. **Las comisiones**, de quien abrió y de quien cerró, imputadas al cliente que
   las generó y no repartidas entre todos. Una comisión es del cliente que la
   provocó, si no el cliente caro de vender se esconde detrás de los baratos.
4. **Las herramientas que existen por tener clientes.** Las de asiento por cliente
   van directas y las de suscripción fija se reparten. Tu ordenador no entra.

**Cómo se reparte lo que no es de un cliente concreto.** Lo atribuible va directo
(sus sesiones, la comisión de su venta, su asiento). Lo compartido se reparte
**por número de clientes de esa cartera, nunca por lo que factura cada uno.** El
motivo es lo que justifica todo el ejercicio: repartir por facturación esconde
justo al cliente que estás buscando, el que paga poco y consume mucho, porque le
asigna poco coste precisamente por pagar poco. Repartido por cabezas, ese cliente
aparece a la primera y en el sitio de abajo.

**La cuenta, con tus números:**

```
ingreso mensual del cliente = precio total cobrado / meses de programa
coste mensual del cliente   = horas tuyas valoradas + sueldo imputado
                              + comisiones repartidas entre los meses
                              + herramientas
margen mensual              = ingreso mensual - coste mensual
margen en porcentaje        = margen mensual / ingreso mensual
```

Se hace cliente a cliente y se ordena la lista de menor a mayor margen. **La lista
ordenada es el entregable, no el promedio.** El promedio te tranquiliza; la lista
te enseña a quién le estás pagando por trabajar.

**Qué decisiones cambia, que es lo único que justifica calcularlo:**

- **Si coges otro cliente o si contratas.** Si el margen del último que entró es
  más bajo que el de los anteriores, no estás escalando: estás comprando
  facturación con tus horas.
- **El precio del tramo bajo.** Si el tramo barato deja menos margen por cliente
  que el caro, la escalera está mal montada, y se arregla por arriba cambiando a
  quién le vendes ese tramo, no dándole menos acceso (`sops/oferta.md`).
- **Qué bloque paquetizas primero:** el que más horas te come dentro de los
  clientes de la parte baja de la lista. Optimizar lo que ya deja margen es
  trabajar para no cambiar nada.
- **Cuánta comisión puedes pagar** sin quedarte sin margen. Esa cuenta se hace
  antes de prometer un porcentaje, no después (`sops/equipo.md`).
- **Cuántos meses de "seguimos gratis" aguanta tu garantía condicional.** Cada mes
  de extensión sale del margen de ese cliente y de ningún otro sitio
  (`sops/oferta.md`).
- **A quién no le renuevas.** Un cliente con margen negativo sostenido no es un
  cliente exigente, es un empleado al que le pagas tú.

**Cada cuánto:** una vez al mes cerrado y con los mismos criterios de reparto que
el mes anterior. Cambiar el criterio entre meses hace que la serie no se pueda
comparar, que es para lo único que sirve medirlo.

**Dos avisos.** Este número es de gestión y no es contabilidad: sirve para
decidir, no para declarar, y lo que sea fiscal se consulta con quien te lleve los
impuestos. Y las horas salen del registro, no de la memoria: apunta un mes las
horas por cliente y con ese patrón ya puedes calcular: si las estimas, el coste
que sale es una opinión con decimales, igual que el número que este SOP te manda
posponer.

## Una métrica que nadie mira se deja de medir

Regla de higiene, y es tan importante como todo lo anterior.

Cada mes, mira tu propia lista y marca qué números ha mirado alguien para decidir
algo. Los que no ha mirado nadie se retiran. No se archivan por si acaso: se
retiran, porque cada campo que hay que rellenar tiene un coste diario y compite
con los campos que sí se usan. Un registro con veinte campos que nadie completa
vale menos que uno con cinco que se rellenan siempre.

**Un sistema de cuatro reglas que se usa vale más que uno de veinte que se lee una
vez.** Y si te cuesta decidir cuál cae, la pregunta es la de siempre: si ese
número se dobla mañana, ¿qué harías distinto?

## Los errores que más se ven

- **Montar el sistema complejo antes de trackear algo.** Se rompe, se abandona, y
  te quedas con cero. Empieza tosco.
- **Reconstruir el mes de memoria el último día.** Produce números altos, sin
  fecha y sin causa, y te hace tomar decisiones con datos inventados de buena fe.
- **Leer ratios sin volumen.** Cambiar el proceso cada semana porque el
  porcentaje se mueve es asegurarte de que nada llega nunca a poder medirse.
- **No actualizar el estado después de una llamada.** Es un minuto de trabajo que
  invalida el panel entero si no se hace.
- **Medir a alguien por algo que no controla.** Convierte la revisión en una
  discusión de excusas legítimas.
- **Mirar solo el último mensaje o el último dato.** Si solo lees el final, se te
  escapan las cosas que se venían repitiendo, y esas se componen hasta convertirse
  en una lista de problemas que hace tres semanas era uno.
- **Mirar el margen medio en vez de la lista de clientes ordenada.** El promedio
  tapa exactamente al cliente que te está costando dinero, que es el único motivo
  por el que hacías la cuenta.
- **Usar la mensajería como CRM.** Ir haciendo scroll para acordarte de quién era
  cada uno funciona con diez personas y con cincuenta pierdes leads que ya habías
  pagado.
- **Meter en un pitch un número que no puedes enseñar.** Antes de que una cifra
  salga de casa, tiene que existir la captura o el registro con fecha que la
  sostiene. Si no, un día te lo preguntan y no sabes contestar.
- **Tratar una pieza de venta como dato.** Lo que dice tu página o el testimonio
  de alguien es promesa comercial. Para decidir se usa el registro, no el
  material que hiciste para convencer.

## Qué no tocar todavía

- **Nada de base de datos compleja ni herramienta de pago mientras la carga
  operativa sea baja.** Te reparte la cabeza en algo que no te devuelve nada, y el
  criterio para cambiar es carga, no facturación.
- **Nada de tests A a B mientras no tengas impresiones suficientes.** Sin volumen
  no puedes distinguir la variante del azar, y vas a "aprender" cosas falsas que
  luego defiendes.
- **Nada de paneles bonitos hasta que los datos entren solos o entren siempre.**
  Un gráfico sobre datos incompletos te da confianza en un número falso, que es
  peor que la duda.
- **Nada de medir el equipo antes de que exista el parte diario.** Primero el
  registro, después la conversación de rendimiento.
- **Nada de calcular valor de vida de cliente ni márgenes finos con pocos meses
  de histórico.** Es la métrica que más se pospone y con razón: sin recorrido, el
  número que sale es una opinión con decimales. Se retoma cuando tengas al menos
  un año de cobros registrados, y hasta entonces se decide con caja. **Con una
  excepción que no es menor: el coste de entrega y el margen por cliente sí se
  calculan en cuanto haya sueldos o comisiones dentro**, porque ese no necesita
  histórico, necesita un mes cerrado y las horas apuntadas. Está más arriba.
