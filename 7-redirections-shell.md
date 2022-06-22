Las entradas de comandos que pasan por la Shell.

File descriptors: 0, 1, 2
    Numeros o codigos que maneja la terminal para referirse a los procesos de uso.


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
        - Sirve para guardar respuestas o retornos de una petición a la Terminal, en un archivo de texto.
        - *No concatena*, solo lo sobreescribe.
        - Revisa si ya hay un archivo existente, y si no hay, lo crea y luego ejecuta el comando que generará la petición, para pasar a guardar la información en el archivo que se ha creado.

    >> :
        Sirve para guardar la respuesta o retorno de una petición de la Terminal, en un archivo de texto.
        *Sí concatena*, no sobreescribe.
    
    - Tener mucho cuidado con '>' porque podemos sobreescribir texto, eliminando el texto que ya se había almacenado anteriormente.


Sintaxis de ejemplo:
    ls archivo-que-no-existe > archivo-de-texto.txt

        - Lo que sucede ahí, es que el retorno de información, la lista de archivos que debería mostrarse en la pantalla, termina trasladándose a dentro del archivo de texto que hemos declarado.
        - No se mueve nada de texto, ni archivos, solo es el retorno que se muestra al ejecutar ese comando.
        * Cuando no existe el archivo de texto que hemos escrito, donde debería de guardarse la información que nos retorna, la Shell crea el archivo automáticamente.


Redirigiendo Standards, de Standard Output (1) a Standard Error (2), y de Standard Error (2) a Standar Output (1):
    Para redirigir la salida de Standard Output (stdout) a Standard Error (stderr):
        a) X 1> Y
        b) Y 1>> Z
    Para redirigir la salida de Standard Error (stderr) a Standard Output (stdout):
        a) X 2> Y
        b) Y 2>> Z
    

- Aquí se redirige el retorno de información, de una vía hacia otra.


Para redirigir la informacion del retorno hacia dos vías, sin importar que la salida del retorno sea Output o Error, se necesita agregar este fragmento de texto en el código:
        * 2>&1 *
    - Así se redirige el retorno, hacia las dos vías, Standard Output y Standard Error.
    - Sirve cuandodo no sabemos si el retorno es un Output o un Error.
    - Sintaxis ejemplo:
                        ls asjdkhasjkd > nota.txt 2>&1
                        ls user >> nota.txt 2>&1
    - Nos ayuda para revisar posteriormente los errores, almacenarlos en un archivo, repasarlos y aprender de ellos.

//

    < :
        Sirve para redirigir de un Standard Output a un Standard Input.
        Hacen uso de la funcionalidad Input para mostrarlo en Standard Output.
        Comandos que nos permiten explorar texto: cat, less, head, etc.
    Ejemplo:
        cat < texto.txt