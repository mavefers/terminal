Aprendiendo a manipular desde la Terminal, todo lo que usualmente haces desde la Interfaz Grafica:

-   Crear archivos
-   Crear directorios
-   Movernos
-   Renombrarlos
-   Copiarlos
-   Eliminarlos


* Todos los archivos que tengan un punto (.) antes de iniciar el nombre, Linux los marca como "archivos ocultos".


Instalar 'tree':
    Comando:
        sudo apt install tree
Commands Tree:
tree
    Sirve para visualizar con anatomia de "arbol", todos nuestros directorios que estan dentro del directorio en el que nos encontramos.

tree [ruta_o_NombreDelDirectorio]
    Sirve para revisar los elementos de un directorio en especifico.

Commands Tree with their options:
    tree -L [1, 2, 3, etc]
        Nos muestra la anatomia de carpetas y sub-carpetas, en niveles, dependiendo del numero de nivel o niveles que hayamos elegido.


Commands 1 / Comandos 1:

    ls -lS (S = Size / Tamanio)
        Ordena todos los directorios y documentos, por tamaño, comenzando desde los archivos más pesados, hasta los más ligeros.
    
    ls -l
        Enlista los archivos, en orden alfabetico, A-Z.
    
    ls -lr
        Enlista los elementos, en orden alfabetico, en reversa, Z-A.
    
    mkdir [nombreDelDirectorio] (mkdir = make directory)
        Sirve para crear directorios.

    mkdir ["Nombre del Directorio"]
        Se usa poniendo el nombre del directorio, entre comillas.
        Que el nombre esté entre comillas, sirve para declarar nombres separados.

* Cuando se manipulan directorios con espacios, se declaran entre comillas de una 'Nombre del Directorio'.
    

    mkdir [dir1 dir2 dir3]
        Se pueden crear varios directorios, en una sola linea de codigo.
        Sirve para crear directorios de una manera rapida.
    
    touch [nombreDelArchivo.extension]
        Sirve para crear archivos de cualquier tipo.
        Se necesita también declarar su extensión ".ejemplo".

    touch [file1 file2 file3]
        Se pueden crear varios archivos en una sola línea de código.
        Sirve para crear varios archivos, de una manera rápida. En simultaneo.
    
    cp [nombreDelDirectorio_oArchivo] [nombreDelDirectorio_respaldo (backup)] (cp = copy)
        Sirve para realizar copias de respaldo (buckup) enel mismo directorio.
        El nombre del nuevo archivo, tiene que ser diferente al original.
    
    cp [nombreDelDirectorio_oArchivo] [../directorio/otroDirectorio/etc (ruta)]
        Sirve para realizar una copia del archivo indicado, en otra carpeta, indicando la ruta del directorio en el que se copiará.
        Se copiará con el mismo nombre, no es necesario tener que declarar el nombre de salida.
    
    mv [elemento] [rutaFinal]
        -Se puede jugar con la la ruta y el elemento, trayendo archivos de otros directorios, al directorio actual; ejemplo: mv ../elemento ./
        -Puedes manipular las posiciones de los elementos, sean archivos o directorios/carpetas, de un lado hacia otro, estando desde un directorio completamente distinto o alejado; ejemplo: mv ../dir1/elemento ./dir3    -   mv ../dir1/elemento ../dir2
        -La primera ruta finaliza con el elemento que se moverá, y la segunda ruta finaliza con el directorio al que se moverá.
    
    mv [nombreViejoArchivo1] [nombreNuevoArchivo1]
        "mv" también funciona para renombrar archivos o directorios/carpetas.
    
    rm -i [archivo] (-i = interactive/interactivo)
        Sirve para consultar si de verdad se quiere eliminar ese elemento/archivo/carpeta.
        Te retorna una pregunta, antes de realizar la operación.
        Para responder a la pregunta, necesitamos escribir 'y' para sí/yes, y 'n' para no/no.
    
    ls [nombreDelDirectorio]
        Sirve para listar el contenido que hay en cualquier directorio.
        Se puede observar el contenido de un directorio, desde cualquier otra ruta; ejemplo: ls ../dir1/dir1_0
    
    
    Los archivos y directorios, Todo Linux en general, se consideran archivos.

    rm -ri
        -Sirve para tener mejor control al momento de borrar elementos.
        -Sirve para remover elementos de manera recursiva.
        -Al tener la opcion 'i', se eleminará elemento por elemento, y en cada operación iniciada, retornará la pregunta de que si estamos seguros de borrar tal archivo.
    
