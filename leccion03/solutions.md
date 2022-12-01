## Crear elementos usando la API de Javascript

El primer ejercicio trata de crear un elemento H1 y una lista al menos dos item utilizando la API de Javascript.

Para esto debes abrir el archivo `index.html` en donde encontrarás que React está ya agregado y que tienes dos elementos llamados root: `root1` y `root2`

Estos elementos `root` servirán como base para poder "hostear" o almacenar, dibujar los elementos que crearemos.

Lo primero es crear nuestro H1. Utilizamos `document.createElement`. Esta es la API que permite crear elementos y manipular sus atributos y propiedades

```html
<script type="text/javascript">
  const root = document.getElementById('root1')
  const h1 = document.createElement('h1')
  h1.innerHTML = 'Hola Mundo'
</script>
```

Ejecutamos ahora la lección número 3 en el terminal y podras ver que todavía no hay nada en la pantalla, ya que aún falta agregar este elemento dentro del `div` que lo contendrá en este caso llamado `root`.

```html
<script type="text/javascript">
  const root = document.getElementById('root1')
  const h1 = document.createElement('h1')
  h1.innerHTML = 'Hola Mundo'
  root.appendChild(h1)
</script>
```

Ahora podrás ver en pantalla que tienes el mensaje `Hola Mundo`.

La segunda parte de esta tarea o ejercicio es crear una lista del menos dos items.

Para eso, crearemos un elemento `ul`, al que agregaras los elementos `li` necesarios.

A cada uno de estos elementos `li`, le agregarás el contenido interno.

```html
<script type="text/javascript">
  const root2 = document.getElementById('root2')

  const ul = document.createElement('ul')

  const l1 = document.createElement('li')
  l1.innerHTML = 'Elemento 1'

  const l2 = document.createElement('li')
  l2.innerHTML = 'Elemento 2'

  ul.appendChild(l1)
  ul.appendChild(l1)

  root2.appendChild(ul)
</script>
```

No olivdes que cada elemento creado debe "agregarse" a un contenedor padre para que sea dibujado en pantalla.

## Utilizar React para create elementos.

En este caso utilizarás React para crear los mismos elementos anteriores.

```html
<script type="text/javascript">
  const root2 = document.getElementById('root2')

  const title = React.createElement('h1', {
    children: 'Hola Mundo',
  })

  ReactDOM.render(title, root2)
</script>
```

Para crear elementos con la API de React usarás `React.createElement` que es similar a la API de javascript, pero a diferencia de la API imperative de JS, la api de React acepta parámetros, llamados props.

`props` es el nombre dado a un objeto que describe los atributos de este elemento.

Hay una particular una propiedad llamada `children`, que es la que describe lo que va dentro de la etiqueta.

Recuerda que para que React renderize los elementos creados estos deben ser "agregados" utilizando ReactDOM.

La segunda parte es crear elementos anidados.

```html
<script type="text/javascript">
  const root2 = document.getElementById('root2')

  const strong = React.createElement('strong', {
    children: 'Mundo',
  })
  const title = React.createElement('h1', {
    children: ['Hola', strong],
  })

  ReactDOM.render(title, root2)
</script>
```

`children` es una prop que puede recibir un arreglo de elementos lo que permite anidar múltiples elementos.
