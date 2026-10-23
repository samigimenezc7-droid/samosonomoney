# Números

Versión 4 · 14/10/2026, cerrada con Sami después del bloque de equipo. **Todo antes de impuestos** (lo que va a Hacienda por la actividad de la madre de Sami está pendiente de hablarlo con ella). Todos los precios son **+ IVA**: el IVA (21 %) se cobra y se paga a Hacienda, no es de Sami. La versión del modelo de contenido está en `archivo/modelo-contenido/1-negocio/6-NUMEROS.md`.

**En hoja de cálculo (con fórmulas: lo amarillo se cambia, lo verde se calcula):** Google Sheets "iAds · Números" → https://docs.google.com/spreadsheets/d/1_YtYYb045YAFnLVsYN_TnUTkDpAGCbeZeLXD8zaNaj0/edit (14/10: con un desplegable para elegir cómo llega el cliente —tú, Álvaro o anuncios de Meta— y cada escalón produciendo Sami y con productor) · copia en Excel: `1-negocio/iAds-Numeros.xlsx`. **Si cambia un número aquí, se cambia también en la hoja.**

**Decisiones del 14/10:** sin precio de arranque (todos pagan el precio entero desde el primer cliente; antes, el primero iba a 1.000 € tres meses) · el productor cobra lo mismo desde el primer mes (antes, menos el primero: venía del modelo viejo) · **la producción siempre se cuenta como coste**, la haga Sami o un productor (SOP de métricas: las horas del dueño se valoran aunque no se las pague; si no, "todo tiene un margen estupendo") · Álvaro cobra lo mismo en el escalón 3 que en el 2 (150 € + 5 %), aunque en euros sean 400 €: así busca clientes grandes.

---

## Lo que deja cada cliente (en papel)

### Escalón 2 · Vídeos + anuncios (el principal)
```
  1.300 €   paga el cliente
−   110 €   créditos de Higgsfield
−   150 €   producción (tu trabajo, o el productor)
−   400 €   anuncios (Marc)
−    24 €   Stripe
─────────
    616 €   te queda cada mes

−   300 €   conseguir el cliente (CAC), solo una vez
─────────
    316 €   te queda el primer mes
```

### Escalón 1 · Vídeos
```
    500 €   paga el cliente
−    90 €   créditos de Higgsfield
−   125 €   producción (tu trabajo, o el productor)
−     0 €   anuncios (los lleva su equipo)
−     9 €   Stripe
─────────
    276 €   te queda cada mes

−   300 €   conseguir el cliente (CAC), solo una vez
─────────
  −  24 €   el primer mes (se recupera el segundo)
```

### Escalón 3 · Todo (borrador)
```
  2.500 €   paga el cliente
−   220 €   créditos de Higgsfield
−   300 €   producción (el productor)
−   800 €   anuncios (Marc)
−    46 €   Stripe
─────────
  1.134 €   te queda cada mes

−   300 €   conseguir el cliente (CAC), solo una vez
─────────
    834 €   te queda el primer mes
```

**Si produces tú,** los 150 € (o 125 €) de producción te los quedas tú: son el pago por tu trabajo, no beneficio.

**El CAC según cómo llega el cliente** (en las cuentas de arriba, el de Meta, que es el más alto):
- **Anuncios de Meta:** unos 300 €. **Es una suposición:** el real es lo que cuesta cada persona que deja sus datos × cuántas hacen falta para una venta (con 15 € por persona y 1 venta de cada 30, serían 450 €). Se sabrá con los primeros anuncios.
- **Álvaro:** escalón 1, 75 € al cerrar + 25 € + 25 € · escalón 2, 150 € + 65 € + 65 € · escalón 3, 150 € + 125 € + 125 € (lo de los meses 2 y 3, solo si el cliente sigue).
- **Prospección de Sami:** 0 €, solo su tiempo.

**Stripe:** 1,5 % + 0,25 € sobre lo cobrado con IVA (1.300 € + IVA = 1.573 € → 24 €; 500 € → 605 € → 9 €; 2.500 € → 3.025 € → 46 €).

