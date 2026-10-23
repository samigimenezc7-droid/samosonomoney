# Scorecard de contenido

> **Rellena esto en `tuyo/`, no aquí.** Esta carpeta se sustituye entera cuando
> te mandamos versión nueva, así que lo que escribas aquí dentro se pierde.

Rejilla vacía para auditar un canal con sus propios números. Se rellena una vez
al mes con el export de la plataforma, no de memoria. Sirve para decidir qué
formato repetir y qué formato matar, que es una decisión de dinero y no de
gusto.

Todos los umbrales de aquí se calculan con TUS datos. Un umbral copiado de otro
canal miente, porque el suelo de distribución depende del tamaño y del histórico
de tu cuenta, no del formato. El criterio de qué hacer con lo que salga está en
`sops/contenido.md` y en `sops/youtube.md`.

Canal: [ ................ ] Periodo: [ ....... ] Piezas analizadas: [ .... ]

## 1 · Los datos, tal como salen del export

Una fila por pieza. Se ordenan por vistas, de mayor a menor.

| Pieza | Duración | Impresiones | CTR | Retención | Vistas | Nuevos seguidores | Trajo lead |
|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |

*El fallo de siempre:* rellenar solo las columnas que salen bien. La columna
"trajo lead" es la única que conecta el contenido con el negocio, y es la que
más se deja en blanco porque exige haber preguntado al lead de dónde salió.
Sin ella estás optimizando vistas, y las vistas no las paga nadie.

## 2 · Tus umbrales, calculados aquí

Se calculan una vez y se anotan. Se recalculan cada tres meses o cuando el canal
doble de tamaño, no antes: un umbral que se mueve cada semana no filtra nada.

**Mediana de vistas del canal**
Ordena tus piezas por vistas y coge la del medio: [ ....... ]
Todo lo que compares a partir de ahora se compara contra este número, no contra
lo que hace otro canal.

**Suelo de CTR**
Mediana del CTR de las piezas que superaron [ ....... ] impresiones: [ ..... ]
Por debajo de ese suelo, con volumen de impresiones suficiente, el packaging
falló. No fue mala suerte: hubo distribución y la gente decidió no entrar.

*Por qué se filtra por impresiones antes de mirar el CTR:* una pieza con muy
pocas impresiones puede marcar un CTR altísimo y no significa nada, porque ese
click viene de tu audiencia propia, que entra a todo. Fija el mínimo de
impresiones en un número que en tu canal solo se alcance cuando la plataforma
te ha empujado de verdad.

**Umbral de outlier**
Outlier es la pieza que multiplica por [ .... ] la mediana de tu canal.
El multiplicador lo eliges tú, pero se fija antes de mirar los resultados. Si lo
decides después, vas a llamar outlier a lo que te gustaba de antemano.

**Conversión a seguidor**
Nuevos seguidores dividido entre vistas, por pieza. Mediana del canal: [ ..... ]
Es lo que separa a la pieza que trae gente de la pieza que trae gente que se
queda. Una pieza puede estar por debajo en vistas y por encima aquí, y esa es
la que hay que repetir.

**Volumen mínimo antes de opinar**
Piezas publicadas en este formato: [ .... ] de las [ .... ] que me di de plazo.
Por debajo de ese número no se diagnostica nada. Concluir que un formato no
funciona con cuatro piezas publicadas es leer ruido, y el coste no es el error:
es que abandonas el único formato que iba a funcionar justo antes de que empiece
a componer.

## 3 · La rejilla de criterios

Una fila por criterio. Se marca cumple o no cumple contra TU umbral de arriba, y
se escribe qué se hace. Nada de "regular".

| Criterio | Tu umbral | ¿Cumple? | Qué se hace |
|---|---|---|---|
| CTR con impresiones suficientes |  |  |  |
| Retención en el tramo de duración que uso |  |  |  |
| Conversión a seguidor |  |  |  |
| Piezas por encima de la mediana del canal |  |  |  |
| Alguna pieza cruzó el umbral de outlier |  |  |  |
| Leads atribuidos a contenido |  |  |  |
| Volumen mínimo alcanzado |  |  |  |
| El formato que trajo clientes se está repitiendo |  |  |  |

## 4 · Retención por duración

Agrupa tus piezas por tramos y saca la retención media de cada tramo. La
duración no es una preferencia estética: cambia lo que el número significa.

| Tramo de duración | Piezas | Retención media | Leads atribuidos |
|---|---|---|---|
| Corto |  |  |  |
| Medio |  |  |  |
| Largo |  |  |  |

*Cómo se lee:* una pieza larga con retención baja no es automáticamente un
fracaso, porque acumula horas de consumo y esas horas son las que alguien
necesita contigo antes de comprar. Pero solo se justifica si el objetivo
declarado de esa pieza era acumular horas. Si el objetivo era conversión, la
retención baja es lo que es.

*El fallo de siempre:* comparar la retención de una pieza larga con la de una
corta y sacar conclusiones sobre el formato. Son dos trabajos distintos con dos
métricas distintas, y mezclarlos te lleva a matar el formato equivocado.

## 5 · Diagnóstico

El formato con más impresiones ha sido: [ ..................... ]
El formato que ha traído leads ha sido: [ ..................... ]
¿Son el mismo? [ ....... ]

*Si no son el mismo:* el que trae leads manda. El de impresiones se mantiene
solo si además convierte a seguidor por encima de tu mediana, porque entonces
está llenando la audiencia que compra dentro de unos meses. Si no hace ni lo uno
ni lo otro, es tráfico que pagas con tu tiempo de grabación.

Lo que se repite el mes que viene: [ ..................... ]
Lo que se mata: [ ..................... ]
Lo que NO se toca todavía y hasta qué señal: [ ..................... ]

*El fallo de siempre:* salir de la revisión con seis ideas nuevas de formato en
vez de con una decisión sobre los que ya tienes. Un formato nuevo cada mes
significa que ninguno llega nunca al volumen mínimo, y entonces el scorecard del
mes que viene vuelve a salir vacío.
