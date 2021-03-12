name: portada
class: center middle black

# .h1[.blanco[remark]]

.remark-code[.blanco[[.red[Daniel - Isabel - Numa]]]]

---
name: presentacion

# Itroducción

**remark** es un procesador de **Markdown**. El proyecto analiza y compila **Markdown**, y permite que los programas procesen **Markdown** sin siquiera compilarlo en HTML (aunque puede hacerlo).

**remark** convierte tu **Markdown** en una pagina web con la aparinecia de una presetación

.center[![EJEMPLO](assets/img/media.io_oxj18jxV.gif)]

---
name: html

# El código HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <title>titulo</title>
    <meta charset="utf-8">
    <!-- enlazamos nuestro css -->
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <textarea id="source">
      <!-- aquí va la presentación -->
    </textarea>
    <!-- enlace al archivo js de remark -->
    <script src="https://remarkjs.com/downloads/remark-latest.min.js">
    </script>
    <script>
      // funcion para que combierta nuestro archivo Markdown en una presentacion
      var slideshow = remark.create({
        sourceUrl: 'manualRemarkjs.md'
      });
    </script>
  </body>
</html>
```

.enlace[.center[[\[una pequeña guia de otras formas de hacerlo\]](https://github.com/gnab/remark/wiki)]]

---
name: paginas

# Separación entre hojas de la presentación

¿*Como se separan esos pequeños trozos*? Cada una de las hojas de la presentación está separada por **tres guiones consecutivos**. Esto en **Markdown** se utiliza para introducir una línea horizontal. Sin embargo, para hacer presentaciones con **Markdown** se utiliza para marcar la división entre cada una de las hojas de la presenteción.

Así, por ejemplo, dos hojas de la presentación sería:

```Markdown
# Hoja 1

Esto es el contenido de la primera hoja
---
# Hoja 2

Este es el contenido de la segunda hoja
```

```Markdown
# Hoja 1

* punto 1
---
# Hoja 2

* punto 1
* punto 2
```

---
name: propiedadesPagina

# Propiedades de las hojas de la presentación en markdown

Las primeras líneas de cada una de las hojas de la presentación nos permiten definir las propiedades de esas hojas. Algunas de estas propiedades son,

* .red[**name**] permite identificar la hoja de la presentación. Esto nos permite ir a ella, desde un enlace, utilizando .red[```\[enlace\]\(#nombre\)```] o con .red[slideshow.gotoSlide('nombre')].

* .red[**class**] nos permite definir los estilos que se aplicarán a la hoja.

* .red[**backgroun-image**] nos servirá para indicar la imagen de fondo que utilizaremos en la hoja.

* .red[**count**] es útil para indicar que esa hoja no se contabilice.

* .red[**template**] define la hoja de la presentación que se utilizará como plantilla para esa hoja.

* .red[**layout**] define que la hoja no se mostrará en la presentación, y sirve como plantilla para las siguientes hojas.

* .red[**exclude**] oculta una hoja de la presentación.
  
---
name: estilos

# Los estilos

A cada una de las hojas de la presentación le podemos asignar una serie de estilos. Para esto, solo tenemos que poner en el encabezado de la presentación, la palabra clave class seguida de los estilos que queremos aplicar. Así para que esté centrado tanto en vertical como horizontal utilizaremos,

```Markdown
class: middle center
```

También es posible aplicar estilos a determinadas partes de nuestro texto. Así, para poner un bloque centrado, utilizaremos,

```Markdown
.center[El texto que queremos que aparezca centrado]
```

Además podemos encadenar estilos. Por ejemplo, si queremos que el color del texto sea blanco, definiremos en nuestra hoja de estilos,

```css
.blanco{color: white;}
```

Así, si queremos un texto blanco y centrado, utilizaremos lo siguiente,

```Markdown
.center[.blanco[El texto que queremos en blanco y centrado]]
```

---
name: biblio
class: center middle black

# .blanco[Bibliografía]

.enlace[.center[[\[El atareado\]](https://www.atareao.es/como/presentaciones-con-markdown/#)]]

.enlace[.center[[\[Guia Markdown\]](https://www.markdownguide.org/basic-syntax/)]]

.enlace[.center[[\[remark\]](https://www.markdownguide.org/basic-syntax/)]]

---
name: indice
class: black

# .blanco[Índice]

.enlace[[\[Portada\]](#portada)]

.enlace[[\[Introdución\]](#presentacion)]

.enlace[[\[El código HTML\]](#html)]

.enlace[[\[Separación entre hojas de la presentación\]](#paginas)]

.enlace[[\[Propiedades de las hojas de la presentación en markdown\]](#propiedadesPagina)]

.enlace[[\[Los estilos\]](#estilos)]

.enlace[[\[Bibliografía\]](#biblio)]
