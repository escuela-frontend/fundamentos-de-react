El primer ejercicio es encontrar componentes en un interfaz. Y para ello, vamos a revisar una interfaz conocida para encontrar dichos componentes.

Usaremos la interfaz de Twitter como modelo. Vamos a empezar dividiendo esta interfaz en diferentes componentes.

Comencemos con esta área de texto. Podemos ver un componente que incluye el avatar del usuario y el área de escritura.

También dibujaremos un cuadro para todo el contenedor y luego para los iconos que actúan como la caja de herramientas y el botón de Tweet.

Moviéndonos a la derecha, podemos ver una columna que se compone al menos de dos componentes:

- la lista en el cuadro de búsqueda.
- El componente del Tweet real construido por otras piezas como el contenido del texto de la vista previa de la imagen y el avatar.

Nuevamente, Esto es particularmente interesante, ya que la avatar es un componente que se usa en toda la aplicación.

La pieza de la avatar aquí es en realidad el mismo componente en todas partes.

Lo que acabamos de ver es como dividir un interface en varios componente. Incluso montar nombres a cada uno de estos componentes para ayudarnos a crear el modelo mental de la interfaz usuario e identificar los componentes compartidos.

Aún más, la notación utilizada aquí para el nombre es como un elemento HTML.

Esto será útil más adelante cuando nos sumergimos en JSX.

Como resumen, necesitamos ver cualquier interfaz e identificar rápidamente los componentes que la construyen para comprender, asi, como interactúan dichos componentes y que se puede compartir.
