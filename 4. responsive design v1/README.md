# RESPONSIVE DESIGN - MOBILE FIRST

Es para detectar las resoluciones y cambiar el tamaño de las etiquetas
y su contenido a los distintos dispositivos.

> Cuando una pagina es mobile first, google les da mejor posicionamiento.

Para poder detectar estos cambios en las resoluciones usamos `@media`.

`@media only screen and(max-width: 800px)` en este caso decimos que Cunando
la pantalla alcance resoluciones menores a 800px vamos a hacer algo

```bash
@media only screen and (max-width: 600px) {
    div {
        display: block;
        width: 100%;
    }
}
```

Es necesario agregar la etiqueta para poder trabajar con responsive. normalmente visual estudio code lo agrega por defecto

```bash
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
