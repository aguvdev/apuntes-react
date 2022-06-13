# Conceptos básicos

### **Componente**:


Es una parte de la interfaz de usuario (lo que el usuario ve cuando accede a la aplicación web) que es independiente y reusable. Es independiente porque cada componente va a tener un cierto estado y una funcionalidad específica, y ese estado y esa funcionalidad va a ser independiente de otros componentes, además es reutilizable porque podemos reutilizar el componente varias veces, lo definimos o lo escribimos una vez y podemos utilizarlo muchas veces si lo necesitamos en nuestra app.

Los **componentes** se pueden dividir en dos categorias principales: **funcionales** y **de clase**.

## **Componentes funcional**:

Es una funcion de JS que retorna una función de **_React (JSX)_**. Un elemento que vamos a escribir en una sintaxis extendida de **_JS_** que se llama **_JSX_**; va a ser como una descripción similar a **_HTML_** que queremos que represente esa función

Ejemplo:

```JavaScript
function Saludo(props) {
    return <h1>¡Hola, {props.nombre}!</hi>;
}
```

### Características:

- Debe retornar un elemento de **_React (SJX)_**.
- Debe comenzar con una letra mayúscula.
- Puede recibir valores si es necesario.

#### Que son los **props**:

Argumentos que puede recibir un componente de **_React_**.

> Los **props** solo pueden ser enviados de "padre a hijo".

---

## **Componente de Clase**:

Clase de ES6 (JavaScript moderno) que retorna un elemento JSX.

Ejemplo:

```JavaScript
class Saludo extends React.Component {
    render() {
        return <h1>¡Hola, {this.props.nombre}!</h1>
    }
}
```

### Características:

- Debe extender **React.Component**.
- Debe tener un método **render()** para retornar un elemento **_JSX_**.
- Puede recibir valores si es necesario.

## Método _render()_:
- Método que retorna la estructura del componente en **_JSX_**.

- Es el único método obligatorio para un componente de clase en **_React_**.

```Javascript
class NombreComponente extends React.Component {
    render() {
        return <p>Mi componente</p>
    }
}
```

## _Estados (State)_:

Representación en **_JS_** del conjunto de propiedades de un componente y sus valores actuales.

> En este concepto, "propiedades" **no** se refiere a los props, sino a información que se representa sobre el componente.

---

## _¿Porque componentes de clase?_

Anteriormente, usábamos componentes de clase para poder trabajar con "_estados_" de nuestros componentes.

En versiones anteriores de React (_anteriores a 16.8_), **no** podíamos hacerlos en componentes funcionales.

Ahora sí podemos asignar y actualizar el estado de un componente funcional en React con los **Hooks**.

## ¿Son releveantes?
La respuesta corta es: ¡Si!

### **Claves**:

> - "**No** hay planes para eliminar las clases de **_React_**".
> - "**No** hay prisa por migrar a los **_Hooks_**".
> - Pretendemos que **_Hooks_** cubra todos los casos de uso existentes para las clases, pero seguiremos soportando los componentes de clase en un futuro previsible".

### **_props_**:
Los componentes de clases también pueden recibir **_props_**.

Para acceder a un **_prop_**:
```Javascript
this.props.nombreDelProp
```

Ejemplo:
```Javascript
class Saludo extends React.Component {
    render() {
        return <h1>¡Hola, {this.props.nombre}!</h1>;
    }
}
```

### **_this_** en Componentens de Clase:
**_this_** se refiere al componente actual.

### **Constructor**:
Método usado para inicializar el estado de un componente de React.

Es llamado automáticamente cuando se crea el componente.

**Ejemplo**:
```Javascript
class Tarea extends React.Component {

    constructor() {
        super();
        this.state = {completada: true}
    }

    render() {
        return <p>Mi tarea</p>
    }
}
```
- Debe llamara a **_super()_** para heredar todas las funciones de su componente "padre" (React.Component).

