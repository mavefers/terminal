GREP.
    *Nos permite encontrar coincidencias de una búsqueda, dentro de cualquier archivo de texto.*
    - Nos sirve para realizar búsquedas profundas o específicas en archivos de gran magnitud.
    - Se pueden incluir wildcard como nombres de archivos. para realizar una busqueda mas compleja.

Sintaxis:
    grep [expresionRegular,palabraABuscar] [archivoDondeBuscar]
    grep [opcion] [expresionRegular,palabraABuscar] [archivoDondeBuscar]

Ejemplo:    '-i' significa "Ignore Key Sensitive".
    grep -i the movies.txt

/

Opciones de grep
    '-i', sirve para realizar una busqueda, y encontrar coincidencias sin importar las mayusculas y minusculas.
    '-c', nos retorna la cantidad de veces que aparece la palabra indicada en el archivo.
    '-v', retorna todos los textos que no coincidan con la palabra indicada.

    Podemos combinar opciones, ejemplo:  '-ci' o '-ic'.
        Asi, tambien con otras opciones.
    
//

Comando 'wc'
    Nos indica la cantidad de "lineas", "caracteres" y "bits" que tiene un archivo.

    Opciones:
        '-l', indica la cantidad de lineas que tiene el archivo.
        '-w', indica la cantidad de palabras.
        '-c', indica la antidad de bits.

    Sintaxis:
        wc [archivo]
            [lineas] [palabras] [bits] [archivo]
        
        wc [option] [archivo]
            [option] [archivo]