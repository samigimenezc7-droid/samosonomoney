# La landing de iAds

Hecha el 23/10/2026. Es la pieza que bloqueaba el canal 3 de `0-CANALES.md`
(anuncios de Meta → landing → formulario que filtra → agenda).

**El archivo:** `index.html`. Todo va dentro: estilos, textos y el formulario.
No hay nada que instalar.

**Para verla y compartirla ya:**
https://claude.ai/artifact/FtdvsWe1teEe9xf3rq7uWQ
Es privada. Para que la abra alguien de fuera hay que compartirla desde el
menú Share de la propia página.

**Para usarla de verdad, con dominio propio:** se sube a Netlify igual que
la página del alta — se arrastra esta carpeta a Netlify y se apunta un
subdominio desde DonDominio. El paso a paso está en
`4-plantillas/clientes/escalon-2/5-ALTA-web/apps-script/LEEME.md`.

---

## La idea

De `0-CANALES.md`, 20/10: *"La demo: un anuncio hecho con su producto... y
ninguna agencia de la competencia hace eso en una landing."*

Eso es la landing. Donde todos ponen "agenda tu llamada estratégica
gratuita", esta pone **"hazme un anuncio con mi producto"**. La demo es la
razón para reservar, y es lo único que no se puede copiar sin saber producir.

**Nada inventado.** No hay ni una cifra de resultados, porque no hay casos
del modelo nuevo. La prueba es el trabajo y la promesa de los 15 días, que
es verificable y está en la cláusula 2 del contrato.

## Lo que tiene, por orden

1. **Hero** — el problema real (4 anuncios al mes) y la demo como entrada.
   Al lado, una ficha estilo gestor de anuncios con la asimetría: 4 tuyos
   frente a hasta 15 nuestros.
2. **Por qué cuatro no llegan** — volumen, lectura y repetición. Es la
   lógica, no una estadística.
3. **Las dos mitades** — la comparación con agencia de anuncios, agencia de
   contenido y productora. Sale de `1-QUIENES-SOMOS.md`.
4. **El muro** — una tanda de un mes en proporciones reales (9:16, 4:5, 1:1).
   **Hoy son huecos: hay que meter 12 creatividades de verdad.**
5. **Los 15 días** — las cuatro paradas de `3-CAMINO-15-DIAS/` con el sello
   del día 15.
6. **Precio** — 1.300 €/mes + IVA, sin permanencia, y qué incluye.
7. **Para quién no es** — los cinco filtros, dichos claro. Esto no lo pone
   nadie y es lo que más filtra.
8. **El formulario** — las cuatro preguntas de `0-CANALES.md` ("el setter,
   hecho por escrito").

## El formulario: qué hace con cada respuesta

Filtra en la propia página, sin guardar nada. La captura la hace Calendly.

| Respuesta | Qué le sale |
|---|---|
| No se anuncia, o menos de 1.000 €/mes | No encaja. Se le ofrece el plan de acción suelto (150-250 €, descontable) |
| Ya tiene agencia que va bien | Encaja por el escalón 1: solo vídeos. Reserva igual |
| Todo lo demás | Encaja. Reserva, y se le hace el anuncio antes de la llamada |

## Pendiente

- [ ] **El enlace de Calendly.** Está puesto
      `https://calendly.com/iads-agency/closing` a modo de apuesta. Hay que
      poner el real — es la variable `AGENDA`, al principio del script.
- [ ] **Las 12 creatividades del muro.** Van como `<img>` dentro de cada
      `.slot`, que ya está preparado para recibirlas.
- [ ] Subirla a Netlify con su subdominio cuando se vaya a usar con anuncios.
