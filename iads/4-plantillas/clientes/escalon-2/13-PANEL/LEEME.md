# El panel del cliente

## Cómo quedó montado (20/10/2026)

- **Aplicación web (Apps Script):** `https://script.google.com/macros/s/AKfycby0xNOBSqBoaEcnQn4FPrvKQazJKPV1VSI4fEFhp-GOt0RgbMEJHqMX0y7WrBXcqKCMeQ/exec` · proyecto **iAds · Panel**
- **La hoja:** `https://docs.google.com/spreadsheets/d/1EfqoYnU_SMmsf0P8fDEofMCDO-x2A8feG_Ij8NBN0ko/edit`
- **La demo, sin contraseña:** `?demo=1` (números inventados de una marca que no existe).
- ⏳ **Falta:** subirlo a Netlify y el dominio `panel.iads-agency.es`.

**`panel.html` es el que se edita.** `web-panel/index.html` es una copia suya: es la carpeta que se arrastra a Netlify. **Antes de subir, siempre:**

```bash
cp 4-plantillas/clientes/escalon-2/13-PANEL/panel.html 4-plantillas/clientes/escalon-2/13-PANEL/web-panel/index.html
```

Si se te olvida, subes la versión vieja. Es lo que ya pasó con el alta.

---

## El texto que se escribe solo

**Solo en la portada**, la pantalla de bienvenida. El titular y el párrafo se escriben letra a letra, como en el alta: es el mismo momento, el cliente acaba de entrar y no hay nada más delante. Los puntos, la línea de abajo y el botón aparecen cuando termina.

**Dentro del panel no se escribe nada**, a propósito: ahí entra cada lunes a mirar números y esperar a que salgan cansa a la segunda vez.

Un toque en la pantalla lo salta. Quien tiene las animaciones desactivadas en su móvil, o abre el enlace en una pestaña de fondo, lo ve entero de golpe.

## Los dos modos

Arriba del todo del `<script>` hay una línea:

```js
var SERVIDOR = '';
```

**Vacío = demo siempre.** La página se pinta sola con los números de ejemplo y no pide nada.

**Para enseñarla en una llamada con el servidor ya puesto:** añade `?demo=1` al enlace. Los números son inventados y la marca no existe, así que no hay nada que proteger.

**Con la dirección puesta = de verdad.** La página llega **vacía**, pide la contraseña, se la manda al script de Google y el script devuelve los números de ese cliente.

**La contraseña no está en la página.** La comprueba el servidor. Si estuviera aquí, cualquiera abriría el código de la página y la leería, y los números estarían dentro de todas formas.

---

## Montarlo (una sola vez)

### 1 · El script de Google

1. Entra en **script.new**.
2. Arriba a la izquierda, ponle de nombre **iAds · Panel**.
3. Borra lo que haya en `Código.gs` y pega **`apps-script/Codigo.gs`** de esta carpeta.
4. Ejecuta la función **`verHoja`** (botón ▶ arriba, eligiéndola en el desplegable). Acepta los permisos. Eso **crea la hoja de cálculo** *iAds · Panel* en tu Drive y te deja su enlace en el registro de abajo.
5. **Implementar → Nueva implementación → Aplicación web.**
   - *Ejecutar como:* **yo**
   - *Quién tiene acceso:* **cualquier usuario**
6. Copia la URL que acaba en **`/exec`**.

> ⚠️ **Tiene que ser "cualquier usuario"**, y si cambias el código hay que **publicar una versión nueva**. Para que la URL no cambie: *Gestionar implementaciones → el lápiz → Versión: Nueva versión*. Si creas una implementación nueva, la URL cambia y hay que volver a pegarla en `panel.html`.

### 2 · La hoja

En *iAds · Panel*, **una fila por cliente**:

| marca | clave | datos |
|---|---|---|
| nordik | la-que-sea | `{"marca":"Nordik", …}` |

- **marca** es lo que va en el enlace (`?c=nordik`). Sin mayúsculas, sin acentos, sin espacios.
- **clave** es su contraseña. Se la mandas por WhatsApp junto al enlace.
- **datos** es el bloque de números en JSON. **Lo deja Claude cada lunes**, con los números que pasa Marc.

**Para probarlo sin cliente:** ejecuta la función **`sembrarPrueba`** desde el editor. Mete una fila con la marca `nordik` y la contraseña `prueba`. Cuando ya no haga falta, borra esa fila de la hoja a mano.

### 3 · La página

1. En `panel.html`, pon la URL en `var SERVIDOR = '…/exec';`
2. Copia el archivo a `web-panel/index.html` (el comando de arriba).
3. Arrastra la carpeta **`web-panel`** a Netlify.

### 4 · El dominio

Igual que el alta, en DonDominio: un **CNAME** `panel` → `[el-sitio].netlify.app`. Netlify te pedirá además un **TXT** de verificación.

> ⚠️ **No pasar los DNS del dominio a Netlify**: se llevaría por delante el correo `sami@iads-agency.es`.

---

## El enlace de cada cliente

```
https://panel.iads-agency.es/?c=nordik
```

Más su contraseña, por WhatsApp. **Si entra desde el mismo móvil otra vez, no se la vuelve a pedir** (se queda guardada en su navegador).

---

## Probarlo

**En una ventana de incógnito, nunca con curl ni desde el navegador de Claude.** Apps Script devuelve error 400 a todo lo que no sea un navegador normal, aunque esté bien publicado. Eso ya costó una hora con el alta.

---

## Lo que falta

- **Los estados que aún no están:** cliente en pausa, cobro fallido, cliente que se va y semana sin datos. Están pensados en `NOTAS.md`, apartado 6.
- **Conectar Meta** en vez de ir a mano: pide verificación de empresa (Marc, 17/10). Se mira cuando la empresa esté registrada.
