# Curso completo de Css parte 1

<hr size="2px" color="black" />

## Tipos de selectores de css:

- Universal
- De tipo
- Clases
- ID
- Por atributo
- Descendiente
- Pseudo-clases

<hr size="2px" color="black" />

## Selectores:

### Universal " \* ":

Selecciona todos los elementos dentro del body del html.

```bash
* {
    color: red;
}
```

### De tipo:

Son los que seleciconamos por el nombre del elemento `(h1 - button - input - p - etc)`

```bash
h1 {
    color: red;
}
```

### clases " . ":

Debemos agregar el atributo `class="algo"`, a las etiquetas específica que queremos estilizar.

```bash
.algo {
color: red;
}
```

> Es importante agregar al punto `.` antes del nombre de la clase, para que pueda detectarlo como tal.

### ID " # ":

El selector de ID está destinada para elementos únicos, y debe especificarse en dicho elemento como atributo. `id="element"`

```bash
#element{
    color: red;
}
```

> Es importante agregar al Hash `#` antes del nombre de la Id, para que pueda detectarlo como tal.

### Por atributo:

De la misma forma que con tipos, utilizamos atributos propios y los seleccionamos
`rancio="epico"`

```bash
[rancio="epico"]{
    color: red;
}
```

> Es importante envolver el atributo con los corchetes `[]` para que pueda detectarlo como tal.

### Descendiente:

Es una forma de modifgicar una etiqueta (hijo) que se encuentra dentro de otra (padre)

```bash
<h2><p>Esto es una etiqueta p</p></h2>
```

> Debe ser escrita de tal forma que primero vaya el contenedor padre, y luego el hijo. De izquierda a derecha.

```bash
h2 p {
    color: red;
}
```

> En este caso solo modifica a los p que estan dentro de un h2

### pseudo-clases:

```bash
p:hover {
color: red;
}
```

> En este caso, la propiedad hover va a hacer que cuando el elemento "p" esté posicionado por un cursor, cambie de color a rojo.

`Existen otras formas de sleccionar elementos, pero estas son las más comunes.`

<hr size="2px" color="black" />

## Especificidad:

> Ordenado de mayor a menor en importancia.

```bash
- !important
```

```bash
- Estilos en linea
```

```bash
- Identificadores (ID)
```

```bash
- clases
- pseudo-clases
- atributos
```

```bash
- elementos
- pseudo-elementos
```

> Important se usa de la siguiente manera, pero no es recomendable y tampoco muy necesario.

```bash
h1{
color : grey !important
}
```

`(puede usarse en html para los requerimientos obligatorios de campo, como por ejemplo, un imput)`

<hr size="2px" color="black" />
