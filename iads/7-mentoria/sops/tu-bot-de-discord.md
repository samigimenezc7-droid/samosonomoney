# Tu bot de Discord, para pedirle cosas a tu IA

Tu servidor ya tiene nuestro bot: es el que te montó las categorías y los
canales, y el que le abre su canal a cada cliente tuyo cuando entra. Eso sigue
funcionando y no hay que tocarlo.

**Antes de leer esto: casi seguro que no lo necesitas.** Crear un rol, dárselo
o quitárselo a alguien y abrir un canal privado lo tienes en la pestaña
**Discord** de tu plataforma, con un botón, y lo ejecuta nuestro bot que ya
está dentro de tu servidor. Sin token y sin salir de ahí. Mira eso primero.

Esto es otra cosa y es opcional: **tu propio bot**, para que le puedas decir a
tu Claude en tu ordenador "créame un rol de alumnos y mételo a estas tres
personas" y lo haga sin pasar por la plataforma. Es gratis y la llave es tuya.
Lo quiere quien ya trabaja con Claude Code a diario; si no es tu caso, cierra
esto y usa la pestaña.

Ábrelo con tu Claude y dile:

> Lee sops/tu-bot-de-discord.md y acompáñame a crear mi bot.

---

## Por qué tu bot y no el nuestro

Te lo decimos claro porque nos lo vas a preguntar: el token de nuestro bot no
te lo podemos pasar. Ese mismo bot está dentro de nuestro servidor y del de
otros clientes, así que quien tiene esa llave puede leer y borrar cosas que no
son suyas. No es desconfianza contigo, es que una llave compartida deja de
proteger a todo el mundo a la vez.

Con el tuyo mandas tú: vive solo en tu servidor, lo revocas cuando quieras y no
depende de nosotros para nada.

---

## Crearlo, paso a paso

1. Entra en https://discord.com/developers/applications con tu cuenta de
   Discord, la misma con la que creaste tu servidor.
2. Arriba a la derecha, **New Application**. Ponle el nombre de tu marca y
   acepta.
3. En el menú de la izquierda, **Bot**. Si te pide confirmar que quieres crear
   el bot, dile que sí.
4. En esa misma pantalla, **Reset Token** y luego **Copy**. Eso es tu token: un
   texto largo que empieza por algo tipo `MTIzN...`. **Cópialo y guárdalo en tu
   gestor de contraseñas ahora**, porque Discord no te lo vuelve a enseñar; si
   lo pierdes, se pulsa Reset Token otra vez y sale uno nuevo.
5. Baja un poco y activa los tres interruptores de **Privileged Gateway
   Intents** (Presence, Server Members, Message Content). Sin el de miembros, tu
   bot no puede ver a tu gente y no podrá asignarle roles.
6. En el menú de la izquierda, **OAuth2**. En **Scopes** marca `bot`, y en
   **Bot Permissions** marca **Administrator**. Es tu servidor y tu bot, así que
   lo más simple es darle permiso completo.
7. Copia la URL que te ha generado abajo, ábrela en otra pestaña, elige **tu
   servidor** y autoriza.
8. Y lo último, que es lo que falla siempre: en tu servidor, **Ajustes del
   servidor, Roles**, arrastra el rol de tu bot **por encima** de los roles de
   tu equipo y de tus clientes.

---

## Cómo pedirle cosas a tu Claude

Abre tu Claude en la carpeta y dale el contexto de una vez, que es lo que evita
que te pregunte cinco veces:

> Tengo un bot de Discord en mi servidor. El token es `MTIzN...` y el ID de mi
> servidor es `123456789`. Léete sops/tu-bot-de-discord.md y usa la API de
> Discord para lo que te pida.

El ID de tu servidor lo sacas así: en Discord, Ajustes de usuario, Avanzado,
activa **Modo desarrollador**. Luego clic derecho en el nombre de tu servidor,
**Copiar ID del servidor**.

A partir de ahí le pides las cosas en cristiano:

> Créame un rol que se llame Alumnos, en gris, y que no pueda mencionar a todos.

> Mete a estos tres al rol Alumnos: [pega los nombres o los IDs].

> Créame un canal privado que se llame seguimiento-marta, que solo lo vean
> Marta y yo.

> Dime quién de mi servidor lleva más de treinta días sin escribir.

> Bórrame los canales de la categoría ANTIGUOS, pero antes enséñame la lista y
> espera a que te diga que sí.

Esa última manía cógela como norma: **antes de borrar nada, que te enseñe la
lista y espere**. Un borrado en Discord no se deshace.

---

## Si no funciona, en orden

1. **"Missing Permissions" o error 403 al crear o asignar un rol.** Es el rol
   del bot, que está por debajo. Discord no deja gestionar roles que están por
   encima del tuyo. Ajustes del servidor, Roles, y sube el del bot. Es el fallo
   número uno y casi siempre es este.
2. **"401 Unauthorized".** El token está mal copiado o lo has reseteado después.
   Vuelve a Developer Portal, Bot, Reset Token, y pásale el nuevo a tu Claude.
3. **No ve a tus miembros, o te dice que la lista está vacía.** Te falta activar
   Server Members Intent en la pantalla del bot.
4. **"Unknown Guild".** El ID del servidor está mal, o el bot no está dentro.
   Repite el paso 7 y comprueba que lo autorizaste en el servidor correcto.
5. Si después de esto sigue sin ir, escríbenos por tu canal con el error tal
   cual te sale. No nos mandes el token por chat: los mensajes se quedan ahí y
   con esa llave se entra en tu servidor.

---

## Dónde acaba tu bot y empieza el nuestro

El nuestro se queda con lo que te montamos: los canales de tu portal y el canal
que se le abre a cada cliente tuyo cuando entra. Si algún día quieres que lo
saquemos de tu servidor, se saca y no pierdes nada de lo que ya está creado.

El tuyo es para todo lo demás: tus roles, tu gente, tus canales, tus limpiezas.
Los dos pueden convivir en el mismo servidor sin pisarse.
