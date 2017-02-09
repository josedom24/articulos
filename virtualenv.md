# Entornos de desarrollo virtuales con python

## Introducción

Un entorno de desarrollo virtual python o simplemente entorno virtual python esn software que me permite gestionar programas y paquetes python sin tener permisos de administración, es decir, cualquier usuario sin privilegios puede tener uno o más "espacios" (ya veremos más adelante que los entornos virtuales se guardan en directorios) donde poder instalar distintas versiones de programas y paquetes python. Para crear los entornos virtuales vamos a usar el programa `virtualenv` y para instalar paquetes python vamos a usar el programa `pip`. La pregunta que nos tenemos que hacer es la siguiente:

## ¿Para qué se usan los entornos virtuales?

Puede haber varios motivos en que su uso es conveniente e incluso necesario:

* Podemos tener necesidad de utilizar versiones de paquetes python que no son las que vienen empaquetadas oficialmente en nuestra distribución linux. La versión que se instala con nuestro gestor de paquetes, por ejemplo con `apt` en GNU/Linux Debian no corresponde con nuestras necesidades. Una solución puede ser usar `pip` como administrador: esta solución nos puede dar muchos problemas  que podemos romper las dependencias entre las versiones de nuestros paquetes python instalados en el sistema, puedo "romper" las dependencia y algún paquete puede dejar de funcionar. En este caso sería necesario la utilización de un entorno virtual.

* En el caso del desarrollo y despliegue de aplicaciones, cada vez es más importante acercar los entornos de desarrollo, prueba y producción. Utilizando entornos virtuales conseguimos que las dependencias entre paquetes que necesita nuestra aplicación estén satisfechas en todos los entornos, además es muy sencillo distribuir la configuración del entorno virtual, así como automatizar su creación, entre los distintos miembros del equipo de trabajo, consiguiendo que todos trabajen bajo el mismo escenario.

* Los ciclos de desarrollo de aplicaciones modernos en lenguajes con python son cada vez más rápido, esto puede suponer que en una misma máquina podemos tener aplicaciones que utilicen diferentes dependencias y versiones de un mismo paquete. Por ejemplo, podemos tener dos aplicaciones web en producción, una que esté desarrollada con django 1.8 otra con django 1.10. En este caso es imprescindible la utilización de entornos virtuales diferenciados, que sean la base de cada aplicación.

Además los entornos virtuales son una herramienta que favorecen las nuevas metodologías de trabajo que se denominan DevOps, que tratan de gestionar y automatizar la configuración. FALTA ALGO

## ¿Los entornos virtuales son propios sólo del lenguaje python?

No, existe herramientas parecidas en distintos lenguajes que nos ofrecen funcionalidad parecida:

* [phpenv](https://github.com/phpenv/phpenv) para php
* [plen](https://github.com/tokuhirom/plenv) y [perlbrew](https://perlbrew.pl/) para perl
* [rbenv](https://github.com/rbenv/rbenv) y [RVM](http://rvm.io/) para ruby
* [nodeenv](https://pypi.python.org/pypi/nodeenv/), [nvm](https://github.com/creationix/nvm), [n](https://github.com/tj/n) y [nave](https://github.com/isaacs/nave) para node.js

## Empecemos a trabajar con entornos virtuales

### Instalación de los paquetes necesarios

En este manual se va a realizar la instalación y configuración en una distribución GNU/Linux Debian  Jessie, en otra versión del sistema u otra distribución puede haber algunas diferencias.

Instalamos los paquetes necesarios