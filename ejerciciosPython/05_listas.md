## Módulo 5: Listas en Python


### ¿Qué es una lista?

Una lista es una colección ordenada de elementos. En Python, las listas pueden contener datos de cualquier tipo y se escriben entre corchetes [].


**Ejemplo básico**

```python
frutas = ["manzana", "naranja", "plátano"]
```
Esta lista tiene 3 elementos.



### Índices y posiciones

Los elementos de la lista tienen un índice (posición), y comienzan en 0.

```python
print(frutas[0])  # manzana
print(frutas[1])  # naranja
print(frutas[2])  # plátano
```



### Modificar elementos
```python
frutas[1] = "pera"
print(frutas)  # ['manzana', 'pera', 'plátano']

```


### Operaciones comunes con listas

1. Añadir elementos
```python
frutas.append("kiwi")       # Añade al final
frutas.insert(1, "fresa")   # Inserta en la posición 1
```



2. Eliminar elementos
```python
frutas.remove("pera")  # Elimina el primer "pera"
del frutas[0]          # Elimina el elemento en la posición 0
frutas.pop()           # Elimina el último elemento

```


3. Tamaño de la lista
```python
print(len(frutas))  # Número de elementos
```



4. Recorrer una lista
```python
for fruta in frutas:
    print("Me gusta la", fruta)

```


5. Comprobar si un elemento está
```python
if "kiwi" in frutas:
    print("Sí hay kiwi")
```



6. Copiar una lista (¡sin errores!)
```python
copia = frutas.copy()
```

⚠️ No hagas: copia = frutas → eso copia la referencia, no los datos.



### Listas con distintos tipos de datos

```python
mezcla = ["hola", 42, True, 3.14]
```


### Listas de números
```python
numeros = [10, 5, 8, 12]

print("Máximo:", max(numeros))
print("Mínimo:", min(numeros))
print("Suma:", sum(numeros))
```



### Listas y range()
```python
lista = list(range(1, 6))  # [1, 2, 3, 4, 5]
```


### Preguntas frecuentes

❓ ¿Qué pasa si accedo a un índice que no existe?
```python
print(frutas[100])
```
Esto da error: IndexError: list index out of range



❓ ¿Puedo tener listas dentro de listas?

Sí. Son listas anidadas:
```python
matriz = [[1, 2], [3, 4]]
print(matriz[0][1])  # 2
```



🧠 Ejercicios propuestos
	1.	Crea una lista con los nombres de 5 amigos y recórrela con un for.
	2.	Pide 5 números al usuario, guárdalos en una lista y muestra su media.
	3.	Crea una lista de números del 1 al 10. Elimina los pares.
	4.	Dada una lista de palabras, muestra cuántas tienen más de 5 letras.
	5.	Crea una lista de temperaturas, y calcula la máxima, mínima y promedio.



### Ejercicio avanzado

Haz un programa que lea números introducidos por el usuario hasta que escriba "fin" y luego muestre:
	•	Cuántos números se han introducido.
	•	Su suma y su media.
	•	El número más alto y el más bajo.

