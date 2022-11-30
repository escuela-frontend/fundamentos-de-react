## Crear un elemento h1 usando JSX

En el archivo `index.html` escribirás la solución. Dentro del mismo encontrarás comentarios y código que implementa la solución usando la API `createElement` de React.

Ejecuta la lección usando la terminal.

El navegador no entiende JSX, para poder ejecutar JSX en el navegador debes "traducirlo" utilizando una herramienta como Babel, por lo que tendrás que agregarla en tus script



```html
<html>
  <head>
      <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>
     Hola Mundo
  </body>
  <script type="text/babel">
    const h1 = <h1 className="title">Hola Mundo</h1>
    
    const root = document.getElementById('root')
    ReactDOM.render(h1,root)
  </script>
</html>
```
  
## Crear elementos anidados usando JSX

```html
<html>
  <head>
      <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>
     Hola Mundo
  </body>
  <script type="text/babel">
    const nestedH1 = <h1>Hola <strong>Mundo</strong></h1>
    
    const root = document.getElementById('root')
    ReactDOM.render(nestedH1,root)
  </script>
</html>
```
