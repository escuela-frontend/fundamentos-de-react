Este ejercicio extra te muestra que `useState` no sólo acepta valores sencillos, si no también puedes utilizar estructuras de datos más complejas como un objeto.

El objeto en este caso se utilizará para mantener el estado de cada uno de los elementos del formulario.

Tamnbién actualizarás el formulario para mantener 3 elementos de formulario cada uno con su propio nombre `name`. Este atributo `name` se usará dentro de la única función que maneja los cambios de los elementos del formualario: `handleChange`.


La función `handleChange` es ejecutada cada vez que uno de los elementos cambia. Esta función obtiene el nombre y el valor de dicho elemento y lo utiliza para formar el nuevo estado.

`useState` puede recibir una función tipo callback. Esta función recibe como parámetro el estado previo y retornará el siguiente estado. Usarás esta idea para poder actualizar el estado sólo en el elemento que lanzó el evento


```js


const root = document.getElementById('root')
const App = () => {
  const [formState, setFormState] = React.useState({
    input1: '',
    select: '',
    input2: ''
  })
  
  const hadleChange = (event) => {
    const { name, value } = event.target 
    setFormState((prev) => {
      ...prev,
      [name]: value
    })
  }
  const onSubmit = event => {
    event.preventDefault()
    console.log(formState)
  }

  return (
    <div>
      <form onSubmit={onSubmit}>
        <input type="text" onChange={handleChange} name="input1"/>
        <select onChange={handleChange} name="select">
          <option value="option 1">Option 1</option>
          <option value="option 2">Option 2</option>
          <option value="option 3">Option 3</option>
        </select>
        <input type="text" onChange={handleChange} name="input2" />
        <button type="submit">Enviar</button>
      </form>
    </div>
  )
}
ReactDOM.render(<App />, root)
```

