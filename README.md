# Fundamentos de React

En este tutorial aprenderás los diferentes conceptos base que fundamentan el cómo y por qué de ciertas prácticas en React. Revisaremos que necesidad viene a cubrir, desde donde nace su API, el uso de JSX, como manejar estilos, eventos y estado de un componente

## ✨ Resumen de lo que aprenderás

Ok. ¿listo y ansioso de aprender?, genial, este será un viaje divertido y lleno de desafíos. Algunas de las cosas que podrás aprender serán:

- Pensando en React
- Como configurar una app React desde cero y de forma estática.
- ¿Por que usamos JSX?
- ¿Qué es un componente? y como pensar en términos de componentes.
- Como crear componentes utilizando React y JSX.
- Cómo manejar estilos en tu aplicación.
- Cómo renderizar listas de datos y que es la prop key.
- Cómo manejar formularios y eventos mendiante manipulación del estado.

## 👨🏻‍💻 ¿Quién soy?

Soy [Matías Hernández](https://matiashernandez.dev), padre, desarrollador, podcaster, escritor e instructor.

Desde hace mucho tiempo (antes de que jQuery existiese) que escribo software y durante todos esos años el desarrollo web ha sido mi pasión. En los últimos 10 años he trabajado oficial y profesionalmente como Ingeniero de Software para diferentes proyectos. Durante esos años he recolectado muchas ideas, conceptos y conocimientos que intento destilar en diferentes formatos para ayudar a otros desarrolladores a mejorar su carrera.

Me encanta lo que hago y trato de traer la misma pasión a la creación de contenido por medio de cursos en [egghead.io](https://matiasfha.dev/egghead), artículos en [FreeCodeCamp](https://matiasfha.dev/fcces), [mi blog](https://matiashernandez.dev), [Cloudinary](https://mediajams.dev/author/matias-hernandez) y otras publicaciones, en mis podcasts [Café con Tech](https://www.cafecon.tech/) y [Control Remoto](https://www.controlremoto.io/) y en mis [cursos via email](https://microbytes.dev).

Puedes encontrarme en twitter como [@matiasfha](https://twitter.com/matiasfha)

## ⏰ Antes del tutorial

¿Que necesitas saber para iniciar tu camino con React?

Primero, y por sobre todo, necesitas conocer conceptos fundamentales sobre desarrollo web y sobre todo tener conocimientos sobre Javascript moderno o avanzado. Durante tu trabajo con React verás mucho ideas y conceptos como:

- Destructuring.
- Spread.
- Ternaries.
- [Closures.](https://www.freecodecamp.org/espanol/news/que-es-un-closure-en-javascript/)
- Parámetros por defecto.
- [Arrow functions.](https://escuelafrontend.com/articulos/arrow-functions)
- [Métodos de arreglos.](https://escuelafrontend.com/articulos/metodos-de-arreglos)
- Promesas, async/await.

Te invito a revisar tus conocimientos en esas áreas para que puedas sacar el máximo provecho a este tutorial.

Puedes revisar mi newsletter [Microbytes](https://microbytes.dev) y unirte al curso Javascript para React donde encontrarás más material al respecto.

## 🛠 Requerimientos

> ❗ Cada ejercicio contiene una inserción de Stackblitz que puede usar si prefiere no instalar este repositorio localmente.

Si prefieres installar este repositorio localmente por favor realiza los siguientes pasos antes de iniciar:

### Requerimientos del sistema

- [git](https://git-scm.com/) v2.13 o superior
- [NodeJS](https://nodejs.org/) `12 || 14 || 15 || 16`
- [npm](https://www.npmjs.com/) v6 o superio

Estas herramientas deben ser parte de tu sistema, para verificar puedes ejecutar en la terminal

```shell
git --version
node --version
npm --version
```

### Configuración

> Si gustas, puedes hacer un fork de este repositorio para poder ir "guardando" tu progreso.

- [ ] Clona este repositorio, en la terminal ejecuta:

```shell
git clone https://github.com/matiasfha/tutorial-react-desde-cero.git
```

- [ ] Instala las dependencias

```shell
cd tutorial-react-desde-cero
npm install
```

> Esto puede tardar unos minutos dependeniendo de tu conexión.

Si tienes algún error durante este proceso por favor [completa un issue](https://github.com/matiasfha/tutorial-react-desde-cero/issues/new) en el reposotiorio. Escribe en el toda la información de los pasos realizados y el resultado del script que ejecutaste

### Ejecutando los ejercicios

Para ejecutar los ejercicios, una vez que tienes los pasos anteriores listos, solo debes abrir la terminal y ejecutar

```shell
npm run dev
```

Esto te mostrará una lista de opciones con el nombre de la lección. Selecciona la que corresponda y luego visita `http://localhost:3000` en tu navegador.

> Para terminar el proceso y cambiar de lección solo presiona CTRL-C, esto detendrá el script y podras ejecutarlo nuevamente

- [ ] Ten listo tu editor de código favorito para resolver los ejercicios

### ❓ ¿Cómo ejecutar las lecciones?

Cada lección "vive" dentro de su propio directorio dentro de este monorepo, para ejecutar el ejercicio de una lección en particular sólo debes, desde la terminal, ejecutar `npm run dev`. Esto te mostrará una lista de las lecciones donde podrás seleccionar utilizando el teclado.

## 📝 Sobre el tutorial

### Estructura de las lecciones

Cada concepto o contenido esta encapsulado en su propia lección y cada lección tiene su propio directorio con recursos, ejemplos de código y desafíos.

En cada directorio encontrarás un nuevo archivo README.md, en el encontrarás una descripción de lo que encontrarás en la lección e instrucciones para llevar a cabo los ejercicios, desafíos o cuestionarios.

Además encontrarás la configuración necesaria para ejecutar el proyecto que te permitirá resolver los ejercicios.

### Ejemplos de Ejercicios

Los ejercicios consisten en el desarrollo y solución de una problemática asociada al concepto que estás aprendiendo en la lección. Esto implica, que el código tendrá pistas y guías para que te mantengas enfocado en el tema correspondiente.

Para esto encontrás comentarios y emojis que te ayudarán en el camino.

- 💡: Indica el contenido del ejercicio.
- 🏋️‍♂️: Indica el ejercicio en particular.
- 🍬: Desafío o crédito extra.

### Listado de lecciones

- [00 - Introducción](./leccion-00/README.md)
- [01 - Componentes](./leccion-01/README.md)
- [02 - Creando una app estática base ](./leccion-02/README.md)
- [03 - El mundo sin JSX](./leccion-03/README.md)
- [04 - Conociendo JSX](./leccion-04/README.md)
- [05 - Props](./leccion-05/README.md)
- [06 - Renderizado Condicional](./leccion-06/README.md)
- [07 - Composición](./leccion-07/README.md)
- [08 - Arrays](./leccion-08/README.md)
- [09 - Estilos](./leccion-09/README.md)
- [10 - Eventos](./leccion-10/README.md)
- [11 - Formularios: Componentes Controlados](./leccion-11/README.md)
- [12 - Formularios: Componentes No-Controlados](./leccion-11/README.md)
- [13 - Construyendo una interfaz](./leccion-11/README.md)
