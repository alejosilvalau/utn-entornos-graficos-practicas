# Ejercicio 1: Responder 

## 1. Qué es CSS y para qué se usa?

CSS son las siglas de Cascade Style Sheet que traducido significa hojas de estilo en cascada.

Las hojas de estilo es una tecnología que nos permite controlar la apariencia de una página web. En un principio, los sitios web se concentraban más en su contenido que en su presentación. HTML no pone atención en la apariencia del documento, sino en la estructura.

CSS describe como los elementos dispuestos en la página son presentados al usuario. CSS es un gran avance que complementa el HTML y la Web en general. Con CSS podemos especificar estilos como el tamaño, fuentes, color, espaciado entre textos y recuadros así como el lugar donde disponer texto e imágenes en la página.


## 2. CSS utiliza reglas para las declaraciones de estilo, ¿cómo funcionan? 
Las reglas de declaración de estilo se componen de dos partes principales:
- *selector*: sirve para identificar el o los elementos HTML a los que se le aplicacará el estilo.
- *declaracion*: se compone de una o varias propiedades y sus valores correspondientes. Las propiedades son los aspectos visuales que se desean cambiar, como el color de fondo, el tamaño de fuente, la fuente y la altura de línea.

La sintaxis es la siguiente:

```html
<selector> {
  <declaracion>
}
```

## 3. Cuáles son las tres formas de dar estilo a un documento? 
Las tres formas más conocidas de dar estilo a un documento son las siguientes:

- Utilizando una hoja de estilo externa que estará vinculada a un documento a través del elemento <link>, el cual debe ir situado en la sección `<head>`.
- Utilizando el elemento `<style>`, en el interior del documento al que se le quiere dar estilo, y que generalmente se situaría en la sección `<head>`. De esta forma los estulos serán reconocidos antes de que la página se cargue por completo.
- Utilizando estilos directamente sobre aquellos elementos que lo permiten a través del atributo `<style>` dentro de `<body>`. Pero este tipo de estilo pierde las ventajas que ofrecen las hojas de estilo al mezclarse el contenido con presentación

## 4. Cuáles son los distintos tipos de selectores más utilizados? Ejemplifique cada uno. 
**Selector Universal:** 

- *Sintaxis:*
```css
* { 
  atributo: valor;
}
```

- *Ejemplo:* El estilo se aplicará a todos los elementos de la página.
```css
* { 
  color: grey; 
}
```

**Selector Etiqueta:**

- *Sintaxis:*
```css
* { 
  atributo: valor;
}
```

- *Ejemplo:* El estilo se aplicará a todos los elementos `<p>`.
```css
* { 
  color: grey; 
}
```

**Selector Clase:**

- *Sintaxis:*
```css
.clase { 
  atributo: valor; 
}
```

- *Ejemplo:* El estilo se aplicará a cualquier elemento que tenga la clase `.blend`.
```css
.blend {
  color: red;
}
```

**Selector Identificador:** El selector identificador utiliza el atributo id para seleccionar un elemento. Solo puede haber un elemento con un id dado en un documento.

- *Sintaxis:*
```css
#id {
  atributo: valor; 
}
```
- *Ejemplo:* El estilo se aplicará al elemento que tenga el id `#cent`.
```css
#cent {
  color: blue;
}
```

**Selector Descendiente:** Un elemento es descendiente de otro cuando se encuentra entre las etiquetas de apertura y de cierre del elemento padre.

- *Sintaxis:* El estilo se aplica sobre el selector `1..N`.
```css
selector1 selector2 selectorN {
  atributo: valor;
}
```

- *Ejemplo:* El estilo se aplica a todos los párrafos que se encuentren dentro de una etiqueta `div`.
```css
div p { 
  color: black;
}
```

**Combinacion de Selectores:** La combinación de selectores nos permite dar un estilo a todos los selectores indicados.

- *Sintaxis:* El estilo se aplica sobre los selectores indicados.
```css
selector1, selector2, selector3 {
  atributo: valor;
}
```
- *Ejemplo:* El estilo se aplica a todos los `div`'s y párrafos `p`.
```css
div, p {
  color: orange;
}
```

**Selector de Hijos:** Se usa para seleccionar un elemento que es hijo de otro elemento.

- *Sintaxis:* El estilo se aplica sobre el selector 2.
```css
selector1 > selector2 {
  atributo: valor;
}
```

- *Ejemplo:* El estilo se aplica a todos los párrafos que sean hijos de un `div`.
```css
div > p {
  color: white;
}
```

**Selector Adyacente:** Se usa para seleccionar elementos que son hermanos, es decir, su elemento padre es el mismo y están seguidos en el código HTML.

- *Sintaxis:* El estilo se aplica al `selector 2`.
```css
selector1 + selector2{ 
  atributo: valor; 
}
```

- *Ejemplo:* El estilo se aplica a todos los párrafos que sean hermanos de un `div`.
```css
div + p { 
  color: black;
} 
```

## 5. Qué es una pseudo-clase? Cuáles son las más utilizadas aplicadas a vínculos?
Una pseudoclase CSS es una palabra clave que se añade a los selectores y que especifica un estado especial del elemento seleccionado. Por ejemplo, `:hover` aplicará un estilo cuando el usuario haga hover sobre el elemento especificado por el selector.

Las pseudoclases, junto con los pseudoelementos, permiten aplicar un estilo a un elemento no sólo en relación con el contenido del árbol de documento, sino también en relación a factores externos como el historial del navegador (`:visited`, por ejemplo), el estado de su contenido (como `:checked` en algunos elementos de formulario), o la posición del ratón (como `:hover` que permite saber si el ratón está encima de un elemento o no).

## 6. Qué es la herencia? 
La herencia en CSS es un mecanismo mediante el cual las propiedades de estilo aplicadas a un elemento se transmiten a sus elementos hijos. Esto significa que, si se define una propiedad de estilo en un elemento padre, todos los elementos hijos van a heredar esa propiedad a menos que se especifique lo contrario.


Por ejemplo, si se define un color de texto en un elemento padre `<div>`, todos los elementos `<p>` que estén dentro de ese `<div>` heredarán ese color de texto a menos que se especifique un color diferente para los elementos `<p>`.


Sin embargo, no todas las propiedades de estilo son heredadas. Ejemplificando, las propiedades de posición, tamaño y margen no se heredan (esto es debido a que su valor depende de la posición del elemento en relación con el documento y no de la posición de sus elementos padres).

## 7. En qué consiste el proceso denominado cascada?
La cascada en CSS es el proceso que determina las propiedades que se asignarán a cada elemento de una página. Cuando se poseen varias reglas CSS que afectan a un mismo elemento, todas ellas deben converger en una serie de estilos en base a las reglas de especificidad, al orden en el que aparecen y a su importancia.
