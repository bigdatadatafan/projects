## Módulo 6: Funciones en Python


### ¿Qué es una función?

Una función es un bloque de código reutilizable que realiza una tarea específica. Sirve para evitar repetir código y organizar mejor los programas.

 **Una función es como una “máquina” a la que le das unas entradas (parámetros), hace algo dentro, y puede darte una salida (return).**



### Sintaxis básica de una función
```python 
def nombre_funcion(parámetros):
    # Bloque de instrucciones
    return resultado
```
Ejemplo simple:

```python 
def saludar():
    print("Hola, ¿cómo estás?")
```



### Llamar (usar) una función
```python 
saludar()
```

### Funciones con parámetros

Los parámetros permiten que una función reciba valores externos. Esto la hace más flexible y reutilizable.

Ejemplo:
```python 
def saludar(nombre):
    print("Hola,", nombre)

saludar("Lucía")  # Hola, Lucía
saludar("David")  # Hola, David
```

### Parámetros vs Argumentos
	•	Parámetro → es la variable que aparece en la definición de la función.
	•	Argumento → es el valor real que pasas cuando llamas a la función.
```python 
def multiplicar(x, y):   # x, y son parámetros
    return x * y

multiplicar(3, 4)        # 3 y 4 son argumentos
```



### Tipos de parámetros

1. Posicionales

Se pasan en el mismo orden que se definen.
```python 
def presentar(nombre, edad):
    print(nombre, "tiene", edad, "años")

presentar("Ana", 22)
```

### Con valores por defecto

Puedes dar un valor por defecto a los parámetros. Si no se pasa argumento, se usa el valor por defecto.
```python 
def saludar(nombre="amigo"):
    print("Hola,", nombre)

saludar()           # Hola, amigo
saludar("Lucía")    # Hola, Lucía
```

### Parámetros nombrados (keyword arguments)

Puedes especificar el nombre del parámetro al llamar la función, sin importar el orden.
```python 
def mostrar(nombre, edad):
    print(nombre, "tiene", edad, "años")

mostrar(edad=20, nombre="Carlos")
```

### Parámetros variables (arbitrarios)

*args: varios argumentos posicionales
```python 
def sumar(*numeros):
    total = 0
    for n in numeros:
        total += n
    return total

print(sumar(1, 2, 3, 4))  # 10

```


### **kwargs: varios argumentos nombrados
```python 
def mostrar_info(**datos):
    for clave, valor in datos.items():
        print(clave, ":", valor)

mostrar_info(nombre="Ana", edad=30, ciudad="Madrid")
```python 


### Funciones con return

El return sirve para devolver un valor.
```python 
def cuadrado(x):
    return x * x

resultado = cuadrado(5)
print("El cuadrado es:", resultado)
```
Si no pones return, la función no devuelve nada (devuelve None).



🚨 Advertencias comunes
	•	No confundas definir la función (def) con llamarla.
	•	Si usas return, se termina la ejecución de la función en ese punto.
	•	Puedes usar return sin valor para salir de la función:

if algo_malo:
    return




###  Preguntas frecuentes

❓¿Cuántos parámetros puede tener una función?

Los que quieras. Pero si necesitas muchos, probablemente tu función hace demasiadas cosas. Mejor dividirla.

❓¿Puedo pasar listas, diccionarios, etc.?

Sí. Todo en Python es un objeto. Puedes pasar cualquier cosa:
```python 
def mostrar_lista(lista):
    for item in lista:
        print(item)

mostrar_lista(["a", "b", "c"])
```



🧠 Ejercicios propuestos
	1.	Crea una función que reciba un nombre y diga “Hola, [nombre]”.
	2.	Haz una función que reciba dos números y devuelva su suma.
	3.	Crea una función que reciba un número y devuelva True si es par.
	4.	Haz una función que reciba una lista y devuelva la media.
	5.	Crea una función que reciba una palabra y devuelva cuántas vocales tiene.



🔥 Ejercicio avanzado

Crea una función llamada evaluar_estudiante que reciba:
	•	Nombre del alumno.
	•	Lista de notas.
	•	Un parámetro opcional mostrar=True.

Y devuelva:
	•	Nombre del alumno.
	•	Nota media.
	•	Si está aprobado o no (nota media ≥ 5).

Si mostrar=False, no imprime nada, solo devuelve los datos.
