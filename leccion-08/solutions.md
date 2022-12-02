## Renderiza manualmente una lista de elementos

Para renderizar una lista de forma manual, debes escribir cada elemento `li` donde corresponda.

En este ejercicio crearemos un componente que renderiza una lista creada con elementos `ul` y `li`
```js
const ManualList = () => {
  return (
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
  )
}



const root = document.getElementById('root')
ReactDOM.render(<ManualList />, root)
```

Si bien esta forma de renderizar elementos es simple puede ser poco eficiente si son muchos los elementos
o si estos elementos vienen como una prop, son dinámicos o de formas complejas (arreglo de objetos)

## Utiliza `Array.map` 

Utilizar `Array.map` es una forma simple de iterar y renderizar múltiples elementos, en este caso, en una lista.

```js
const MapList = () => {
  const strings = ['string 1','string 2','string 3']
  return (
    <ul>
        {strings.map(item => <li>{item}</li>)}
    </ul>
  )
}


const root = document.getElementById('root')
ReactDOM.render(<MapList />, root)
```

## Utiliza la prop `key`

La prop key permite a React crear una heurística confiable para conocer cuando un elemento renderizado de forma iterativa cambia o no y así poder ejecutar un renderizado mas eficiente.

[Revisa este artículo](https://www.escuelafrontend.com/prop-key-en-react) para saber más sobre la prop `key`