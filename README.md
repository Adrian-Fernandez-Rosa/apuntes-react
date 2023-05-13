
## ¿Qué es un SPA?

Una web SPA (single page applicattion) es una forma de desarrollo web en la que la página web está contenida en un único archivo HTML.

mientras se navega por la web, se irán solicitando contenidos al servidor.

De esta forma se mejoran los tiempos de respuesta y, por lo tanto, la experiencia de usuario.
Hay que hacer esfuerzos extras para aplicar SEO.

## ¿Qué es ReactJS?

React JS es una librería de JavaScript para crear interfaces de usuario.

Esta librería, (QUE NO ES UN FRAMEWORK), fue creada por Facebook en 2013.
Es de código abierto.

React también es famoso por otra serie de características:

* Velocidad
* Componentes
* Desarrollo Declarativo
* Anidación de Componentes (componentes de orden superior y de orden inferior) 
* Isomorfismo
* Agilidad de Desarrollo


 ### Velocidad:

Uno de los aspectos que más destacan de React es su velocidad de renderizado.

Esto lo consigue trabajando sobre un DOM Virtual sobre el que aplica los cambios que sufra la aplicación y luego actualiza únicamente los elementos que se hayan modificado.

### Componentes

docs react: "Los componentes permiten separar la interfaz de usuario en piezas independientes, reutilizables y pensar en cada pieza de forma aislada. "

Al trabajar con componentes estamos forzando nuestro desarrollo a ser más mantenible.

React nos proporciona varios tipos de componentes (Puros, de contenedor, de clase, de función, etc). con los que facilitar su reutilización en todos nuestros proyectos,tanto dentro como entre ellos.
A estos componentes se le puede pasar información a travez de lo que son las props.

### Anidación (de componentes)

Los componentes pueden ser *anidados*, de forma que los componentes de orden superior propagan datos a los de orden inferior.
La comunicación entre ellos es **unidireccional** y se usan los **eventos** para que los componentes inferiores sean **reconocidos** por los de orden superior.

En la Jerarquia haremos pasar la información desde arriba hacia abajo (pasar objetos, datos), Y los eventos suelen ser de abajo hacia arriba.

<p align="center">
  <img src="imagenes/Jerarquia1.png" alt="Jerarquia1">
</p>

### Declarativa

React sigue el paradigma del **desarrollo declarativo.**

Las aplicaciones que creemos estarán formadas por componentes.
Tanto la aplicación global como cada componente tiene un estado propio, y es por este motivo que React es declarativo.

Con Javascript puro (vanilla) se trabaja creando scripts que informan al DOM de qué debe realizar o cómo hacerlo: Se está siguiendo un paradigma imperativo.

Sin embargo, esta librería trabaja sobre el estado global de la aplicación y responde a los cambios de cada componente en su estado por separado, actualizando únicamente lo necesario.

### Isomorfismo

React permite el isomorfismo, también conocido como JS Universal, capacidad con la que podemos redenrizar tanto en servidor como en cliente.

Esto hace que solucione problemas y mejore el posicionamiento.

### Agilidad

Con ReactJS disponemos de todas las funcionalidades que nos ofrece jQuery.

Ambas tecnologías pueden convivir, aunque no es necesario tener que usar JQuery en nuestros proyectos.

***

React está basado en el uso de eventos asíncronos y en él destaca el uso de HTTP, lo que lo hace perfercto para trabajar con librerías o frameworks web.

*** 

## create-react-app

En la actual documentación de react es evidente la falta de mención de create-react-app. Si bien es funcional, la documentación recomienda usar herramientas alternativas por lo que en mi opinion personal y solo para esta ocasión me quedo con VITE. Para mis emprendimientos tengo pendiente de analizar Gatsby, Remix.




