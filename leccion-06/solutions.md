# Renderizado Condicional


## Utilizando ternary

```js
    // 💡 objeto que representa un usuario -  datos de ejemplo
    const usuarioWithContacts = {
        name: 'User 1',
        contacts: [
            {
                name: 'Contact 1',
            },
            {
                name: 'Contact 2',
            },
            {
                name: 'Contact 3',
            },
        ],
    }

    // 💡 usuario sin contactos
    const usuarioWithoutContacts = {
        name: 'User 2',
        contacts: [],
    }

    // 💡 Componente que mostrá los contactos del usuario
    function Contacts(props) {
        return (
            <div className="contacts-list">
                {props.map(contact => {
                    return <div className="contact">{contact.name}</div>
                })}
            </div>
        )
    }

    function NoContacts() {
        return <h1>No hay Contactos</h1>
    }

    function RenderUsersWithTernary(props) {
        /* 1. Utiliza un operador ternario para renderizar los componentes
        <Contacts contacts={props.users.contacts /> y <NoContacts /> */
        return (
            <div>
                <h3>{props.user.name}</h3>
                {props.user.contacts.length > 0 ? 
                <Contacts contacts={props.user.contacts} />
                : <NoContacts />
                }
            </div>
        )
    }

    // 🍬 Crea un componente para renderizar condicionalmente
    // utilizando un bloque if-else.
    // ¿qué ocurre y por que?

    function App() {
        return (
            <div>
                <h1>Lista de Contactos por usuario</h1>
                <RenderUsersWithTernary user={usuarioWithContacts} />
                <hr />
                <RenderUsersWithTernary user={usuarioWithoutContacts} />
            </div>
        )
    }

    ReactDOM.render(<App />, root)
```

## Utilizando operador `&&`

```js
    // 💡 objeto que representa un usuario -  datos de ejemplo
    const usuarioWithContacts = {
        name: 'User 1',
        contacts: [
            {
                name: 'Contact 1',
            },
            {
                name: 'Contact 2',
            },
            {
                name: 'Contact 3',
            },
        ],
    }

    // 💡 usuario sin contactos
    const usuarioWithoutContacts = {
        name: 'User 2',
        contacts: [],
    }

    // 💡 Componente que mostrá los contactos del usuario
    function Contacts(props) {
        return (
            <div className="contacts-list">
                {props.map(contact => {
                    return <div className="contact">{contact.name}</div>
                })}
            </div>
        )
    }

    function NoContacts() {
        return <h1>No hay Contactos</h1>
    }

    function RenderUsersWithLogic(props) {
        /* 2. Utiliza el operador lógico && para renderizar los componentes 
        <Contacts contacts={props.users.contacts /> y <NoContacts /> */
        return (
            <div>
               <h3>{props.user.name}</h3>
                {props.user.contacts.length > 0 && <Contacts contacts={props.user.contacts} />}
                {!props.user.contacts.length <= 0 && <NoContac />}
            </div>
        )
    }

    function App() {
        return (
            <div>
                <h1>Lista de Contactos por usuario</h1>
                <RenderUsersWithLogic user={usuarioWithContacts} />
                <hr />
                <RenderUsersWithLogic user={usuarioWithoutContacts} />
            </div>
        )
    }

    ReactDOM.render(<App />, root)
```