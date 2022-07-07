Temas:
terminar aprocesos
visualizar
manejar
filtrar

Comandos (Solo nos mostrará los procesos que tenemos en Ubuntu, más no los procesos que tengamos en Windows, ya que Windows no se lo permite)

* Cuando un proceso está en ejecución, en segundo plano, se dice que se está ejecutando en el "background".
* Si la ejecución del comando se muestra en primer plano, se dice que está en "foreground".

ps
    Nos muestra los procesos o comandos que estan corriendo actualmente en la Terminal.

    PID:
        Significa "Process ID".
        Es el "ID" o "numero ID" del programa o comando, con el cual podremos interactuar, detener, visualizar o filtrar.


top
    Nos muestra todos los procesos que estan en segundo plano, en una lista de procesos, catalogados por el consumo de recursos.
    'h'
     Nos retorna la pantalla de ayuda, donde muestra todos los comandos que incluye el programa.
    'u'
     Sirve para filtrar por usuario.

/*

htop:
    Funciona muy similar a "top", pero con una interfaz mas amigable al usuario, incluyendo colores, más filtros y opciones.

Instalar "htop"
    'sudo apt install htop'

Iniciar programa "htop"
    'htop'

/

Terminar procesos:
    kill [PID]