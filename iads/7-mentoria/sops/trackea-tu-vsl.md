# Trackea tu VSL

Este fichero está escrito para que se lo pases a tu IA y lo haga ella. Tú solo
tienes que tener la llave de tu CRM a mano.

Ábrelo con tu Claude dentro de esta carpeta y dile:

> Lee sops/trackea-tu-vsl.md y móntame la página del VSL con el tracking
> conectado a mi CRM.

---

## Qué vas a poder responder cuando esté

- Qué vídeo tuyo trae leads y cuál no trae ninguno.
- Cuántos de los que ven el VSL dejan sus datos.
- Cuántos de esos agendan, cuántos se presentan y cuántos cierran.
- Cuánto te cuesta cada lead por pieza, si haces anuncios.

Y esto es lo importante: todo eso sale **dentro de tu CRM**, no en cinco
herramientas distintas. El mismo lead que entra por el VSL es el que luego
aparece en Pipeline, en Cobros y en Métricas.

## Cómo funciona, en una frase

Tu página del VSL manda el lead a tu CRM por la misma puerta que ya usa
ManyChat, y le pega los UTM del enlace por el que llegó. El CRM cuelga ese lead
del enlace y a partir de ahí cuenta solo.

```
vídeo de YouTube  →  enlace con UTM  →  tu página del VSL
                                            ↓ opt-in
                                        tu CRM (lead con su UTM)
                                            ↓
                                        calendario  →  llamada  →  cierre
```

## Paso 1 · El enlace, antes de publicar el vídeo

Esto va primero y es donde casi todo el mundo la caga. Si publicas el vídeo con
el enlace pelado, el lead entra sin saber de dónde viene y ya no hay forma de
recuperarlo.

En la plataforma, **CRM → Enlaces → Crear enlace**:

- **Título**: el nombre del vídeo, para reconocerlo tú.
- **Fuente**: YouTube, Instagram, TikTok, Facebook.
- **Dónde se pega**: descripción, comentario fijado, bio, historia, reel o
  anuncio.
- **Destino**: la URL de tu página del VSL.

Te devuelve un enlace ya marcado. **Ese es el que pegas en la descripción del
vídeo**, no el de tu página a secas. Uno por pieza. Cuesta veinte segundos y es
lo único que hace que el resto tenga sentido.

## Paso 2 · La página tiene que arrastrar los UTM hasta el final

Cuando alguien llega a tu página, los UTM vienen en la dirección. Tu página
tiene que guardarlos en el navegador en cuanto carga, y volver a mandarlos
cuando la persona rellena el opt-in.

Si el formulario está en otra dirección que la página, o si el calendario está
en otro dominio, **los UTM se pierden en el salto**. Hay que pasarlos a mano en
la URL. Tu IA sabe hacerlo, pero díselo, porque si no lo pides no lo hace.

## Paso 3 · El opt-in entra en tu CRM

La puerta de entrada de tu CRM es la misma de siempre:

**Dirección:** `POST https://clientes.infocapitals.com/api/crm/entrada`

**Llave:** la tuya, en la plataforma en **CRM → Conectar**. Empieza por `ic_`.
Va en la cabecera `Authorization: Bearer TU_LLAVE`, o pegada en la dirección
como `?k=TU_LLAVE` si la herramienta no deja poner cabeceras.

Lo que manda la página cuando alguien rellena el opt-in del VSL:

```json
{
  "nombre": "Marta Lopez",
  "telefono": "+34 600 000 000",
  "email": "marta@ejemplo.com",
  "instagram": "@marta.lopez",
  "origen": "vsl",
  "nota": "Opt-in del VSL",
  "utm_source": "youtube",
  "utm_medium": "descripcion",
  "utm_campaign": "como-escalar-sin-ads",
  "utm_content": "enl_a1b2c3"
}
```

Los cuatro `utm_` son los que traía el enlace. **No los inventes ni los
recortes**: se copian tal cual llegaron en la dirección. El que une el lead con
el enlace es `utm_content`.

