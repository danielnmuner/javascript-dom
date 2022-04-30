## Frontend Developer

### Introduccion
  - [x] [¿Qué es HTML y CSS? ¿Para qué sirven?](#¿-qué-es-html-y-css-?-¿-para-qué-sirven-?)
  - [x] [Motores de render](#motores-de-render)
### Maquetación con HTML
  - [x] [Anatomía de un documento HTML](#anatomía-de-un-documento-html) 
  - [x] [¿Qué es HTML semántico?](#¿-qué-es-html-semántico-?)


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









