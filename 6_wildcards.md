Wildcards

Es una serie de carácteres que nos permiten encontrar patrones y realizar busquedas más avanzadas.

Sirve para realizar manipulaciones en base a ciertos patrones.

Podemos realizar manipulaciones y búsquedas, básandonos en la extensión o tipo de archivo o documento.
La sintaxis es un asterisco : *.extension
    Como por ejemplo:
        La declaración de extensiones:
            ls *.js
                (cuando queremos ver solo los archivos .js o Javascript que se encuentran en la carpeta)
        Archivos que tengan un mismo carácter:
        -    mv *.js ../directorioDeBackup
                (cuando quieres mover archivos .js a una carpeta que se encuentra en la carpeta padre, da un paso hacia atrás)
        -    mv ./html/*.html .
                (cuando quieres traer archivos .html de la carpeta 'html' hacia acá)
                -Siempre es necesario agregar el operador '.' cuando queramos iniciar la ruta, desde el directorio actual.

Podemos realiz

Sintaxis:
    [comando que realice manipulación] *[wildcard] [ruta/directorio]
