Wildcards:

Wildcard '*'

Es una serie de carácteres que nos permiten encontrar patrones y realizar busquedas más avanzadas.

Sirve para realizar manipulaciones en base a ciertos patrones, coincidencias y filtrados.
- Se tienen que respetar las mayusculas y minusculas.


* Podemos realizar manipulaciones y búsquedas de archivos, básandonos en el 'string' que conforma el nombre del archivo, incluyendo la extensión de este.
* El wildcard '*' define una sola posición de lateralidad del nombre del archivo que querermos manipular o buscar.
    - Funcionan con comandos de búsqueda, como 'ls', y con comandos de manipulacion de archivos, como: 'mv' 'cp' y 'rm'.
* La sintaxis es un asterisco (*):
                                Archivo a manipular o buscar. 'palabra.extension', se realiza como [palabra*] o [*.extension].

Sintaxis de un comando compuesto con el Wildcard '*':
    [comando que realice la búsqueda o manipulación] [string*] [ruta/directorio]
    [comando que realice la búsqueda o manipulación] [*string] [ruta/directorio]

    Como por ejemplo, archivos que tengan un mismo carácter:
            ls *.js
                (cuando queremos ver solo los archivos .js o Javascript que se encuentran en la carpeta)

            ls repo*
                (cuando queremos ver solo los archivos que comiencen con el nombre "repo")
                
            mv *.js ../directorioDeBackup
                (cuando quieres mover archivos .js a una carpeta que se encuentra en la carpeta padre, da un paso hacia atrás)

            mv ./html/*.html .
                (cuando quieres traer archivos .html de la carpeta 'html' hacia acá)
                -Siempre es necesario agregar el operador '.' cuando queramos iniciar la ruta, desde el directorio actual.

            mv ../clase* ./clases/
                (cuando queremos mover solo los archivos que empiezan con el string 'clase', hacia una carpeta llamada 'clases/')


Wildcard '?'
    Sirve para realizar coincidencias estrictas, en busquedas y manipulacion de archivos.

    '?' se convierte en cualquier tipo de caracter para que el comando de busqueda o manipulacion, ejecute una lista de archivos que coincidan.
        - Como decir,
                        buscar anios 2019 < 202x = 'ls 202?'
                        buscar todos los archivos de los anios 2000 = 'ls 2???'
        * Podemos declarar todos los '?' que sean necesarios, ?????..., para la busqueda o manipulacion.
    Por ejemplo, si en una carpeta tenemos los archivos:
                                                        'hola1.js', 'hola2.js', 'hola3.js', 'hola4.js', 'hola5.js', 'hola5.1', 'hola5.2', 'hola6'.
    Y queremos eliminar solo los archivos copias de hola5, sean '5.1' y '5.2', tenemos que ejecutar el siguiente comando:
                                                                                                                    rm -iv hola5.?.js
        - Esto borrará solo los archivos 'hola5.1.js' y 'hola5.2.js'.



Flags/Options:
    
    -d
        Sirve para seleccionar solo los archivos de la carpeta actual en la que nos encontramos.



Clases:

'[...]'
    '[]' : Podemos introducir, entre los corchetes, caracteres especificos que queremos buscar o manipular, filtrando asi una lista que contengan los caracteres que hemos declarado.
    
    Ejemplo:
            La carpeta 'dir' contiene los siguientes archivos: 'arch1.sh', 'arch2.sh', 'arch3.sh', 'arch4.sh', 'arch5.sh' y 'arch6.sh'.
            
            -   Si queremos realizar la busqueda de solo los archivos 'arch3.sh' y 'arch4', tenemos que ejecutar el siguiente comando:
                                                            'ls arch[34].sh'

    * No es necesario separar los caracteres que van dentro de '[ ]' con alguna coma, guion o algo similar.
        - Los caracteres no se separan con nada.


'[[:upper:]]*'
    Clase que sirve para seleccionar solo los archivos y directorios que comiencen con mayúscula, *Y QUE COMIENCEN EL NOMBRE CON NÚMERO*.

'[[:upper:]]*/'
    Clase que sirve para seleccionar solo los directorios del directorio actual, que comiencen en Mayúscula, *añadiendo todos los archivos que contienen los directorios seleccionados, sean archivos y directorios, solo los que cumplan con la regla de '[[:upper:]]*', *Y QUE COMIENCEN EL NOMBRE CON NÚMERO*.
    - Solo funciona para dos niveles en el arbol de directorios, contando desde el directorio actual, hacia adelante; directorios del directorio actual y todos tipo de contenido que contengan estos directorios, pero solo muestra a los hijos.
        Ejemplo:
        Cuando querermos buscar solo los directorios que comiencen en mayuscula, y en nuestro directorio actual tenemos lo siguiente:
                Dir1/:
                    Arch1.js
                    Gool/
                Dir2/:
                    Arch2.js
                    Pool/:
                        Arco/
                        Barco/
                        Bote.js
                di3/:

        Ejecutamos el comando: ls [[:upper:]]*/
            Nos mostrara solo estos datos: El primer nievel, o sea el actual, y el siguiente, los hijos. No mostrará el contenido de los hijos.
                Dir1/:
                    Arch1.js
                    Gool/
                Dir2/:
                    Arch2.js
                    Pool/

