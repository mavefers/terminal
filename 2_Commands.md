Simbolos que hacen referencia a directorios:
    ~ (virgulilla) > user
    / (diagonal)   > root

Comandos de la Shell:
    echo $SHELL
        -sirve para conocer cual Shell se esta ejecutando.
    echo $TERM
        -sirve para
    env
        -sirve para ver informacion detallada de la Bash Shell.
    ls
        -Sirve para enlistar los elementos que tenemos almacenados en ese directorio, sean archivos o carpetas.
        -Enlista nuestro sistema de archivos.
        -Determina colores para diferenciar entre archivos y directorios.
    
    cd [parametro: ruta o nombre de la carpeta]     (change directory / cambiar directorio)
        -Nos cambia de posicion entre los directorios que elijamos estar.
    
    clear
    Ctrl + l
        -Sirve para limpiar la Terminal.
    
    ls -l
        l = long / largo
        Sirve para visualizar los elementos, con informacion más detallada.
        Te muestra el peso de los archivos, en bytes.
    ls -lh
        l = long / largo
        h = human / humano
        Sirve para visalizar los elementos, con informacion mas detallada de manera simplificada; con lectura "humana".
        Te muestra el peso de los archivos, en kilobytesm, megabytes, gigabytes, etc <.
    
    cd ~
        Te redirige a la carpeta 'usuario'.
    
    cd / Te redirige a la carpeta root.

    pwd (print working directory)
        Imprime la ruta en la que nos encontramos.


    Operadores de Rutas Relativas:
        .
            Sirve para ubicarnos en nuestro directorio actual.
        ..
            Sirve para retroceder un directorio atrás. Nos dirige al directorio padre.
            Podemos retroceder cuantas veces querramos, ejemplo: cd ../../.. (esto hace retoceder tres directorios)


    Podemos autocompletar el nombre de un elemento, escribiendo la parte inicial del archivo y utilizando el tabulador (botón Tab).
    

    file [archivo.extension]
        Sirve para visualizar la informacion y el tipo de archivo de cualquier elemento, sean archivos o directorios.
    
    