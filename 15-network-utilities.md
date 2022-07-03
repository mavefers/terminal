Utilidades de la Terminal.

Utilidades de Red:
    (Es muy util en el campo de Ciberseguridad)
    Son herramientas extras para poder defenderse en los problemas que se presentaran con el pasar del tiempo, al momento de avanzar proyectos.

Comandos de usos de red:

ifconfig
    Nos muestra informacion de nuestra red.
    -Nos es util para configurar algunos puertos, servidores, etc.

ping [url]
    Nos indica el estado de una página web.
    Nos muestra el tiempo de respuesta.
    -Nos sirve para saber si una página web está activa o no, o también para verificar si nuestra conección de red está funcionando correctamente.

curl [url]
    Nos retorna la plantilla de la pagina web, en un archivo html de forma de texto plano, a través de la red.
    Podemos guardar el output en un archivo local, a través del operador '>' o '>>'.

wget [url] (funciona para descargar directamente a tu computadora, la plantilla de la pagina web que estas colocando)
    Es similar a 'curl', pero te descarga el texto en un archivo de texto plano, directo a tu computadora.

netstat -i
    Nos muestra nuestros dispositivos de red, indicando si estan trabajando correctamente o si hay algun error.