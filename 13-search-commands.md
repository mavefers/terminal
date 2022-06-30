Comandos de búsqueda:
    Nos permiten buscar archivos o directorios, donde también podemos usar filtros para realizar una mejor búsqueda, tales como son: su extensión, su nombre, su ubicación, etc.

-
Archivos .log:
    Son archivos de texto plano que recopilan informacion de un archivo en ejecución.
    Como por ejemplo, el navegador Chrome cuando recopila información de eventos y los adjunta en archivos .log para recopilar datos, como por ejemplo, cuando una perstaña se crashea o hay algún error en el sistema.
-

Comandos de búsqueda:
    'which': Nos ayuda a buscar la ruta de los binarios que tenemos.
        Ejemplo:
            which code

    'find': Nos permite encontrar un archivo.
    Sintaxis:
        find [ruta] [opcion] [valor]
        ejemplo:
            Para buscar por tipo de archivo
                find ./ -type f -name *.log
                find [ruta] [tipodeOpcion] [valor: f=file] [tipodeOpcion] [valorDeOpcion, expresion regular, en 'name' tambien puedes usar *wildcards]
            Para buscar por tipo de peso/tamaño (archivos mayores a 20M = 20 megabytes):
                find ./ -size 20M

    Ejemplos de uso:
        -Para encontrar carpetas Node Modules que crea JavaScript cuando se está ejecutando, y borrarlas porque cuanto más se van creando, más ocupa espacio innecesario en la memoria.
    
/

Reto:
    Buscar todos los archivos con la extension .txt, guardarlos en un archivo, y que al ejecutar el comando, aparezca un mensaje de "listo". DONE!

        find ~ -name *.txt > mis-archivos-de-texto.txt && cowsay "LiSTO!" | lolcat