Utilidades de la Terminal.

Utilidades de Red:
    (Es muy util en el campo de Ciberseguridad)
    Son herramientas extras para poder defenderse en los problemas que se presentaran con el pasar del tiempo, al momento de avanzar proyectos.

Comandos de usos de red:

ifconfig
    Nos muestra informacion de nuestra red.
    Sirve para ver la mascara de red, puerto de transmisión, tarjeta de red, etc
    -Nos es util para configurar algunos puertos, servidores, etc.

ping [url]
    Nos muestra el tiempo de respuesta.
    -Nos sirve para saber si una página web está activa o fuera de linea, ya que nos indica el estado de esta misma, como también nos sirve para verificar si nuestra conección de red está funcionando correctamente.

curl [url]
    Nos retorna la plantilla de la pagina web, en un archivo html de forma de texto plano, a través de la red.
    Podemos guardar el output en un archivo local, a través del operador '>' o '>>'.

wget [url] (funciona para descargar directamente a tu computadora, la plantilla de la pagina web que estas colocando)
    Es similar a 'curl', pero te descarga el texto en un archivo de texto plano, directo a tu computadora.

traceroute [url]
Nos sirve para ver por cuales computadoras tenemos que ir pasando para llegar, por ejemplo, a una pagina web.
-Nos saldrán todas las IPs por las que tenemos que pasar para llegar a la pagina web que hemos indicado.

netstat -i
    Nos muestra nuestros dispositivos de red, indicando si estan trabajando correctamente o si hay algun error.