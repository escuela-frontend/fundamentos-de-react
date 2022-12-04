## Usar props en los componentes hijos

Ahora que ya sabes usar composición para pasar componentes como props: ¿Cómo puedes darle props a esos componentes hijos?

> Es importante notar aqui una nueva sintaxis `<></>` esta es un atajo para escribir `<React.Fragment></React.Fragment>`.
> Este componente `Fragment` te permite anidar componentes sin necesidad de renderizar un contendor como un `div`

```js
// 💡 Estos son los componentes bases que usarás para completar el ejercicio
// la idea es que puedas crear una interfaz usando estos componentes y la técnica de
// composición
const NavBar = () => {
  return <h2>Barra de navegacion</h2>
}

const PageBody = ({title, content}) => {
  return (
    <>
        <h1>{title}</h1>
        <p>{content}</p>
    </p>
  )
}

const Footer = ({content}) => {
  return <h3>{content}</h3>
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
    const title = 'Este es el títutlo'
    const mainContent = 'Contenido del Main'
    const footerContent = 'Contenido del Footer'
    return (
        <body>
        <Page 
            nav={<NavBar />}
            main={<PageBody title={title} content={mainContent}/>} 
            footer={<Footer content={footerContent}/>}
        </body>
    )
}

const root = document.getElementById('root')
ReactDOM.render(<App />, root)
```