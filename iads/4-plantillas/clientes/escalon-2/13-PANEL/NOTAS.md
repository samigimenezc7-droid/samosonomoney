# El panel del cliente · notas para decidir

16/10/2026. **Esto no es la plantilla todavía:** es lo pensado mientras Sami no estaba, para decidirlo juntos. Cada apartado acaba con una recomendación.

**Por qué importa:** el contrato lo promete (cláusula 1d: *"un panel con sus resultados, un informe cada lunes y una llamada al mes"*), y el informe del lunes acaba diciendo *"tienes el detalle en tu panel"*. Sin panel, esa frase es mentira.

---

## ✅ DECIDIDO (17/10, hablado con Marc) · a mano, de momento

Marc, literal: *"para conectar la meta… tu panel necesita una verificación de empresa para pedir [la API] a Meta, es una locura. Es mucho más cómodo con reportes."* **Se queda a mano**, y se conecta el día que la empresa esté registrada y verificada.

**Cómo, sin que nadie teclee números:**
1. **Marc deja los números en una hoja de Google** cada domingo (o sube ahí el informe que saque de Meta).
2. **Claude lee esa hoja** por el conector de Drive.
3. **Claude actualiza el panel y Sami arrastra la carpeta** a Netlify.

**Pendiente de la segunda llamada con Marc** (cuando esté con el Mac): lo visual, qué métricas se quedan en "El detalle", la ventana de atribución y si falta alguna columna. El panel ya está público para enseñárselo: https://creative-baklava-859ee2.netlify.app

## ✅ DECIDIDO (20/10, segunda llamada con Marc) · los dos números

Marc lo dijo sin rodeos: el panel le parece **demasiado transparente**. *"Hay semanas de Meta que el retorno es -1."* Y propuso **meter la facturación entera de Shopify en la casilla de las ventas de los anuncios**, porque así *"el retorno va a subir"* y *"se puede maquillar"*. Su argumento de fondo sí es verdad: Meta no ve todas las ventas que provoca (alguien ve el anuncio por la tarde y compra de noche por Google).

**Lo que se hizo con eso:** el argumento se queda, el maquillaje no.

**Arriba (Resumen): solo lo de los anuncios.** Las ventas, la inversión, el coste por venta y el retorno salen **siempre de lo que cuenta Meta**.

**Debajo, un bloque nuevo, "Tu tienda este mes":** el total que ha facturado su Shopify, comparado con el mes anterior. **Va solo: de ese número no se calcula nada.** Ni retorno ni coste por venta.

**Y debajo del total, siempre esta frase:**

> *Meta solo cuenta las ventas que puede seguir hasta el final. Mucha gente ve el anuncio, no compra en ese momento y vuelve más tarde por Google o buscando tu nombre. Esa venta está en el total de tu tienda, pero Meta no se la apunta.*

**Por qué el retorno sale de Meta y no del total** (los tres motivos, para no volver a discutirlo):

1. **El cliente tiene ese mismo número.** Es su Shopify. Si ve su facturación repetida en nuestra casilla, no piensa "qué retorno", piensa "me están enseñando lo mío".
2. **Se pierde la historia.** Con el total, el primer mes sale un retorno enorme (lleva dentro lo que ya vendía sin nosotros) y después **no se mueve**: de x10,9 a x11,4. Con el de Meta se empieza en x3,4 y se sube a x4,1, y **eso es lo que se enseña el día 25 para que renueve**.
3. **Sin el número real no se sabe qué anuncio apagar.** Es el número con el que se decide, no solo el que se enseña.

**No se dice "la mayoría de esas ventas vienen de los anuncios".** No por delicadeza: porque no se sabe, y es la clase de frase que un cliente te pide que demuestres. Dicho como está, la conclusión la saca él.

**Y una cosa en la que Marc tenía razón entera:** el retorno semanal asusta y no dice nada. **El panel habla siempre del acumulado del mes**, nunca de la semana suelta: dos semanas buenas y una mala hacen balance en el total (Sami, 20/10).

---

## ⏳ LO QUE FALTA · para la próxima vez que se toque (20/10)

El panel está montado y funcionando (dominio, contraseña y certificado). **Lo que queda son cuatro pantallas**, y Sami ha decidido cuáles importan:

- ✅ **Semana sin datos** (Marc no los pasó): tiene que poner *"última actualización: [fecha]"* en vez de parecer roto. **Sami, 20/10: hay que acordarse de meterlo la próxima vez que se toque el panel.**
- ✅ **Cliente que se va:** se queda **congelado** con su último mes, no se borra.
- ⏸️ **Cliente en pausa y cobro fallido:** *"ahora mismo da igual"* (Sami, 20/10). Se verá cuando pase.

---

## 1 · De dónde salen los datos (la decisión gorda)

**A · A mano.** Marc rellena una hoja cada domingo con los números de la semana y el panel la lee. Cero infraestructura, funciona la semana que viene, le cuesta 5 minutos.

