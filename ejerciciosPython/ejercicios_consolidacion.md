
# Ejercicio 1: Palabra más larga de una lista
def palabra_mas_larga(lista):
    mayor = ""
    for palabra in lista:
        if len(palabra) > len(mayor):
            mayor = palabra
    return mayor

print("Más larga:", palabra_mas_larga(["hola", "universidad", "sol", "informática"]))

# Ejercicio 2: Contar cuántas veces aparece cada vocal en una frase
def contar_vocales(frase):
    conteo = {"a": 0, "e": 0, "i": 0, "o": 0, "u": 0}
    for letra in frase.lower():
        if letra in conteo:
            conteo[letra] += 1
    return conteo

print("Vocales:", contar_vocales("Python es una herramienta educativa poderosa"))

# Ejercicio 3: Encontrar todos los divisores de un número
def divisores(n):
    resultado = []
    for i in range(1, n+1):
        if n % i == 0:
            resultado.append(i)
    return resultado

print("Divisores de 12:", divisores(12))

# Ejercicio 4: Determinar si un número es primo
def es_primo(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

print("¿17 es primo?", es_primo(17))

# Ejercicio 5: Extraer palabras únicas de una frase eliminando repeticiones
def palabras_unicas(frase):
    palabras = frase.lower().split()
    resultado = []
    for p in palabras:
        if p not in resultado:
            resultado.append(p)
    return resultado

print("Únicas:", palabras_unicas("Python es divertido y Python es útil"))

# Ejercicio 6: Sumar los elementos de una lista de listas
def suma_total(matriz):
    total = 0
    for fila in matriz:
        for num in fila:
            total += num
    return total

print("Suma total:", suma_total([[1, 2], [3, 4], [5, 6]]))

# Ejercicio 7: Convertir una frase en lista de palabras sin puntuación
def limpiar_frase(frase):
    import string
    for simbolo in string.punctuation:
        frase = frase.replace(simbolo, "")
    return frase.lower().split()

print("Limpio:", limpiar_frase("¡Hola, mundo! Python es genial."))

# Ejercicio 8: Invertir el orden de las palabras en una frase
def invertir_palabras(frase):
    palabras = frase.split()
    palabras.reverse()
    return " ".join(palabras)

print("Invertida:", invertir_palabras("Aprender Python es útil"))

# Ejercicio 9: Verificar si una lista está ordenada de forma creciente
def esta_ordenada(lista):
    for i in range(len(lista)-1):
        if lista[i] > lista[i+1]:
            return False
    return True

print("¿Ordenada?", esta_ordenada([1, 2, 3, 4]))
print("¿Ordenada?", esta_ordenada([3, 2, 1]))

# Ejercicio 10: Eliminar duplicados pero conservar el orden original
def sin_duplicados(lista):
    vistos = []
    for elem in lista:
        if elem not in vistos:
            vistos.append(elem)
    return vistos

print("Sin duplicados:", sin_duplicados(["a", "b", "a", "c", "b", "d"]))

# Ejercicio 11: Contar cuántas palabras tienen más de 5 letras
def palabras_largas(frase):
    contador = 0
    for palabra in frase.split():
        if len(palabra) > 5:
            contador += 1
    return contador

print("Palabras largas:", palabras_largas("Python es divertido y desafiante"))

# Ejercicio 12: Intercalar dos listas elemento a elemento
def intercalar(l1, l2):
    resultado = []
    for i in range(min(len(l1), len(l2))):
        resultado.append(l1[i])
        resultado.append(l2[i])
    return resultado

print("Intercalado:", intercalar([1, 3, 5], [2, 4, 6]))

# Ejercicio 13: Encontrar la palabra con más vocales
def mas_vocales(lista):
    def contar_v(palabra):
        contador = 0
        for c in palabra:
            if c.lower() in "aeiou":
                contador += 1
        return contador
    mayor = lista[0]
    for palabra in lista:
        if contar_v(palabra) > contar_v(mayor):
            mayor = palabra
    return mayor

print("Más vocales:", mas_vocales(["sol", "universidad", "computadora", "mar"]))

# Ejercicio 14: Buscar palabras palíndromas en una lista
def palindromos(lista):
    resultado = []
    for palabra in lista:
        palabra_limpia = palabra.lower()
        if palabra_limpia == palabra_limpia[::-1]:
            resultado.append(palabra)
    return resultado

print("Palíndromos:", palindromos(["oso", "python", "radar", "hola"]))

# Ejercicio 15: Sumar dígitos de una cadena numérica
def suma_digitos(cadena):
    suma = 0
    for c in cadena:
        if c.isdigit():
            suma += int(c)
    return suma

print("Suma de dígitos:", suma_digitos("abc1234xyz"))

# Ejercicio 16: Mostrar los primeros N múltiplos de un número
def multiplos(n, cantidad):
    resultado = []
    for i in range(1, cantidad+1):
        resultado.append(n * i)
    return resultado

print("Multiplos:", multiplos(4, 5))

# Ejercicio 17: Encontrar la segunda palabra más larga
def segunda_mas_larga(lista):
    lista_ordenada = sorted(lista, key=len, reverse=True)
    return lista_ordenada[1]

print("Segunda más larga:", segunda_mas_larga(["sol", "luz", "montaña", "relámpago"]))

# Ejercicio 18: Calcular promedio de números pares en una lista
def promedio_pares(lista):
    suma = 0
    cantidad = 0
    for n in lista:
        if n % 2 == 0:
            suma += n
            cantidad += 1
    if cantidad > 0:
        return suma / cantidad
    else:
        return 0

print("Promedio pares:", promedio_pares([1, 2, 4, 7, 8]))

# Ejercicio 19: Reemplazar cada vocal de una frase con "*"
def censurar_vocales(frase):
    resultado = ""
    for c in frase:
        if c.lower() in "aeiou":
            resultado += "*"
        else:
            resultado += c
    return resultado

print("Censurado:", censurar_vocales("Aprender Python es divertido"))

# Ejercicio 20: Verificar si una frase contiene todas las vocales
def contiene_todas(frase):
    frase = frase.lower()
    for vocal in "aeiou":
        if vocal not in frase:
            return False
    return True

print("¿Contiene todas?", contiene_todas("Educación universal y objetiva"))