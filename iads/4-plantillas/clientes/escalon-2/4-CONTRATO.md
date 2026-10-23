# Contrato del escalón 2

🟩 **Se rellenan los huecos** (nombre, NIF, marca, fecha, precio) y se genera el PDF con `4-plantillas/scripts/contrato_escalon2_pdf.py`. **El texto no se toca cliente a cliente:** lo distinto va en un anexo aparte.

*(🟦 guion que se usa tal cual · 🟩 se copia y se rellenan huecos · 🟧 se escribe nuevo para cada cliente)*

> **Lo único que queda abierto: quién sale como Prestador.** Lo demás está cerrado y el PDF se puede generar en cuanto lleguen esos datos.
>
> ### El Prestador · lo que falta (20/10)
>
> **Lo que dijo la madre de Sami:** sale **la empresa**, con su **CIF**. No su nombre ni el de Sami. *(Hasta el 15/10 el plan era que saliera Sami; queda descartado.)*
>
> **Faltan dos datos, y los tiene la gestora:**
> 1. **La razón social exacta**, con su forma (*"Tal y Cual, S.L."*).
> 2. **El CIF** de esa empresa.
>
> **Y una pregunta para la gestora, no para nosotros: ¿hace falta nombrar a quien firma?** Una sociedad no firma sola. Lo normal es *"representada por [nombre], con NIF [ ], en calidad de administrador"*, y es lo que menos preguntas genera si algún día hay un problema; pero para un contrato de este tamaño también vale solo la empresa con su firma. **La cabecera y el PDF ya admiten las dos formas:** si no se pasa representante, esa línea no sale.
>
> **Lo que arrastra este dato:** la factura la emite el Prestador (cláusula 7), así que tiene que cuadrar con lo que facture la empresa, y con lo que ponga en los recibos de Stripe.
>
> ### La garantía · fuera (20/10)
>
> **Decisión de Sami: no hay garantía de ningún tipo.** *"Vamos viendo si hace falta cuando hablemos con clientes, pero ahora mismo sin ninguna."*
>
> **De dónde sale:** en la grupal de InfoCapitals le dijeron que **la garantía solo atrae leads malos**, gente que trabaja contigo esperando a ver si cobra. Marc opinó lo mismo: *"solo sirve para atraer gente de mierda que te va a tocar los cojones"*. Y Sami lo cerró: si filtras bien, el cliente ya sabe que esto lleva tiempo.
>
> **Lo que SÍ se queda:** el compromiso de **lanzar la campaña con al menos 5 anuncios en 15 días**. Eso no era la garantía, era la promesa de entrega, y es la columna vertebral del camino, del alta y de la llamada de arranque. **Ahora vive en la cláusula 2**, sin devolución de dinero detrás.
>
> **Qué pasó con la cláusula 3:** se borró y **el contrato se renumeró entero** (la 4 pasó a 3, la 5 a 4… hasta la 12, que es la 11). Las cláusulas eran 12 y ahora son **11**.
>
> **Lo que aporta Marc, por si algún día se vuelve a abrir:** promesa y garantía no son lo mismo. *"Promesa es: te mejoro tu mejor anuncio. Garantía es: si no lo hago, te devuelvo el dinero."* Él iría por promesa, y si hay garantía, **con letra pequeña siempre**. Lo de "mes 2 rentable o no pagas el mes 3" está sin contestar: faltan las cuatro preguntas a Marc (`3-equipo/5-media-buyer/marc/llamada-2026-10-20.md`).


Empezado el 14/10/2026 con Sami. **No es la versión buena todavía:** se va escribiendo por tandas y, cuando esté entero y con el OK de Sami, sustituye a `../2-CONTRATO-CLIENTE.md` (el viejo va a `archivo/modelo-contenido/`) y se cambia también `../../scripts/contrato_pdf.py`.

> ⚠️ **Las notas de abajo son del 14-15/10 y están reescritas con la numeración nueva** (la de 11 cláusulas). Si algo no cuadra con un contrato ya firmado, la equivalencia es: 4→3, 5→4, 6→5, 7→6, 8→7, 9→8, 10→9, 11→10, 12→11.

