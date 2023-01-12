# Teoria de Cajas

<hr size="2px" color="black" />

Hay 2 tipos de Cajas: en `lineas` o en `bloques`.

-   los bloques ocupan el ancho total de la caja
-   los elementos en linea el ancho es en base al ancho del elemento

Con display le podemos cambiar las propiedades a las cajas

> Algunas propiedades de las cajas: `tamaño`, `background-color`, `image`, `border`, `border-radius`,
> `padding`, `margin`, `box-shadow`

## padding:

Es la distancia entre el texto y la caja.

```bash
  padding: 20px (todos igual)
  : 20px 30px (eje x - eje y)
  : 20px 10px 30px 25px (top left bottom right)
```

## margin:

Es la distancia que hay entre cajas. Si tenemos dos cajas al lado, el margin de ambas se suman

## border-radius:

Es cuanto redondeamos el borde.

## border:

Trata del tamaño (grosor) - estilo - color

```bash
border: 15px solid red;
```

## box-shadow:

Es el sombreado que vamos a darle a la caja.

```bash
box-shadow: 1px 2px 15px 0 #000;
```

> Eje x - eje y - tamaño del desenfoque - cuanto borde - color.
> el `text-shadow` es igual que el box-shadow, pero sin la cantidad de borde.

Repetir la linea de codigo varias veces, separados por comas, hará que su intencidad aumente:

```bash
box-shadow: 1px 2px 15px 0 #000, 1px 2px 15px 0 #000, 1px 2px 15px 0 #000
```

# AUMENTO INTENSIDAD

-   Displays: block, inline-block, Flex, Grid, None
    > Especifica si un elemento es tratado como `block` o `inline` `element` y el diseño usado por sus hijos
-   Positions: Absolute, Relative, inherit
    > Especifica la posicion de un elemento en concreto.
-   Hover: Top, Left, right, bottom

<hr size="2px" color="black" />

0. Outline: Es como border pero sin afectar a las demas cajas, no ocupa un espacio real en el DOM, y puede servir para marcar objetos por ejemplo.

1. Position: Cuando algo adquiere una nueva posicion adquieren nuevas propeidades (`top`, `left`, `right`, `bottom`) que nos permite modificar el tamaño y la posicion del elemento, tratandose de posiciones visuales y no de codigo, o viceversa, y entre otras referente al contenido del elemento. Con las posiciones alteramos el flujo de html.

-   STATIC: valor por defecto.

-   RELATIVE: Hacemos que el espacio original en el dom se siga conservando. Entonces se mueve pero su espacio original sigue en el mismo lugar. Ademas el punto de referencia sigue siendo el mismo. `Top` y `left` predominan sobre `bottom` y `right`, son mas importantes.

-   ABSOLUTE: A diferencia de relative, el espacio no se guarda. Cuando tenemos un contenedor y le damos `pocision absoluta` a un hijo, si no le damos `top` y `left`, toma `referencia/herencia` del padre. AHORA si le damos `top` y `left` la referencia es el `VIEWPORT`. Cuando uso `absolute` la caja se ajusta al contenido. Para que tome de referencia al padre, debemos posicionarlo (Ej: `position: relative` al contenedor)

-   FIXED: Es igual que `absolute`, pero queda fijado en un lugar. (por ejemplo en las publicidades que te siguen el scroll)

-   STICKY: Al igual que en `relative`, el espacio que se reserva en el DOM lo conserva. Se comporta como un `fixed` cuando llegamos a un punto que nosotros les decimos.

2. Z index: Posiciona en el `eje Z`, conviene usar numeros grandes, dejando espacios de 50 para poder poner más elementos en el medio en el futuro, y evitar que no sea escalable.

> Conflicto: la unica forma de poner un padre por debajo de un hijo es usando un `z-index negativo` en el hijo y no definirlo en el padre.
