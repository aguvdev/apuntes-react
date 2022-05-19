# ¿Qué es React?

* React es una librería (o biblioteca) de vistas de código abierto* creada y mantenida por Facebook. Es una gran herramienta para hacer la interfaz de usuario (UI) de aplicaciones web modernas.
    - Biblioteca o libreria: es un conjunto de implementaciones o subprogramas que podemos usar en nuestro código. Básicamente son como herramientas que otros devs ya han desarrollado para nosotros.
---

* React usa una extensión de sintaxis de JavaScript llamada JSX que te permite exribir HTML directamente dentro de JavaScript. Esto tiene muchos beneficios. Te permite utilizar el poder programático completo de JavaScript dentro de HTML que ya has aprendido. Sin embargo, hay algunas diferencias clave que se abordaran a lo largo de los desafíos.

* Por ejemplo, dado que JSX es una extensión sintáctica de JS, se puede escribir JS directamente dentro de JSX. Para hacer esto, simplemente incluye el código que deseas que sea tratado como JS entre llaves:

    ```JavaScript
    { 'esto se trata como codigo de JS' }
    ```

* Sin embargo, debido a que JSX no es JS válido, el código JSX debe ser compilado en JS. El transpilador ***Babel*** es una herramienta muy popular para este proceso.
---
```JavaScript
ReactDOM.render(JSX, document.getElementById('root'))
```
* Esta llamada de función es la que coloca tu JSX en la representación ligera del DOM de React. React entonces utiliza capturas instantáneas de su propio DOM para optimizar actualizando sólo partes específicas del DOM.

---
## Ventaja de aprender React:
* Fácil de aprender y usar.
* Componentes reutilizables.
* Crear aplicaciones dinámicas.
* Buen desempeño.
---
#### Esto imprime un titulo en el DOM.
```JavaScript
const JSX = <h1>Hello JSX</h1>;
```