## Utilizando JSX crea una lista de 3 elementos utilizando ul y li.

Esto es similar al ejercicio anterior de anidación de elementos, simplemente deberás escribir los elementos como si se tratase de etiquitas HTML

```html
<html>
  <head>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>
    Hola Mundo
  </body>
  <script type="text/babel">
    const lista = (
      <ul>
        <li>Elemento 1</li>
        <li>Elemento 2</li>
      </ul>
    )

    const root = document.getElementById('root')
    ReactDOM.render(lista, root)
  </script>
</html>
```

Como ves, la implementación de elementos anidados es sencilla al utilizar JSX y bastante declarativa en comparación con la API cruda.

## usando la lista antes creada ¿Cómo automatizarías la creación de múltiples items li ?

Para esto debes asumir que los elementos que quieres renderizar están agrupados en un arreglo, y dado que JSX es una extensión de Javascript, usarás métodos nativos de Javascript para iterar sobre el arreglo.

Deberás utilizar un método que te permita iterar sobre el arreglo pero que retorne un nuevo arreglo para ser renderizado: `Array.map`, `Array.filter`, `Array.some`, etc.

```html
<html>
  <head>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>
    Hola Mundo
  </body>
  <script type="text/babel">
    const elements = ['Elemento 1', 'Elemento 2']
    const lista2 = (
      <ul>
        {elementos.map(function (element) {
          return <li>{elemento}</li>
        })}
      </ul>
    )

    const root = document.getElementById('root')
    ReactDOM.render(lista2, root)
  </script>
</html>
```

Para esta operación debes usar las llaves `{}` entre el código JSX para poder ejecutar operaciones javascript, esto se llama interpolación y te permite salir del mundo de JSX (que recuerda es una forma declarativa de escribir una llamada a la función `React.createElement`) y entrar en el mundo de javascript puro.
