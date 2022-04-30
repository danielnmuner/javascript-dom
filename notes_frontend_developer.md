## Frontend Developer

### Introduccion
  - [x] [¿Qué es HTML y CSS? ¿Para qué sirven?](#¿-qué-es-html-y-css-?-¿-para-qué-sirven-?)
  - [x] [Motores de render](#motores-de-render)
### Maquetación con HTML
  - [x] [Anatomía de un documento HTML](#anatomía-de-un-documento-html) 
  - [x] [¿Qué es HTML semántico?](#¿-qué-es-html-semántico-?)
  - [x] [Etiquetas de HTML más usadas](#etiquetas-de-html-más-usadas)
### Maquetación con CSS
  - [x] [Anatomía de una declaración CSS](#anatomía-de-una-declaración-css)
  - [x] [Tipos de selectores](#tipos-de-selectores) 


### ¿Qué es HTML y CSS? ¿Para qué sirven?

- **HTML**: Es un lenguaje de marcado de texto, es la infraestructura de una pagina web
- **CSS**:  Permite estilizar la pagina web.
En el inspector de elementos de Google podemos identificar el **HTML** y **CSS**

### Motores de render

Permite que todo nuestro lenguaje de marcado y estilos se pueda visualizar en pantalla. **DOM** (__Document Object Model__), Comprende nuestro **HTML** y **CSS** como un objeto. 

### Anatomía de un documento HTML

Un elemento de HTML puede ser:
```html

<!-- 
El cual se encuentra dentro de estiquetas 
de apertura y cierre, aunque hay algunas que no tienen
etiqueta. Atributos como class= 'title' 
donde asi nos podemos comunicar con CSS
-->

<h1 class='title'> Platzi </h1>
```
Las etiquetas en HTML tiene una estructura de anidamiento dependiendo de la funcion de la etiqueta. 

- Podemos inicia la estructura basica de html escribiendo: `html:5`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
</body>
</html>
```
Luego de haber creado la estructura basica podemos ir estructuranto nuestro documento paso a paso:

```html
<body>
    <section>
        <h1>Platzi</h1>
        <p>Incredible</p>
        <ul>
            <li>Breathtaking</li>
            <li>Marvelous</li>
        </ul>
    </section>
</body>
```
### ¿Qué es HTML semántico?

Nos anima a utilizar las etiquetas adecuadas en dentro del documento dependiendo del tipo de informacion consignada, en otras palabras no solo valernos de la etiqueta `<div>`. Asi el codigo es mas accesible y mayor posicionamiento en SEO.

```html
<header></header>
<nav></nav>
<article></article>
<img src="" alt="">
```
### Etiquetas de HTML más usadas
En [HTML Reference](http://htmlreference.io/), podemos descubrir mas etiquetas.😊

|**Layout** | **Formularios** | **Otros**
| --- | --- | --- |
|header | form | a
|nav | input | h1..h6, p
|section | label | span
|article | button | img,svg,iframe,video
|aside | - | ul, li, ol
|footer | - | - |

```html
<!-- 
Podemos colocar listas dentro de la etiqueta [nav]
-->
<nav>
    <ul>
        <li>About Us</li>
        <li>Home</li>
    </ul>
</nav>

<!-- 
Podemos colocar de todo dentro de la etiqueta [section]
-->
<section>
    <h1>Pictures Pexels</h1>
    <img src="https://images.pexels.com" alt="Picture">
</section>
<!-- 
Un [form] usualmente cuenta con [label] para indicar
que se debe colocar en un [input]
-->
<form action="">
    <label for="name">Form</label>
    <input type="text" id="name">
</form>
```
### Anatomía de una declaración CSS

- **Selector**: Comunica HTML con CSS
![image](https://user-images.githubusercontent.com/60556632/166086015-b36f914a-3298-42a0-b9a5-96c83aa11f42.png)

### Tipos de selectores
Podemos utilizar la etiqueta `style` arriba de `head` para estilizar dentro del HTML. Los **Selectores Basico** son los siguientes: 

```html
<style>
/* Selector de Tipo */
    div {
        background: pink;
    }
/* Selector de Clase como .titulo
donde algunas etiquetas pertenecen 
a esta clase */
    .titulo {
        color:blueviolet
/* Selector de Id el cual usualmente solo
pertenece a una etiqueta especifica*/
    }
    #kws {
        color: yellowgreen;
    }
/* Selector de Atributos aqui el atributo es
href el cual especificamente apunta a platzi.com */
    a[href="platzi.com"] {
        color: blue;
    }
/* Selector Universal se aplica principlamente
sobre todo el HTML */
    * {
        background: papayawhip;
    }
</style>
```

Los **Selectores Combinadores** son los siguientes: 

```html
<style>
    /*Desendiente se refiere a todos los
    selectores o etiquetas que estan dentro 
    de una etiqueta padre, como [p] dentro de [div]*/
    div p {
        color: aqua;
    }
    /*Hijo Directo consite en aplicar la 
    propiedad de div justo al primer div dentro 
    de la etiqueta padre, no afectara otras etiquetas*/
    div > div {
        background: blueviolet;
    }
    /*Elemento Adyacente A diferencia del caso anterior
    aplica la propiedad a la etiqueta que le sigue en orden
    y no que esta dentro de la misma
    */
    div + div {
        background: blueviolet;
    }
    /*General de Hermanos es muy similar al caso 
    anterior, solo que no solo se aplica la propiedad
    al primer elemento si no a todas las etiquetas por
    ejemplo p seguidas y despues de div
    */
    div ~ p {
        background: blueviolet;
    }
</style>
```

