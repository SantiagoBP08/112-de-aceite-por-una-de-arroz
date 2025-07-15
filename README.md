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

## 2. Procesar el archivo y extraer:


