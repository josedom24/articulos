# Vistas (views) en el servidor DNS Bind9

En alguna circunstancia nos puede interesar que un mismo nombre que resuelve nuestro DNS devuelva direcciones IP distintas según en que red este conectada el cliente que realiza la consulta. Por ejemplo:

	* Si tenemos un servidor DNS que da servicio a internet y a intranet. Si se realiza la consulta desde internet, por ejemplo al nombre `www.example.org` debe devolver a la IP pública, sin embago si se hace la misma consulta desde la intranet la resolución deberá ser a una IP privada.
	* Otro ejemplo es en la resolución de nombres de instancias de OpenStack. En este caso una instancia tiene asignada una IP privada en el rango en el que hemos configurado la red interna, además puede tener asignada una IP flotante en el rango de la configuración que hayamos hecho de la red externa. En este caso sería deseable que cuando hago una consulta desde el exterior me resuelva con la IP flotante, y cuando haga una consulta desde otra instancia conecta da a la red interna me devuelva la dirección fija asignada a la instancia.

Vamos a ver un ejemplo del uso de vistas (views) en bind9 para configurar dos zonas diferenciadas para el mismo nombre de dominio y que se utilicen según desde donde se solicite la resolución.

