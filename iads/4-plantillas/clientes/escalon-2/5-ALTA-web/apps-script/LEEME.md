# El alta, funcionando de verdad (Google Apps Script)

> ⏳ **Pendiente, sin prisa (20/10): jubilar la copia vieja.** El `doGet` de `Codigo.gs` todavía sirve `Pagina.html`, que es **el alta con el flujo de accesos antiguo** (el ID del portfolio y el "acceso como socio"). El enlace que se manda es el de `alta.iads-agency.es`, así que hoy no molesta, pero **es una copia que ya ha divergido** y algún día se manda por error. Lo suyo: que ese `doGet` redirija a `alta.iads-agency.es` y borrar `Pagina.html`. Son dos líneas y pegar el `Codigo.gs` una vez. *(Sami, 20/10: "apúntalo para después, da igual ya".)*


> **Los dos escalones van en la misma página (19/10).** El enlace manda: `alta.iads-agency.es/?c=Nordik` da el formulario del escalón 2 (30 preguntas) y `?c=Nordik&e=1`, el del escalón 1 (25). Dentro del archivo son `PREGUNTAS_E2`/`INTROS_E2` y `PREGUNTAS_E1`/`INTROS_E1`.
>
> **Tipos de pregunta nuevos:** `multi` (casillas, se puede marcar más de una: los formatos y dónde publica) y `gustan` (dos áreas: los anuncios que le gustan y los que no).
>
> ⚠️ **Antes de mandárselo a un cliente, hay que rellenarlo entero una vez**, los dos escalones, y comprobar que llega bien al Drive. **Probado el 19/10 solo hasta la pregunta 2.**
>
> ⚠️ **Pendiente de subir a Netlify (19/10).** La página publicada está desfasada en dos cosas: el enlace de la llamada (ahora `/arranque`) y el nombre del documento del día 6 (ahora "tu plan de vídeos"). **Se sube cuando estén todos los cambios del onboarding** (Sami, 18/10), arrastrando la carpeta `web-alta`.


> **El enlace de la llamada** está en `web-alta/index.html`, en la línea `var CALENDLY = …`. Hoy es `https://calendly.com/sami-iads-agency/arranque`. **Si se cambia, hay que volver a arrastrar la carpeta `web-alta` a Netlify** o el cliente sigue viendo el viejo.


La misma página del prototipo, **con el mismo diseño**, servida desde el Google de Sami. Cada cliente tiene **su propio documento** en el Drive, que se escribe solo con sus respuestas. Cuesta 0 €, no hay servidor y no hace falta ninguna cuenta nueva.

**Por qué no se queda dentro de Claude:** una página publicada ahí solo guarda datos de quien entra con la cuenta de Sami. Un cliente de fuera puede verla y rellenarla, pero lo que escribe no sale de su navegador (comprobado el 16/10). El diseño no se pierde: es el mismo archivo HTML.

## Montarlo (una sola vez)

1. Entra en **script.new** (se abre un proyecto de Apps Script vacío).
2. Arriba a la izquierda, ponle de nombre **iAds · Altas**.
3. Borra lo que haya en `Código.gs` y pega **`Codigo.gs`** de esta carpeta.
4. En **Archivos**, pulsa **+ → HTML**, llámalo **`Pagina`** (sin .html) y pega dentro **`Pagina.html`**.
5. **Implementar → Nueva implementación → Aplicación web.** *Ejecutar como:* **yo**. *Quién tiene acceso:* **cualquier usuario**. Acepta los permisos (Google avisa de "app no verificada": Configuración avanzada → Ir a iAds · Altas).
6. Copia la URL, que acaba en `/exec`.

## El enlace de cada cliente

La URL de arriba más `?c=` y el nombre de su marca:

```
https://script.google.com/macros/s/AKfy…/exec?c=Nordik
```

La pantalla le saluda por su marca y sus respuestas van a **su documento**. Si cierra y vuelve con el mismo enlace, sigue donde lo dejó.

## Dónde caen las respuestas

En una carpeta del Drive llamada **iAds · Altas**, un documento por cliente: *Alta · Nordik*. Dentro, cada bloque con su título, cada pregunta en negrita y la respuesta debajo. Lo que aún no ha contestado pone "— sin contestar —".

El documento se reescribe **cada vez que el cliente pasa de pregunta**, no en cada letra.

