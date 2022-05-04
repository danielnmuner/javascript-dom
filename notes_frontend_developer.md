## Frontend Developer
### [Colors HTML](https://htmlcolorcodes.com/)

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
  - [x] [Pseudoclases y Pseudoelementos](#pseudoclases-y-pseudoelementos)
  - [x] [Cascada y especificidad en CSS](#cascada-y-especificidad-en-css)
  - [x] [Tipos de display](#tipos-de-display)
  - [x] [Flexbox y CSS grid](#flexbox-y-css-grid)
  - [x] [Modelo de Caja](#modelo-de-caja)
  - [x] [Colapso de Margenes](#colapso-de-margenes)
  - [x] [Posicionamiento en CSS](#posicionamiento-en-css)
  - [x] [Z index y el contexto de apilamiento](#z-index-y-el-contexto-de-apilamiento)
  - [x] [Propiedades](#propiedades)
  - [x] [Unidades de medida](#unidades-de-medida) 
  - [x] [Responsive Design](#responsive-design)
  - [x] [Arquitecturas CSS](#arquitecturas-css)


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
### Pseudoclases y Pseudoelementos

Las [**Pseudoclases :**](https://css-tricks.com/pseudo-class-selectors/) se refiere a las acciones realizadas por el usuario que activaran estilizaciones dinamicas.

```css
    /*Definimos el color de p*/
    p {
        color: salmon;
    }
     /*Cambiamos las propiedades de estilo de p con hover*/
    p:hover {
        color:skyblue;
        font-weight: 700;
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
     /*p dentro de div ubicado en el 2do logar hereda este estilo especial*/
    }
    div p:nth-child(2){
        color: black;
    }
```

Los [**Pseudoelementos ::**](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) son elementos que escribimos desde CSS, por ejemplo, el **::after** y el **::before** nos puedes funcionar como `divs`, como su nombre lo dice, son elementos, pero no necesariamente están escritos desde el HTML 

```css
    /*Pseudoelementos afectan al HTML
    indirectamente, aqui se modifica solo la primera letra*/
    p::first-letter{
        color: blue;
    }
    /*Añade texto o emoji antes o despues de p*/
    p::before {
        content: "🤠";
    }
    p::after {
        content: "👽"
    }
```
### Cascada y especificidad en CSS
El orden en que escribimos **CSS** importa y existen reglas de especificidad, donde indicamos quien **prevalece** sobre quien. Como podemos ver hay mayor relevancia sobre `#Id` que `Selector Universal`.

![image](https://user-images.githubusercontent.com/60556632/166581318-0fcd8c89-cead-400b-bf84-bcc6a0ca664a.png)

La relevancia se mide en puntos y entre mas puntos mayor especificidad luego **CSS** prevalecera sobre otras propiedades.

![image](https://user-images.githubusercontent.com/60556632/166583181-c858ace6-6cef-42d9-ad30-580d7cb740ff.png)

Podemos utilizar la calculadora de especificidad y asi saber cuantos puntos tiene nuestra regla. [Calculadora](https://specificity.keegan.st/)

### Tipos de display
![image](https://user-images.githubusercontent.com/60556632/166584335-5210ed5a-2bfb-4ebd-8f4d-368b5e3c22a1.png)

- **inline**: Estos elementos son los que su caja mide exactamente lo mismo que su contenido. Estos elementos los podemos usar en textos y en lugar de que se agreguen en una nueva línea se agregaran justo al ladito del texto. ❗ Tienen como desventaja que no podemos ponerles márgenes ni tampoco podemos cambiar su tamaño.

```css
/*Este codino haria nada cuando la etiqueta es de tipo inline
pero si funcionaria si fuera en etiquetas tipo bloque como div*/
div {
    background: salmon;
    width: 200px;
    height: 100px;
    margin: 20px;
}
```

- **block**: Estos elementos ocupan toda la pantalla, por lo que si quieres agregar otro elemento, este se agregará automáticamente abajo. No importa que tengas poco contenido, el elemento sí o sí va a ocupar toda la pantalla.

- **inline-block**: Esto mezcla lo mejor de ambos mundos. Con este display podemos tener tanto los beneficios de inline como de block, es decir, podemos tener elementos que no ocupen todo el ancho de la pantalla, sino que ocupen solamente lo que su contenido ocupa, pero también vamos a poder darle márgenes y podremos cambiar su tamaño 🤠.

```css
/*Button es una etiqueta inline-block, luego por default seria inline pero puede llegar a ser block si cambiamos su estilos */

button {
    background: salmon;
    width: 200px;
    height: 100px;
    margin: 20px;
}

<button>I'm a Button</button>
```
### Flexbox y CSS Grid

Cursos para entender mejor **Flexbox y CSS Grid**
- [Flexbox VS CSS Grid](https://platzi.com/blog/flexbox-vs-css-grid-cual-es-la-diferencia/)
- [CSS Grid Layout](https://platzi.com/clases/css-grid-layout/)
- [Flexbox y CSS Grid](https://platzi.com/clases/flexbox-css-grid/)
- [🚀 Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Platzi Course](https://platzi.com/clases/2229-flexbox-css-grid/36134-diferencias-entre-flexbox-y-css-grid/)

En **HTML** creamos un `.contenedor` con varios `.items`

```html
<div class="container">
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
</div>
```
En **CSS** no encargamos disñar la distribucion que tendra el sitio web, como se ve a continuacion en el caso de Flexbox.

```css
  .container {
  /*Indicamos si es grid o flex y alineamos o centramos los items*/
      display: flex;
      background: papayawhip;
      justify-content: center;
      height: 100px;
      align-items: center;
  }
  /*Estilizamos los items y validamos en el inspeccionador de elementos
  que estos esten ubicados en la posicion correcta.*/
  
  .item {
      width: 30px;
      height: 30px;
      background: purple;
  }
  .container .item:nth-child(2n+1){
      background: orange;
  }
```

### Modelo de Caja

Debemos entender que al final las etiquetas de **HTML** son cajas con diferentes tipos de visualizacion. Y cada caja tiene ciertas propiedades que podemos o a veces debemos modificar.

![image](https://user-images.githubusercontent.com/60556632/166590647-9058d33d-c25a-466f-8ab9-467f6238fb93.png)

- **padding:** Es básicamente el espaciado que hay entre la caja y el contenido de la caja, es un espaciado interno. Lo solemos usar mucho para permitir que los elementos “respiren”.

- **border**: Es el delineado que le podemos dar a una caja, y un borde puede ser tan grueso como quieras. Simplemente debemos ponerle el grosor, el tipo de borde y el color del borde.

- **margin:** Este es básicamente el espaciado entre elementos. Es la distancia que podemos dejar de un elemento hacia otro.

- **box-sizing: border-box;** es sencilla: si pones esta propiedad, el tamaño final de tu caja va a ser del width que tú le pongas, si no la pones, el tamaño final de tu caja va a ser del width que tú le pongas más el tamaño de tu padding. 

```html
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
- **box-sizing: border-box;** Es muy importante si no queremos que width total sea mayor a un limite definido.

### Colapso de Margenes

Cuando colocamos concecutivamente dos elementos de tipo **bloque** las margenes de van a solapar esto ocurre **cuando no** tenemos contenedores tipo **grid** o **flexbox**. Por lo tanto si esto ocurre lo mejor es utilizar un contenedor:

```html
<section class="container">
    <div>Platzi</div>
    <div>Master</div>
</section>    
```
Y posteriormente utilizar **flexbox** o **CSS Grid**

```css
.container {
    display: flex;
    flex-direction:column;
}
div {
    margin: 20px;
}
```

### Posicionamiento en CSS
![image](https://user-images.githubusercontent.com/60556632/166615461-cafe5c99-18b8-410d-90ba-20bbdf0d8d8e.png)

Usualmente es preferible trabajar con nuestras técnicas de alineamiento comunes como CSS Grid o Flexbox, pero suele haber casos donde sí o sí necesitamos usar position.

En este ejemplo creamos un contenedor de dos imagenes.
```html
<div class="container">

<img id="estambre" src="https://pixabay.com/get/gcace262ba99b669194b5054d0a18589d64d2858de5ccde802a2bd69112122969cc55406c4d138c9738ad55e21d831bab_640.png" alt="Estambre">

<img id="michi" src="https://static.platzi.com/media/user_upload/michi-0cd46b59-feda-4746-81a0-cc48179411ae.jpg" alt="Michi">

</div>
```
Simplemente a mi container le pongo un **position: relative;** y al estambre le pongo un **position: absolute;**. Recuerda que cuando usamos un **absolute**, este elemento se va a mover con respecto al elemento relative más cercano, así que en este caso moveremos el estambre con respecto a nuestro **contenedor**😄.

```css
.container {
 position: relative;
}

.container,
#michi {
    width: 800px;
}
#estambre {
    width: 100px;\
    position: absolute;
    top: 190px;
    right: 245px;
}

```
![image](https://user-images.githubusercontent.com/60556632/166616196-49a9a043-92af-43b7-ab60-42defb503e30.png)

![image](https://user-images.githubusercontent.com/60556632/166616251-c0e2a6fc-2df8-4eca-b4e6-8cc273f3e8a8.png)


### Z index y el contexto de apilamiento

Se trata del **eje Z** donde podemos colocar varias capas o sobre poner elementos como los pop-ups de ads. A continuacion se observa que **yellow** esta contenido dentro de **blue**, luego al heredar la posicion de **blue** aunque yellow **Z-index** sea mas grande que **red**, no lograra sobreponerse a **red**.

![image](https://user-images.githubusercontent.com/60556632/166617316-0632ddd8-9474-4f03-926f-5df96cb0fd3e.png)

```html
<body>
<!--
  Al usar las clases no importa el orden
  de las etiquetas.
-->
  <div class="one">Platzi</div>
  <div class="two">Master</div>
</body>
```
Si modificamos `Z-index` se veria de la siguiente forma: 
```css
<style>
  div {
    background: paleturquoise;
    /*Al ser absolute, div se sobrepone*/
    position: absolute;  
  }
  .one {
      z-index: 4;
  }
  .two {
      z-index: 5;
  }
</style>
```
### [Propiedades](https://cssreference.io/)
![image](https://user-images.githubusercontent.com/60556632/166618556-3da38369-9589-46a4-a8b9-dd5609743148.png)

### Unidades de medida
![image](https://user-images.githubusercontent.com/60556632/166619382-4eebf7ab-dcb7-4507-ab22-9a864b2710b2.png)

- **Absolutas** No dependen de factores externos.
- **Relativas** Estás si pueden cambiar en relación con el dispositivo que lo estamos viendo.

![image](https://user-images.githubusercontent.com/60556632/166619503-daf2769e-53df-4920-81b4-c25330cfd50e.png)

Si establecemos que `1rem` es igual a `10px` en vez de `16px` sera mas sensillo utilizar `rem`, esto se logra `font-size = 62.5%;` en vez de `font-size = 100%;`

```html
html {
  font-size = 62.5%;
}
```
### [Responsive Design](https://platzi.com/clases/1906-diseno-programadores/28552-diseno-responsivo/)

```css
  div {
      background: purple;
  }
  /*Indica que si la pantalla es menor
  a 300px cambia a rojo sino se mantiene
  en morado, en general podemos colocar 
  todo tipo de propiedades dependiendo el 
  tamano*/
  @media (min-width:300px) {
      div {
          background: red;
      }
  }
```

### Arquitecturas CSS

- **Código predecible**  

Dentro de una arquitectura predecible las nuevas reglas de estilo que son añadidas reaccionan de forma previsible: no sufren contaminación alguna por parte de otras reglas (tampoco hacia otros elementos) ni existen dependencias incongruentes entre las reglas de los diferentes elementos del plano.

- **Código reutilizable**  

La abstracción (aislar un elemento de su contexto o del resto de los elementos que lo acompañan) es un paradigma de programación con una útil aplicación en nuestro entorno. Mantener la abstracción en la arquitectura de CSS nos permitirá diseñar reglas modelo, aptas para infinidad de elementos con características comunes

- **Código mantenible**  

Esta característica está referida a la facilidad con la que puede realizarse una modificación y/o mantenimiento de un código. Algunas de las prácticas que garantizarán este aspecto son:

- Ordena, comenta y categoriza tu código de forma lógica y jerárquica
- Crea código legible
- Crea código intuitivo
- Declara clases descriptivas

- **Código escalable**  

Salvaguardar la escalabilidad de tu CSS supondrá que éste podrá ser manipulado de una forma sencilla al realizar las tareas necesarias para abordar el crecimiento de la plataforma. En estos casos la curva de aprendizaje que permitirá comprender y adquirir las capacidades necesarias para alterar tu código no debería ser excesivamente grande

#### [OOCSS](https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/#top), [BEM](https://platzi.com/blog/bem/), [SMACSS](https://medium.com/@GreenXIII/organize-your-css-smacss-way-89c087db5092), [ITCSS](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/) y [Atomic Design](https://bradfrost.com/blog/post/atomic-web-design/)





