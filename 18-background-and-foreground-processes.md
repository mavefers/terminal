* Cuando un proceso está en ejecución, en segundo plano, se dice que se está ejecutando en el "background".
* Si la ejecución del comando se muestra en primer plano, se dice que está en "foreground".

Mover procesos que están en background, a foreground.

Primero tenemos que saber la diferencia entre 'Ctrl + C' y 'Ctrl + Z':
'Ctrl + C'
    lo que hace es finalizar o terminar el proceso indicado.
'Ctrl + Z'
    lo que hace es pausar o suspender momentaneamente un proceso, el cual despues lo podremos reanudar con el comando 'fg [numero-de-trabajo]'.

* Para consultar todos los procesos que tenemos en *background*, podemos hacerlo con el comando 'jobs'.
* En la lista mostrada, podrás observar los "números de trabajo" correspondientes a cada proceso en estado background.

Para reanudar un proceso que está en *background*, debemos usar el comando 'fg [numero-de-proceso]' (sin corchetes), para así mandarlo al *foreground*.

En caso se esté usando ZSH o ZBash como shell, al formato para definir el trabajo [numero-de-proceso] se le añaría un procentaje (%) antes del número. ZSH tiende a interpretar algunas cosas, incluyendo las wildcards, de manera diferente.
    'fg %[numero-de-proceso]'

/
Un ejercicio para poner en práctica estos datos, es el siguiente:
    Introducir el comando 'cat > archivodetexto.txt'.
    Escribimos el texto que querramos, luego apretamos la combinación "Ctrl + Z".
    Después, al introducir el comando 'jobs', podrás observar los procesos que están en el apartado del "background".