Pon siempre `origen: "vsl"`. Es lo que te deja filtrar en Leads y comparar el
VSL contra tus otros embudos.

Para comprobar que la llave va, sin crear ningún lead:

```
GET https://clientes.infocapitals.com/api/crm/entrada?k=TU_LLAVE
```

## Paso 4 · El calendario, conectado

En **CRM → Conectar** enchufas tu Cal.com o tu Calendly con su clave de API. A
partir de ahí, cuando alguien reserva, el lead pasa a agendado solo y la
llamada aparece en Hoy. No hace falta que la página haga nada más.

Un detalle que cambia el número: en el calendario, pide el mismo email que
pediste en el opt-in. Es lo que hace que el CRM reconozca que el que agenda es
el mismo que dejó los datos, y no te cree un lead duplicado.

## Paso 5 · Qué miras cada semana

En **CRM → Enlaces** tienes leads y cierres por pieza. Esa tabla es la que
decide qué grabas la semana que viene.

En **Métricas** tienes el embudo completo de los leads del VSL, igual que el de
cualquier otro origen.

La pregunta que respondes con las dos: no es qué vídeo tiene más visitas, es
qué vídeo trae clientes. Casi nunca es el mismo.

## Lo que hoy NO llega a tu CRM

Sé honesto contigo con esto: el CRM cuenta **personas**, no segundos de vídeo.
Cuántos le dieron al play y en qué minuto se fueron no entra hoy.

Si lo necesitas, tienes dos formas de saberlo:

- El sitio donde alojas el vídeo te da la curva de retención. Míralo ahí.
- Cuando tengas volumen de verdad, pídenoslo. Es una pieza que se añade, no un
  invento.

Mientras tanto, con leads y cierres por pieza tienes lo que decide el dinero.
La retención decide dónde cortar el vídeo, y eso es el segundo problema, no el
primero.

## Errores que se pagan caro

- **Publicar el vídeo con el enlace sin marcar.** El lead entra como directo y
  no se puede atribuir. No tiene arreglo a posteriori.
- **Un enlace para todo.** Si todos tus vídeos llevan al mismo enlace marcado,
  sabes que YouTube funciona y no sabes qué vídeo. Uno por pieza.
- **Pedir más datos de los necesarios en el opt-in.** Nombre, WhatsApp y email.
  Cada campo de más son leads de menos.
- **Meter pasos entre el vídeo y el calendario.** Cada pantalla extra pierde a
  quien ya estaba convencido.
- **Cambiar el email entre el opt-in y el calendario.** Te duplica el lead y te
  rompe el embudo.
- **Enseñar el botón de agendar desde el segundo cero.** Que aparezca cuando el
  vídeo ya ha hecho su trabajo.

## Cómo pedírselo a tu IA

Ábrele Claude dentro de esta carpeta y pégale esto, cambiando lo que va en
mayúsculas:

> Lee sops/trackea-tu-vsl.md entero.
>
> Móntame la página del VSL en MI-DOMINIO.COM con esta estructura: titular,
> vídeo, y un botón de agendar que lleva a mi calendario. El opt-in de nombre,
> WhatsApp y email sale encima del vídeo a los dos segundos de cargar, o antes
> si pulsan play.
>
> El tracking: guarda los utm_ de la dirección en cuanto cargue la página,
> mándalos al webhook de mi CRM junto con los datos del opt-in, y pásalos
> también al calendario en la URL. Mi llave es la que te doy aparte, no la
> escribas en ningún sitio público del código.
>
> Cuando termines, haz una prueba de punta a punta con datos falsos, enséñame
> el lead en el CRM y luego bórralo.

Dos cosas que le tienes que dar tú y no están aquí: **tu llave** del CRM y **la
URL de tu calendario**.

## Cuidado con la llave

Tu llave abre la puerta de tu CRM. No la pegues en un sitio público, no la
subas a un repositorio abierto y no la mandes por un grupo. Si crees que se ha
visto, en **CRM → Conectar** la cambias y la vieja deja de valer al momento.