* Se pueden borrar varios archivos y directorios, al mismo tiempo.

    Recomendación (rm):
        Revisar bien los nombres antes de borrar archivos o elementos.
        Usar el comando 'ls' o 'tree' para revisar los elementos que borraremos, antes de hacerlo.
        Es muy *importante* eliminar archivos con la opcion de interactividad (-i).
    

* Anatomy/Anatomia de la Linea de Comandos:
    [projects]$ rm -f example.txt
                [projects]$ > prompt
                rm          > command/comando
                -f          > option/opcion
                example.txt > argument/argumento


* Options:
    Se declaran después de colocar un guión (-[o]).
    -i
        Interactive: Pregunta si estamos seguros de borrar el archivo que hemos elegido.
    -v
        Sirve para ver qué está haciendo el comando que estámos ejecutando, en segundo plano.


Commands 2 / Comandos 2:

-   Explorar archivos de texto, desde la Terminal. head/tail/less
-   Abrir el sistema de archivos. xdg-open


    head [archivoDeTexto.extension]
        Sirve para mostrar las primeras 10 lineas de cualquier archivo de texto, de cualquier formato. (Formato = tipo de archivo o .extension)
    
    head [archivoDeTexto.extension] -n [#]
        Modifica la cantidad de las primeras 10 lineas que vienen por defecto; ejemplo: head terminal.md -n 15
    
    tail [archivoDeTexto.extension]
        Sirve para mostrar las ultimas 10 lineas de cualquier archivo de texto, de cualquier formato. (Formato = tipo de archivo o .extension)
    
    tail [archivoDeTexto.extension] -n [#]
        Modifica la cantidad  de las ultimas 10 lineas que vienen por defecto; ejemplo: tail terminal.md -n 5
    
    less [archivoDeTexto.extension]
        Comando de interaccion de texto de cualquier formato.
        Nos envía a otra interfaz, una interfaz bastante poderosa e interactiva.
        Nos muestra todo el archivo de texto.
        Genera una especie de scroll, usando las flechas.
        -Al apretar la Barra Espaciadora, nos dirigirá rápidamente al final del contenido del archivo de texto.
        -Cuando apretamos el botón '/' (slash), nos permitirá realizar una búsqueda de alguna palabra que esté dentro del archivo de texto.
            /palabraX   > (al buscar la palabra, debemos respetar las minusculas y mayusculas)
        -Para salir de la interfaz de 'less', solo tenemos que apretar el botón 'q' de "quit".
    
    code [ruta/archivo]
        Sirve para abrir cualquier archivo de texto, de cualquier formato, en VSCode.

    xdg-open [ruta/archivo]
        Sirve para abrir un archvio
    xdg-open [directorio]
        Sirve para abrir directorios.

    wslview [nombreArchivo.extencionArchivo]
        Sirve para abrir un archvio
    wslview [nombreDirectorio]
        Sirve para abrir directorios.
    
    explorer.exe .
        Sirve para abrir el explorador de archivos en el directorio actual, en el que nos encontramos.

* Para parar forzosamente un proceso que se está ejecutando en la Terminal, solo debemos presionar la siguiente combinación: Ctrl + C


Sintaxis de una ruta:
    ./dir1/dir2/archivo.extension
        -Al final siempre tendrá que estar el archivo que estaremos manipulando, con su respectivo nombre y extensión.

    