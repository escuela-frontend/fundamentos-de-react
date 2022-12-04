## Permite que `Item` reciba una prop para modificar la clase base


Aquí lo que buscas es poder mezclar diferentes estilos de un compomente utilizando props

Finalmente simplificarás el componente `Ul` para renderizar sólo la prop `children`y el manejo de estilos se hará directamente en el componente `List`

```js
const root = document.querySelector('#root')

const Ul = ({ children, clase}) => {
    return (
        <ul className={clase}>
            {children}
        </ul>
    )
}

const Item = ({ children, style }) => {
    const classNames = `item item--${color}`
    return <li style={style} className={classNames}>
        {children}
    </li>
}

const List = ({items}) => {
    const fontSizes = ['16px','20px','24px']
    const colors = ['red','blue','purple']
  return (<Ul lista={items} 
    class="list">
        {items.map((item, index) => 
            <Item 
                key={index}
                style={{fontSize: fontSizes[index]}}
                colors={colors[index]}>
                {item}
            </Item>
        )}
    </Ul>)
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