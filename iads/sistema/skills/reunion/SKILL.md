---
name: iads-reunion
description: "Prepara una reunión de venta (closing) de iAds con un PROSPECTO que todavía no paga, en formato corto: una sola pantalla con lo que Sami tiene que traer a la llamada (¿encaja?, quién es la marca, pack recomendado con precio, 2-3 ángulos y el vídeo demo de 5-10 segundos) más los mensajes para calentar la reunión por WhatsApp. NO hace guiones, ni listas de 20 preguntas, ni dossiers largos: la llamada la lleva Sami con naturalidad siguiendo 4-plantillas/clientes/escalon-2/1-LLAMADA-VENTA.md. Úsala siempre que haya una reunión o prospecto por delante: 'tengo reunión con X', 'prepárame la llamada de X', 'he agendado con X', 'mírame esta marca', 'qué le propongo a X', o cuando Sami pegue la web o el Instagram de una marca con la que va a hablar. También para apuntar cómo fue la llamada después ('ha cerrado X', 'X me ha dicho que se lo piensa'). Si la marca YA paga, es /iads-client-pack."
---

# iAds — Preparar una reunión de venta

> **Antes de cada llamada, la pantalla del camino con su nombre** (Sami, 18/10): se abre `4-plantillas/clientes/escalon-2/3-CAMINO-15-DIAS/camino.html?c=[Marca]` y se comparte pantalla en el bloque de la propuesta. No hay que editar el archivo: el nombre va en la dirección.


Sustituye a la antigua `iads-prep-reunion` (24/09/2026). Aquella devolvía un dossier
enorme con guion y decenas de preguntas; a Sami le funcionan mejor las reuniones
naturales. Esta skill le da **munición, no un guion**: lo que tiene que traer a la
llamada, en una sola pantalla que lee en 2 minutos.

## Antes de nada: leer la fuente de verdad

Leer siempre, porque precios y criterios cambian:
- `1-negocio/2-A-QUIEN-VENDEMOS.md` — el filtro de las 4 condiciones, perfil 1 y perfil 2.
- `1-negocio/3-QUE-VENDEMOS.md` — los packs y los precios vigentes.
- `4-plantillas/clientes/escalon-2/1-LLAMADA-VENTA.md` — cómo va la llamada (fases 0 a 5). La preparación sirve a la fase 0.

(Rutas relativas a la carpeta `iads/` de Sami: `/Users/samigimenez/iads`.)

## Paso 1 — Investigar la marca sola

Sami da el nombre y la web o el Instagram. No preguntarle nada que esté en internet.

- **Web:** qué vende, producto estrella, precios, si es tienda online de producto físico.
- **Biblioteca de Anuncios de Meta:** ¿tiene anuncios activos? ¿Cuántos, desde cuándo, de qué tipo (creadoras, estáticos, IA mala…)? Es la mejor señal de perfil 1.
- **Instagram:** tamaño, tono, qué contenido hacen.

Solo si falta algo que no se puede ver desde fuera, preguntárselo a Sami, **una sola pregunta**.

## Paso 2 — La preparación (una sola pantalla)

Devolver exactamente esto, nada más:

```
[Marca] — reunión del [día y hora]

¿ENCAJA? ✅ / ⚠️ / ❌
1. Tienda online de producto físico: ✅/❌
2. Anuncios activos ahora mismo: ✅/❌ (lo que se ha visto)
3. Alguien en marketing o que lleve las campañas: ✅/❌/? 
4. ≥350 €/mes en anuncios: ? → se confirma en la llamada (fase 2)
[Si falla la 2 o la 3: una línea — "perfil 2: da caja, no recurrencia; la gestión de campañas es el extra (por definir)".]

QUIÉN ES
[3-4 líneas: qué vende, producto estrella, cómo se anuncia hoy.]

PACK RECOMENDADO
[Base / Crecimiento / Escala] — [precio] — [por qué, en una línea]

2-3 ÁNGULOS
1. [qué pasa en el vídeo, en palabras de cliente, sin jerga]
2. …
3. …

VÍDEO DEMO (5-10 s)
[La idea, en una frase: producto, qué pasa, con qué ángulo.] ¿Lo genero?

OJO
[1-2 cosas como mucho: socio que no está, detalle fino del producto, perfil 2…]
```

**Cómo elegir el pack:**
- **Base** por defecto. Es la puerta de entrada y la única con primer mes con descuento.
- **Crecimiento** si ya invierte fuerte, se ven muchos anuncios activos o tiene mucho catálogo.
- **Escala** si es marca grande con equipo de marketing que testea mucho.
- Perfil 2 → Base, y avisar en OJO de que sin nadie lanzando anuncios es un cliente de un mes.

**Los ángulos** van en lenguaje del cliente ("un chico mirándose al espejo hablando de la tripa que no baja"), nunca en jerga (ángulo/formato/hook/avatar). En la llamada se presentan como hechos sin conocer la marca y sin compromiso.

**El demo** se propone y **no se genera sin el OK de Sami**. Cuando diga que sí, se produce con `/ugc-ad-script-generator` (vídeo con avatar) o con la herramienta que toque. Su coste en créditos cuenta como coste de conseguir el cliente (CAC).

## Paso 3 — Los mensajes para calentar la reunión

Justo debajo, listos para copiar en el grupo de WhatsApp de la fase 0:

- **Al crear el grupo:** presentarse y pedir que venga quien decide ("estaría genial que viniera también la persona de marketing / tu socio").
- **El día antes:** recordar la reunión y la hora.
- **El mismo día:** "¡nos vemos hoy a las X!".

Cortos y naturales, con el tono de Sami. Nada de mensajes largos.

## Lo que NO hace esta skill

- No escribe guion de la llamada ni frases para leer. La estructura está en `4-plantillas/clientes/escalon-2/1-LLAMADA-VENTA.md` y Sami la cuenta con sus palabras.
- No saca listas de preguntas: las 4 preguntas de la fase 2 ya están fijadas en la guía.
- No prepara respuestas a objeciones por adelantado, salvo que la investigación muestre una muy probable (va en OJO).

## Después de la llamada

Cuando Sami cuente cómo fue ("ha cerrado", "se lo piensa", "me ha dicho que es caro"), apuntarlo en `3-equipo/3-ventas/LLAMADAS-VENTA.md` (crearlo si no existe), una fila por llamada:

| Fecha | Marca | Qué vende | Factura al mes | Invierte en Meta | De dónde salió | Resultado | Objeción real | ¿Trabajaríamos a gusto? |
|---|---|---|---|---|

Esto es lo que convierte la lista de objeciones de la guía (v1, supuestas) en objeciones reales. Cada 5 llamadas, proponerle a Sami actualizar la fase 5 de `4-plantillas/clientes/escalon-2/1-LLAMADA-VENTA.md` con lo aprendido.

- **Si no cerró:** recordar el siguiente paso y la fecha que quedaron (fase 5, C).
- **Si cerró:** pasa a cliente → `/iads-client-pack` (onboarding, contrato y llamada de briefing).
