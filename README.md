
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

## create-vite

```bash
npm install -g create-vite
```

Creando proyecto
```bash
create-vite my-react-project --template react

cd my-react-project
npm run dev

```


## TEORIA REACT

En react hay 2 tipos de componentes.

* Componentes de clase (Class Components)

Componentes de Clase (Class Components): Antes de la introducción de Hooks en React 16.8, los componentes de clase eran la única forma de tener estado y ciclo de vida en tus componentes. Un componente de clase se define como una subclase de React.Component, y tiene métodos de ciclo de vida como componentDidMount, componentDidUpdate, y componentWillUnmount. Aquí tienes un ejemplo de un componente de clase:


```jsx

import React from 'react';

class MyClassComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { counter: 0 };
  }

  componentDidMount() {
    // Aquí puedes hacer algo cuando el componente se monta en el DOM
  }

  render() {
    return <div>{this.state.counter}</div>;
  }
}

```

* Componentes Funcionales (Function Components)

Estos componentes son simplemente funciones JavaScript que devuelven JSX. Antes de la introducción de Hooks, los componentes funcionales eran "tontos" y no podían tener estado ni métodos de ciclo de vida. Pero con la introducción de Hooks como useState y useEffect, ahora puedes tener estado y efectos secundarios en tus componentes funcionales. Aquí tienes un ejemplo de un componente funcional con Hooks:

```typescript
import React, { useState, useEffect } from 'react';

function MyFunctionComponent() {

   // Breve introducción a useState
    /**
     * const [variable, método para actualizar] = useState(valor inicial);
     * (useState es método hook)
     */
  const [counter, setCounter] = useState(0);

  useEffect(() => {
    // Aquí puedes hacer algo cuando el componente se monta o se actualiza
  }, []);

  return <div>{counter}</div>;
}
```

# Estructura de un proyecto

Las carpetas que nombro estan todas dentro de src

- **src**: Esta es la carpeta raíz de tu código fuente. Todos los componentes, hooks, modelos, estilos y cualquier otro código que escribas para tu aplicación estarán dentro de esta carpeta.

- **src/components**: Esta carpeta contiene todos los componentes de React que se utilizan en tu aplicación. Los componentes son los bloques de construcción en React y esta carpeta los agrupa en un solo lugar.
    - **src/components/pure**: La subcarpeta "pure" puede contener componentes que son "puros", lo que significa que siempre renderizan la misma salida para las mismas props y estado. Estos componentes no tienen efectos secundarios y no dependen de nada más que de sus props y estado. Por lo general, son componentes funcionales que no usan hooks como `useEffect`.
        - **src/components/pure/forms**: La subcarpeta "forms" dentro de "pure" podría contener componentes que representan formularios o elementos de formulario, como inputs, botones y selects. Estos componentes serían puros y no tendrían efectos secundarios.
    - **src/components/container**: La subcarpeta "container" puede contener componentes que se conectan a tu estado global (como Redux) o que manejan la lógica de la aplicación. Estos componentes "envuelven" o contienen otros componentes y les proporcionan las props que necesitan.

- **src/hooks**: Esta carpeta puede contener hooks. Los hooks son funciones que permiten a los componentes funcionales utilizar estado y otras características de React que antes solo estaban disponibles en componentes de clase.

- **src/models**: La carpeta "models" puede contener modelos de datos y funciones relacionadas con la lógica de negocio. Estos modelos podrían representar objetos del dominio de la aplicación, como usuarios, productos o pedidos, y las funciones asociadas para manipular y gestionar estos objetos.

- **src/styles**: Esta carpeta puede contener archivos de estilos CSS, SCSS, o cualquier otro sistema de estilos quese esté utilizando en tu proyecto. Aquí podrías almacenar estilos globales, variables de colores, fuentes y otros estilos compartidos en toda la aplicación.

- **src/routes**: Esta carpeta puede contener tu configuración de enrutamiento. En una aplicación de React, puedes utilizar bibliotecas como `react-router-dom` para definir múltiples rutas (como `/`, `/about`, `/contact`, etc.) y especificar qué componente se debe renderizar para cada ruta.
