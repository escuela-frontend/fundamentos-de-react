## Utiliza composición e interpolación para renderizar componentes  

Para resolver este ejercicio usarás dos conceptos: Composición y slots.

Tal como leíste en en el `README.md`, el modelo de composición es nativo a React y puedes implementarlo con simples props, en donde un componente recibe como props otros componentes y luego renderiza esos componentes en ciertas partes: `slots`.

Ahora el componente que recibe estas props utilizará interpolación `{}` para definir el lugar donde dichos componentes se renderizarán.

```js
// 💡 Estos son los componentes bases que usarás para completar el ejercicio
// la idea es que puedas crear una interfaz usando estos componentes y la técnica de
// composición
const NavBar = () => {
  return <h2>Barra de navegacion</h2>
}

const PageBody = () => {
  return <h1>Main Con†ent</h1>
}

const Footer = () => {
  return <h3>Footer Content</h3>
}

// 2.¿Que props deberia recibir este componente para poder renderizar los componentes correctos?
// Tip: usarás interpolación para poder renderizar las props/comopnentes en el lugar correspondiente
const Page = ({ nav, main, footer }) => {
  return (
    <div>
      <nav>{nav}</nav>
      <main>{main}</main>
      <footer>{footer}</footer>
    </div>
  )
}

// 1. Pasa las props correctas al componente Page
const App = () => {
  return (
    <body>
      <Page 
        nav={<NavBar />}
        main={<PageBody />} 
        footer={<Footer />}/>
    </body>
  )
}

const root = document.getElementById('root')
ReactDOM.render(<App />, root)
```

