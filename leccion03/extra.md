## Tarea extra

Crear un elemento lista con dos elementos li.

Para esto se deben utilizar elementos anidadados utilizando la api de React.


`React.createElement` acepta 3 o más  argumentos:

- El primero es el nombre del elemento a crear
- El segundo es el objeto props (puede ser `null`)
- El tercero (o subsiguientes) hacen referencia a los elementos  `children` que el nuevo elemento aceptará. (al igual que `props.children`)

```html

<script type="text/javascript">
  const root2 = document.getElementById('root2');
 
  const l1 = React.createElement('li', { children: 'Elemento 1')
  
  const l2 = React.createElement('li', null, 'Elemento 2')
  
  const ul =  React.createElement('ul', null, l1, l2)
  
 
  ReactDOM.render(ul, root2)
</script>

```
