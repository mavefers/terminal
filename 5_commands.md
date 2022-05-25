¿QUÉ ES UN COMANDO?
    - Un *programa ejecutable*.
        Se compilo en algun lenguaje de programacion, y nosotros lo podemos ejecutar.
        Los ejecutables usualmente se guardan en la ruta: /user/bin
    - Un *comando de utilidad* de la Shell.
        La Shell es un programa en sí, y dentro de los programas, suelen tener funciones.
        Son comandos que ya vienen dentro, por defecto, del programa Shell.
    - Una *funcion de Shell*, que no viene incluido en la instalacion de la Shell.
        Son funciones externas a la Shell que estamos usando.
    
    - Un alias
        Es la manera de crear un nuevo comando, que almacenará un comando, por dentro, o una estructura de comando.


Comando 'type'
    type [comando]
        Nos permite ver la clase de comando que es.
        Ejemplo: 'type ls'
            return: ls is aliased to 'ls --color=auto'
    

Commands/Comandos:
    alias [comandoNuevo="comandoGuardado"]
        Sirve para crear un nuevo comando, que guardará un comando o una estructura de comando, ya existente.
        Ejemplo: 'alias t="ls -a"', para ejecutar el comando 'ls -a', solo debemos ejecutar el comando 't'.
        -Solo son temporales, duran hasta que se cierra la terminal. Se guardar con una configuracion especial.
        -Es un comando muy útil.

    help [comando]
        Sirve para solicitar informacion de uso del comando que estamos declarando.
        -'help' es un comando de utilidad de Bash, puede no funcionar en otro tipo de Shell que no sea BashShell.
    [comando] --help
        Sirve para solicitar informacion de uso del comando que estamos declarando.
    
    man [comando]            (man = manual de usuario)
        Sirve para solicitar un manual de usuario, o manual de uso, de un comando.
        Retorna:  La sinopsis, descripcion, ejemplos de uso, manual de uso.
        Nos lleva a una interfaz independiente.
        -Es un comando muy util.
        -Debemos apretar el boton 'q' de quit, para salir de la interfaz.
    
    info [comando]
        Es un comando similar a 'man', pero de una manera mas resumida. Solo cambia el tipo de interfaz.
        Nos lleva a una interfaz independiente.
        -Debemos apretar el boton 'q' de quit, para salir de la interfaz.

    whatis [comando]
        Nos muestra en una linea, una descripción muy corta de la función del comando que hemos elegido.
        -No funciona para todos los comandos.
        -Es un comando binario.
    
    echo "Texto a imprimir."
        Sirve para imprimir texto.
        -Se recomienda no escribir doble signo de exclamacion (!!), porque crea un error al imprimir.
    
    echo $SHELL
        Muestra el tipo de Shell que estamos usando.
        
    echo $0
        -Sirve para ver qué Shell estamos usando.
        Muestra el nombre del proceso que se está ejecutando. Si lo usa dentro de una terminal, devolverá el nombre de la terminal. Si lo usa dentro de un script, será el nombre del script.


* Algunos comandos no tienen manual de referencia.