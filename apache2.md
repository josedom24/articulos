# Módulos de multiprocesamiento en apache2

## Introducción al servidor web apache2

El servidor web apache2 es uno de los servidores web más utilizado actualmente, sobre el 40 % de los sitios de intenet están servidos por este servidor. Sl servidor apache fue creado en 1995 por Robert McCool y ha sido desarrollado bajo las directrices de la "Apache Software Foundation" desde 1999, siendo el primer proyecto de la fundación y su proyecto principal.

Podemos indicar mucas características del servidor, siendo las más importantes: que es un software de código abierto, multiplataforma, modular y extensible y muy popular, podemos encontrar un buen soporte y documentación y existe una comunidad muy activa que lo soporta.

En este artículo vamos a abordar las distintas posibilidades que nos brinda apache para gestionar las peticiones, tenemos a nuestra disposición distintas formas de procesar las peticiones y responderlas, y dependiendo de nuestras necesidades podemos configurar nuestro servidor para aumentar su rendimiento, es decir el número de respuestas generadas por segundos.

Este aspecto puede ser menos importante a la hora de desplegar un sitio web personal que no tenga mucho tráfico, pero es crucial cuando tenemos un sitio en producción con muchas peticiones y más importante aún, cunado estas peticiones son concurrentes.

