
Aquí encontrarás la solución final a los 3 objetivos mencionados en el `README.md`

1. Define el evento `onSubmit` para el form.
2. Define los manejadores de eventos para el input y para el select.
3. Actualiza el método `onSubmit` para que no refresque la página.

El elemento `form` puede lanzar el evento `onSubmit` cuando su contenido es enviado. Es posible capturar ese evento con React y ejecutar una función arbitraria.

Esta es tu primer acercamiento a como React maneja el estado de un component por medio del hook `useState`. Este hook es una simple función que recibe un valor y que retorna una `tupla`.

Esta tupla esta constituida por dos valores, el primero, el valor actual del estado, y el segundo es una función que te permite actualizar el estado.

En React, cada vez que el estado se actualiza el componente se re-renderizará modificando así la interfaz desplegada.

En este caso, se utilizan dos `useState` para manejar el estado de los elementos de formulario existentes en la interfaz, para así utilizarlos en la función `onSubmit`


Este elemento `form` emite el evento `onSubmit` cuando el único botón es clickeado ya que dicho botón está definido como `submit`.

```js


const root = document.getElementById('root')
const App = () => {
  const [inputState, setInputState] = React.useState('')
  const [selectState, setSelectStat] = React.useState('')

  const handleInput = event => {
    setInputState(event.target.value)
  }

  const handleSelect = event => {
    setSelectStat(event.target.value)
  }

  const onSubmit = event => {
    event.preventDefault()
    console.log({
      input: inputState,
      select: selectState,
    })
  }

  return (
    <div>
      <form onSubmit={onSubmit}>
        <input type="text" onChange={handleInput}/>
        <select onChange={}>
          <option value="option 1">Option 1</option>
          <option value="option 2">Option 2</option>
          <option value="option 3">Option 3</option>
        </select>
        <button type="submit">Enviar</button>
      </form>
    </div>
  )
}
ReactDOM.render(<App />, root)
```

