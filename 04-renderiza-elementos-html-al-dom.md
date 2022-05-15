# **Renderiza** elementos **HTML** al **DOM**

Hasta ahora has aprendido que **JSX** es una **herramienta** conveniente para escribir **HTML legible** dentro de **JS**. Con **React**, podemos renderizar este **JSX** directamente al **DOM HTML** usando la **API** de renderizado de **React** conocida como **ReactDOM**.

### **ReactDOM**
**ReactDOM** ofrece un método simple para renderizar elementos **React** al **DOM** que se ve así:``
ReactDOM.render(componenteARenderizar, targetNode);``
* el primer argumento es el elemento o componente **React** que deseas renderizar.

* y el segundo argumento es el nodo **DOM** al que se quiere renderizar el componente.

como era de esperarse ``ReactDOM.render()`` debe llamarse después de las declaraciones de los elementos **JSX**, al igual que hay que **declarar** las variables **antes** de usarlas.

### Ejemplo práctico:
```JavaScript
const JSX = (
  <div>
    <h1>Hello World</h1>
    <p>Lets render this to the DOM</p>
  </div>
);

ReactDOM.render(JSX, document.getElementById('challenge-node'));
```