Si pierdes el enlace de un documento, en el editor de Apps Script ejecuta la función `verAltas()` y los verás todos en el registro.

## Cuando haya que cambiar algo

El texto de las preguntas vive en `Pagina.html`, igual que en el prototipo. Si se añade o se quita una pregunta, hay que tocarla también en la lista `PREGUNTAS` de `Codigo.gs`, que es la que ordena el documento.

## Lo que falta

- **El botón de grabar la nota de voz.** Ahora mismo esa pregunta se contesta escribiendo.
- **El ID del portfolio** de la guía de accesos (pendiente de Marc). El correo de Shopify ya está puesto: `sami@iads-agency.es`.
- **El dominio propio.** Si algún día quieres que el enlace sea `alta.iads-agency.es`, es una redirección; la página no cambia.

---

## Cómo quedó montado (16/10/2026)

- **URL de la aplicación web:** `https://script.google.com/macros/s/AKfycbyNQvZi0dcU6oKSZpdxDYPQsWsv0fXyAZ2RoK-95HsoUgOkEKZHBoDyp2ngt4KmIFqf9Q/exec`
- **Enlace de un cliente:** esa URL + `?c=Nordik`.
- **Dos cosas que costaron una hora, para no repetirlas:**
  - El acceso tiene que ser **Anyone** y hay que crear una **implementación nueva** (editar la que había no bastó).
  - **Desde fuera de un navegador normal, Google devuelve error 400** aunque esté bien publicada: no es un fallo. Se comprueba **en una ventana de incógnito**, nunca con curl ni con el navegador de Claude.
- **Probado el 16/10:** un alta de prueba escribió su documento en la carpeta *iAds · Altas* del Drive de Sami, con cada respuesta debajo de su pregunta.

## Cómo quedó montado de verdad (16/10, probado de punta a punta)

**La página es de iAds, y a Google solo le llegan los datos.** No hay iframe: se probó y **no vale**, porque una página de Apps Script metida dentro de otra depende de cookies de terceros y Safari las bloquea de serie — la mitad de los clientes, los del iPhone, verían un error de Google Drive.

**Las tres piezas:**

1. **`alta.iads-agency.es`** (DonDominio) → CNAME a Netlify.
2. **Netlify** (proyecto `eclectic-souffle-a4b028`) sirve `web-alta/index.html`, que es **la página entera**: las 30 preguntas, el diseño, todo.
3. **La página manda las respuestas por POST** a la aplicación web de Apps Script, que las escribe en el documento del cliente, en la carpeta **iAds · Altas** del Drive de Sami.

**Los datos concretos (16/10):**
- **Enlace del cliente:** `https://alta.iads-agency.es/?c=Nordik`
- **Aplicación web:** `https://script.google.com/macros/s/AKfycbw2QSZF00y0i18-26DjuxhEdVxFV4g4phuYtIpPEV9xYSc3vhpkgNGpVq55OpWHR6K1Og/exec` (versión 5)
- **DNS:** CNAME `alta` → `eclectic-souffle-a4b028.netlify.app` · TXT `subdomain-owner-verification` → `d331f13974a825ce703598829c93b400`
- **Probado el 16/10:** rellenando desde el navegador apareció *Alta · Nordik* en el Drive, con las respuestas debajo de cada pregunta.

**Cuando haya que cambiar la página** (texto, preguntas, diseño): se toca `web-alta/index.html` y **se arrastra la carpeta `web-alta` otra vez** a Netlify (Deploys → el recuadro de abajo). Arrastrarla es "guardar": se queda el mismo sitio con el contenido nuevo.

**Cuando haya que cambiar el script** (`Codigo.gs`): se pega en Apps Script y se publica. **Ojo:** si se crea una implementación nueva, **la URL cambia** y hay que meterla en `web-alta/index.html` (la constante `GUARDAR_EN`) y volver a arrastrar la carpeta. Para que no cambie, usar *Manage deployments → lápiz → Version: New version*.

**Lo que costó una hora, para no repetirlo:**
- El acceso de la aplicación web tiene que ser **Anyone**.
- **Desde fuera de un navegador normal Google devuelve error 400** aunque esté bien publicada: no es un fallo. Se comprueba en **incógnito**, nunca con curl.
- **No pasar los DNS del dominio a Netlify:** se llevaría por delante el correo `sami@iads-agency.es`.

