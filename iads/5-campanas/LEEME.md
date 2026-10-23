# campanas — contenido + gestión de campañas

> **Estado (19/10/2026):** **vivo y aparte.** El proceso es el mismo que el de iAds, pero **Marc se lleva el 50 % como media buyer**, así que **no cuenta en los números ni en las metas de iAds**. Va por su cuenta: sin formulario previo y sin llamada de arranque.
>
> **Venice Eyewear** lleva unos 25 días y **renueva el 25/10**.
>
> **Se revisa en un mes** (hacia el 19/11) para decidir si se incorpora como cliente normal de un escalón o se queda así.


**Esto NO es iAds.** El negocio de siempre (los clientes, el panel, las plantillas, los
packs) está en las otras carpetas de `iads/`. Esta va aparte y **no se mezcla con
aquello**, por decisión de Sami el 30/09/2026: mismo sitio para no perder el contexto,
carpetas separadas para que no se junten.

Aquí va el **servicio nuevo**: además del contenido, se lleva la **gestión de las
campañas**. Es a medias con **Marc** (50/50) y es el primer encargo de este tipo, así
que **todavía no hay estructura**: no hay contrato, no hay onboarding, no hay proceso de
4 llamadas, no hay closer y no hay precio de catálogo. Se va aprendiendo con el cliente
delante.

## Lo que no aplica aquí

Nada del resto de `iads/` gobierna esta carpeta:

- **El panel** (`../scripts/hoy.py`) no lee esto. Los clientes de aquí no salen en `HOY.md` y no disparan alertas de briefing, entrega ni renovación.
- **Las plantillas** de `../plantillas/clientes/` (contrato, onboarding, las 4 llamadas).
- **Los packs y precios** de `../negocio/3-QUE-VENDEMOS.md`.
- **La skill `/iads-client-pack`** como proceso de cliente. Sirve para producir contenido, no para llevar estos clientes.

**Qué sí se mantiene:** todo en disco, una carpeta por cliente, la ficha de marca como
activo, el registro pieza a pieza, y commitear los cambios.

## Cuándo deja de ser un experimento

La estrategia completa de este servicio se cierra a **mediados de octubre de 2026**, en
el chat de *mentoría de negocio iAds*. Ahí se decide qué es rentable, si entran contrato
y onboarding, cómo se reparte, y si esto vuelve a juntarse con iAds o se queda aparte.
Hasta entonces el foco es el cliente, no la estructura.

## Clientes

| Cliente | Desde | Paga | Reparto | Estado |
|---|---|---|---|---|
| [Venice Eyewear](venice-eyewear/interno/MARCA.md) | 30/09/2026 | 849 € mes 1 · 999 €/mes desde el 2 | 50 % Sami / 50 % Marc | hoja de alcance por acordar con Marc, luego accesos |

## Copia de seguridad

Va dentro de la de iAds, así que no hay nada nuevo que recordar: `bash sistema/scripts/copia.sh`
desde `iads/` ya se lleva esta carpeta también.
