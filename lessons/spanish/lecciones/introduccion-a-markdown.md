---
title:  |
   Introducción a Markdown
authors:
- Sarah Simpking
date: 2015-11-13
reviewers:
- John Fink
- Nancy Lemay
translator:
- Víctor Gayol
layout: lesson
---

Introducción a Markdown
---------------

### Objetivos de la lección

En esta lección se ofrece una introducción a Markdown, un lenguaje de marcado con sintaxis en texto plano para generar textos con formato. Descubrirás el porqué se utiliza, cómo dar formato a los archivos de Markdown y cómo obtener una vista previa en la web de los documentos formados con Markdown.

Dado que las lecciones de Programming Historian deben ser enviadas como archivos Markdown, he incluido ejemplos específicos de PH en la medida de lo posible. Espero que esta guía sea útil si estás considerando contribuir con una lección en este sitio.

### ¿Qué es Markdown?

Markdown fue desarrollado en 2004 por [John Gruber](http://daringfireball.net/projects/markdown/), y se refiere tanto a (1) una manera de formar archivos de texto, así como a (2) una una utilidad de Perl para convertir archivos Markdown en HTML. En esta lección nos centraremos en la primera acepción y aprenderemos a escrivir archivos utilizando la sintaxis de Markdown.

Los archivos de texto plano tienen muchas ventajas sobre otro tipo de formato. Por un lado, se pueden leer prácticamente en todos los dispositivos. También han resistido la prueba del paso del tiempo mejor que otro tipo de archivos -si alguna vez has intentado abrir un documento guardado en un formato de [procesador de textos heredado] (https://es.wikipedia.org/wiki/Sistema_heredado), estarás familiarizado con los problemas de compatibilidad de implican.

Al utilizar la sintaxis de Markdown, serás capaz de producir archivos que pueden ser legibles como texto plano y que a la vez están listos para ser formados en otras plataformas. Muchos generadores de bitácoras y de sitios estáticos, así como sitios como GitHub, también soportan Markdown y traducen estos archivos a HTML para su visualización en la web. Además, herramientas como Pandoc pueden convertir archivos en o desde Markdown. Para más información sobre Pandoc puedes consultar la lección sobre [Autoría sustentable utilizando Pandoc y Markdown] de Dennise Tenen y Grant Wythoff.

### Sintaxis en Markdown

Los archivos en Markdown se guardan con la extensión `.md` y se pueden abrir en un editor de texto como TextEdit, Notepad, Sublime Text o Vim. Muchos sitios web o plataformas de publicación también ofrecen editores basados en la web y/o extensiones para introducir texto utilizando la sintaxis de Markdown.

En este tutorial vamos a practicar la sintaxis de Markdown en el navegador usando [StackEdit]. Podrás introducir texto formado en Markdown a la izquierda e inmediatamente ver la versión traducida junto a él a la derecha.

Dado que todas las lecciones de Programming Historian están escritas en Markdown, también podemos examinar sus archivos en StackEdit. Desde el [editor de StackEdit], haz click en el `#` en la esquina superior izquierda del menú. Selecciona `Import from URL` y entonces pega la siguiente URL para ver la lección "Introducción a Bash" en el editor:

```
https://raw.githubusercontent.com/es.programminghistorian/jekyll/gh-pages/lecciones/intro-a-bash.md
```

Verás que el panel de la derecha cuenta con una presentación más elegante del texto, mientras que el archivo de Markdown a la izquierda es aún bastante legible.

Vamos a sumergirnos ahora en la lección escribiendo nuestra propia sintaxis de Markdown. Crea un nuevo documento en StackEdit haciendo click en el icono de la carpeta en la esquina superior derecha seleccionando "New document". Debes ponerle nombre al documento en la caja de texto en la parte superior de la página.

#### Encabezados
Markdown dispone de cuatro niveles de encabezados qu eestán indicados por el número de `#` antes del texto del ecabezado. Pega los siguientes ejemplos en la caja de texto de tu izquierda:

```
# Primer nivel de encabezado
## Segundo nivel de encabezado
### Tercer nivel de encabezado
#### Cuarto nivel de encabezado
```

El primer y segundo nivel de encabezado también se pueden escribir como sigue:

```
Primer nivel de encabezado
==========================

Segundo nivel de encabeado
--------------------------
``` 

Estos se representarán como:
 
# Primer nivel de encabezado

## Segundo nivel de encabezado

### Tercer nivel de encabezado

#### Cuarto nivel de encabezado


Primer nivel de encabezado
==========================

Segundo nivel de encabeado
--------------------------

Observa que la sitaxis de Markdown sigue siendo comprensible aún en la versión de texto plano.

#### Párrafos y saltos de línea

Escribe la siguiente frase en la caja de texto:

```
¡Bienvenidos a Programming Historian!

Hoy aprenderemos sintaxis de Mardown.
Esta frase esta separada de la anterior por un solo salto de línea.
```

**Esto queda representado como:**

¡Bienvenidos a Programming Historian!

Hoy aprenderemos sintaxis de Mardown.
Esta frase esta separada de la anterior por un solo salto de línea.

Los párrafos deben estar separados por una línea vacía. Deja una línea entre `Markdown.` y `Esta` para que veas cómo trabaja. Los saltos de línea sencillos deben indicarse con dos espacios en blanco en algunas implementaciones de Markdown. Esto no es necesario en la variente de [GitHub Flavored Markdown], que es la que utiliza por defecto StackEdit.

#### Añadir énfasis

El texto se puede poner en cursivas encerrándolo entre los símbolos `*` o `-`. De la misma forma, el texto en negritas se escribe encerrando la palabra entre `**`o `__`.

Añade énfasis a una frase  utilizando estos métodos:

```
¡Estoy **muy** entusiasmado con los tutoriales de _Programming Historian en español_!
```

Lo cual queda representado así:

¡Estoy **muy** entusiasmado con los tutoriales de _Programming Historian en español_! 

#### Listados

Markdown soporta la creación de listas ordenadas y sin ordenar. Escribe la siguiente lista dentro de la caja de texto:

```
Lista de compras
---------------
* Frutas
  * Manzanas
  * Naranjas
  * Uvas
* Lácteos
  * Leche
  * Queso
```

Poner sangría al `*` te permite crear listas anidadas.

**Esto se depliega así:**

Lista de compras
---------------
* Frutas
  * Manzanas
  * Naranjas
  * Uvas
* Lácteos
  * Leche
  * Queso

Las listas ordenadas se escriben numerando cada línea. Una vez más, el objetivo de Markdown es producir documentos que sean legibles como texto plano y a la vez ser trasladados a otros formatos.

```
Lista de pendientes
------------------
1. Terminar el tutorial de Markdown
2. Ir a la tieda de abarrotes
3. Preparar el almuerzo
```

Lo cual se despliega:

Lista de pendientes
------------------
1. Terminar el tutorial de Markdown
2. Ir a la tieda de abarrotes
3. Preparar el almuerzo

#### Fragmentos de código

Representar fragmentos de código en forma distinta al resto del documento es una buena práctica que lo hace más legible. La escritura de código se representa generalmente a espacio sencillo. Dado que Markdown no distingue las tipografías involucradas, representamos los fragmentos de código encerrados entre dos signos de acento grave `````. Por ejemplo: ```<br/ >```. Cuando queremos representar un bloque completo de código lo debemos encerrar entre dos líneas de tres acentos graves. En la ventana de vista previa de StackEdit esto se representará como una caja de texto sombreada y escrita a espacio seguido.

Escribe lo siguiente en la caja de texto:

   ```html
   <html>
       <head>
	    <title>Título del sitio web</title>
       </head>
       <body>
       </body>
   </html>
  ```

**Y se representará así:**

```
<html>
       <head>
	    <title>Título del sitio web</title>
       </head>
       <body>
       </body>
   </html>
```

Observa cómo el bloque de código se representa a renglón seguido.

#### Bloque de citas

Escribe el siguiente texto en la caja de texto:

```
> Hola. Éste es un párrafo de texto incluido en un bloque de cita. Toma en cuenta que tengo una sangría con respecto al margen izquierdo. 
```
Lo cual se representará:

> Hola. Éste es un párrafo de texto incluido como un bloque de cita textual. Toma en cuenta que tengo una sangría con respecto al margen izquierdo. 

#### Enlaces de Internet

Los enlaces de Internet (*links*) se pueden escribir de dos maneras.

El título del enlace se encierra primer entre corchetes y despues se incluye la dirección completa del URL entre paréntesis.

`Para más tutoriales visita la página [Programming Historian en español] (es.programinghistorian.org "Programming Historian main page").`

**Lo cual se representa así:**

Para más tutoriales visita la página [Programming Historian en español] (es.programinghistorian.org/"Programming Historian main page").

Los enlaces tipo referencia son muy útiles para notas a pie de página y ayudan a mantener más ordenado tu documento en texto plano. Éstas se escriben con un par adicional de corchetes con el número de referencia para establecer el vínculo que identifique la etiqueta.

`Un ejemplo es el sitio de [Programming Historian] [1]`

Entonces puedes incluir el URL en otra parte del documento:

`[1]: http://programminghistorian.org/ "The Programming Historian"`

Lo cual se despliega de la siguiente manera:

Un ejemplo es el sitio de [Programming Historian] [1]

[1]: http://programminghistorian.org/ "The Programming Historian"


#### Imágenes

Se pueden referir las imágenes mediante el udo de `!`, seguido de un texto alternativo entre corchetes, seguido a su vez por el URL de la imagen y un título opcional entre comillas. Esto no se representará como texto en tu documento pero te permitirá incluir la imagen en la visualización de una página en HTML.

`![Logo de Wikipedia](http://upload.wikimedia.org/wikipedia/en/8/80/Wikipedia-logo-v2.svg "Wikipedia logo")`

**Esto aparece como:**

![Logo de Wikipedia](http://upload.wikimedia.org/wikipedia/en/8/80/Wikipedia-logo-v2.svg "Wikipedia logo")

#### Reglas y líneas horizontales

Puedes incluir líneas horizontales si escribes en una misma línea cualquiera de los siguientes tres signos: `-`. `*` o `_`, sin importar los espacioes que dejes entre ellos. Cualquiera de estas combinaciones generarán una línea horizontal:

```
___
* * *
- - - - - -
```

Lo cual genera:

___
***
- - - - - -

#### Tablas

El núcleo de Markdown no incluye tablas; sin embargo, algunos sitios web y aplicaciones usan variantes de Markdown que pueden incluuir tablas y otras características especiales. [GitHub Flavored Markdown] es una de estas variantes y es utilizado para visualizar archivos `.md` en el navegador del sitio de GitHub.

Para crear una tabla en GitHub, usa barras verticales `|`para separar columnas y guiones entre los encabezados y el resto del contenido de la tabla. Dado que las barras verticales son sólo estrictamente necesarias entre columnas, puedes usarlas en los extremos de la tabla para darle una vista más acabada. Las celdas pueden tener contenido de cualquier extensión, y no es necesario que las barras verticales estén alineadas verticalmente entre sí.

```
| Encabezado 1 | Encabezado 2 | Encabezado 3 |
| --------- | --------- | --------- |
| renglón 1, columna 1 | renglón 1, columna 2 | renglón 1, columna 3|
| renglón 2, columna 1 | renglón 2, columna 2 | renglón 2, columna 3|
| renglón 3, columna 1 | renglón 3, columna 2 | renglón 3, columna 3|
```

**Esto se despliega así:**

| Encabezado 1 | Encabezado 2 | Encabezado 3 |
| --------- | --------- | --------- |
| renglón 1, columna 1 | renglón 1, columna 2 | renglón 1, columna 3|
| renglón 2, columna 1 | renglón 2, columna 2 | renglón 2, columna 3|
| renglón 3, columna 1 | renglón 3, columna 2 | renglón 3, columna 3|

Para especiicar la alineación del contenido de cada columna se pueden agregar dos puntos `:`al renglón de los encabezados como sigue: 

```
| Alineado-izquierda | Centered | Alineado-derecha |
| :-------- | :-------: | --------: |
| Manzanas | rojo | 5000 |
| Plátanos | amarillo | 75 |
```

Lo cual se despliega:

| Alineado-izquierda | Centered | Alineado-derecha |
| :-------- | :-------: | --------: |
| Manzanas | rojo | 5000 |
| Plátanos | amarillo | 75 |

Aunque Markdown se está haciendo cada vez más popular, particularmente para los documentos con formato que se pueden ver en la web, muchas persones y editores siguen solicitando archivos tradicionales en Word, PDF y otros formatos. Esto puede arreglarse de alguna manera utilizando herramientas de conversión en línea como [Pandoc]. No obstante, algunas características de los procesadores de texto, como la de control de cambios, no tienen soporte aún. Por favor, visita la lección de Programming Historian en español sobre [Autoría sustentable en texto plano usando Pandoc y Markdown] para mayor información sobre Pandoc.

### Conclusiones

Markdown es un término medio muy útil entre los archivos de texto plano sin estilo y los documentos de procesadores de texto heredados. Su sintaxis simple se aprende rápidamente y es altamente legible en el mismo documento y cuando se despliega en HTML u otro tipo de documentos. En conclusión, escribir tus documentos en Markdown significa que serán capaces de ser utilizados y leídos a largo plazo.


[John Gruber]: http://daringfireball.net/projects/markdown/
[Autoría sustentable utilizando Pandoc y Markdown]: http://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown
[StackEdit]: https://stackedit.io
[editor de StackEdit]: https://stackedit.io/editor
[GitHub Flavored Markdown]: https://help.github.com/articles/github-flavored-markdown/
[GitHub Flavored Markdown]: https://help.github.com/articles/github-flavored-markdown/
[Pandoc]: http://johnmacfarlane.net/pandoc/
[Autoría sustentable en texto plano usando Pandoc y Markdown]: http://es.programminghistorian.org/lecciones/autoria-sustentable-usando-pandoc-y-markdown

