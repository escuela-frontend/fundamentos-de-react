Una última cosa que podemos hacer es escribir nuestro primer script y hacer un simple `console.log` para comprobar que React está disponible.

Esto nos mostrará el resultado en la consola lo mismo con React DOM

```html
<html>
  <head›
    <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
  </head>

  <body>
    Hola Mundo
  </body>

  <script>
    console.log(React)
  </script>
</html>

```

En resumen configurar una app con React, es sencillo, al menos en esta versión estática, simplemente agregamos los archivos correspondientes como un scripts aqui utilizando el servicio unpkg.
