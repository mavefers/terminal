Manejo de permisos desde la Terminal


'> mitexto.txt'
    Al ejecutar este comando, estaras creando el documento "mitexto.txt". Funcionaria como el comando 'touch', ya que, al ejecutar el operador '>', y no existe el documento donde se reservará la información, la terminal lo crea automáticamente.

        1. [vacio] > lugar-de-reserva.txt
        2. "Archivo creado".
        =
        a. touch lugar-de-reserva.txt
        b. "Archivo creado".


//

Dar permisos y quitarlos, en la Terminal

Para dar permisos se necesita ejecutar el comando 'chmod'.
    Sintaxis:
        chmod [permisos-de-manera-octal-owner-group-others] [archivo-de-texto]
    
    Ejemplo:
        chmod 755 mitexto.txt

        Dándole permiso total, lectura(r) , escritura(w) y ejecución(x), al owner, permiso de lectura(r) y ejecución(x) al group, y permiso de lectura(r) y ejecución(x) a others.

/
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

Quitar permisos al usuario, en la Terminal.

Sintaxis:
    chmod u-[permiso] [archivo-de-texto]

Ejemplo:
    chmod u-r documento.pdf
        El '-' funciona como resta hacia el usuario, que es representado como 'u', que en este caso viene a restar el permiso 'r' de read/lectura.

    chmod u-x documentoX.pdf
        El '-' funciona como resta hacia el usuario, que es representado como 'u', que en este caso viene a restar el permiso 'x' de execute/ejecución.

//

Agregar permisos al usuario, en la Terminal.

Sintaxis:
    chmod u+[permiso] [archivo-de-texto]

Ejemplo:
    chmod u+w documentoY.doc
        El '+' funciona como suma hacia el usuario, que es representado como 'u', que en este caso viene a sumar el permiso 'w' de write/escritura.

    chmod u+r documentZ.doc
        El '+' funciona como suma hacia el usuario, que es representado como 'u', que en este caso viene a sumar el permiso 'r' de read/lectura.

//

Sobrescribir permisos: Sobrescribe los permisos de uno o más modos de permisos. Cuando son más de un modo de permiso, estos se escriben todo junto, sin espacios.
    Sintaxis:
        chmod [modomodos]=[permiso]
            El operador '=' funciona para sobrescribir.

    Ejemplo:
        chmod go=r
    
/

Cuando se ejecuta una combinación de comandos para agregar, quitar, o sobrescribir permisos, se ejecuta de la siguiente manera.
    Las operaciones se separan con coma (,) y se escriben juntos, sin espacio.

    Sintaxis:
        chmod [modo][operador][permiso],[modomodos][operador][permiso] [archivo-de-texto]
    
    Ejemplo:
        chmod o-r,ug=rwx documentoA.pdf


//

Comando 'whoami', que se traduce del inglés como "quién soy".
    Sirve para saber el nombre del user/usuario.