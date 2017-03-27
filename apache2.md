# Módulos de multiprocesamiento en apache2

## Introducción al servidor web apache2

El servidor web apache2 es uno de los servidores web más utilizado actualmente, sobre el 40 % de los sitios de intenet están gestionados por este servidor. Sl servidor apache fue creado en 1995 por Robert McCool y ha sido desarrollado bajo las directrices de la "Apache Software Foundation" desde 1999, siendo el primer proyecto de la fundación y su proyecto principal.

Podemos indicar mucas características del servidor, siendo las más importantes: que es un software de código abierto, multiplataforma, modular y extensible y muy popular, podemos encontrar un buen soporte y documentación y existe una comunidad muy activa que lo soporta.

En este artículo vamos a abordar las distintas posibilidades que nos brinda apache para gestionar las peticiones, tenemos a nuestra disposición distintas formas de procesar las peticiones y responderlas, y dependiendo de nuestras necesidades podemos configurar nuestro servidor para aumentar su rendimiento, es decir el número de respuestas generadas por segundos.

Este aspecto puede ser menos importante a la hora de desplegar un sitio web personal que no tenga mucho tráfico, pero es crucial cuando tenemos un sitio en producción con muchas peticiones y más importante aún, cunado estas peticiones son concurrentes.

Hay que señalar que aunque la mayoría de los sitios web actualmente servidor por apache todavía están utilizando la versión 2.2, en este artículo nos vamos a centrar en estudiar la versión 2.4, cuyas principales mejoras han ido encaminadas a mejorar los disintos mecanismos de procesamiento de peticiones y de esta manera poder ser más competitivo frente a nuevas alternativas como el servidor web nginx.

## Apache2 es un servidor web modular

La modularidad es una de las características principales de Apache2. Si queremos añadir nuevas funcionalidades al servidor tenemos a nuestra disposición diferentes módulos que nos ofrecen esa funcionaldad.

Por ejemplo, podemos hacer que apache2 sea el responsable de interpretar el código PHP de nuestras páginas, activando para ello el módulo apache2-mod-php5. De esta manera no dejamos a otro programa externo la ejecución de dicho código. 

Siguiendo esta filosófia tenemos a nuestra disposición los Módulo de Multiprocesamiento (MPM), que son los responsables de configurar el comportamiento del servidor para gestionar las peticiones. Dependiendo del que tengamos activado apache2 utilizará mecanismos distintos para responder las peticiones, además cada uno de estos módulos lo podemos configurar para adaptarnos lo máximo posible a nuestras necesidades.

## Módulos de multiproceso en Apache2

Como hemos comentado anteiormente tenemos varios mecnismos para gestionar las peticiones que llegan al servidor, cada una de ellas se activarán habilitando el correspondiente módulo:

* prefork: En este primer mécanismo cada petición se responde por un proceso individual de apache2. Cuando se inicia el servicio se crean varios procesos hijos prearados para responder peticiones HTTP. cuando aumenta el número de peticiones se crean nuevos procesos, y cuando disminuyen se van eliminando, pero siempre se quedan a la espera un número mínimo de procesos esperando para responder las futuras peticiones.

* worker: En este caso cada proceso apache2 es capaz de responder a varias peticiones, para ello se utilizan la programación basada en hilos (thread). Por lo tanto con este MPM tenemos procesos apache2 que trabajan concurrentemente, cada hilo de ejecución del proceso puede responder a una petición HTTP. Por lo tanto con menos procesos que el anterior se pueden responder a más peticiones, sin embargo si tenemos un proceso que tenga un problema y termine puede dejar sin gestionar un número mayor de peticiones. En este mecanismo también se crean procesos al iniciar el servicio, perpradaos para responder, y si van aumentando las peticiones se van creando nuevos procesos, y evidentemente cuando no hay suficiente peticiones esos procesos se van eliminando, dejando siempre alguno activo preparado para responder. Este MPM es el que viene por defecto activo en Apache2.2.

* event: En Apache2.2 estaba considerado experimental, en la nueva versión 2.4 pasa a ser el MPM por defecto. Podemos considerar este MPM como una mejora del anterior. También utiliza hilos de ejecución, pero aumenta el rendimiento de worker. Para explicarlo, necesitamos recordar que significa la persistencia de la conexión en HTTP (keep alive). Un cliente puede hacer diversas peticiones HTTP a un servidor utilizando la misma conexión TCP. En el MPM worker todas las peticiones de un cliente realizadas en una conexión persistente se servían con un mismo hilo de un proceso, la gran novedad de event es que las peticiones dentro de una conexión persistente la pueden responder hilos distintos de procesos distintos. Esto aumenta el rendimiento (número de peticiones respondidas por segundo) ya que si dentro de una conexión persistente las peticiones estaban espaciadas en el tiempo, teníamos un hilo bloqueado e inactivo en el MPM worker, mientras que con el MPM event ese bloque no existe.

## Configuración de los MPM en apache2

	El MPM event es el que viene instalado en apache2.4: