
## Módulo 4: Bucles en Python

### ¿Qué es un bucle?

Un bucle permite repetir un bloque de instrucciones varias veces, sin tener que escribir el código una y otra vez.

**Ejemplo real:** imagina que quieres imprimir “Hola” 5 veces. En vez de escribir 5 veces print("Hola"), usas un bucle.



### Tipos de bucles en Python

Python tiene dos bucles principales:
	•	for: se usa para repetir una acción un número conocido de veces o recorrer una colección (lista, cadena, etc.).
	•	while: se usa cuando no sabes cuántas veces repetirás, pero sí hasta cuándo.



### El bucle for paso a paso

La forma general es:
```python
for variable in secuencia:
    # Código que se repite

Donde secuencia puede ser un rango de números, una lista, una cadena, etc.
```


### Usando range()

La función range() genera una secuencia de números.
```python
for i in range(5):
    print(i)
```
🔍 Esto imprime:

0
1
2
3
4

Empieza en 0 y llega hasta 5 sin incluirlo.



Podemos personalizar el range():
```python
range(inicio, fin)        # De inicio a fin (sin incluir fin)
range(inicio, fin, paso)  # De inicio a fin, de paso en paso
```



Ejemplo 1: De 1 a 5
```python
for i in range(1, 6):
    print(i)
```
Imprime:

1
2
3
4
5




Ejemplo 2: De 10 a 0, bajando de 2 en 2
 ```python
for i in range(10, -1, -2):
    print(i)
```
Imprime:

10
8
6
4
2
0




Ejemplo 3: Repetir un mensaje 3 veces
 ```python
for _ in range(3):
    print("Bienvenido al curso")
```
Aquí usamos _ porque no necesitamos el valor del bucle.



### Recorrer cadenas con for
```python
nombre = "Lucía"
for letra in nombre:
    print(letra) 
```
Imprime cada letra en una línea.



### Recorrer listas con for
```python
numeros = [3, 7, 2, 9]

for n in numeros:
    print("Número:", n)
```



🚨 Advertencias comunes
	•	range(5) va de 0 a 4, no incluye el 5.
	•	El bloque que se repite debe tener sangría (4 espacios).
	•	No confundas print(i) con print("i"): lo primero imprime el valor de i, lo segundo la letra i.



El bucle while (solo una pincelada aquí)
```python
x = 0
while x < 5:
    print("x vale:", x)
    x += 1
````

Usamos while cuando no sabemos cuántas veces repetiremos, pero sí la condición de parada.



### Ejercicios propuestos
	1.	Imprime los números del 1 al 10 usando for.
	2.	Imprime los pares del 2 al 20.
	3.	Recorre una lista de frutas y muestra cada una.
	4.	Pide al usuario 5 números y calcula la suma total.
	5.	Recorre la palabra "programar" y cuenta cuántas veces aparece la letra r.



### Ejercicio con dificultad media

Haz un programa que pida al usuario un número n y dibuje una pirámide con ceros así:

n = 4
0
00
000
0000

