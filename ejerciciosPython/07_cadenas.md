## Módulo 7: Cadenas de texto en Python

## ¿Qué es una cadena?

Una cadena (o string) es una secuencia de caracteres encerrada entre comillas simples ' o dobles ".

```python
texto1 = "Hola mundo"
texto2 = 'Python es genial'
```
Ambas son válidas.



### Características clave de las cadenas
	•	Se pueden recorrer con for.
	•	Son inmutables: no se pueden modificar directamente.
	•	Son indexables: puedes acceder a cada carácter por su posición.



### Índices en cadenas
```python
nombre = "Lucía"
print(nombre[0])  # L
print(nombre[4])  # a
````

### Índices negativos

Permiten contar desde el final:
```python
print(nombre[-1])  # a
print(nombre[-2])  # í
```



### Recorrer una cadena

```python
for letra in nombre:
    print(letra)
```



### Slicing (subcadenas)

```python
frase = "programar es divertido"

print(frase[0:9])   # "programar"
print(frase[:9])    # desde el inicio
print(frase[10:])   # desde el 10 hasta el final
print(frase[-9:])   # los últimos 9 caracteres
```



### Funciones útiles de cadenas

```python
len(cadena)	len("hola")	4
cadena.lower()	"Hola".lower()	"hola"
cadena.upper()	"hola".upper()	"HOLA"
cadena.capitalize()	"python".capitalize()	"Python"
cadena.title()	"python es genial".title()	"Python Es Genial"
cadena.strip()	" hola ".strip()	"hola"
cadena.replace(a, b)	"hola".replace("a", "e")	"hole"
cadena.count(sub)	"banana".count("a")	3
cadena.find(sub)	"banana".find("na")	2 (posición)
cadena.startswith(sub)	"python".startswith("py")	True
cadena.endswith(sub)	"mundo".endswith("do")	True
cadena.split(sep)	"a,b,c".split(",")	["a", "b", "c"]
sep.join(lista)	",".join(["a", "b", "c"])	"a,b,c"
```



### Comparación de cadenas

```python
a = "hola"
b = "Hola"

print(a == b)  # False
print(a.lower() == b.lower())  # True
```

**Python distingue mayúsculas de minúsculas**



### Preguntas frecuentes

❓ ¿Cómo puedo saber si una letra está en una cadena?

```python
letra = "a"
palabra = "manzana"

if letra in palabra:
    print("Sí está")
```



### ¿Puedo convertir números a cadenas?

Sí, con str():
```python
edad = 20
print("Tengo " + str(edad) + " años")
```



### Ejercicio con varias funciones

```python
frase = "  Python es sencillo pero potente  "

# Mostrar cuántas palabras tiene
palabras = frase.strip().split()
print("Número de palabras:", len(palabras))

# Pasarla a mayúsculas
print(frase.upper())

# Reemplazar "sencillo" por "fácil"
nueva_frase = frase.replace("sencillo", "fácil")
print(nueva_frase.strip())
```



🧠 Ejercicios propuestos
	1.	Pide al usuario una frase y cuenta cuántas vocales tiene.
	2.	Pide una palabra y comprueba si es un palíndromo (igual al revés).
	3.	Dada una frase, elimina los espacios de los extremos y conviértela en formato título (title()).
	4.	Divide una cadena en palabras y muestra cuántas hay.
	5.	Escribe una función que reciba una cadena y devuelva cuántas veces aparece cada vocal.