Comprimiendo archivos.

Formatos de compresion:

.tar (son muy usados para comprimir repositorios)

comando: tar
Sintaxis:
    tar [opciones] [el-que-sera-el-archivo-comprimido.tar] [archivo-a-comprimir]

    opciones:
        -c = create//crear un archivo
        -v = verbose// Nos muestra, en la Terminal, todo lo que estuvo comprimiendo // lista todos los ficheros que trata//verbosely list files
        -f = sirve para indicar que nos retorne un file.

        -z = gzip// se encarga de procesar el archivo con gzip // gzip es una mejora de la compresion *tar*
            gzip: es un algoritmo de compresion bastante eficiente, se recomienda usarlo para la mayoria de los archivos de texto plano, como lo son "repositorios de codigo".
            Sintaxis: (solo cambia la extension del archivo a comprimido, agregandole '.gz' al final)
                tar [-cvzf] [el-que-sera-el-archivo-comprimido.tar.gz] [archivo-a-Comprimir]

/

    Para descomprimir:
        Se sustituye la opciones (-c) por '-x'.
            -x = excluye los ficheros/archivos creados en file.
        Sintaxis:
            tar [-xvzf] [el-que-sera-el-archivo-comprimido.tar.gz]

/

.zip
(
    viene instalado en todas las distribuciones, tanto en Linux como en Mac. Si no esta instalado en tu distribucion de Linux, se puede instalar con el manejador de paquetes: Ubunto > 'apt', Fedora/RedHat > 'dnf', ArchLinux > 'pacman'
)

comando: zip
Sintaxis:
    zip -r [el-que-sera-el-archivo-comprimido.zip] [archivo-directorio-a-Comprimir]

    opciones:
        -r = recursiva
/

    Para descomprimir:
        ejecuta el comando 'unzip', seguido del archivo comprimido.
        Sintaxis:
            unzip [directorio-comprimido.zip]

/

.rar (mismo proceso que zip)

comando: rar
Sintaxis:
    rar -r [el-que-sera-el-archivo-comprimido.rar] [archivo-directorio-a-Comprimir]

    opciones:
        -r = recursiva

/

    Para descomprimir:
        Se ejecuta el comando 'unrar', seguido del archivo comprimido.
        Sintaxis:
            unrar [directorio-comprimido.rar]