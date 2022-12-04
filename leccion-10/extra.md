
## Crea un **componente** `Button` que acepta una prop `onClick`. Esta función estará definida en el componente padre.

Este ejercicio extra si bien es similar al anterior ejercicio de crar un botón tiene como objetivo reforzar el hecho de que en React un componente es sólo una función.

La función `Button` recibe como parámetros un objeto llamado `props` y dentro de dicho objeto irá una propiedad llamada `onClick` que recibirá una función.

Esta prop `onClick` es entonces pasada como argumento al evento `onClick` del botón
```js
const root = document.getElementById('root')
const options = ['Option 1', 'Option 2', 'Option 3']

const onSelectChange = (event) => {
  alert(event.target.value)
} 

const onInputChange = (event) => {
  console.log(event.target.value)
}

const Button = ({ onClick }) => {
  return (
    <button
        onClick={onClick}
    >
      Componente Button
    </button>
  )
}
const App = () => {
  const onClickButton = event => {

    console.log('Componente Button');

  }
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

<Button onClick={onClickButton} />

    </div>
  )
}
ReactDOM.render(<App />, root)
```
