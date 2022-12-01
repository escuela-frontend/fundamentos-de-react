Para lograr este pequeño challenge.

Lo primero es abrir un archivo `index.html` que está vacío.

Por tanto, no tenemos nada que ver en la pantalla.

Agregaremos un pequeño esqueleto de un archivo html.

```html
<html>
  <head> </head>
</html>
```

Dentro del head, utilizaremos este snippet de código que lo que hace es traer o agregar , utilizando los scripts, React y ReactDOM desde unpkg.

```html
<html>
  <head>
    <script
      src="https://unpkg.com/react@17/umd/react.development.js"
      crossorigin
    ></script>
    <script
      src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"
      crossorigin
    ></script>
  </head>
</html>
```

Luego un simple body para poner que eestamos utilizando esto de alguna manera.

```html
<html>
  <head>
    <script
      src="https://unpkg.com/react@17/umd/react.development.js"
      crossorigin
    ></script>
    <script
      src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"
      crossorigin
    ></script>
  </head>
  <body>
    Hola Mundo
  </body>
</html>
```

Entonces tenemos nuestro hola mundo funcionando. Vemos en la consola y podemos verificar que React está disponible en el elemento global. A

quí está React y todos sus componentes y métodos. Y también podemos ver que está React DOM disponible

Con esto ya hemos configurado React para comenzar a trabajar con él