'-d [[:upper:]]*'
    Clase que sirve para seleccionar todos los archivos que comiencen con la primera letra del nombre en mayuscula, sean archivos/files o directorios, y que solo se encuentren en la carpeta actual.

'-d [[:upper:]]*/'
    Clase que sirve para seleccionar solo los directorios que comiencen con la primera letra del nombre en mayuscula, y que solo se encuentren en la carpeta actual.



'[[:lower:]]*'dd
    Clase que sirve para seleccionar solo los archivos/files o directorios que comiencen con la primera letra del nombre en minúscula, *Y QUE COMIENCEN EL NOMBRE CON NÚMERO*.

'[[:lower:]]*/'
    Clase que sirve para seleccionar solo los directorios que tengamos en el directorio actual, que solo comiencen con la primera letra de su nombre en minúscula, *añadiendo todos los archivos que contienen los directorios seleccionados, sean archivos/files y directorios, solo los que cumplan con la regla de '[[:lower:]]*', *Y QUE COMIENCEN EL NOMBRE CON NÚMERO*.
    - Solo funciona para dos niveles en el arbol de directorios, contando desde el directorio actual, hacia adelante; directorios del directorio actual y todos tipo de contenido que contengan estos directorios, pero solo muestra a los hijos.
        Ejemplo:
        Cuando querermos buscar solo los directorios que comiencen en minúscula, y en nuestro directorio actual tenemos lo siguiente:
                dir1/:
                    Arch1.js
                    gool/
                dir2/:
                    Arch2.js
                    pool/:
                        arco/
                        Barco/
                        bote.js
                dir3/:
                    12.js
                    57/:
                        atr.sh
                    111.js
                    ab/:
                        123.js
                Di4/:
                
        Ejecutamos el comando: ls [[:upper:]]*/
            Nos mostrara solo estos datos: El primer nievel, o sea el actual, y el siguiente, los hijos. No mostrará el contenido de los hijos.
                dir1/:
                    Arch1.js
                    gool/
                dir2/:
                    Arch2.js
                    pool/
                dir3/:
                    12.js
                    57/
                    111.js
                    ab/

'-d [[:lower:]]*'
    Clase que sirve para seleccionar todos los archivos que comiencen con la primera letra del nombre en minúscula, sean archivos/files o directorios, y que solo se encuentren en la carpeta actual.

'-d [[:lower:]]*/'
    Clase que sirve para seleccionar solo los directorios que comiencen con la primera letra del nombre en minúscula, y que solo se encuentren en la carpeta actual.