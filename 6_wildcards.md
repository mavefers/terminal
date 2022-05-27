Wildcards

Es una serie de carácteres que nos permiten encontrar patrones y realizar busquedas más avanzadas.

Sirve para realizar manipulaciones en base a ciertos patrones.


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