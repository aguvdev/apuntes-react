# **Define una clase HTML en JSX**

Ahora que te sientes cómodo escribiendo **JSX**, te preguntarás cuanto difiere de **HTML**.

Hasta hoara, se puede parecer que **HTML** y **JSX** son exactamente iguales.

Una diferencia clave en **JSX** es que ya no puedes usar la palabra *``class``* para definir clases **HTML**. Esto es debido a que *``class``* es una **palabra reservada en JS**. En su lugar, **JSX** utiliza *``className``*.

De hecho, la convención de nomenclatura para todos los atributos **HTML** y referencias a eventos en **JSX** se convierte a **camelCase**. Por ejemplo, un evento de clic en **JSX** es *``onClick``*, en lugar de *``onclick``*. Del mismo modo, *``onchange``* se convierte en *``onChange``*. Si bien se trata de diferencias sutil, es importante tenerlo en cuenta de ahora en adelante.

### *Ejemplo práctico*:
```JavaScript
const JSX = (
  <div className="myDiv">
    <h1>Add a class to this div</h1>
  </div>
);
```