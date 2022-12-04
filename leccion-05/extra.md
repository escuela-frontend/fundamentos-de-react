## Considera que tienes un objeto con varios atributos, ¿cómo puedes pasar ese objeto directamente como props a tu componente?

El proceso de pasar props puede ser tedioso, pero hay formas de escribir la misma lógica de forma más concisa: Destructuring.

Recuerda que un componente React es una función que recibe un sólo argumento tipo objeto y que JSX es una forma declarativa de escribir `React.createElement(tipo, props)`.

Considerando eso, puedes hacer uso de la sintaxis spread de Javascript para pasar un objeto directamente `{...obj}`.

```js 
    // 💡 Crea un componente quie muestre la información del usuario
    // ¿Como recibes las props nombre, email y telefono?
    // despliega la información de las props
    const UserInfo = (props) => {
        const { nombre, email, tel } = props
        return <p>{nombre} - {email} - {tel}</p>
    }

    // 💡  Este es el component padre que deberá contener al componente UserInfo
    const ParentComponent = () => {
        const obj = {
            telefono: '123344556',
            nombre: 'User',
            email: 'user@email.com'
        }
        // ¿Que debe retornar este componente padre?
        return <UserInfo {...obj} />
    }

    const root = document.getElementById('root')
    // 💡  sRenderiza el componente padre
    ReactDOM.render(<ParentComponent />, root)
```