### **_props_** en el Constructor:
Si el componente tiene un método constructor y recibe props deben ser pasados al **_constructor_** y a **_super()_**.

**Ejemplo**:
```Javascript
class Tarea extends React.Component {

    constructor(props) {
        super(props);
    }

    render() {
        return <p>Mi tarea</p>
    }
}
```

### Estado en el **constructor**:
El objeto "**_state_**" (estado) se inicializa en el **_constructor_**.

**Ejemplo**:
```Javascript
class Tarea extends React.Component {

    constructor() {
        super();
        /* --------------------------------------------- */
        this.state = {completada: true}/* this es el objeto del state(estado), y a ese objeto le vamos el objeto inical: la propiedad {completada: true} */
        /* --------------------------------------------- */
    }

    render() {
        return <p>Mi tarea</p>
    }
}
```
Puede tener varias propiedades separadas por comas.

**_Ejemplo_**:
```Javascript
class Tarea extends React.Component {

    constructor(props) {
        super(props);
        /* ------------------ */
        this.state = {
            completada: true,
            color: azul,
            prioridad: 1
        };
        /* ------------------ */
    }

    render() {
        return <p>Mi tarea</p>
    }
}
```

### Accediendo al **_state_**(estado):
```Javascript
this.state.propiedad
```

**_Ejemplos_**:
```Javascript
class Tarea extends React.Component {

    constructor(props) {
        super(props);
        /* ------------------ */
        this.state = {
            completada: true, /* => this.state.completada */
            color: azul, /* => this.state.color */
            prioridad: 1 /* => this.state.propiedad */
        };
        /* ------------------ */
    }

    render() {
        return <p>Mi tarea</p>
    }
}
```

**dentro de la clase**:
```Javascript
class Tarea extends React.Component {
    
    constructor(props) {
        super(props);
        this.state = {
            completada: true,
            color: azul,
            prioridad: 1
        };
    }

    render() {
        return <p>Mi tarea tiene prioridad: {this.state.prioridad}</p>
    }
}
```

### Actualizando el estado:
Para actualizar una o más propiedades del objeto "**_state_**", se llama a **_this.setState()_**.
Y se pasa como argumento un objeto con las propiedades que se van a actualizar y sus nuevos valores.

```Javascript
this.setState({
    completada: false,
    color: verde
});
```

### Métodos de Ciclos de Vida:
Métodos **especiales** de **_React_** usados para realizar **operaciones con componentes** en momentos específicos de su vida en el **DOM**.

---

## **Hooks**

Función especial que te permite trabajar con estados en componentes funcionales y otros aspectos de React.

---

## **Event Listener**

Función en JavaScript que es ejecutada cuando ocurre un evento específico.

> También podemos referirnos a esta función como "_Event Handler_".

---

## **Introducción a JSX**

## **JSX**:

Extensión de React para la sintaxis de JavaScript.

> JSX = JavaScript XML.

Nos permite describir en JavaScript cómo se verán los componentes usando una estructura similar a **HTML**.

> Su estructura (no necesariamente su estilo).

---

## Ventajas de JSX

- Estructura más fácil de visualizar.
- Errores y advertencias más útiles.
  > JSX es opcional, pero altamente recomendado.

Ejemplo de JSX:

```JavaScript
const elemento = <h1>¡Hola, mundo!</h1>;
```

---

Ejemplo Componente:

```JavaScript
import React from 'react';
import '../css/Contador.css';

function Contador({ numClics }){
    return (
        <div className="contador">
            {numClicks}
        </div>
    );
}

export default Contador;
```

```JavaScript
import React from 'react';
import '../css/Contador.css';

const BotonClear = (props) => (
    <div className="boton-clear">
        {props.children}
    </div>;
);

export default BotonClear;
```

---

## **Elementos en JSX**

## Elemento:

Unidades más pequeñas en React. Definen lo que se ve en la pantalla.

---

### **Elementos vs Componente**:

Los componentes en React estan "hechos" de elementos.

