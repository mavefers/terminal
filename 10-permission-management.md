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



drwxrwxrwx


-rwxrwxrwx
-(type)rwx(owner)rwx(groupUsers)rwx(otherUsers)