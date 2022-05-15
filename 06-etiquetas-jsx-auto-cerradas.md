# **Aprende sobre las etiquetas JSX auto-cerradas**

Hasta ahora, has visto cómo **JSX** difiere de **HTML** de una manera clave con el uso de *``className``* vs. *``class``* para definir clases **HTML**.

Otra forma importante en la que **JSX** está en la idea de la etiqueta de auto-cierre.

En **HTML**, casi todas las etiquetas tiene una etiqueta de apertura y cierre: *``<div></div>``*; la etiqueta de cierre siempre tiene una barra inclinada antes del nombre de la etiqueta que está cerrando. Sin embargo, hay instantcias especiales en **HTML** llamadas "*etiquetas auto-cerradas*", o etiquetas que no requieren una etiqueta de apertura y cierre antes de que otra etiqueta pueda comenzar.

Por ejemplo, la etiqueta de salto de linea puede escrbirse como *``<br>``* o como *``<br />``*, pero nunca debe escribirse como *``<br></br>``*, ya que no contiene nungún contenido.

En **JSX**, las reglas son un poco diferentes. Cualquier elemento **JSX** se puede escribir con una etiqueta de *auto-cierre*, y cada elemento deve ser cerrado. La etiquetade salto de línea, por ejemplo, siempre debe escribirse como *``<br />``*  para ser un **JSX** válido que puede ser transpilado. Por otra parte, un *``<div>``* puede escribirse como *``<div />``*. Verñas en desafíos posteriores que esta sintaxos es útil al renderizar componentes de React.

### *Ejemplo práctico*:
```JavaScript
const JSX = (
  <div>
    <h2>Welcome to React!</h2> <br />
    <p>Be sure to close all tags!</p>
    <hr />
  </div>
);
```