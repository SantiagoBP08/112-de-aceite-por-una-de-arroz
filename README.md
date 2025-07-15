# RETO #11
## 1. Consulte que hacen los siguientes métodos de cadenas en Python: termina con, comienza con, isalpha, isalnum, isdigit, isspace, istitle, islower, isupper.

¿Qué hace endswith() o "termina con"?
Verifica si una cadena termina con un determinado substring (subcadena).
Retorna: True si termina con ese substring, False si no.

    cadena = "Hola mundo"
    print(cadena.endswith("mundo"))  # True
    print(cadena.endswith("Hola"))   # False

¿Qué hace startswith() o "empieza con"?
Verifica si una cadena comienza con un determinado substring.
Retorna: True si empieza con ese substring, False si no.
    
    cadena = "Hola mundo"
    print(cadena.startswith("Hola"))   # True
    print(cadena.startswith("mundo"))  # False
 
¿Qué hace isalpha()?
Comprueba si todos los caracteres de la cadena son letras del alfabeto (no permite espacios, números, ni símbolos).
Retorna: True si solo hay letras, False si hay otros caracteres.

    cadena = "Python"
    print(cadena.isalpha())  # True

    cadena = "Python3"
    print(cadena.isalpha())  # False

¿Qué hace  isalnum()?
Verifica si todos los caracteres son letras o números (no permite espacios ni símbolos).
Retorna: True si son letras o números, False si no.

    cadena = "Python3"
    print(cadena.isalnum())  # True

    cadena = "Python 3"
    print(cadena.isalnum())  # False (espacio)

¿Qué hace isdigit()?
Comprueba si todos los caracteres son números (dígitos).
Retorna: True si todos son números, False si hay algo diferente.

    cadena = "12345"
    print(cadena.isdigit())  # True

    cadena = "123a"
    print(cadena.isdigit())  # False


¿Qué hace isspace()?
Verifica si todos los caracteres de la cadena son espacios en blanco (espacio, tabulaciones \t, saltos de línea \n...).
Retorna: True si son solo espacios, False si hay algo más.

    cadena = "   "
    print(cadena.isspace())  # True

    cadena = " hola "
    print(cadena.isspace())  # False

¿Qué hace istitle()?
Comprueba si cada palabra de la cadena comienza con una letra mayúscula y las demás son minúsculas.
Retorna: True si está en formato título, False si no.

    cadena = "Hola Mundo"
    print(cadena.istitle())  # True

    cadena = "Hola mundo"
    print(cadena.istitle())  # False
    
¿Qué hace  islower()?
Verifica si todos los caracteres de la cadena están en minúscula.
Retorna: True si todos son minúsculas, False si no.

    cadena = "python"
    print(cadena.islower())  # True

    cadena = "Python"
    print(cadena.islower())  # False

¿Qué hace isupper()?
Verifica si todos los caracteres de la cadena están en mayúscula.
Retorna: True si todos son mayúsculas, False si no.

    cadena = "PYTHON"
    print(cadena.isupper())  # True

    cadena = "Python"
    print(cadena.isupper())  # False

## 2. Procesar el archivo (mbox.txt) y extraer:

codigo para Cantidad de vocales: (a,e,i,o,u)

    # Leer el archivo
    with open('mbox.txt', 'r') as archivo:
        texto = archivo.read().lower()  # Leer todo el archivo y pasar a minúsculas

    # Inicializar contador de vocales
    vocales = 'aeiou'
    contador_vocales = 0

    # Contar las vocales
    for caracter in texto:
        if caracter in vocales:
            contador_vocales += 1

    print(f'Cantidad total de vocales: {contador_vocales}')

codigo para Cantidad de consonates (b,c,d,f...)

    # Leer el archivo
    with open('mbox.txt', 'r') as archivo:
        texto = archivo.read().lower()

    # Inicializar contador de consonantes
    vocales = 'aeiou'
    contador_consonantes = 0

    # Contar las consonantes (letras que no son vocales ni espacios ni signos)
    for caracter in texto:
        if caracter.isalpha() and caracter not in vocales:
            contador_consonantes += 1

    print(f'Cantidad total de consonantes: {contador_consonantes}')

codigo para Listado de las 50 palabras que más se repiten:

    from collections import Counter

    # Leer el archivo
    with open('mbox.txt', 'r') as archivo:
        texto = archivo.read().lower()

    # Limpiar y separar las palabras
    for simbolo in '.,;:!?()"[]{}<>|/*\\=-_—\n':
        texto = texto.replace(simbolo, ' ')
    palabras = texto.split()

    # Contar palabras
    contador = Counter(palabras)

    # Obtener las 50 más comunes
    mas_comunes = contador.most_common(50)

    # Imprimir resultados
    print('Las 50 palabras más repetidas:')
    for palabra, cantidad in mas_comunes:
        print(f'{palabra}: {cantidad}')

Al ejecutar obtenemos como respuesta:

    Vocales: 1597835
    Consonantes: 2612121
    Palabras más frecuentes:
    from : 18126
    by : 18028
    with : 12756
    id : 12607
    dec : 9267
    nov : 8988
    for : 7714
    esmtp : 7188
    oct : 4164
    you : 3621
    murder : 3594
    smtp : 3594
    to : 2767
    the : 2544
    svn : 2528
    modify : 1884
    new : 1877
    this : 1877
    message : 1839
    was : 1834
    sakai : 1823
    at : 1822
    using : 1821
    can : 1821
    set : 1812
    my : 1811
    source : 1807
    notification : 1806
    how : 1802
    server : 1801
    sent : 1800
    receive : 1798
    workspace : 1798
    cmu : 1797
    sieve : 1797
    innocent : 1797
    automatic : 1797
    collab : 1797
    notifications : 1797
    sender : 1791
    apache : 1790
    jan : 1310
    in : 951
    thu : 791
    tue : 751
    fri : 639
    mon : 607
    u : 604
    wed : 589
    merge : 576

BIBLIOGRAFIA:

Documentación oficial de Python (Python.org)
https://docs.python.org/3/library/stdtypes.html#string-methods

W3Schools - Python Strings Methods
https://www.w3schools.com/python/python_ref_string.asp

GeeksForGeeks - String Methods in Python
https://www.geeksforgeeks.org/python-string-methods/

Programiz - Python String Methods
https://www.programiz.com/python-programming/methods/string