---

## Lo que queda al mes con varios clientes

Escalón 2, ya en marcha, menos los gastos fijos (328 €):

| Clientes | Cuenta | Queda al mes |
|---|---|---|
| 1 | 616 − 328 | 288 € |
| 2 | 1.232 − 328 | 904 € |
| 3 | 1.848 − 328 | 1.520 € |
| 5 | 3.080 − 328 | 2.752 € |
| 10 | 6.160 − 328 | 5.832 € |

**Más lo de producir:** por cada cliente que produce Sami, súmale 150 € (con 3 clientes producidos por él, 450 € más).

---

## Gastos fijos (se pagan con 1 cliente o con 30)
| Concepto | €/mes |
|---|---|
| Claude | 22 € |
| Wispr Flow | 15 € |
| Calendly | 10 € |
| Formación InfoCapitals (271 €/mes, 12 meses; quedan 11 desde noviembre de 2026) | 271 € |
| Comunidad de Skool | 9 € |
| Dominio `iads-agency.es` (10 €/año, ya pagado) | ~1 € |
| **Total** | **328 €** |

Gratis: Make, Fireflies, Loom, el email de empresa y el CRM de InfoCapitals. Higgsfield (136 €/mes) no va aquí: se cuenta dentro de los créditos de cada cliente.

---

## Lo que entra y NO está contado aquí (18/10)

**A propósito**, porque ahora mismo no va a entrar nada de esto (Sami, 18/10). Si algún día entra, se suma aparte y no cambia las cuentas de arriba:

- **Vídeos sueltos** a un cliente del escalón 1: 50-60 €, cuestan 8 € de créditos.
- **Aplicarle las mejoras de su web:** 150 €.
- **El plan de acción suelto:** 150-250 €, para el que no entra en ningún escalón.
- **La cuota que sube** cuando un cliente del escalón 2 invierte más de 3.000 € al mes.

## Lo que estas cuentas no dicen (para no engañarse)
- **Que el cliente se quede.** El momento en que más se van es el segundo pago (SOP de entrega); aquí, el día 30, cuando la campaña lleva unos 17 días. Si se va después del primer mes, el escalón 2 deja 316 € (CAC de Meta) o 466 € (si lo trajo Álvaro: 616 − 150). **Lo que se vigila es cuántos renuevan el segundo mes.**
- **Los impuestos.** Pendiente con la madre de Sami. **Cómo se le paga a Marc ya está cerrado:** transferencia de Revolut (19/10).
- **Las horas de Sami en llamadas, informes y mensajes**, que de momento no se delegan. Se miden con los dos primeros clientes.
- **El valor de vida de un cliente** (cuánto deja en total) no se calcula todavía: depende de renovaciones que aún no han pasado (SOP de métricas).

## Cuántos clientes caben
- **Producción:** Sami produce hasta 3 clientes; a partir del cuarto, con productor (Sami, 14/10).
- **Marc y su chico:** no se sabe. Hay que preguntárselo (en la lista de `la skill `iads-client-pack``).
- **Las horas de Sami:** se miden con los primeros clientes.

## Referencia
- **Precios** (`3-QUE-VENDEMOS.md`): escalón 1, 500 € · escalón 2, 1.300 € · escalón 3, 2.500 € (3.000 € cuando entren TikTok y Google Ads). Todo al mes, + IVA, sin precio de arranque.
- **Créditos** (con un 20 % por si hay que repetir; probablemente sobren): 90 € · 110 € · 220 €.
- **Productor, al mes por cliente, desde el primer mes:** 125 € · 150 € · 300 € (quizá más en el 3). Aparcado: de momento produce Sami.
- **Marc:** 400 €/mes por cliente del escalón 2 (aceptado el 12/10; es el máximo que se puede pagar) y 800 € en el escalón 3. La parte variable no se comparte de momento.
- **Orden de canales:** primero prospección y llamadas en frío; anuncios de Meta cuando la oferta esté probada. A los leads de Meta se les llama en menos de 1 hora.
