# FLEX-BOX

Se le aplica flex-box a un contenedor (`display: flex`), y pasa a comportarse como bloque.
Los cambios los vamos a ver en los items contenidos en esta caja.

Flex-box tiene 2 ejes:

-   Main axis: eje x. Tienen un inicio y final, son las direcciones donde apunta. `Main-start` hacia `main-end`.
-   Cross axis: eje y. `Cross-start` a `cross-end`.

<hr size="2px" color="black" />

# Propiedades del contenedor

Propiedades que generalmente son usadas para los contenedores de items.

## flex-direction:

-   `row` (por defecto), `column`, `row-reverse` y `column-reverse` cambian los inicios logicamente (un efecto espejo)
    > Cambiar la direccion del main-axis: si cambio un eje, automaticamente el otro tambien se cambia.

## flex-Wrap:

-   `wrap` y `wrap-reverse`, `non-wrap`. respeta el ancho especifico de las cajas, las tira para abajo, reverse los tira para arriba.

## flex-flow:

-   sirve para hacer `direction` y `wrap` juntos.Ej: `flex-flow: column wrap`
    conviene usarlo cuando se cambian las 2 props juntas.

## justify-Content:

-   `center`, `space-around`, `space-between`, `space-evenly` (main axis).

## aling-items:

-   `flex-start`, `center`, `flex-end`, `strech` (default), `baseline` (cross-axis)
    se usa para cuando hay una linea de items que son flex items.

## align-content:

-   para cuando hay mas de una linea de items. tiene los mismos valores
    que `align-items`, pero en boxes.

<hr size="2px" color="black" />

# Propiedades de los items

Propiedades que generalmente son usadas para los items dentro de los contenedores.

FUNCIONAMIENTO DEL MARGIN:

> `margin-(direction)`: auto -> margin = contenedor - tamaño de la caja en el eje en el que corre (direction)

-   `align-self`: (cross axis) `flex-start` `flex-end` y `baseline`, mueve una sola caja en particular en el eje y.

-   `flex-grow`: (espacio asignado + sobrante / grows) (main axis)
    `"agarra"` el espacio sobrante y lo distribuye en los items restantes.
    los valores se asignan en numeros , y son las partes en las que se divide el sobrante

-   `flex-shrink`: espacio que `"cede"` cada item (main axis)
    decide que caja va aceder mas espacio cuando no alcance (Lo mísmo que con flex-grow, pero al revés)

-   `flex-basis`: medicion antes de encogerse
    (En auto(default value), agarra el with, y sino tiene mas priridad) (main axis)
    Es como el width pero tiene mas improtancia

-   `flex`: `flex-grow`, `flex-shrink`, `flex-basis` es para abreviar parametros, en vez de estarlos escribiendo a todos uno por uno.
    (al menos el primer parametro obligatorio)

-   `order`: (como el `z-index`, pero en el eje en el que apunta el main axis)

<hr size="2px" color="black" />