**Cómo se está haciendo:**
- **El contenido** sale del contrato que ya teníamos y de las condiciones de `1-negocio/3-QUE-VENDEMOS.md` ("Condiciones (van al contrato)" y "Lo que no incluye").
- **La forma ("la piel")** se copia de la plantilla de un colega de Sami (`~/Downloads/Alejo Torrente Garay Acuerdo de Growth Partner_EGP.docx`): cabecera con los datos de las dos partes, "Se celebra entre", "Exponen", cláusulas numeradas con título y bloque de firmas al final. De su contenido no se usa nada: es una plantilla genérica traducida, con contradicciones y sin lo que nos protege.
- **Decidido (14/10):** en la cabecera, **sin domicilio**; el NIF sí se queda.
- **Decidido (15/10):** **sale Sami como Prestador** (nombre y NIF suyos). ⏳ **Se habla el 19/10** con su madre y la gestora: él tiene 16 años y es ella quien factura.
- **Estado:** OK de Sami a la cabecera y a **las 11 cláusulas**. *(El 15/10 eran 12 y la 3 era la garantía; el 20/10 se borró y el contrato se renumeró.)*
- **Decidido (15/10), cláusula 5:** la etiqueta de IA **la pone iAds** al publicar y se recomienda mantenerla, pero **decide el Cliente**; si pide quitarla, la responsabilidad es suya. No se nombran las herramientas (Seedance, Higgsfield, GPT Image) para no tener que cambiar el contrato si cambian. La responsabilidad de lo que el anuncio diga del producto no se repite aquí: está solo en la 4.5.
- **Decidido (15/10), cláusula 6:** se queda corta a propósito. Sami quitó tres cosas que yo había propuesto: que el contenido no pase al Cliente si un cobro falla (si no paga, no se trabaja, y eso ya está en la 7), que los métodos y plantillas de iAds no se transmiten, y los 6 meses de acceso a la carpeta de Drive después de terminar. Se queda: su material es suyo y tiene derecho a dárnoslo, el contenido es del Cliente para siempre, y iAds puede enseñarlo como ejemplo salvo que diga que no.
- **Decidido (15/10), cláusula 7:** el 10 % se cobra **por detrás** (se mira el mes que termina y se suma al cobro siguiente), porque por delante sería cobrar una inversión que aún no ha hecho. El **primer pago va antes de los accesos**, para que el plazo de lanzamiento no empiece antes de cobrar. El ejemplo del 10 % se escribe con la cuenta a la vista: es sobre **la parte que pasa de 3.000 €**, no sobre toda la inversión (así se leía mal). **Son 5 días**, no 7, para dar por cancelado un cobro fallido (lo dijo Sami el 15/10). ⚠️ **Pendiente de cuadrar:** `archivo/modelo-contenido/4-plantillas/clientes/11-MENSAJES.md` todavía dice 7 días; hay que pasarlo a 5 cuando se rehagan los mensajes del bloque C.
- **Decidido (15/10), cláusula 8:** la cancelación y la pausa **por escrito** (SOP de oferta: lo cerrado de palabra se reabre). iAds también puede salir, para no quedarse atado a un cliente malo. **Sami quitó** la letra que decía que no se devuelve la parte del mes sin usar, porque da por hecho que el mes se trabaja hasta el final aunque el cliente avise el día 23. ⚠️ Queda apuntado: si algún día un cliente pide la parte proporcional de un mes ya cobrado, el contrato no dice que no. **Desde el 20/10 el contrato no obliga a devolver dinero en ningún caso**, así que esto es lo único por donde podría pedirse.
- **Decidido (15/10), cláusula 9:** **se queda el tope de responsabilidad** (letra e): como máximo una cuota mensual y sin daños indirectos. Sami lo quería fuera; se quedó tras explicarle que es un techo, no una obligación de devolver nada, y que protege también a su madre, que es quien factura. **Fuera** la letra que repetía la consecuencia del mínimo de inversión: la b) ya dice que lo que invierte el Cliente es una de las cosas que iAds no controla. Con esto, el pendiente que venía de la cláusula de la inversión queda cerrado.
- **Decidido (15/10), cláusulas 10 y 11:** confidencialidad **un año** después de terminar (Sami; yo había puesto dos). **Fuera** la letra que decía que iAds puede dar acceso a la información a quien trabaja en la cuenta (Marc, producción): Sami dice que ya se sabe que iAds tiene equipo. **Fuera** la excepción que remitía al permiso de portfolio de la 6.3, por no repetirlo. Aceptación por **tres vías**: firma, "de acuerdo" por escrito o el primer pago, porque con clientes pequeños lo que pasa de verdad es que contestan y pagan.
- **Decidido (15/10), cláusula 3:** el mínimo de inversión se mide por **su mes de servicio** (los 30 días desde su pago), no por mes natural, para que vaya igual que el cobro. Sami quitó el punto que decía qué pasa si baja del mínimo (aviso por escrito y salida a los dos meses): no hace falta porque, sin permanencia (cláusula 8), basta con no renovar. **Pendiente para la cláusula 9:** la consecuencia de invertir menos del mínimo (si invierte menos de 1.000 €, no se puede juzgar si los anuncios funcionan y eso no es responsabilidad de iAds), porque ahora la letra b) es una obligación sin consecuencia escrita.
- **Decidido (15/10), cláusula 4:** **5 días** seguidos sin responder para la pausa (el contrato viejo decía 7; manda la condición nueva de `1-negocio/3-QUE-VENDEMOS.md`). La lista de accesos **no se cierra en el contrato a propósito** (confirmado el 18/10): se nombran los importantes y se añade "los demás que iAds le indique en la guía de accesos". **Para el contrato no queda nada pendiente**; la lista exacta es cosa de la guía del onboarding. **El PDF ya está hecho:** `4-plantillas/scripts/contrato_escalon2_pdf.py` (15/10). Sale en **6 páginas** y la forma se copió del contrato del colega de Sami: márgenes de una pulgada, cuerpo a 11 pt con aire entre bloques, cabecera con el título en todas las páginas y número de página en el pie, datos de cada parte en líneas sueltas, "EXPONEN" y la frase en mayúsculas antes de las cláusulas, y las firmas sobre línea con su fecha. **Si cambia el texto del contrato, se cambia también en el script.**
- **Cerrado (18/10):** **se firma a mano** sobre el PDF, por WhatsApp. La firma digital se descarta por ahora.

