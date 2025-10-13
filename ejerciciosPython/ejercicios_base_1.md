
# Ejercicio 1: Variables y operadores
precio = 20
cantidad = 3
total = precio * cantidad
print("Total a pagar:", total)

# Ejercicio 2: Condicional simple
edad = 17
if edad >= 18:
    print("Puedes votar")
else:
    print("No puedes votar")

# Ejercicio 3: Bucle for con range
for i in range(5):
    print("Repetición:", i)

# Ejercicio 4: Listas y bucles
numeros = [4, 7, 2, 9]
for n in numeros:
    print("Número:", n)

# Ejercicio 5: Función que suma dos números
def suma(a, b):
    return a + b

print("Suma:", suma(5, 8))

# Ejercicio 6: Función que dice si un número es par o impar
def es_par(n):
    if n % 2 == 0:
        return True
    else:
        return False

print("¿Es par 7?", es_par(7))

# Ejercicio 7: Contar vocales en una palabra
def contar_vocales(palabra):
    contador = 0
    for letra in palabra.lower():
        if letra in "aeiou":
            contador += 1
    return contador

print("Vocales en 'Educacion':", contar_vocales("Educacion"))

# Ejercicio 8: Lista de cuadrados con función y for
def cuadrados(lista):
    return [x**2 for x in lista]

print("Cuadrados:", cuadrados([1, 2, 3, 4]))

# Ejercicio 9: Buscar si una palabra contiene una letra concreta
palabra = "bicicleta"
letra = "c"
if letra in palabra:
    print(f"La letra '{letra}' está en '{palabra}'")

# Ejercicio 10: Convertir cadena a mayúsculas
titulo = "python para principiantes"
print("Mayúsculas:", titulo.upper())

# Ejercicio 11: Recorrer cadena y mostrar letras
texto = "Hola"
for letra in texto:
    print(letra)

# Ejercicio 12: Contar cuántos números son mayores a 5 en una lista
valores = [1, 8, 3, 9, 2, 10]
contador = 0
for v in valores:
    if v > 5:
        contador += 1
print("Mayores a 5:", contador)

# Ejercicio 13: Sumar todos los números de una lista con función
def sumar_lista(lista):
    return sum(lista)

print("Suma total:", sumar_lista([2, 4, 6, 8]))

# Ejercicio 14: Mostrar elementos pares de una lista
def pares(lista):
    return [x for x in lista if x % 2 == 0]

print("Pares:", pares([1, 2, 3, 4, 5, 6]))

# Ejercicio 15: Palíndromo (palabra igual al revés)
def es_palindromo(palabra):
    palabra = palabra.lower()
    return palabra == palabra[::-1]

print("¿'Oso' es palíndromo?", es_palindromo("Oso"))

# Ejercicio 16: Mostrar nombre y edad desde diccionario
persona = {"nombre": "Lucía", "edad": 28}
print("Nombre:", persona["nombre"])
print("Edad:", persona["edad"])

# Ejercicio 17: Buscar número mayor en lista sin max()
def maximo(lista):
    mayor = lista[0]
    for num in lista:
        if num > mayor:
            mayor = num
    return mayor

print("Mayor:", maximo([4, 9, 2, 7]))

# Ejercicio 18: Reemplazar letras en cadena
original = "programacion"
nueva = original.replace("o", "0")
print("Reemplazo:", nueva)

# Ejercicio 19: Mostrar tabla de multiplicar de un número
def tabla(n):
    for i in range(1, 11):
        print(f"{n} x {i} = {n * i}")

tabla(4)

# Ejercicio 20: Convertir lista de cadenas a mayúsculas
def mayusculas(lista):
    return [x.upper() for x in lista]

print("Mayúsculas:", mayusculas(["hola", "adios", "python"]))
