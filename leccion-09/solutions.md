## Renderiza una lista de elementos

En este ejercicio combinarás conocimientos ya adquiridos para crear una lista de elementos con estilos diferentes

```js
const root = document.querySelector('#root')

const Ul = ({ children, clase, lista}) => {
    return (
        <ul className={clase}>
            {lista.map(item => <Item>{item}</Item>)}
        </ul>
    )
}

const Item = ({ children }) => {
    return <li style={{fontSize: '18px'}}>
        {children}
    </li>
}

const List = ({items}) => {
  return (<Ul lista={items} class="list" />)
}

const data = [
  'Primer Item',
  <strong>Segundo Item</strong>,
  <em>Tercer Item</em>,
]

const App = () => {
  return <List items={data} />
}
ReactDOM.render(<App />, root)
```

## Utiliza diferentes tamaños de fuentes 

Para completar este ejercicio, harás uso de `Array.map` para recorrer el arreglo de elementos y usarás el segundo argumento del callback de map para accedder al indice del elemento y usarlo como `key`

También modificarás el componente Item para aceptar un estilo como prop.

Finalmente el componente `Ul` recibirá una cuerta prop con un arreglo de los diferentes tamaños de fuentes que puede usar lo pasará al `Item`.

```js
const root = document.querySelector('#root')

const Ul = ({ children, clase, lista, fontSizes}) => {
    return (
        <ul className={clase}>
            {lista.map((item, index) => <Item key={index} style={{fontSize: fontSizes[index]}}>{item}</Item>)}
        </ul>
    )
}

const Item = ({ children, style }) => {
    return <li style={style}>
        {children}
    </li>
}

const List = ({items}) => {
    const fontSizes = ['16px','20px','24px']
  return (<Ul lista={items} class="list" fontSizes={fontSizes}/>)
}

const data = [
  'Primer Item',
  <strong>Segundo Item</strong>,
  <em>Tercer Item</em>,
]

const App = () => {
  return <List items={data} />
}
ReactDOM.render(<App />, root)
```