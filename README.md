# Introducción  al análisis y visualización de datos con R para Ciencias Sociales y  Humanidades
Curso de verano para el [Magíster en Investigación Social y Desarrollo](http://www.magisterinvestigacionsocial.cl/) de la Universidad de Concepción, a realizarse entre el 7 y el 11 de enero de 2019. El enlace directo a este repositorio es: http://bit.ly/udec_curso_r

> El curso tiene por objetivo introducir a sus participantes en el manejo de R para el procesamiento, análisis y visualización de datos. A partir de las realización de ejercicios prácticos, se espera que los participantes se familiaricen con el uso de esta herramienta y comprendan el potencial que tiene para la investigación en Ciencias Sociales y Humanidades.

## Preparación para el curso
Para el curso es necesario que traigan su computador personal. Lo ideal sería que ya tuvieran R y RStudio instalados. A continuación están las indicaciones para hacerlo.

### Instalación de R y RStudio

En este curso utilizaremos R a través del IDE RStudio. ¿Qué es un IDE? IDE es el acrónimo de *Integrated Development Environment* (*Entorno de Desarrollo Integrado*). Esto quiere decir que RStudio es una aplicación que nos entrega herramientas para hacer más fácil el desarrollo de proyectos usando R.

Para poder instalar R y RStudio, sigue los siguientes pasos:

- Descarga R desde https://cran.r-project.org/. Debes elegir la opción que corresponda, según tu sistema operativo.
- Instala R en tu computador, tal como lo haces con cualquier programa.
- Una vez que R ha quedado correctamente instalado, descarga RStudio desde https://www.rstudio.com/products/rstudio/download/. Elige la primera opción, es decir, "RStudio Desktop Open Source License" (gratuita).
- Instala RStudio en tu computador, tal como lo haces con cualquier programa.

Si quedó todo bien instalado, cuando abras RStudio deberías ver algo así:

![](https://github.com/rivaquiroga/RLadies-Santiago/blob/master/images/rstudio.png)

En este curso usaremos la última versión de R y RStudio, así que si tienes instalada una versión previa, puede que algunas cosas se vean un poco distintas.

IMPORTANTE: Si te aparece algún error durante este proceso, lo más probable es que sea por alguna configuración de tu sistema operativo. En ese caso, la mejor manera de buscar una solución es copiar el error que arroja R, pegarlo en tu motor de búsqueda favorito y ver cómo alguien que se enfrentó a eso antes lo resolvió.

### Instalación de los paquetes de R que utilizaremos

Cuando instalamos R por primera vez en nuestro computador, lo que estamos instalando es lo que se conoce como "R Base", es decir, los elementos centrales del lenguaje de programación. Una de las ventajas de R es que se trata de un lenguaje extensible: la propia comunidad de usuarios puede desarrollar nuevas posibilidades para utilizarlo. La manera de compartir estos nuevos desarrollos es a través de "paquetes", que incluyen, entre otras cosas, código y datos. Una analogía que se suele utilizar para explicar esto es que R Base es un teléfono celular tal como viene de fábrica y los paquetes las _apps_ que descargamos para que tenga más funcionalidades.

En la primera sesión del curso usaremos tres paquetes: `gapminder`, `babynames` y `tidyverse`. Los dos primeros (`gapminder` y `babynames`) son paquetes que incluyen datos que nos servirán para algunos de los ejercicios que realizaremos. `tidyverse`, por su parte, es un "megapaquete" que incluye otros paquetes en su interior. Todos los paquetes que conforman "el Tidyverse" comparten la misma visión sobre el trabajo con datos y la escritura de código. Quizás ahora eso suene un poco enigmático, pero más adelante explicaremos qué quiere decir.

Para instalarlos,

1. copia el siguiente código:

```r
install.packages("tidyverse")
install.packages("gapminder")
install.packages("babynames")
```

2. pégalo en la consola (_Console_) de RStudio:

![](https://github.com/rivaquiroga/RLadies-Santiago/blob/master/images/install.packages.png)

3. presiona 'enter'.
El último paquete es un poco más pesado que el resto, así que, dependiendo de tu conexión, podría tomar alrededor de un minuto en descargarse. El resultado se debería ver parecido a esto:

![](https://github.com/rivaquiroga/RLadies-Santiago/blob/master/images/paquetes_instalados.png)

¿Salió todo bien? ¡Excelente! Ya escribiste tus primeras líneas de código :)

#### Warnings / Errores
Si no tienes la última versión de R, puede que aparezca un "Warning" durante la instalación, que te avisa que el paquete fue construido bajo otra versión de R. Un "Warning" es distinto a un error: R ejecuta el código que le pides, pero te advierte que no todo puede resultar como esperas. Cuando aparece un error, en cambio, el código no se ejecuta.

### En caso de que tengan un Mac

Es posible que a algunas personas que usen sistemas operativos Mac les aparezca un mensaje similar a este cuando abren R/RStudio:

``` r

'Durante la inicializaci''on - Warning messages:
1: Setting LC_CTYPE failed, using "C"
2: Setting LC_COLLATE failed, using "C"
3: Setting LC_TIME failed, using "C"
4: Setting LC_MESSAGES failed, using "C"
5: Setting LC_MONETARY failed, using "C"
[R.app GUI 1.70 (7521) x86_64-apple-darwin15.6.0]

WARNING: You''re using a non-UTF8 locale, therefore only ASCII characters will work.
Please read R for Mac OS X FAQ (see Help) section 9 and adjust your system preferences accordingly.'
```

Esto ocurre porque existe un problema con la codificación de caracteres definida en su computador. Para resolverlo, deben cerrar R/RStudio, abrir el "Terminal" de su computador, pegar el siguiente código: `defaults write org.R-project.R force.LANG en_US.UTF-8` y ejecutarlo. Si nunca han ocupado el Terminal, no se preocupen, porque dedicaremos un tiempo al inicio de la primera clase para resolver este tipo de asuntos.

### Dudas sobre el proceso de instalación
Si te encuentras con algún problema en las instalación que no sabes cómo resolver, puedes enviarme un correo para que tratemos de buscarle una solución: `riva.quiroga` arroba `uc.cl`.

## Sesión 1
En esta primera sesión hablaremos acerca de qué es un lenguaje de programación y cuáles son las ventajas que tiene utilizarlo en el marco de la investigación en Ciencias Sociales y Humanidades. Conoceremos cómo se ejecuta el código en R, las herramientas que ofrece RStudio y algunas funciones básicas para el trabajo con datos.

El código que vayamos escribiendo durante la sesión estará disponible [en el siguiente enlace](http://bit.ly/udec_r_sesion1).

### Recursos adicionales

* Sitio web [Tidyverse](https://www.tidyverse.org/)
* Webinar: [Usando R para Ciencia de Datos](https://resources.rstudio.com/webinars/2018-05-23-13-01-usando-r-para-la-ciencia-de-datos-edgar-ruiz-edited)

* [Sitio para para seleccionar colores según código hexadecimal](www.color-hex.com).

## Sesión 2
En esta sesión revisaremos distintas formas de leer datos hacia R. Usaremos el paquete `haven` para importar archivos en formatos propios de programas como SPSS y STATA y veremos como leer un archivo que está en internet directamente (es decir, sin guardarlo antes localmente en el computador). Revisaremos funciones para limpiar y ordenar datos, y otras para unir y transformar datasets.

Los paquetes nuevos que instalaremos en esta sesión son:

```r
install.packages("downloader")
install.packages("readxl")
```

El código de hoy aparecerá [en este enlace](http://bit.ly/udec_r_sesion2).

Si no tienen un programa para descomprimir archivos `.rar` en su computador, pueden descargar los datos para el ejercicio 1 desde [acá](https://www.dropbox.com/s/ohdb4hr6rpajpld/Casen%202017.sav?dl=0).

### Recursos adicionales

* Pueden encontrar información adicional sobre el paquete `haven` en este [enlace](https://haven.tidyverse.org/).

* [ModernDive](https://moderndive.com/): Tutorial sobre análisis estadístico en R

## Sesión 3
En la primera parte de la sesión de hoy haremos un par de ejercicios breves sobre limpieza y transformación de datos que quedaron pendientes de la sesión de ayer, y luego nos enfocaremos en el análisis de datos textuales.

Para uno de los ejercicios pendientes usaremos los datos que se encuentran en [este enlace](https://www.dropbox.com/s/7hhznyuzfzdsrpl/datos_s3.xls?dl=0).

Los paquetes nuevos que instalaremos en esta sesión son:
```r
install.packages("tidytext")
install.packages("quanteda")
install.packages("readtext")
install.packages("syuzhet")
```
El código de hoy aparecerá en [este enlace](http://bit.ly/udec_r_sesion3) y los datos que es necesario que descarguen [en este otro](http://bit.ly/udec_r_datos_sesion3).

### Recursos adicionales

* El [sitio web](https://quanteda.io/) del paquete `quanteda` es muy completo. Incluso tiene un [tutorial en español](https://quanteda.io/articles/pkgdown/quickstart_es.html)

* Existe un libro asociado al paquete `tidytext` que está [disponible en línea](https://www.tidytextmining.com/). Ahí encontrarán ejemplos de otros tipos de análisis que no alcanzaremos a ver acá, como _topic modeling_.

* [Ejemplo en español sobre el uso de expresiones regulares con el paquete stringr](https://github.com/C-Lara/Curso-R/blob/master/Lista-dataframes-factores-tablas/expresiones-regulares.R)

* [Lista de expresiones regulares en R](http://www.diegocalvo.es/expresiones-regulares-en-r/)

* [Tutorial sobre uso de expresiones regulares en español](https://www.datanalytics.com/libro_r/manipulacion-basica-de-texto.html)


## Sesión 4

En la primera parte de la sesión de hoy seguiremos explorando las posibilidades del paquete `quanteda` para hacer análisis de textos. Luego, nos enfocaremos en estrategias para hacer _web scraping_, es decir, para extraer información de sitios web.

Los paquetes nuevos que instalaremos en esta sesión son:

```r
install.packages("rvest")
install.packages("janitor")
```
* El código que vayamos escribiendo hoy irá apareciendo en [este enlace](https://www.dropbox.com/s/ekko5h3wpgp92sd/script_sesion4.R?dl=0). El archivo ya tiene algunas líneas del código de ayer que usaremos para empezar hoy.
* Seguiremos trabajando con los mismos datos de ayer, así que no es necesario descargar nada nuevo. En caso de que no hayan alcanzado a guardar el corpus como objeto de R (`corpus_programas.rds`), [pueden descargarlo acá](https://www.dropbox.com/s/hxw0uemd0i1znjs/corpus_programas.rds?dl=0).
* En la segunda parte de la sesión extraeremos datos de las siguientes páginas: 1) [registro de asesorías externas de la cámara de diputados](https://www.camara.cl/camara/transparencia_asesorias.aspx) y 2) [registro de reuniones y audiencias de senador\*s](http://www.senado.cl/appsenado/index.php?mo=lobby&ac=GetReuniones).
* [Selector gadget](https://selectorgadget.com/): para que Chrome muestre las etiquetas html y sea más fácil escrapear la página.


### Recursos adicionales

## Sesión 5

Esta última sesión se iniciará a las 17:00 con una actividad abierta sobre cómo se organiza la comunidad de R a través de iniciativas como RLadies y LatinR, entre otras.

![](https://github.com/rivaquiroga/curso-r-udec/blob/master/images/r-en-conce.png)

Luego, en nuestra última sesión del curso veremos algunos ejemplos adicionales que complementan lo que revisamos a lo largo de esta semana.

* El código que vayamos escribiendo hoy irá apareciendo en [este enlace](https://www.dropbox.com/s/ruupf6x497e9ma7/script_sesion5.R?dl=0). El archivo ya tiene algunas líneas del código de ayer que usaremos para empezar hoy (básicamente, reconstruiremos lo que hicimos al final de la clase de una forma mucho más rápida y eficiente).

* Los datos que usaremos están en [esta carpeta](https://www.dropbox.com/sh/lz6p9jgk1qz1lvt/AAAJjbIdfqHBrSUW_uqb8YBaa?dl=0)

### Recursos para seguir profundizando sobre temas que vimos o sobre otros que no eran parte del curso pero que les pueden interesar

#### Recursos en español

* [Ciencia de Datos para gente sociable](https://bitsandbricks.github.io/ciencia_de_datos_gente_sociable/). Este tutorial tiene por destinatarios principales personas de Ciencias Sociales. La última parte está enfocada en el trabajo con datos espaciales.
* [The Programming Historian](https://programminghistorian.org/es/lecciones/) publica tutoriales revisados entre pares que buscan acercar herramientas digitales a personas que vienen de las humanidades. Encontrarán recursos sobre R, Python y entre otros. También hay una versión en inglés del sitio.
* **Próximamente** [R para Ciencia de Datos](http://es.r4ds.hadley.nz). En este enlace pueden ver la traducción en proceso del libro [R for Data Science](https://r4ds.had.co.nz) que está realizando la comunidad de R de Latinoamérica.

#### Visualización de datos
 Durante el curso trabajamos principalmente con el paquete `ggplot2`. Pueden encontrar la documentación del paquete con la indicación de qué hace cada función en el [sitio web del Tidyverse](https://ggplot2.tidyverse.org). Otros paquetes que pueden explorar:

* [`plotly`](https://plot.ly/r/)
* [`gganimate`](https://gganimate.com/)
* [`highcharter`](http://jkunst.com/highcharter/)
* [`patchwork`](https://github.com/thomasp85/patchwork) (este paquete sirve para combinar gráficos de `ggplot2`)

#### Datos espaciales
Paquetes que sirven para hacer análisis de datos especiales:
* `leaflet`. Su [sitio web](https://rstudio.github.io/leaflet/) es muy completo.
* [`sf`](http://r-spatial.github.io/sf/)

#### Machine Learning
* `caret`. [Tiene un sitio web muy completo](https://topepo.github.io/caret/index.html).

#### Otros recursos

## Evaluación del curso

Aquellas personas interesadas en tener una evaluación del curso tienen la posibilidad de realizar un ejercicio en el que apliquen una o más estrategias de análisis revisadas. La idea es que piensen en algún problema que quieran resolver usando R y que generen una posible solución para ese problema.

Algunas ideas:
* Limpiar y ordenar una base de datos con la que les interesa trabajar en el futuro.
* Crear una base de datos a partir de la unión de datos provenientes de distintas fuentes.
* Hacer _web scraping_ de algún sitio web del que quieran obtener datos.
* Explorar otros datos de la [Unión Interparlamentaria](https://data.ipu.org) y generar alguna visualización.
* Aplicar alguna de las estrategias de análisis de textos revisadas en el curso, pero con un corpus que sea de su interés.
* Leer desde internet un archivo `.csv` hacia R, explorar los datos usando alguna de las funciones que vimos (`filter()`, `group_by`, `mutate()`, `summarize()`, `select()`, etc.) y visualizarlos con el paquete `ggplot2`.
* Una mezcla de alguno de los ejemplos anteriores.

Si tienen alguna idea en mente y quieren discutirla antes de empezar, pueden enviarme un correo: `riva.quiroga` arroba `uc.cl`.

#### Modalidad de trabajo
El trabajo se puede realizar de forma individual o en parejas.

#### ¿Qué debo entregar?
Si la propuesta **no** implica la carga de archivos locales (es decir, que estén en el computador de quien ejecuta el código), pueden entregar solo el _script_. Si lo que quieren hacer implica leer algún archivo desde el computador a R, entonces deben entregar la carpeta con su proyecto comprimida, que incluya el _script_ y los archivos que se utilizarán. La entrega se hace a través del [siguiente enlace](https://www.dropbox.com/request/HOdBuxCZv9Unj7vCa18w).

#### ¿Hasta cuándo puedo entregar el ejercicio?
El plazo para entregar el ejercicio es el lunes **21 de enero**.
Cualquier situación especial, podemos resolverla por correo **antes** de esa fecha (por ejemplo, si necesitan tener su nota antes o requieren más plazo para poder desarrollar el ejercicio).
Es importante que consideren que si entregan después de esa fecha su nota no alcanzará a quedar registrada ahora en enero y tendrán que esperar hasta marzo para que aparezca.