## Cómo se manda y cómo se firma (decidido el 16/10)

**No va dentro del onboarding** (se probó y Sami lo quitó: dentro del formulario de alta queda fatal). Va **aparte, por WhatsApp**, y se firma **a mano sobre el PDF**:

1. Se genera su PDF con `../../scripts/contrato_escalon2_pdf.py`, con sus datos.
2. **Lo firma primero iAds.** Sin imprimir: en el Mac, con Previsualización (la firma se dibuja una vez con el trackpad y queda guardada); en el iPhone, firmando encima del PDF.
3. Se le manda por el grupo de WhatsApp con el mensaje de abajo.
4. Él firma encima donde pone "El Cliente" y lo devuelve por el mismo sitio.
5. Se guarda el PDF devuelto **y una captura del chat** en `2-clientes/[marca]/1-contrato/`. La captura es lo que ata el documento a la persona.

**Por qué así y no con firma electrónica:** un contrato de servicios no necesita forma especial; vale con poder probar que las dos partes dijeron que sí, y entre el chat, el pago y el trabajo hecho hay prueba de sobra. Además, **hasta que la empresa no esté registrada no se puede dar de alta en un servicio de firma** en condiciones. Cuando lo esté, pasar a firma electrónica avanzada (tipo Firmafy, española y eIDAS, mirando el precio ese día) es media hora: el contrato no cambia.

