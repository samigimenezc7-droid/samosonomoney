# Conecta tu contenido (YouTube e Instagram)

Tu plataforma tiene una pestaña Contenido que enseña tus piezas con sus
números, en el mismo sitio que tus leads. Todo el sistema ya está montado; lo
único que queda es enchufarlo a tus cuentas, y eso lo haces tú porque las
claves son tuyas.

Este fichero está escrito para dárselo a tu IA. Ábrelo con tu Claude y dile:

> Lee sops/conecta-tu-contenido.md y acompáñame a conectar mi Instagram.

---

## YouTube: dos minutos, sin claves

1. Copia la URL de tu canal (la de youtube.com/@tucanal vale).
2. En tu plataforma, pestaña Contenido, pégala en el cuadro de YouTube y pulsa
   Conectar.
3. Ya está. Tus vídeos con vistas, likes y comentarios aparecen ahí.

Si dice que no encuentra el canal, abre la URL en el navegador para comprobar
que es la buena y vuelve a pegarla.

---

## Instagram: un token tuyo, una sola vez

Instagram no da los números de una cuenta sin permiso de esa cuenta. El
permiso es un token que se saca desde Meta. Son unos veinte minutos la primera
vez y no se vuelve a hacer salvo que caduque.

Antes de empezar, dos condiciones que causan casi todos los fallos:

- Tu Instagram tiene que ser cuenta profesional (de empresa o de creador). Se
  cambia gratis en Instagram: Configuración, Herramientas para empresas.
- Si vas por la vía de Facebook, tu Instagram tiene que estar conectado a una
  página de Facebook tuya.

### Sacar el token, paso a paso

1. Entra en developers.facebook.com con tu cuenta y pulsa My Apps, Create App.
2. Tipo de app: elige la que ofrezca Instagram (según la pantalla que te
   salga: "Business" o directamente "Instagram"). Ponle de nombre tu negocio.
3. Dentro de la app, añade el producto Instagram y sigue su asistente de
   configuración: te pedirá conectar tu cuenta profesional de Instagram.
4. Busca la sección de generar token (según la versión de la pantalla se llama
   "Generate token" en Instagram, o se hace desde Tools, Graph API Explorer
   eligiendo tu app). Genera el token con tu cuenta de Instagram.
5. Copia el token entero. Empieza por IGAA (Instagram) o por EAA (Facebook).
   Los dos valen: la plataforma distingue solos.
6. En tu plataforma, pestaña Contenido, pégalo en el cuadro de Instagram y
   pulsa Conectar. Si Meta lo reconoce, verás tu usuario y tus publicaciones.

No pases el token por WhatsApp ni por Discord: se pega directo del navegador a
la plataforma. Quien lo tenga puede leer los datos de tu cuenta.

### Si no funciona, en orden

1. "Meta no reconoce ese token": casi siempre está cortado al copiarlo. Son
   larguísimos: vuelve a copiarlo entero, sin espacios ni saltos de línea.
2. "No encuentra tu cuenta de Instagram": tu Instagram no es cuenta
   profesional, o (vía Facebook) no está conectado a tu página. Arregla eso y
   genera el token otra vez.
3. Funcionaba y un día deja de funcionar: el token caducó, es normal en Meta
   (los de larga duración viven unos 60 días). La pestaña te lo dirá con el
   arreglo al lado: generas uno nuevo con los mismos pasos y lo pegas otra
   vez. Tus datos vuelven solos.
4. Si después de todo esto sigue sin ir, escríbenos por tu canal con una
   captura del error exacto. Meta cambia estas pantallas cada pocos meses y
   preferimos corregir esta guía a que pierdas la tarde.

---

## Qué mirar una vez conectado

No entres cada día a mirar números: entra el viernes, en tu cuarto de hora de
métricas. Las preguntas que valen: qué pieza trajo leads (eso está en el CRM,
en el origen de cada lead), y qué pieza se movió mucho sin traer ninguno, que
es la señal de contenido que gusta pero no vende.
