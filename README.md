# Introducción  al análisis y visualización de datos con R para Ciencias Sociales y  Humanidades
Curso de verano para el [Magíster en Investigación Social y Desarrollo](http://www.magisterinvestigacionsocial.cl/) de la Universidad de Concepción, a realizarse entre el 7 y el 11 de enero de 2019.

## Instalación de R y RStudio

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

## Instalación de los paquetes de R que utilizaremos

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

## En caso de que tengan un Mac

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

## Dudas sobre el proceso de instalación
Si te encuentras con algún problema en las instalación que no sabes cómo resolver, puedes enviarme un correo para que tratemos de buscarle una solución: `riva.quiroga` arroba `uc.cl`.
