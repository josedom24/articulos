# Módulos de multiprocesamiento en apache2

## Introducción al servidor web apache2

El servidor web apache2 es uno de los servidores web más utilizado actualmente, sobre el 40 % de los sitios de intenet están gestionados por este servidor. Sl servidor apache fue creado en 1995 por Robert McCool y ha sido desarrollado bajo las directrices de la "Apache Software Foundation" desde 1999, siendo el primer proyecto de la fundación y su proyecto principal.

Podemos indicar mucas características del servidor, siendo las más importantes: que es un software de código abierto, multiplataforma, modular y extensible y muy popular, podemos encontrar un buen soporte y documentación y existe una comunidad muy activa que lo soporta.

En este artículo vamos a abordar las distintas posibilidades que nos brinda apache para gestionar las peticiones, tenemos a nuestra disposición distintas formas de procesar las peticiones y responderlas, y dependiendo de nuestras necesidades podemos configurar nuestro servidor para aumentar su rendimiento, es decir el número de respuestas generadas por segundos.

Este aspecto puede ser menos importante a la hora de desplegar un sitio web personal que no tenga mucho tráfico, pero es crucial cuando tenemos un sitio en producción con muchas peticiones y más importante aún, cunado estas peticiones son concurrentes.

Hay que señalar que aunque la mayoría de los sitios web actualmente servidor por apache todavía están utilizando la versión 2.2, en este artículo nos vamos a centrar en estudiar la versión 2.4, cuyas principales mejoras han ido encaminadas a mejorar los disintos mecanismos de procesamiento de peticiones y de esta manera poder ser más competitivo frente a nuevas alternativas como el servidor web nginx.

## Apache2 es un servidor web modular

La modularidad es una de las características principales de Apache2. Si queremos añadir nuevas funcionalidades al servidor tenemos a nuestra disposición diferentes módulos que nos ofrecen esa funcionaldad.

Por ejemplo, podemos hacer que apache2 sea el responsable de interpreta el código PHP de nuestras páginas, activando para ello el módulo apache2-mod-php5. De esta manera no dejamos 