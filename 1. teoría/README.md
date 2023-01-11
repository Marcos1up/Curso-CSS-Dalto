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

# Selectores:

## Universal " \* ":

Selecciona todos los elementos dentro del body del html.

```bash
* {
    color: red;
}
```

## De tipo:

Son los que seleciconamos por el nombre del elemento `(h1 - button - input - p - etc)`

```bash
h1 {
    color: red;
}
```

## clases " . ":

Debemos agregar el atributo `class="algo"`, a las etiquetas específica que queremos estilizar.

```bash
.algo {
color: red;
}
```

> Es importante agregar al punto `.` antes del nombre de la clase, para que pueda detectarlo como tal.

## ID " # ":

El selector de ID está destinada para elementos únicos, y debe especificarse en dicho elemento como atributo. `id="element"`

```bash
#element{
    color: red;
}
```

> Es importante agregar al Hash `#` antes del nombre de la Id, para que pueda detectarlo como tal.

## Por atributo:

De la misma forma que con tipos, utilizamos atributos propios y los seleccionamos
`rancio="epico"`

```bash
[rancio="epico"]{
    color: red;
}
```

> Es importante envolver el atributo con los corchetes `[]` para que pueda detectarlo como tal.

## Descendiente:

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

## pseudo-clases:

```bash
p:hover {
color: red;
}
```

> En este caso, la propiedad hover va a hacer que cuando el elemento "p" esté posicionado por un cursor, cambie de color a rojo.

`Existen otras formas de sleccionar elementos, pero estas son las más comunes.`

<hr size="2px" color="black" />

# Especificidad:

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

# METODOLOGIA BEM

Nos basamos en las clases para saber el elemento específico que estamos seleccionando

```bash
<div class="contact-form">
   <input type="text" class="contact-form__input">
   <input type="password" class="contact-form__input">
</div>
```

- Ejemplo si solo quiero modificar el primero:

```bash
<div class="contact-form">
   <input type="text" class="contact-form__input--active" >
   <input type="text" class="contact-form__input">
   <input type="text" class="contact-form__input">
   <input type="text" class="contact-form__input">
   <input type="password" class="contact-form__input">
</div>
```

```bash
.contact-form__input:first-child {
color: red;
}
```

> Es importante tener en cuenta que, para aplicar la metodología BEM, despues de colocar el nombre del bloque, los dobles guiones bajos `__` sumado al nombre de la clase, la seleccion de éstos es mucho más fácil e intuitivo dentro del codigo de css.

Otra forma es gregando `--"loquesea"` y los `--` indicará su `sub-clase` particular, a diferencia del ejemplo anterior, que usaba los dos puntos `contact-form__input:active`

```bash
.contact-form__input--active {
color: red;
}
```

- OTRO Ejemplo:

```bash
<div class="contact-form">
  <p> class="contact-form__p">
    <h2 class="contact-form__p-h2"></h2>
  </p>
</div>
```

<hr size="2px" color="black" />

# Unidades

- Relativas(variables)
- Fijas

> `Estas unidades de medida, serán las encargadas de convertir nuestas fuentes de texto, en fuentes de texto responsive.`

```bash
---fijas: px, cm, mm ,etc
```

```bash
---relativas: rem, em.
```

> REM tiene como referencia el root.
> Por defecto(se la da el navegador) `1em = 16px`. Sino la clase o caja contenedora establece la equivalencia.
> Sirve para cualquier propiedad que trabaje con unidad de medida.

```bash
.contact-form{
font-size: 20px;
}
```

```bash
.contact-form__h2 {
font-size: 5em;
}
```

> En este caso 1em = 20px -> 5em = 100px

`View-port` - Estas medidas ocupan todo el ancho de la pantalla

- vw -> view port width. with: `100vw`
- vh -> view port heigth. height: `50vh`
