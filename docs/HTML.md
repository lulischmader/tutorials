---
layout: default
title: HTML
date:   2020
author: Susanna Allés Torrent
nav_order: 3
---

Websites are built with a language called Hypertext Markup Language or HTML. It is called "hypertext" simply because it goes beyond the text and creates links among texts. 

In fact, when you open the browser, you are seeing the result of the code in which the page is written. The sections, titles, menus, paragraphs, etc., even the colors, do not exist as such, like in a print document, but they are only code. 

HTML determines the structure of the page, whereas the design is given by another language: the Cascading Style Sheet or CSS. 

To begin, we can create a test page. Follow this steps: 

-	Open the terminal and go to our course folder
-	Create a new folder calle `Site`: `mkdir Site`
-	Create a new HTML document: `touch test1.html`

To work with a HTML file you only need a text editor, such as [Visual Studio Code](https://code.visualstudio.com/) for instance. 

An static website is a group of HTML files that are hosted in a server. In general, a site is structured in different folders, in the main one there is the `index.html` which is the one the browser opens by default, plus other html files. Normally there is a CSS folder with one or several .css files that give the design to the site, anthoter folder for Javascript scripts, and another one for the images. 

 ![Estructura página HTML](https://github.com/susannalles/susannalles.github.io/blob/master/_teaching/SPA322/img/html1.png)

Let's imagine that we have a page called "courses" and that inside it we have a welcome page (`index.html`), and three different links that take us to three different folders. Let's imagine also that while browsing we arrive at the page `emperadores.html`; in the browser it will appear:  

![Estructura página HTML](https://github.com/susannalles/susannalles.github.io/blob/master/_teaching/SPA322/img/html2.png)
 
The mechanism is exactly the same as when we navigate through our Finder, so if we want to modify a specific page, we will have to open and manipulate that file, in this case `emperadores.html`. 

## HTML

The HTML language has its own syntax, based on "tags". These tags are composed of an opening tag `<tag>` and a closing tag `<tag/>`. They are nested inside each other, as if they were a family tree. And remember: everything that opens closes. 

```html
<tag1>
    <tag2>
       <tag3>This is content</tag3>
    </tag2>
</tag1>
```

There are some preliminary concepts to retain:

-	A tag is composed of the element (or name), and sometimes of an attribute that must carry a value:

```html
<element attribute=“value”>content</element>
```

-	Sometimes a tag can be empty, meaning it has no meaning, in which case we use: `<tag/>`. This is the case, in HTML, of line breaks `<br/>` or images `<img/>`. 

  The HTML document is composed of several mandatory sections: 

- `<!DOCTYPE html>` Tells the browser that the document type is HTML. 
- `<html>` is the tag that will contain all the content, both the `<head>` and the <body>.
- `<head>` contains all metadata and the information in the file that will not appear in the browser.
- `<title>` is the title that appears on the browser tab.
- `<body>` is the actual body of the page, which we will see in the browser.
  
The structure of any HTML file is: 

```html
<!DOCTYPE html>
<html>
    <head>
   	 <title>Title of my page</title>
    </head>
    <body>
    </body>
</html>
```

### Basic HTML structures and elements

- `<p>` is used to create paragraphs.  
- `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>` serve to indicate the title, fom highest to lowest. 
- `<a href= “www.link.html”>the link</a>` The tag `<a>` is used to create links. 
- `<img scr=“URL”>` to insert images inside the page. This element must contain a scr attribute which must contain the location of the image file. If we wanted to convert our image into a link, we would simply nest the image inside a `<a>` tag:  `<a href="http://www.direccion.com"><img src="imagen.png"/></a>`

### Lists: 
  
- `<ol>` ordered lists, it will create a numerical list; inside, the items will be nested.
- `<ul>` unordered list,  it will create a list; inside the list the items will be nested.
- `<li>` list item. 

Lists can be nested inside each other, for example:

```html
<ol>
      <li>item</li>
          <ul>
             <li>subitem</li>
          </ul>
      <li>item</li>
      <li>item</li>
</ol>
```

Commenting the code is always very important, for this we can use a special tag that will not appear in the browser: `<!-- comment -->` 

### Simple typography
  
- `<strong>` - bold
- `<em>` - italic
- `<i>` - italic


### Tables

- `<table>
- `<tr>` (table row): rows (horizontally)
- `<td>` (table data): columns (vertically)
	
```html
<table border="1px">
        	<tr>
            	<td>Row 1: Column 1</td>
            	<td>Row 1: Column 2</td>	 
        	</tr>
       	 
        	<tr>
            	<td>Row 2: Column 1</td>
            	<td>Row 2: Column 2</td>
           	 
        	</tr>
       	 
        	<tr>
            	<td>Row 3: Column 1</td>
            	<td>Row 3: Column 2</td>
           	 
        	</tr>
 </table>
```

Optionally we can use: 

- `<thead>` for a title, and it has `<tr>` and `<th>`
- `<tbody>` for data in the table

```html
<table border="1px">
      <thead>
           <tr>
			<th>Title column 1</th>
			<th>Title column 2</th>
 	</tr> 
      </thead>
      <tbody>
        	<tr>
            	<td>Row 1: Column 1</td>
            	<td>Row 1: Column 2</td>	 
        	</tr>
       	 
        	<tr>
            	<td>Row 2: Column 1</td>
            	<td>Row 2: Column 2</td>
           	 
        	</tr>
       	 
        	<tr>
            	<td>Row 3: Column 1</td>
            	<td>Row 3: Column 2</td>
           	 
        	</tr>
       </tbody>
 </table>
```

If we want to merge cells, we will use `colspan` followed by the `=` sign and the number of cells to merge in quotation marks:
  
```html
<thead>
	<tr>
		<th colspan=”2”>Title column 1</th>
	</tr> 
</thead>
```

### Divisions 
  
Divisions are very important elements and they are used to create divisions on the page: `<div>`.

You can make a first test by adding width and height, and also color:

```html
<div style="width:50px; height:50px; background-color:red"></div>

<div style="width:50px; height:50px; background-color:blue"></div>

<div style="width:50px; height:50px; background-color:green"></div>
```

### Span
  
- `<span>` To style small parts of the page (e.g. words or group of words). 

### Useful tutorials: 
  
-	[Codecademy: HTML & CSS](https://www.codecademy.com/tracks/web) 
-	[W3Schools](http://www.w3schools.com/html/)


## CSS: Style

To give style to a page, we can proceed in three different ways: 

1. Include the command inside the tag (not a good practise). E.g. `<p style=“font-size:12px”>`
2. Add the css inside the `<head>` tag, like this:

```html
<head>
	<title>Title of the page</title>
	<style type= “text/css”>
	(...)
	</style>
</head>
```

3. Create a different file that will contain all CSS rules `style.css` and will be included in the `<head>` of the HTML document:

`<link type="text/css" rel="stylesheet" href="style.css" />`

The most used option is the 3, because when we create, for example, a static website, we will not have to change the rules every time we create a page or HTML file, but all the rules will be in a separate file and we will have to change it only once.

The CSS syntax is simple but can get quite complicated. The basic structure of a CSS rule is as follows: 

```css
selector{
property: value; 
}
```

The selector can be any HTML tag or element or any class or identifier. The property is the characteristic that we want to modify, such as the background or font color, the font size and family, etc. Whereas the value is the actual aspect that we want to give to that or those HTML elements. 

The comments inside the CSS are marked like this: `/* Comment */`

Let's see which commands are the most basic: 
 
### Font Type:

- `font-size: Xpx;`
- Family font (Arial, Verdana, Impact, … ): `font-family: Arial;`
- There are different types of fonts: serif, sans-serif, cursive… Normally we choose several font types, in case the machine does not have the first one, it goes to the second one: `font-family: Tahoma, Verdana, sans-serif;`
- The sizes can be given in `px` pixels (e.g. `font-size:15px;`) and set to a fixed size, or in `em` which gives a size relative to the screen: `1em` corresponds to the default size, `0.5em` to half the size, and `2em` to twice the size. 

### Colors:

- `color: green;`
- Colors can be expressed in different ways: 
  * simple colors with names: `black`, `pink`, `violet`, `green`, `yellow`
  * hexadecimal values (# and 6 digits). Vid. [HTML Color Picker](https://www.w3schools.com/colors/colors_picker.asp).
- `background-color: red;`

### Alignment:
  
- center, right, left : `text-align:center;`


### Sizes: 
  
- `height:` the height is expressed in pixels
- `width:` the width is also expressed in pixels

It is especially useful for `div`: 

```css
div{
	background-color:#cc0000;
	height:100px;
	width:100px;
}
```

### Text decoration: 

We can give an special feature to certain elements. For instance, for the links, `<a>`, we can determine what color we want to be or if it needs to be underlined or not: 

```css
a{
	text-decoration: none;
}
```

### Borders:
  
Specially for tables, but also for `<div>`,  is useful to use borders. For instance, if we have a table: 

```css
selector{
	border: 1px solid black;
}
```

- `border-radius:` this would be to round the borders. 


Las reglas CSS pueden y deben darse de manera general, sin necesidad de añadir el atributo style a cada etiqueta. Para ello utilizaremos los atributos `@class` y `@id`: 
- `@class` sirve para dar estilo a una clase de elementos que comparten una serie de características. 
- `@id` sirve para dar un identifador único y por tanto otorogar una serie de características propias. 

Por ejemplo: 

- `<div class=“texto”>` suponemos que hay más de una `<div>` que queremos con las mismas características. En la CSS deberíamos señalarlo así, por ejemplo: 

```css
.texto{
	font-size:15px;
	font-family:Arial;
	color:blue;
}
```

Mientras que una `<div id= “contenedor”>` señala que es la única en todo el documento que habrá unas características concretas. En la CSS se reflejaría con el símbolo `#`:

```css
#contenedor{
	background-color: yellow;
}
```

#### Pseudo-selectores
  
Muy utilizado cuando queremos modificar parcialmente el comportamiento de un elemento, como en los links. Hay tres tipos diferentes: 

- `a:link:` link que no se ha todavía consultado
- `a:visited:` link consultado
- `a:hover:` cuando pasamos el cursor por encima. 

```css
selector:pseudo-class-selector{
	propiedad:valor}

a:hover {
    color: #cc0000;
    font-weight: bold;
    text-decoration: none;
}
```

#### Posición de los elementos `<div>`

- Apariencia:
	- `display` puede contener 5 valores:
	- `block`: los sitúa en bloque
	- `inline-block`: los sitúa en bloque sin sus medidas originales
	- `inline`:los sitúa en bloque sin sus medidas originales
	- `none`: desaparecen

- Margen: 
	- `margin`: espacio que hay fuera del elemento
	- `margin-top: /*some value*/`
	- `margin-right: /*some value*/`
	- `margin-bottom: /*some value*/`
	- `margin-left: /*some-value*/`

Pueden marcarse todos a la vez empezando por el de arriba: `margin: 1px 2px 3px 4px;`

- `border`: el borde es lo que delimita el elemento propiamente dicho
- `padding`: es el espacio entre el contenido y el borde

- Floatting:
	- `float:right`
	- `float:left;`

- Position: Hay cuatro tipos de posición: 
	- `absolute`: se posiciona en relación al primer elemento padre que no tiene `position:static`; si no hay tal elemento, el elemento con posición absoluta se coloca en relación al elemento `<html>`. 
	- `static`: La posición por defecto es `static`.
	- `relative`: es la más utilizada
	- `fixed`: para fijar un elemento en la pantalla (los menús por ejemplo)


Actualmente existen diferentes opciones para construir un sitio web estático. [Bootstrap](http://getbootstrap.com/) y [Foundation](http://foundation.zurb.com/) son dos de ellos, así como [Jekyll](http://jekyllrb.com/). 
