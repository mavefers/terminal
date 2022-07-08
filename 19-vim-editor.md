vim
    editor de texto entro de la Terminal

* Para *ingresar al editor* "VIM", solo necesitas ejecutar el comando 'vim' dentro de la Terminal.
* Para salir de "VIM", solo teiens que apretar ":" + "q" y el botón "Enter".

* Para *crear un archivo* usando "VIM", solo debemos agregar el nombre del archivo que vamos a crear, al comando 'vim'.
    Comando:
        vim [nombre-del-archivo-de-texto-plano.extension]
    
    Ejemplo:
        vim index.html

* Para *comenzar a escribir / modo editor* en el editor "VIM", debemos apretar el botón "I" del teclado.

* Para dejar de escribir en el editor "VIM", debemos apretar el botón "Esc" del teclado.
    Así tendremos la oportunidad de navegar dentro del editor "VIM".

* Para *realizar una búsqueda* de alguna palabra dentro de nuestro documento en "VIM", solo debemos apretar el botón "/", y nos enviará al apartado de búsqueda. En el apartado de búsqueda, que se encuentra en el lado inferior, podremos realizar búsqudas por palabras.
    Por ejemplo: /hey!
                 /the
                 /Hello!
                 /is
        Si llega a haber más de una coincidencia en la búsqueda, demos volver a realizar la búsqueda, con los mismos datos, para saltar de coincidencia en coincidencia.

* Para *eliminar* una linea de nuestro documento, de un solo golpe, debemos presionar el botón "D", dos veces. [DD]/[dd]

* Para *guardar* el avance de un documento dentro de "VIM", debemos *salir del modo editor* con la tecla "Esc", presionar los botones ":" y "w", y luego "Enter". [:w]

* Para *guardar el avance de un documento dentro de "VIM" y luego salir*, debemos *salir del modo editor* con la tecla "Esc", presionar los botones ":", "w" y "q",y luego "Enter". [:wq]

* Para realizar cambios forzados, se escribe el signo "!" después de escribir la ejecucion, por ejemplo: [:q!].