---

## **Como mostramos los elementos en HTML**:

```HTML
<div id="root"></div>
```

**_root_** significa raíz, es como el elemento principal que va a contener a toda nuestra app.

Esa app se va a color dentro de:

> id="root"

dentro del div, gracia al _id root_.

Todo este proceso de incersión de la app, va a estar manejado por React DOM.

## **React DOM**

Paquete que facilita la interacción y actualización del DOM en aplicaciones React.

## ¿Que es DOM?

Es Document Object Model. Es básicamente la representación en el navegadro de todos los elementos que conforman una página o aplicación web.


Elementos
---
>Con JSX, puedes crear y usar cualquier elemento HTML.

>En **JSX**, los **elementos** HTML se representan con etiquetas en letras **minúsculas**.

>Los **componentes** definidos por el usuario comienzan con una letra **mayúscula**.

Atributos:
---
>Puedes agregar **atributos** a tus elementos en JSX para especificar ciertas características.

>Pero... algunos se escriben de forma distinta si los comparamos con HTML.


Cambios en los nombres de los atributos:


HTML:

```HTML
<div class="css"></div>
<label for="css"></label>
```

JSX:

```HTML
<div className="css"></div>
<label htmlFor="css"></label>
```


Para agregar estilos si hay cambios importantes

>El atributo **style** acepta un objeto de JavaScript con propiedad CSS escritas en **camelCase**.

Por ejemplo:

| Css | JSX |
|-----|-----|
|background-image|backgroundImage|
|background-color|backgroundColor|
|font-family|fontFamily|


```JavaScript
const estiloDiv = {
    color: 'yelow';
    backgroundColor: 'black';
}
```

```HTML
<div className={estiloDiv}>¡Hola, mundo!</div>
```

Otra alternativa:

```
<div style={{color: 'yellow'}}>¡Hola, mundo!</div>
```

esto se hace cuando hay pocos estilos.

---

## **Estructura**


>Al igual que en HTML, los elementos pueden ser **anidados** en JSX para formar estructuras más complejas.

```JavaScript
return (
    <div className="app">
        <div className="ffCodeCamp">
            <img
                src={freeCodeCampImage}
                className="ffCoCamp"
                alr="Logo"
             />
        </div>
        <div className="contenedor-calculadora">
            <Pantalla input={input} />
            <div className="fila">
                <Boton manejarClic={agregarInput}>1</div>
                <Boton manejarClic={agregarInput}>2</div>
                <Boton manejarClic={agregarInput}>3</div>
                <Boton manejarClic={agregarInput}>4</div>
            </div>
            <Pantalla input={input} />
            <div className="fila">
                <Boton manejarClic={agregarInput}>1</div>
                <Boton manejarClic={agregarInput}>2</div>
                <Boton manejarClic={agregarInput}>3</div>
                <Boton manejarClic={agregarInput}>4</div>
            </div>
        </div>
    </div>
)
```

Renderizar Componentes:
---

```JavaScript
const elemento = <h1>¡Hola!</h1>

ReactDOM.render(
    elemento,
    document.getElementById('root')
)
```

* Primer argumento es el elemento a renderizar, y el segundo es la raíz.

* Para poder usar **ReactDOM** tenemos que importarlo a nuestro documento:

```JavaScript
import ReactDOM from 'react-dom';
```

### **Self-Closing Tags**:

Elementos que solo posee una etiqueta de apertura ya que no contiene texto u otros elementos.

Ejemplo:

```HTML
<img src="logo.png" alt="Mi imagen" />
```

### **JavaScript en JSX**:

```JavaScript
const adjetivo = "Interesante";

<p>React es {adjetivo}</p>
```

Puede escribir cualquier expresión válida de JavaScript entre las llaves y su valor será reemplazado.

```JavaScript
let nombre = "Gino";

<p>Su nombre es: {nombre.toUpperCase()}</p>
```

**Fin (ahre que no sé)**.