**Quien firma por iAds es quien factura**, así que depende de lo que diga la gestora.

**El mensaje con el que se manda:**

> Te paso el contrato ya firmado por nuestra parte. Es corto: cómo funciona el servicio, los plazos, el precio y cómo cancelar. Léelo con calma, fírmalo donde pone "El Cliente" y me lo devuelves por aquí. Si algo no te cuadra, me lo dices y lo hablamos antes de firmar nada.

---

**CONTRATO DE SERVICIO · iAds**
**Escalón 2 · Vídeos + anuncios**

**EL PRESENTE CONTRATO SE CELEBRA ENTRE:**

**El Prestador:** [razón social de la empresa], con CIF [ ], que presta el servicio con el nombre comercial **iAds** (en adelante, "iAds").
*(Si la gestora lo pide: representada por [nombre y apellidos], con NIF [ ], en calidad de administrador.)*
Correo electrónico: sami@iads-agency.es · Teléfono: [ ]

**Y el Cliente:** [razón social o nombre], con NIF/CIF [ ], titular de la marca **[marca]** (en adelante, "el Cliente").
Persona de contacto: [nombre] · Correo electrónico: [ ] · Teléfono: [ ]

Fecha: [fecha]

**EXPONEN**

I. Que iAds crea anuncios en vídeo e imagen con inteligencia artificial y gestiona campañas de publicidad en Meta para tiendas online.

II. Que el Cliente tiene una tienda online y quiere contratar ese servicio para su marca.

III. Que ambas partes acuerdan dejar este contrato por escrito, con las siguientes:

**CLÁUSULAS**

**1. Objeto del servicio.** iAds prestará al Cliente, cada mes:
**1.1. Creación de anuncios:** hasta 15 vídeos y hasta 35 imágenes al mes (incluidas las de su web), hechos con inteligencia artificial, en los formatos de Meta y listos para publicar.

**1.2. Gestión de sus campañas en Meta** (Facebook e Instagram): montar las campañas, probar los anuncios, apagar los que no venden, invertir más en los que sí y hacer retargeting.

**1.3. Revisión de su web y su página de producto al empezar**, con una lista de mejoras.

**1.4. Seguimiento:** un panel con sus resultados, un informe cada lunes y una llamada al mes.

**No incluye:** el dinero de la publicidad (cláusula 3) · aplicar las mejoras de la web, salvo que se contrate aparte por 150 € · rodajes con personas reales · hacer una web nueva · sus redes sociales, el email o la atención a sus clientes · anuncios fuera de Meta · nada de su producto (stock, envíos o precios).

**2. Cómo funciona el servicio.**
- **Al empezar:** el Cliente recibe el documento de bienvenida (el formulario de su marca, la guía para darnos los accesos y la reserva de la llamada de arranque). Después vienen la llamada de arranque, su plan de acción, la primera tanda de anuncios y el lanzamiento de las campañas.
- **Plazo de lanzamiento:** la primera campaña de Meta estará funcionando, **con al menos 5 anuncios**, en un plazo de **15 días naturales** desde que el Cliente ha pagado y ha dado todos los accesos de la cláusula 4. El día en que los accesos están completos, iAds se lo comunica al Cliente por escrito con la fecha de lanzamiento. Ese plazo **no corre** mientras falte algún acceso, ni cuando el retraso se debe al Cliente (no responde o no reserva la llamada de arranque), ni por causas ajenas a iAds (bloqueo o restricción de su cuenta de Meta, o anuncios rechazados por su producto, su web o su historial).
- **Cada mes:** anuncios nuevos cuando hagan falta, y como mínimo una tanda al mes. Un informe cada semana y una llamada al mes con los resultados y el plan del mes siguiente.
- **El día a día lo lleva iAds.** Los anuncios no necesitan la aprobación del Cliente uno a uno. Antes de lanzar cada tanda, el Cliente la recibe y tiene 24 horas para decir si algo no encaja con su marca. Si no responde, se sigue adelante.
- **iAds consulta antes al Cliente** si hay que subir o bajar el presupuesto del mes, cambiar de estrategia (otro producto, otra oferta o un descuento) o decir algo de su producto que él no haya aprobado.

