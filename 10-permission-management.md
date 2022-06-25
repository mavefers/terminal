Tipos de archivos:

Atributos y su significado
- : Es un archivo normal.
d : Es un directorio.
l : Es un link simbólico.
b : Es un archivo de bloque especial. Son archivos que manejan la información de los bloques de datos, como algún archivo de una USB o de un disco duro externo.


"Los permisos nos permiten definir de una manera simple y efectiva las reglas de acceso como lectura (r), escritura (w) o ejecución (x), a determinados archivos o directorios."

- Tipos de permisos y sus funciones:
    r = read:
        (Archivo) Permite abrir y leer un archivo.
        (Directorio) Permite listar el contenido de un directorio, solo si el permiso de ejecución (x) también está activo.
    w = write:
        (Archivo) Permite escribir en un archivo; sin embargo, este atributo no permite cambiar el nombre de los archivos o poder eliminarlos. La capaidad de eliminar o editar el nombre de los archivos, está determinado por los atributos del directorio.
        (Directorio) Permite que los archivos dentro de un directorio sean creados, eliminados, y renombrados si también se establece el atributo de ejecución.
    x = execute:
        (Archivos) Permite que un archivo sea tratado como un programa y pueda ser ejecutado.
        (Directorio) Permite entrar al directorio.

//

Modos de permisos:
    Dueño
        - Persona que crea el grupo.
    Grupo
        - Un grupo, donde los archivos se comparten entre los diferentes usuarios pertenecientes al clan.
        - Un ejemplo claro, sería como compartir un archivo de música, de una computadora hacia otra.
    World/Otros
        - Cualquiera que no sea perteneciente a los grupos anteriores.


r   w   x
1   1   1   -   cada "1" significa que el permiso está activo.

-   -   - 
0   0   0   -   cada "0" significa que el permiso está inactivo.

/

r-x
101   /   Significa que tiene el permiso de lectura (read) y el permiso de ejecución (execute), no tiene el permiso de escritura (write).

/

rwx
111   /   El "dueño" / "jefe" / "boss", el que tiene todos los permisos.


//

Representacion en Sistema de 3 bits:
    Representacion del Sistema Octal

    Permisos    Binario     Octal
    ---         000         0
    --x         001         1
    -w-         010         2
    -wx         011         3
    r--         100         4
    r-x         101         5
    rw-         110         6
    rwx         111         7


//
    Ejercicios

Dueño
    rwx
    111
        7
Group
    r-x
    101
        5
World
    r-x
    101
        5


//

Modo simbólico:
    Símbolo
    u   :   Solo para el usuario.
    g   :   Solo para el grupo.
    o   :   Solo para otros (que no sean usuarios, ni grupo)/ World.
    a   :   Aplica para todos.