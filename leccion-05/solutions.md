## Props en React

En este ejericio ya dejamos de lado el uso de la API `createElement` y de utilizar elementos HTML y comenzamos a crear componentes React.

En este primer ejercicio debes crear un componente que recibe ciertas props para ser luego desplegadas.

Un componente en React es sólo una función que recibe un único argumento llamado `props`.
Este argumento es un objeto que es después expuesto en JSX como atributos del componente.

Todo componente React retorna algo que pueda ser renderizado, eso incluye arreglos, texto, `null`, elementos html y más JSX.

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
        const nombre = 'User'
        const email = 'user@email.com'
        const telefono = '123344556'
        // ¿Que debe retornar este componente padre?
        return <UserInfo nombre={nombre} email={email} tel={telefono} />
    }

    const root = document.getElementById('root')
    // 💡  sRenderiza el componente padre
    ReactDOM.render(<ParentComponent />, root)
```



Finalmente, le indicas a React que renderice el componente padre `<ParentComponent />` que a su vez renderizará `<UserInfo>` que finalmente renderizará el elemento `<p>` creando un árbol de componentes.
