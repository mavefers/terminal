Variables de Entorno
    Definición y Modo de uso.

Sirven para acceder a la configuración y a los difentes valores del sistema.

//

Links simbolicos:
    Son accesos directos desde la terminal.
    Son un tipo de archivos que hacen referencia a un lugar.

ln = link
-s = simbolico

Sintaxis:
    ln -s [ruta/] [nombreDelLink]

/

Los links simbolicos como tal, no tienen permisos.

//

Comando para conocer la configuración y valores del sistema, de las variables de Entorno.
    'printenv'

/

Una vez conocido el nombre de la variable, ya podemos...
    Imprimir variables de entorno:
        'echo $[nombreDeLaVarible]
    
    Ejemplos de variables de entorno:
        $HOME   >>>     nos muestra la ruta del user.
        $PATH   >>>     nos muestra todas las rutas de los binarios que ejecutan nuestro sistema.