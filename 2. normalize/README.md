# Normalize

<hr size="2px" color="black" />

Lo usamos para reiniciar todos `los valores por defecto` que establece el navegador.
Lo utilizamos importandolo o haciendo npm, y luego importandolo o directamente usamos la url

Para ello, debemos instalarlo. Puede instalarse de varias maneras:

- Usando `npm install normalize.css`.
- Descargandolo directamente de la página.

> Puedo realizar modificaciones:

- 1- Para que las imagenes en los mobiles las ajuste al 100%

```bash
  img {
  border-style: none;
  max-width: 100%; <-
  }
```

- 2- box-sizing es para que cuando por ejemplo modifico el padding de una caja siempre se respete
  el tamaño de la caja

(arriba de todo)

```bash
- * {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  }
```
