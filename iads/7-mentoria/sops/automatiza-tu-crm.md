# Automatiza tu CRM

Este fichero está escrito para que se lo pases a tu IA y lo haga ella. Tú solo
tienes que decirle con qué herramienta quieres conectar tu CRM.

Ábrelo con tu Claude dentro de esta carpeta y dile, por ejemplo:

> Lee sops/automatiza-tu-crm.md y conéctame ManyChat para que cuando alguien me
> escriba por Instagram entre solo en mi CRM.

---

## Lo que hay que saber

Todo el trabajo ya está hecho: el CRM, la puerta de entrada y el conector del
calendario existen y funcionan. Lo único que queda es enchufarlos a tu negocio,
y eso lo haces tú porque las claves y los datos son tuyos y no deben pasar por
las manos de nadie.

Tu CRM tiene una puerta de entrada. Le mandas un mensaje con los datos de una
persona y aparece como lead, sin que nadie pulse nada.

**Dirección:** `POST https://clientes.infocapitals.com/api/crm/entrada`

**Llave:** la tuya, la que sale en la plataforma en CRM → Conectar. Empieza por
`ic_`. Va en la cabecera `Authorization: Bearer TU_LLAVE`, y si la herramienta
no deja poner cabeceras, vale también pegándola en la dirección como
`?k=TU_LLAVE`.

**Lo que se manda**, en JSON:

```json
{
  "nombre": "Marta Lopez",
  "telefono": "+34 600 000 000",
  "instagram": "@marta.lopez",
  "email": "marta@ejemplo.com",
  "nota": "Pidió precio por Instagram",
  "origen": "manychat"
}
```

Solo hace falta el nombre o un contacto (teléfono, Instagram o email). Todo lo
demás es opcional. Y no hay que renombrar campos: entiende también `name`,
`full_name`, `phone`, `whatsapp`, `ig`, `correo`, `message`, `source`, y un
`contacto` genérico que reparte solo según sea teléfono, email o usuario, así
que casi siempre se puede mandar lo que la herramienta ya manda por su cuenta.

Campos que puedes añadir si los tienes: `avatar` (a qué tipo de cliente
corresponde), `capacidad` (cuánto factura o puede invertir, tal cual lo diga),
`etapa` (`cualificado`, `seguimiento`, `no_show` o `ganado`; si no la pones
entra como cualificado) y `origen`, que es el que te va a decir qué embudo te
trae gente de verdad. Ponlo siempre. Cada lead entra con su fuente (`source`)
puesta al mismo valor que `origen`, así sale en los filtros de Leads.

**Comprobar que va**, sin crear ningún lead:

```
GET https://clientes.infocapitals.com/api/crm/entrada?k=TU_LLAVE
```

Si responde `{"ok":true,"conectado":true}`, la llave funciona.

---

## Dos cosas que hace solo y conviene que sepas

**No duplica.** Si el mismo contacto entra dos veces, no se crea un lead nuevo.
Puedes reintentar un webhook sin miedo a ensuciarte el CRM.

**Entra sin próxima acción, a propósito.** El lead aparece en la pantalla Hoy,
en el bloque "Sin próxima acción", esperando a que alguien decida qué hacer con
él. Es deliberado: si le pusiéramos una fecha automática parecería atendido sin
estarlo, y esa es exactamente la forma de que un lead se muera sin que nadie se
entere.

---

## Antes de nada: tu calendario, que no necesita nada de esto

Si agendas llamadas con Cal.com o con Calendly, la conexión más valiosa no
lleva webhook ni JSON: en la plataforma, CRM, pestaña Conectar, eliges tu
proveedor y pegas tu API key. Desde ese momento cada reserva entra sola como
lead agendado, con nombre, email, la fecha de la llamada y lo que contestó en
tu formulario de reserva.

Dónde se crea la key: en Cal.com, Settings, Developer, API keys. En Calendly,
Integrations, API and webhooks, Personal access token.

Hazlo lo primero. La puerta de abajo es para todo lo demás (ManyChat,
formularios, tus propios cacharros); las llamadas agendadas ya vienen solas.

---

## Recetas

### ManyChat (Instagram y WhatsApp)

En el flujo que quieras, añade un paso **External Request**:

- Método: POST
- URL: `https://clientes.infocapitals.com/api/crm/entrada`
- Headers: `Authorization` con valor `Bearer TU_LLAVE`, y `Content-Type` con
  valor `application/json`
- Body (JSON), usando los campos del contacto de ManyChat:

```json
{
  "nombre": "{{first name}} {{last name}}",
  "contacto": "{{phone}}",
  "nota": "{{last text input}}",
  "origen": "instagram"
}
```

Ponlo después de tus preguntas de cualificación, no al principio. Si lo pones en
el primer mensaje te va a entrar en el CRM todo el que abra la conversación,
incluido el que pasaba por ahí, y el CRM deja de servir.

Ojo con las variables: en el body de ManyChat se insertan con el selector de variables (se ven como fichas de color). Si escribes las llaves a mano, ManyChat manda el texto literal y el lead llega vacío.

### Un formulario (Tally, Typeform, Framer, tu web)

Casi todos tienen webhooks. Apúntalo a la misma dirección con la misma cabecera.
Si el tuyo manda los campos con sus propios nombres, prueba primero tal cual:
entiende los nombres habituales y lo más probable es que funcione sin tocar nada.

### Zapier, Make o n8n

Un paso de tipo "Webhook / HTTP Request", método POST, misma URL y misma
cabecera. Es el camino si quieres meter de por medio tu calendario, tu pasarela
de pago o una hoja de cálculo.

### Una página de VSL

Tiene su propio procedimiento porque lleva una pieza más, los UTM por vídeo:
`sops/trackea-tu-vsl.md`. La puerta de entrada es la misma de aquí.

### Tu hoja de cálculo de siempre

Si llevas los leads en un Sheets y no quieres cambiar de sitio, pídele a tu IA
que te escriba un Apps Script que mande cada fila nueva a esa dirección. Así
sigues apuntando donde apuntas hoy y el CRM se rellena solo.

---

## Cómo pedírselo a tu IA

Dale el contexto entero de una vez, que es lo que hace que no tenga que
preguntarte cinco veces:

> Lee sops/automatiza-tu-crm.md. Mi llave es `ic_...`. Uso [tu herramienta] y mi
> embudo es así: [cuéntalo en dos frases]. Móntame la conexión y dime
> exactamente dónde pego cada cosa. Cuando esté, comprueba con el GET que
> responde ok.

Si tienes varios embudos (por ejemplo Instagram por un lado y anuncios por
otro), no montes uno solo: monta uno por embudo y cambia el `origen` en cada
uno. Es la única forma de saber después cuál de los dos te trae clientes y cuál
te trae ruido. Díselo así a tu IA y lo hace.

---

## Cuidado con la llave

Es la llave de escritura de tu CRM. Quien la tenga puede meter leads.

No la pegues en un sitio público ni en un repositorio, no la mandes por
WhatsApp y no la enseñes en un directo. Si se te escapa, entra en CRM →
Conectar y pulsa Rehacer la llave: la vieja deja de funcionar en el acto y solo
tienes que actualizar tus conexiones con la nueva.
