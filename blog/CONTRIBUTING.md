# Contribuciones



## Colaborar con posts

Un post puede tratar sobre cualquier tema que te parezca interesante relacionado
con matemáticas e informática. Exponer características de un lenguaje de programación,
resolver un problema de geometría clásica, explicar un sistema de paquetes, una
aplicación de la programación lineal, qué es un comonoide, cómo trata Ruby la
visibilidad de los métodos o la sintaxis del cálculo lambda son ideas
muy válidas para un post. Además, entre las [issues de este repositorio](https://github.com/libreim/blog/labels/post) podrás encontrar
varios temas que querríamos tratar y que están todavía abiertos.

### Añadir un nuevo post

Hemos tratado de ponerlo fácil, y para las tareas sistemáticas de creación de
ramas y posts tenemos un archivo `Rakefile` que las automatiza. Para usarlo
necesitarás [tener Ruby instalado](https://rvm.io/). Para crear un nuevo post, clona este repositorio
y escribe en tu terminal

~~~sh
$ rake post
~~~

Esto lanzará una serie de preguntas (el título del post, el nombre del autor
en [`_config.yml`](https://github.com/libreim/blog/blob/gh-pages/_config.yml), etc.),
creará una rama del repositorio para que trabajes a gusto y creará el archivo
Markdown del post para que puedas escribir.

Los posts así creados se encuentran en la carpeta `/_posts`, ordenados por fecha
y nombre. En esta carpeta pueden añadirse posts manualmente en el formato de los
anteriores; aunque se recomienda usar el `Rakefile`. En caso de que no funcionara lo anterior, puede enviarse
el post a dgiim.blog@gmail.com y dejar que alguien se
encargue de publicarlo.


### Contenido

La [guía de estilo](http://libreim.github.io/blog/styleguide) te servirá de
chuleta para la sintaxis de Markdown y algunas peculiaridades acerca de como dar
formato correctamente a tu post.

### Construir localmente

Para comprobar si tu post queda como quieres, puedes construir y servir el blog
de forma local. Para ello necesitarás tener Ruby instalado en tu máquina. La
primera vez que vayas a construir el blog tendrás que obtener las dependencias:

~~~sh
$ gem install bundler
$ bundle
~~~

Tras este paso, cada vez que quieras construir el blog, simplemente ejecuta

~~~sh
$ rake
~~~

y lo tendrás disponible en `http://localhost:4000/blog/`.

### Enviar a revisión

Revisamos los posts entre colaboradores para asegurar en la medida de lo posible
la corrección de los posts. Cuando creas que tu post está listo para revisar,
solo tienes que utilizar el siguiente comando:

~~~sh
$ rake submit
~~~

Se abrirá una pestaña de navegador preparada para que crees una *pull request*
al repositorio original del blog. Rellena un poco la descripción y créala. A
partir de entonces espera a que al menos dos colaboradores den su visto bueno,
y pide a alguno de ellos que mezcle la *pull request*.

## Otras formas de colaborar

Este blog no solo vive de los posts escritos. También puedes ayudar de otras
maneras.

### Revisión

Si el blog recibe un post mediante una [*pull request*](https://github.com/libreim/blog/pulls)
y crees que tienes conocimientos generales sobre el tema suficientes para
revisarlo y corregir posibles errores, clona el repositorio y cambia a la rama
conveniente:

~~~sh
$ git clone https://github.com/libreim/blog.git
$ cd blog
$ git checkout post-nombre-del-post
~~~

Utiliza `rake` para [construir el blog localmente](#construir-localmente).
Los errores que encuentres y correcciones que quieras realizar puedes comentarlos
en la *pull request* asociada.

Cuando consideres que el post esté listo para ser publicado, asegúrate de dejar
un comentario en la *pull request* dando tu visto bueno.

### Parte técnica

En el repositorio del blog tenemos más issues además de los posts, relacionadas con el aspecto técnico
de mantener un blog. Puedes colaborar intentando solucionar cualquiera de ellas, o abriendo una nueva en
caso de que detectes algún error.


## Escribir artículos para el blog

Cualquier tema relacionado con las matemáticas y la ingeniería informática es apto para este blog.

Si quieres empezar a escribir tu artículo, puedes usar [**StackEdit**](https://stackedit.io/), que es un editor online de [Markdown](https://daringfireball.net/projects/markdown/)
y [Mathjax](https://www.mathjax.org/) con el que puedes previsualizar cómo quedarán las fórmulas matemáticas y el formato de tu artículo antes de enviarlo. 
Cuando lo termines, puedes enviarlo a **dgiim.blog+posts@gmail.com**. A partir de ahí, empezaremos un proceso de revisión desde [GitHub](https://github.com/libreim/blog/pulls)
para asegurarnos de que no haya ninguna errata y que sigue la [guía de estilo](http://tux.ugr.es/dgiimblog/styleguide/). En cuanto
esté revisado, lo publicaremos en el blog.

### Licencia
Los contenidos del blog se publican por defecto en licencia de [Creative Commons Reconocimiento-CompartirIgual 4.0 Internacional](http://creativecommons.org/licenses/by-sa/4.0/).
Si nos envías tu artículo, asumiremos esta licencia a no ser que prefieras indicarnos otra licencia libre. En cualquier caso,
incluye tu nombre para que podamos indicar tu autoría a la hora de publicarlo; así como el de otros autores o colaboradores
del artículo.


### Usando GitHub
También puedes presentar tu artículo como un pull-request a este repositorio. Puedes orientarte viendo otros posts escritos en la carpeta `blog/_posts`.

### Usando nuestro formulario
Si GitHub se te hace demasiado complicado, puedes usar directamente el editor de Markdown que tenemos preparado en nuestro formulario de [nuevo artículo](http://tux.ugr.es/dgiim/new/post). Cuando envíes un artículo, [**@libreimbot**](https://github.com/libreimbot) hará todo el trabajo para presentar tu artículo en GitHub y pasaremos a revisarlo desde allí. 

## Contribuciones técnicas

Este blog usa Jekyll para generar un sitio estático. Puedes contribuir en las plantillas (en HTML) o mediante plugins de Jekyll (en Ruby).
