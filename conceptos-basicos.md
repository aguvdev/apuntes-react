# Conceptos básicos

### Componente: 
Es una parte de la interfaz de usuario (lo que el usuario ve cuando accede a la aplicación web) que es independiente y reusable. Es independiente porque cada componente va a tener un cierto estado y una funcionalidad específica, y ese estado y esa funcionalidad va a ser independiente de otros componentes, además es reutilizable porque podemos reutilizar el componente varias veces, lo definimos o lo escribimos una vez y podemos utilizarlo muchas veces si lo necesitamos en nuestra app.

Los **componentes** se pueden dividir en dos categorias principales: **funcionales** y **de clase**. 


## Componentes funcional:

Es una funcion de JS que retorna una función de ***React (JSX)***. Un elemento que vamos a escribir en una sintaxis extendida de ***JS*** que se llama ***JSX***; va a ser como una descripción similar a ***HTML*** que queremos que represente esa función

Ejemplo:
```JavaScript
function Saludo(props) {
    return <h1>¡Hola, {props.nombre}!</hi>;
}
```

### Características:

* Debe retornar un elemento de ***React (SJX)***.
* Debe comenzar con una letra mayúscula.
* Puede recibir valores si es necesario.

#### Que son los **props**:
Argumentos que puede recibir un componente de ***React***.

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

* Debe extender **React.Component**.
* Debe tener un método **render()** para retornar un elemento ***JSX***.
* Puede recibir valores si es necesario.

*Estados (State)*:
---
Representación en ***JS*** del conjunto de propiedades de un componente y sus valores actuales.
> En este concepto, "propiedades" **no** se refiere a los props, sino a información que se representa sobre el componente.
---

*¿Porque componentes de clase?*
---
Anteriormente, usábamos componentes de clase para poder trabajar con "*estados*" de nuestros componentes.

En versiones anteriores de React (*anteriores a 16.8*), **no** podíamos hacerlos en componentes funcionales.

Ahora sí podemos asignar y actualizar el estado de un componente funcional en React con los **Hooks**.

---
**Hooks**
---
Función especial que te permite trabajar con estados en componentes funcionales y otros aspectos de React.

---

**Event Listener**
---
Función en JavaScript que es ejecutada cuando ocurre un evento específico.
> También podemos referirnos a esta función como "*Event Handler*".