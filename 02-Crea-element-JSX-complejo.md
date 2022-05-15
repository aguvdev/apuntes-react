# Crea un elemento JSX complejo
* Una cosa importante sobre JSX anidado es que debe devolver un solo elemento.
* Este elemento principal contendría a todos los demás niveles de elementos anidados.
* Por ejemplo, varios elementos JSX escritos al mismo nivel sin elemento contenedor principal no se transpilarán.
* Aquí va un ejemplo:

    * **JSX válido:**
    ```html
    <div>
        <p>Párrafo Uno</p>
        <p>Párrafo Dos</p>
        <p>Párrado Tres</p>
    </div>
    ```
    * **JSX inválido**
    ```html
    <p>Párrafo Uno</p>
    <p>Párrafo Dos</p>
    <p>Párrafo Tres</p>
    ```

### Ejemplo práctico:
```JavaScript
const JSX = (
  <div>
    <h1>This is a block of JSX</h1>
    <p>Here's a subtitle</p>
  </div>
);
```