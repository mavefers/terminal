Variables de Entorno
    Definición y Modo de uso.

Son como variables predeterminadas por parte del sistema, donde guardan como valor, información relevante del sistema.
Sirven para acceder a la configuración y a los diferentes valores del sistema.

//

Links simbólicos:
    Son accesos directos desde la terminal.
    Son un tipo de archivos que hacen referencia a un lugar.

ln = link
-s = simbolico

Sintaxis:
    ln -s [ruta/] [nombreDelLink]

/

Los links simbólicos como tal, no tienen permisos.

//

Comando para conocer la configuración y valores del sistema, de las variables de Entorno.
    'printenv'

/

Una vez conocido el nombre de la variable, ya podemos...
    Imprimir variables de entorno:
        'echo $[nombreDeLaVarible]
    
    Ejemplos de variables de entorno:
        $HOME   >>>     nos muestra la ruta del user. Nos sirve para configurar alguna ruta específica.
        $PATH   >>>     nos muestra todas las rutas de los binarios que ejecutan nuestro sistema. Funciona cuando usamos Pearl o NodeJS
                        La variable $PATH es muy importante para ver los binarios que llevan los manejadores de paquetes.
                        - Los manejadores de paquetes son los encargados de traer un repositorio e instalar algún binario, todo dentro de la computadora. Algunos manejadores de paquetes: APT, DNF, NVM, Node, Python.
                        No todas las rutas de los binarios de los paquetes que se pretenden extraer e instalar, se encuentran listos para su función. Normalmente nos piden que agreguemos las rutas a la variable $PATH
                        -Path es una variable de entorno que me muestra la ubicación de nuestros archivos binarios.

/

CREAR UNA VARIABLE DE ENTORNO:
    Normalmente el nombre de la variable, se escribe con mayuscula.
    NOMBRE_DE_VARIABLE="Say hi!"

    USER_MESSAGE="Hola amigos"

/

Crear un alias, ejemplo:
    alias l='ls -lh'

    Funciona dependiendo del trabajo constante que estés realizando, por ejemplo, cuando usamos constantemente Git, podemos codificar rápido creando *alias*.
    -No lo recomiendo para principiantes, solo para personas con experiencia.

    Si vamos a usar alias debemos tener cuidado con no asignar un nombre de algún comando que ya exista.

/

* Editar el valor de $PATH para agregar una ruta hacer funcionar correctamente un programa compilado.

PATH=$PATH:/rutaparaaniadir

Los dos puntos ':', funcionan como suma '+'.

Tener mucho cuidado al modificar el valor de PATH, ya que de eso dependen muchos programas que hayamos instalado anteriormente.