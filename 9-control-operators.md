Operadores de control
    Son símbolos reservados por la Terminal ('&' y ';'), que nos permiten ejecutar más de un comando, o encadenar comandos. Nos permite correr comandos de manera síncrona o asíncronamente, e incluso con condicionales.
Ejemplos de uso:
    - Crear una carpeta y luego movernos a ella.
    - Para configurar que un comando se ejecute exitosamente, luego de un segundo.

//

Correr comandos de manera síncrona:
    - Son comandos que se van ejecutando, uno detrás de otro, como una cadena.
    -Se separan con el signo de punto y coma (;).
    Ejemplo:
        ls; mkdir hola; cal
            - Aquí, lo que estamos realizando es: 1. Un retorno de la lista de archivos. 2. Luego se crea el directorio "hola". 3. Para último generar una solicitud de calendario, usando el comando 'cal'.
            - Se respeta el orden en la ejecución.

//

Correr comandos de manera asíncrona:
    - Son comandos que se ejecutan al mismo tiempo, al haberse creado Shells en segundo plano, creados por hilos del procesador, según la cantidad de comandos que hemos ejecutado de manera asíncrona.
    - Se separan con el signo 'ampersand' (&).
    Ejemplo:
        ls & date & cal
            - Aquí, lo que se está realizando es un proceso múltiple, en paralelo, donde se ejecuta: 1. la visualización de la lista de archivos. 2. la fecha. 3. y la solucitud del calendario.
    
    - Cuando se ejecutan comandos de manera asíncrona, la terminal genera Hilos/Threads de proceso para ejecutar los comandos, de manera independiente.

//

Correr comandos de manera *condicional*.
    - Se ejecuta el comando si, y solo si, el comando anterior se ejecutó correctamente, de lo contrario, "la cadena se rompe" y se dejará de ejecutar los comandos siguientes.
    - Los comandos redactados se separan con el signo 'ampersand', escrito de manera doble (&&).
    - En *comparación* con la ejecución de *comandos* de manera *síncrona* y *asíncrona*, cuando es *condicional* se respeta la correcta *ejecución* de los comandos, de *manera estricta*.

    Example:
        mkdir conditional-test && cd test
            - Aquí se crea un directorio, "conditional-test", y luego se ingresa al directorio creado.
        
        cd directorioQueNoExiste && date && cal && ls -a
            - Aquí se está intentado ingresar a un "directorio que no existe", y como sale un error, los siguientes comandos no se ejecutarán.

//

Operador "or":
    - Nos permite ejecutar solo el primer comando de la cadena, que pase por el Standard Output (stdout).
    - No importa la cantidad de comandos que tengamos en la cadena, si están separados por el operador '||', solo se efectuará el primero que se ejecute de forma correcta, descartando todos los comandos restantes.
    - Cuando en un inicio solo se ejecutan comandos de manera incorrecta, la cadena seguirá activa hasta que se encuentre el comando que se ejecute de manera correcta, y ahí finaliza la ejecución de la linea de comando.

    Example:
        cd ashjdkadh || touch text.pdf || date
            - Aquí se está intentando ingresar a un directorio que no existe, por ende es un error, así que pasa al siguiente comando, touch, donde se intenta crear un archivo 'text.pdf', y como se ejecuta de manera exitosa, finaliza la ejecución de la linea de comando.

//
Challenge:
    cd asjkdhak || touch file-x.txt || echo "The file was created."
        - Por lógica, en esta cadena de comandos, solo se ejecutará el comando 'touch file-x.txt'.
        - El reto es también poder ejecutar el comando 'echo "The file was created"'.
    
Problem solution:
    - En base a la lógica de los "redirections", podemos deducir que el operador 'or', (||), solo admite el primer comando que pase por el Standard Output (stdout), el resto de comandos, sea que pasen por el Standard Output (stdout) o Standard Error (stderr), el operador || siempre los convertirá a stderr, por defecto.
    Entonces, nosotros, forzadamente tenemos que convertir los siguientes comandos que ya no son admitidos por pasar a ser "stderr", a "stdout", redirigiendo su "File descriptor" a (1), para que sea admitido.
    - En un inicio, podemos deducir que ocultamente los "File descriptors" lucen así:
    cd asjkdhak (2) || touch file-x.txt (1) || echo "The file was created." (1)
    - Pasando a ser así:
    cd asjkdhak (2) || touch file-x.txt (1) || echo "The file was created." (2)
    - Por lo tanto, tenemos que redirigirlo de la siguiente manera:
    cd asjkdhak || touch file-x.txt 1|| echo "The file was created."

Cito: '7-redirections-shell.md'
Redirigiendo Standards, de Standard Output (1) a Standard Error (2), y de Standard Error (2) a Standar Output (1):
    Para redirigir la salida de Standard Output (stdout) a Standard Error (stderr):
        a) X 1> Y
        b) Y 1>> Z
    Para redirigir la salida de Standard Error (stderr) a Standard Output (stdout):
        a) X 2> Y
        b) Y 2>> Z

//

Webpack, es un empaquetador de archivos de diferentes lenguajes de programacion.