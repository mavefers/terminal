Comandos / Commands

echo
- genera un standard output (stdout), en la Terminal, de cualquier cosa que le escribamos.
Ejemplo:
    echo "hey! What's up? This is the command 'echo'"
        hey! What's up? This is the command 'echo'
-Prácticamente sirve para imprimir todo tipo de texto, pasándolo como string.


cat
- Sirve para visualizarla información de un archivo, en Terminal, y concatenar la información de dos o más archivos en stdout / Standard Output. También podemos redirigir la información de salida, hacia un nuevo o existente archivo, usando el operador ">".
Ejemplo:
    cat list1.txt list2.txt > list1-2.txt


tee
    Funciona igual a la redirección '>'.



//

Pipe Operator '|'
    Nos permite convertir el Standard Output en el Standard Input de otro comando.
    El pipe operator '|' hace que el *stdout* de un comando sea el stdin de otro comando.
    - Es usado para generar filtros, cuyos retornos pasan de un comando hacia otro.

Sintaxis:
    comando(Stdin/Stdout) |(Stdin) comando(Stout) |(Stdin) comando(Stdin) |(Stdin) comando(Stdout) ...
Ejemplo:
    ls -l | tee nuevo-archivo.txt | less


//

cowsay
    sudo apt install cowsay
    'cowsay -l'
lolcat
    sudo apt-get update
    sudo apt install lolcat

- Hay comandos que no se ejecutan correctamente cuando pasan por el Standard Output (stdout). Uno de esos comandos es 'lolcat', cuya función es dotar de colores la información que nos retorna la Terminal.
Ejemplo:
    ls | lolcat | tee lista.txt
- Entonces, la mejor manera de usar el comando 'lolcat' es al final de la concatenación de códigos.
Ejemplo:
    ls | tee lista.txt | lolcat