**3. La inversión en publicidad.**
**3.1.** El dinero de la publicidad **no está incluido en el precio.** El Cliente lo paga directamente a Meta, desde su propia cuenta de anuncios y con su propio método de pago. iAds no adelanta ni administra ese dinero en ningún momento.

**3.2.** Mientras el contrato esté vigente, el Cliente mantendrá una inversión de **al menos 1.000 € al mes** en Meta. Por debajo de esa cifra no hay datos suficientes para probar anuncios y el servicio no puede hacer su trabajo.

**3.3.** El presupuesto del día a día lo configura iAds dentro de ese marco. Para subirlo o bajarlo de forma importante, iAds lo consulta antes con el Cliente (cláusula 2). Si el Cliente quiere otro presupuesto, lo pide por escrito y iAds lo aplica.

**3.4.** Si los anuncios se paran porque Meta no puede cobrar al Cliente (tarjeta caducada, límite de gasto, impago) o porque el Cliente retira o agota su presupuesto, no es responsabilidad de iAds. El tiempo que las campañas estén paradas no cuenta para ningún plazo.

**3.5.** Cuando la inversión pasa de 3.000 € al mes, la cuota de iAds sube según la cláusula 7.

**4. Obligaciones del Cliente.** El Cliente se compromete a:
**4.1. Dar los accesos desde el primer día.** Acceso de administrador a su cuenta publicitaria y a su portfolio empresarial de Meta (Business Manager), a su píxel, a su catálogo si lo tiene, a sus perfiles de Facebook e Instagram y a su web o tienda online, además de los demás accesos que iAds le indique en la guía de accesos del onboarding. Su cuenta de Meta tiene que estar activa, sin restricciones y con un método de pago que funcione. **Mientras falte algún acceso, el plazo de lanzamiento de la cláusula 2 no empieza a contar.**

**4.2. Entregar el formulario de su marca y su material** (logo, fotos y vídeos del producto y lo que tenga grabado) antes de la llamada de arranque.

**4.3. Reservar y asistir a la llamada de arranque y a la llamada de cada mes.** Si el Cliente cambia una llamada o no se presenta, **los plazos de iAds se mueven en la misma medida.**

**4.4. Responder en 24-48 horas** cuando iAds le pide una decisión o un dato, por el grupo de WhatsApp o por correo. **Si pasan 5 días seguidos sin respuesta, el servicio queda en pausa** hasta que conteste, y el cobro mensual no se detiene.

**4.5. Dar información veraz de su producto.** Lo que se diga en los anuncios sobre el producto tiene que ser cierto y demostrable. Si el Cliente pide afirmar algo que no puede demostrar, la responsabilidad es suya (cláusula 9).

**4.6.** Los accesos se mantienen mientras dure el contrato. Si el Cliente los retira, iAds no puede prestar el servicio y se aplica la pausa de la letra d).

**5. Contenido hecho con inteligencia artificial.** El Cliente sabe y acepta que los vídeos y las imágenes se producen con herramientas de inteligencia artificial, y que las personas que aparecen en ellos pueden ser **avatares generados, no personas reales.**
**5.1.** Los avatares no representan a clientes reales de la marca ni a personas concretas. iAds no usa la imagen, la voz ni el nombre de una persona real sin su permiso por escrito. Si el Cliente quiere que aparezca él o alguien de su equipo, lo graba él y lo entrega como material (cláusula 4b).

**5.2.** Al publicar los anuncios, **iAds pone la etiqueta de contenido generado con inteligencia artificial** que pide Meta, y recomienda al Cliente mantenerla. La decisión final de ponerla o no es del Cliente: si pide que no se ponga, se hace como diga y la responsabilidad es suya.

**5.3.** Las herramientas de inteligencia artificial pueden fallar, cambiar sus condiciones o dejar de estar disponibles. Si eso retrasa una tanda de anuncios, iAds avisa al Cliente y entrega en cuanto puede; no es un incumplimiento del contrato.

