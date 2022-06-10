Operadores de control
    Son símbolos reservados por la Terminal, que nos permiten ejecutar más de un comando, o encadenar comandos. Nos permite correr comandos de manera síncrona o asíncronamente, e incluso con condicionales.
Ejemplos de uso:
    - Crear una carpeta y luego movernos a ella.
    - Para ver que un comando se ejecute exitosamente, y luego 

//

Correr comandos de manera síncrona:
    - Son comandos que se van ejecutando, uno detrás de otro, como una cadena.
    Ejemplo:
        ls; mkdir hola; cal
            - Aquí, lo que estamos realizando es: 1. Un retorno de la lista de archivos. 2. Luego se crea el directorio "hola". 3. Para último generar una solicitud de calendario, usando el comando 'cal'.
            - Se respeta el orden en la ejecución.

//

Correr comandos de manera asíncrona:
    - Son comandos que se ejecutan al mismo tiempo, al haberse creado Shells en segundo plano, creados por hilos del procesador, según la cantidad de comandos que hemos ejecutado de manera asíncrona.
    Ejemplo:
        ls & date & cal
            - Aquí, lo que se está realizando es un proceso múltiple, en paralelo, donde se ejecuta: 1. la visualización de la lista de archivos. 2. la fecha. 3. y la solucitud del calendario.