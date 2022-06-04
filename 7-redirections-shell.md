Las entradas de comandos que pasan por la Shell.

File descriptors: 0, 2, 3
    Numeros o codigos que maneja la terminal para referirse a los procesos  de uso.


Standards:
    Standard Imput - stdin (0)
    Las entradas de comandos, naturalmente provienen desde nuestro teclado, pero tambi[en podemos realizarlas desde archivos de texto.

    Standard Output - stdout (1)
    Proceso que muestra un retorno cualquiera, ejemplo, lista de archivos cuando ejecutamos el comando 'ls'.

    Standard Error - stderr (2)
    Proceso que muestra un mensaje de error, en un retorno.

* Ambos retornos son manejados por diferentes vias.



Redirectors, simbolos:
    > :
        Sirve para guardar nombres de archivos en un archivo de texto.
        No concatena, solo lo sobreescribe.

    >> :
        Sirve para guardar nombres de archivos en un archivo de texto.
        *Sí concatena*, solo lo sobreescribe.


Sintaxis de ejemplo:
    ls archivo-que-no-existe > archivo-de-texto.txt

        - Lo que sucede ahi, es que el retorno de información, la lista de archivos que debería mostrarse en la pantalla, termina trasladándose a dentro dal archivo de texto que hemos declarado.
        - No se mueve nada de texto, ni archivos, solo es el retorno que se muestra al ejecutar ese comando.
        * Cuando no existe el archivo de texto que hemos escrito, donde debería de guardarse la información que retorna, la Shell lo crea automáticamente.