**6. El material del Cliente y de quién es el contenido.**
**6.1.** El Cliente garantiza que el material que entrega (logo, fotos, vídeos, textos y referencias) **es suyo o tiene derecho a usarlo**, y **autoriza a iAds a utilizarlo** para crear sus anuncios. Si ese material incluye a personas, el Cliente garantiza que tiene su permiso.

**6.2. Los vídeos y las imágenes que iAds crea son del Cliente, para siempre.** Puede usarlos donde quiera: anuncios, redes, web o email, también si deja de trabajar con iAds.

**6.3.** iAds **podrá mostrar los anuncios y los resultados del Cliente como ejemplo de su trabajo**, con el nombre de la marca, **salvo que el Cliente diga que no** por escrito en cualquier momento.

**7. Precio y pagos.**
**7.1. Precio: 1.300 € al mes, más IVA.** Cubre todo lo de la cláusula 1. No incluye el dinero de la publicidad, que el Cliente paga aparte a Meta (cláusula 3).

**7.2. La cuota sube con la inversión.** Si el Cliente invierte más de 3.000 € al mes en Meta, paga 1.300 € más el **10 % de la parte que pasa de 3.000 €** (no de toda la inversión). Ejemplos: si invierte **5.000 €**, pasa 2.000 € del límite, el 10 % de esos 2.000 € son 200 €, y paga **1.500 €**. Si invierte **10.000 €**, pasa 7.000 €, el 10 % son 700 €, y paga **2.000 €**. Se mira lo invertido en el mes de servicio que termina, en su propia cuenta de Meta, y la diferencia se suma al cobro siguiente.

**7.3. El primer pago se hace antes de empezar.** iAds no pide accesos ni empieza a trabajar hasta que está hecho.

**7.4. Forma de pago y renovación.** El pago **se renueva solo cada 30 días** desde la fecha del primer pago, con tarjeta, a través de Stripe. El Cliente autoriza ese cobro al aceptar este contrato.

**7.5. Cambios de precio:** iAds puede cambiar su precio avisando con **30 días**. No afecta a un mes ya cobrado. Si el Cliente no está de acuerdo, puede cancelar antes de que el precio nuevo entre en vigor (cláusula 8).

**7.6. Si un cobro falla:** iAds avisa al Cliente ese mismo día con el enlace para actualizar el pago. **Mientras no esté pagado, iAds no crea contenido nuevo;** las campañas que ya están en marcha siguen funcionando. A los 3 días se vuelve a avisar y, si a los **5 días** no ha pagado ni ha contestado, el contrato se da por cancelado (cláusula 8).

**7.7.** La factura la emite el Prestador con los datos de la cabecera, al cobrar cada mes.

**8. Duración, pausas y cancelación.**
**8.1. Sin permanencia.** El contrato se renueva solo cada 30 días con el cobro de la cláusula 7, y dura mientras las dos partes quieran.

**8.2. Para cancelar, el Cliente avisa por escrito al menos 5 días antes de la renovación**, por el grupo de WhatsApp o por correo. Si avisa más tarde, el cobro de ese mes se mantiene y el servicio se presta hasta el final del mes.

**8.3. Pausa:** el Cliente puede **pausar el servicio un mes sin perder su precio**, avisando con los mismos 5 días de antelación, y como mucho una vez cada 4 meses. Durante la pausa no se cobra, iAds no crea contenido nuevo y las campañas se dejan como el Cliente pida (paradas o funcionando a su cargo).

**8.4. iAds también puede terminar el contrato** avisando con 5 días antes de la renovación. Y puede terminarlo en cualquier momento si el Cliente no paga (cláusula 7f), retira los accesos (cláusula 4) o pide algo ilegal o contrario a las normas de Meta.

**8.5. Al terminar:** iAds **deja las campañas funcionando**, entrega un resumen de qué hay montado y qué está funcionando, y sale de las cuentas del Cliente en 7 días. El Cliente se queda con su cuenta, sus campañas y todo el contenido (cláusula 6).

