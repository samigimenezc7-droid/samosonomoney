# Contrato de colaboración y confidencialidad (productor)

> ⏸️ **Aparcado** (18/10/2026). Los productores no están en marcha: **produce Sami** hasta el cuarto cliente. Estos once documentos están completos pero son **del modelo viejo** (packs Base y 65/125 € por pack). **Al desaparcarlos hay que repasar los precios:** hoy serían **125 € (escalón 1), 150 € (escalón 2) y 300 € (escalón 3) al mes por cliente**, desde el primer mes (`1-negocio/6-NUMEROS.md`). El paso a paso de meter a un productor también se repasa: está en `CLAUDE.md`.


Versión 2 · 01/10/2026 (cerrado con Sami el 27/09 cláusula a cláusula; el 01/10 cambia el nombre a "contrato" y el pago pasa a tarifa fija). **Es la plantilla por defecto para todo productor nuevo.** Se firma **después del filtro y antes de darle el Loom**: hasta que lo acepta, no recibe nada del método de iAds.

**Es una plantilla que se rellena con cada productor** (igual que el contrato del cliente): su nombre, la fecha, si hace o no las llamadas con clientes y cuándo prefiere cobrar. Si cambia algo aquí, se cambia también en `scripts/contrato_productor_pdf.py`.

**Cómo se comparte el material con el productor:** siempre con **enlaces de Sami** (Loom, Drive…), nunca como archivos descargados. Al terminar la colaboración, se le quita el acceso.

## Cómo se genera

```bash
python3 4-plantillas/scripts/contrato_productor_pdf.py \
  --colaborador "Nombre y apellidos" \
  --pago "al entregar cada pack" \
  [--llamadas] \
  --salida "3-equipo/2-produccion/[clave]/plantillas/CONTRATO.pdf"
```

- `--pago`: "al entregar cada pack" o "a final de mes", lo que prefiera el productor.
- `--llamadas`: solo si también va a hacer las llamadas de briefing y validación con los clientes.

## Cómo se manda

> Te paso el contrato de colaboración: cómo trabajamos, cómo se paga y la confidencialidad. Si te vale, respóndeme "de acuerdo" y te paso el acceso a la formación.

---

## El texto

**CONTRATO DE COLABORACIÓN Y CONFIDENCIALIDAD**

**Partes:** iAds y **[nombre del productor]** ("el Colaborador"). Fecha: [fecha].

**1. Objeto.** El Colaborador produce para iAds los packs de contenido que se le encarguen: ángulos, guiones, vídeos y creatividades estáticas, siguiendo el método y el nivel de calidad de iAds. **[Si aplica: también realiza las llamadas de briefing y validación con los clientes.]** Cada pack se le encarga por separado, y puede aceptarlo o no.

**2. Pago.** El Colaborador cobra por pack. En un pack Base (10 vídeos), **65 € el primer mes de cada cliente y 125 € a partir del segundo**. En los packs más grandes, el doble (Crecimiento) o el triple (Escala). Si además hace las llamadas de briefing y validación, se suman **25 €, 30 € o 40 €** según el pack.

iAds cubre los créditos de producción necesarios para cada pack.

El pago se hace **[al entregar cada pack / a final de mes]**, según prefiera el Colaborador.

**3. Plazos y avisos.** El Colaborador se compromete a cumplir el plazo acordado en cada encargo, porque de él depende la entrega al cliente. **Si sabe que no va a poder cumplirlo, lo avisa en cuanto lo sepa**, no el día de la entrega. Cada pack se entrega a iAds en una llamada corta de revisión antes de que llegue al cliente.

**4. Confidencialidad.** El Colaborador no compartirá con nadie ni usará para otros fines la información de iAds ni de sus clientes a la que tenga acceso: quiénes son los clientes, sus productos, su material, sus datos, sus resultados, los precios y la forma de trabajar de iAds. Esta obligación dura **mientras dure la colaboración y 1 año después** de que termine.

**5. El método de iAds.** El material de formación y de trabajo que iAds le facilita (vídeos de formación, herramientas, skills, plantillas, guiones y procesos) **es propiedad de iAds**. El Colaborador solo puede usarlo para los encargos de iAds. **No puede copiarlo, compartirlo, venderlo ni usarlo** para trabajos propios o de otros clientes.

**6. Clientes de iAds.** Mientras dure la colaboración y **durante los 12 meses siguientes**, el Colaborador **no trabajará directamente**, ni a través de otras personas, **con ningún cliente de iAds** que haya conocido por esta colaboración, ni le ofrecerá sus servicios.

**7. Propiedad del trabajo.** Todo lo que el Colaborador produce en los encargos (ángulos, guiones, vídeos y creatividades) **pertenece a iAds y a sus clientes**. El Colaborador no puede publicarlo ni usarlo en su portfolio **sin permiso por escrito de iAds**.

**8. Fin de la colaboración.** Cualquiera de las dos partes puede terminar la colaboración cuando quiera, avisando por escrito. Los encargos que estén en marcha se terminan y se pagan. Al terminar, iAds retira el acceso a su material, y el Colaborador **deja de usarlo y no guarda copias del material de los clientes**.

**9. Incumplimiento.** Si el Colaborador incumple este contrato, sobre todo en confidencialidad, en el uso del método o con los clientes de iAds (cláusulas 4, 5 y 6), iAds puede **terminar la colaboración de inmediato** y reclamar los daños que le cause.

**10. Aceptación.** El Colaborador acepta este contrato respondiendo **"de acuerdo"** al mensaje en el que se le envía. Hasta que lo acepte, no se le da acceso al material de iAds.

---

*Descartada por Sami: cláusula de "relación entre las partes" (colaboración independiente, no laboral). Nota de Claude: en España, si alguien trabaja de forma habitual para iAds, conviene dejar claro que es colaborador independiente para evitar que se considere falso autónomo. Revisarlo con la gestoría cuando haya productores fijos.*