**B · Conectado a Meta.** El panel lee la API de Meta y se actualiza solo. Hace falta una app de Meta, pasar su revisión, tokens que caducan y mantenerlos. Es un proyecto, no una tarde. Y ahora mismo la empresa no está registrada.

**C · Informes automáticos de Meta por correo** y procesarlos. Ni una cosa ni la otra, y se rompe en cuanto Meta cambia el formato.

**Recomendación: A ahora, B cuando haya 5 o más clientes.** Y montar el panel de forma que **la fuente sea intercambiable**: hoy los datos entran por una hoja, mañana los mete un script y el panel no se entera. Con 1-3 clientes, automatizar esto es perder una semana para ahorrar quince minutos.

## 2 · Dónde vive

Lo mismo que el alta, que ya está montado y funcionando: **Netlify + el dominio propio**.

- `panel.iads-agency.es/?c=nordik&k=[token]`
- Los datos los sirve el mismo proyecto de Apps Script (otra función que devuelve los números de ese cliente).

**Recomendación:** reusar la arquitectura del alta. Cero euros, ya sabemos que funciona y el diseño es el mismo.

## 3 · Quién puede verlo (privacidad)

Son datos de facturación de otra empresa: si el enlace es `?c=nordik`, cualquiera que pruebe nombres de marcas ve sus ventas.

**Recomendación: un token largo por cliente en el enlace** (`&k=8f3a9c…`), como los enlaces de Drive de "cualquiera con el enlace". Sin contraseñas ni registro: fricción cero para él y suficiente para esto. El token se genera al crear el cliente y vive en su ficha.

## 4 · El acceso de Marc

Necesita dos cosas distintas:

- **Meter los datos:** es editor de la hoja. Ahí ya tiene acceso.
- **Ver el panel de cualquier cliente:** un enlace interno, `panel.iads-agency.es/interno?k=[token de iAds]`, con la lista de todos los clientes y su estado.

**Recomendación:** ese enlace interno sirve también para Sami, y de paso es el germen del panel de iAds (el de "qué toca hoy"), que está aparcado en `IDEAS.md`.

## 5 · Qué enseña (y qué no)

**Arriba, lo que de verdad le importa:** ventas e ingresos del mes, inversión y **coste por venta**. Y su objetivo a 3 meses con dónde está.

**Después:** sus anuncios, con el que mejor va destacado, y qué se apagó.

**Después:** qué hemos hecho esta semana (tres líneas, las mismas del informe del lunes).

**Y abajo:** enlace a su carpeta de vídeos e imágenes.

**Lo que NO lleva:** impresiones, alcance, CTR, frecuencia. Son números de vanidad que no le dicen si gana dinero, y abren conversaciones que no llevan a ningún sitio. Si algún día los pide, van en un bloque aparte al final.

## 6 · Los casos que hay que tener resueltos

1. **Cliente recién entrado, sin campañas todavía** (días 0-13): el panel existe desde el primer día y dice *"tus campañas salen el [fecha]"*. Vacío no, nunca.
2. **Primera semana en marcha:** los números van a ser malos porque Meta está aprendiendo. El panel lo dice en esa semana, no después.
3. **Mes 2 en adelante:** comparación con el mes anterior.
4. **Los números de Meta no cuadran con su Shopify.** Pasa siempre (atribución). **Hay que decirlo en el propio panel**, en una línea, antes de que lo pregunte: evita la discusión incómoda del día 25.
5. **Semana sin datos** (Marc no los metió): "última actualización: [fecha]", para que no parezca roto.
6. **Cliente en pausa o con un cobro fallido:** el panel deja de actualizarse y lo dice.
7. **Cliente que se va:** se queda congelado con el resumen final, no se borra de golpe.
8. **Móvil:** la mayoría lo va a abrir en el móvil, así que se diseña para móvil primero.
9. **Moneda y fechas** en formato español.

## 7 · El diseño

El mismo lenguaje visual que el alta, que ya está aprobado: blanco puro, columna centrada con el texto a la izquierda, el violeta del logo, Bricolage Grotesque para los titulares.

**Pocos números y grandes**, cada uno con una línea de lectura debajo (*"34 € por venta: por debajo de tu objetivo"*). Ni tablas densas ni gráficos de colores: eso es lo que hace que un panel parezca de agencia y no se mire.

---

## Lo que hay que decidir con Sami

1. **¿A mano o conectado a Meta?** (recomendación: a mano, de momento).
2. **¿Token en el enlace o algo más cerrado?** (recomendación: token).
3. **¿Qué cuatro números van arriba?** (propuesta: ventas, ingresos, inversión, coste por venta).
4. ~~**¿Se enseña el ROAS?**~~ ✅ **Sí, y se calcula siempre con las ventas que cuenta Meta** (20/10, arriba del todo).
5. **¿Marc mete los datos el domingo con los del informe, o cada día?** (recomendación: el domingo, en el mismo momento en que pasa su lectura).
