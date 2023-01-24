# GRID

<hr size="2px" color="black" />

# Conteptos basicos

Es un estilo de layout, y es un valor d ela propiedad display. Lo que se hace
es trabajar en el layout a traves de grillas.

-   Grid container: es todo el contenedor completo de las celdas

-   Grid item: son cada unos de los elementos que forme parte del container. son elementos los cuales obligaoriamente son hijos del `Grid container`.

-   Grid Cell: es como un item pero no necesariamente, los items son hijos directos
    del `Grid container`, la division posterior pueden ser 4 celdas pero estan en un item.

-   Grid Tracks (column y Row): filas + columnas = grid tracks

-   Grid Area: las areas las definimos nosotros, no estan definidas por defecto.
    las areas tienen que ser consecutivas tanto horizontal como verticalmente

-   Grid Line (column line y Row line)

<hr size="2px" color="black" />

# PROPIEDADES DE GRID:

-   grid-template-rows
-   grid-template-column

-   unidades "auto" y `fr`

    > `fr`: es "como" decir flex grow para que se entienda, todo lo que quede libre daselo a la que se le asigne.

-   grid-row-gap: es como una especie de margin, pero entre celdas. CON LOS BORDES DEL CONTENEDOR NO SE SEPARA.
    grid-column-gap: row column

-   grid-item\_

para seleccionar childs que no son el first es:

```bash
grid-tem:nth-child(hijo){
    . . .
}
```

> `grid-row-start`,
> `grid-row-end`,
> `grid-column-start`,
> `grid-column-end`,

Sirven para fucionar celdas, les indicamos donde empezar y en que borde terminar.

```bash
grid-item:first-child {
    grid-column : 1 / 3
}
```

Empieza en uno y termina en el borde de la 3 esto me desplaza las celdas. Si usamos

```bash
grid-column : 1 / span 3

```

Le decimos que empiece en la linea uno y ocupe 3 columnas
`ES MEJOR USAR SPAN PARA EVITAR CONFLICTOS`.
abreviados en:
`grid-row
grid-column`

-   `repeat(cantidad,tamaño/s)`
    sirve para abreviar la creacion

```bash
grid-template-columns: repeat (3, 150px) 1fr;
```

Tambien usando:

```bash
grid-template-columns: repeat (3, 150px 150px) 1fr;
```

crearia 6 columnas

<hr size="2px" color="black" />

# GRID IMPLICITO Y EXPLICITO:

3 nuevas propiedades del grid implicito

-   `grid-auto-rows`: (igual que el template) repeat no sirve acá, no se define la cantidad sino cuanto mide, solo se pondría por ejemplo solo 200px
-   `grid-auto-columns`: (igual que el template)
-   `grid-auto-flow`: Row(default), `column` y `dense`. podemos hacer que las implicitas cambien de ser filas a columnas. Con dense rellenos campos vacios

<hr size="2px" color="black" />

# GRID DINAMICO

Tiene propiedades como columnas o estructuras auto ajustables, o que cambien los tamaños

valores que generalmente se ponne en repeat(segundo parametro):

-   minmax(): establecemos el min y el max de la celda repeat(3, minmax(100px,200px))
    Para ajustar al contenido usamos:
    -   `min-content`
    -   `max-content`

> Podemos combinar `min-content` y `max-content` con `maxmin()`, generalmente en minmax al max le damos `1fr`

cantidad:

-   `auto-fill`: Genera filas con los elementos, para llenar el espacio sobrante, con el item, y si hay espacio suficiente como para que entre otro, coloca otro item, y asi sucesivamente.
-   `auto-fit`: Es parecido a auto-fill, solo que cuando haya pocos elementos, los escala y hace que ocupen el espacio.

Podemos hacer que se generen columnas o filas dinamicamente si hay espacio o no.

EJEMPLO:

```bash
.grid-container{
    display: grid;
    grid-template-column: repeat(auto-fill, minmax(120px, 1fr));
    grid-template-rows: repeat(3, 100px);
    . . .
}
```

auto-fit los escala, auto-fit genera

<hr size="2px" color="black" />

# ALINEACION Y CONTROL DE FLUJO

diferencia con flex:

La alineacion es dentro de cada celda y no alineacion total del flex
container. Cada celda seria un "flex-container"

(propeidades del grid-container)

## alineacion de items

-   `justify-items(horizontalmente)`: ajusta al contenido y los centra(center) a los items
-   `align-items(verticalmente)`: igual pero verticalmente, depende el parametro con los 2 se centra completamente!

-   `stretch(default: "rellenar")` -start - center - end

## alineacion de filas y columnas

-   justify-content (horizontalmente)
-   align-content (verticalmente)

-   stretch(default) - start - center - end
    > mas las de flex:
        `space-around
        space-between
        space-evenly`

# Aplicado al grid ITEM

-   `align-self (verticalmente)`
-   `justify-self (horizontalmente)`
-   `place-self`: align-self justify-self (shorthand)

-   `stretch(default)` - start - center - end

-   `order(igual que en flex)`: cambio de lugar la celda segun la prioridad
    si a la uno le doy `order 3`, se posiciona en el lugar de la 3 y el resto se
    mueven para atras.

<hr size="2px" color="black" />
