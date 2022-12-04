## Mostrar una alerta a hacer click

Para completar este primer ejercicio solo requieres crear un elemento `<button>` y definir el evento `onClick`.

```js
const root = document.getElementById('root')
const options = ['Option 1', 'Option 2', 'Option 3']
const App = () => {
  const onClickButton = event => {}
  return (
    <div>
       <button onClick={() => alert('Boton presionado')}>Botón</button>

      <select>
        {options.map(option => (
          <option value={option} key={option}>
            {option}
          </option>
        ))}
      </select>


      <input type="text" placeholder="Escribe algo" />

    </div>
  )
}
ReactDOM.render(<App />, root)
```

## Crear un elemento select


En este caso, debes definir el evento `onChange` y definir que función se ejecutará.

La función, en este caso llamada `onSelectChange` recibirá un evento, en donde puedes acceder a los atributos del elemento que recibió el evento.

```js
const root = document.getElementById('root')
const options = ['Option 1', 'Option 2', 'Option 3']

const onSelectChange = (event) => {
  alert(event.target.value)
} 

const App = () => {
  const onClickButton = event => {}
  return (
    <div>
       <button onClick={}() => alert('Boton presionado')}>Botón</button>

      <select onChange={onSelectChange}>
        {options.map(option => (
          <option value={option} key={option}>
            {option}
          </option>
        ))}
      </select>


      <input type="text" placeholder="Escribe algo" />

    </div>
  )
}
ReactDOM.render(<App />, root)
```

## Crear un elemento input

De forma similar al ejercicio anterior, el elemento `input` también lanza el evento `onChange` cada vez que el contenido del input cambiar. Para capturar ese valor basta con definir una función que recibirá el evento y acceder a sus propiedades como `event.target.value`.


```js
const root = document.getElementById('root')
const options = ['Option 1', 'Option 2', 'Option 3']

const onSelectChange = (event) => {
  alert(event.target.value)
} 

const onInputChange = (event) => {
  console.log(event.target.value)
}

const App = () => {
  const onClickButton = event => {}
  return (
    <div>
       <button onClick={}() => alert('Boton presionado')}>Botón</button>

      <select onChange={onSelectChange}>
        {options.map(option => (
          <option value={option} key={option}>
            {option}
          </option>
        ))}
      </select>


      <input type="text" placeholder="Escribe algo" onChange={onInputChange}/>

    </div>
  )
}
ReactDOM.render(<App />, root)
```