**9. Resultados y responsabilidad.**
**9.1.** iAds se compromete a hacer su trabajo con profesionalidad y en los plazos de este contrato. **No garantiza un número de ventas, ni un retorno concreto de la inversión, ni un coste por venta.** Este contrato no lleva ninguna garantía de resultados.

**9.2.** Los resultados dependen también de cosas que iAds no controla: el producto del Cliente, su precio, su web y su página de producto, su stock y sus envíos, cómo atiende a sus clientes, la competencia de su sector y cuánto invierte en publicidad.

**9.3. Meta decide sobre su propia plataforma.** Si Meta restringe o bloquea la cuenta del Cliente, o rechaza anuncios por su producto, su web o su historial, no es responsabilidad de iAds, que trabaja siguiendo las normas de Meta.

**9.4.** El dinero invertido en publicidad es una inversión con riesgo. iAds toma las decisiones de campaña con criterio profesional, pero **no responde del dinero gastado en anuncios que no vendan.**

**9.5.** La responsabilidad de iAds por este contrato se limita como máximo **al importe de la última cuota mensual pagada** por el Cliente, y no alcanza a daños indirectos como pérdida de ventas o de beneficios.

**10. Confidencialidad y datos personales.**
**10.1.** iAds tratará como confidencial toda la información del Cliente que no sea pública: sus ventas, sus precios y márgenes, su estrategia, sus proveedores y los datos de sus campañas. No la compartirá con nadie ajeno al servicio.

**10.2.** El Cliente mantendrá también como confidencial la forma de trabajar de iAds, sus precios y los documentos internos que reciba.

**10.3.** Esta obligación sigue en vigor **un año después** de que termine el contrato.

**10.4. Datos personales.** Para prestar el servicio, iAds accede a la cuenta de anuncios, al píxel y a la web del Cliente, donde hay datos de sus clientes. iAds solo los usa para este servicio, no los descarga ni los cede a terceros. El Cliente es el responsable de esos datos y iAds actúa por cuenta de él. Las dos partes cumplirán la normativa de protección de datos (RGPD).

**11. Ley aplicable, aceptación y firmas.**
**11.1.** Este contrato se rige por la **ley española**. Para cualquier conflicto, las partes se someten a los juzgados y tribunales competentes.

**11.2.** Este contrato sustituye cualquier acuerdo anterior de palabra entre las partes. Cualquier cambio tiene que ser **por escrito** y aceptado por las dos.

**11.3. Aceptación.** El Cliente acepta este contrato **firmándolo**, o respondiendo **"de acuerdo"** por escrito al mensaje con el que se le envía, o **haciendo el primer pago**. Cualquiera de las tres vale.

**11.4. Firmas.**

| | El Prestador (iAds) | El Cliente |
|---|---|---|
| Nombre | [ ] | [ ] |
| NIF/CIF | [ ] | [ ] |
| Fecha | [ ] | [ ] |
| Firma | | |

---

**Las 11 cláusulas (OK de Sami):** 1 · Objeto del servicio ✅ · 2 · Cómo funciona el servicio, con quién decide qué y el plazo de lanzamiento ✅ · 3 · La inversión en publicidad ✅ · 4 · Obligaciones del Cliente, con los accesos y su cuenta de Meta ✅ · 5 · Contenido hecho con IA ✅ · 6 · El contenido: el material del Cliente y de quién es lo que hacemos ✅ · 7 · Precio y pagos (precio, cuota que sube con la inversión, cambios de precio, cobro automático y qué pasa si falla) ✅ · 8 · Duración, pausas y cancelación ✅ · 9 · Resultados y responsabilidad ✅ · 10 · Confidencialidad y datos personales ✅ · 11 · Ley aplicable, aceptación y firmas ✅.

*(El 15/10 eran 12: la 3 era la garantía de rapidez. Se borró el 20/10 y el compromiso de los 15 días se mudó a la 2.)*
