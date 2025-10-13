
# Ejercicio 1: Sistema de evaluación por tramos
# Descripción: El programa calcula la media de varias notas y muestra el resultado final según los siguientes tramos:
#  - < 5: Suspenso
#  - 5 a <7: Aprobado
#  - 7 a <9: Notable
#  - >=9: Sobresaliente

notas = [6, 7, 8, 5, 9]

# TODO: Implementar la función 'clasificar_media'
# Esta función debe recibir la lista de notas, calcular la media y devolver el texto correspondiente al tramo

def clasificar_media(lista):
    pass

resultado = clasificar_media(notas)
print("Resultado del alumno:", resultado)


# Ejercicio 2: Filtrado de inventario
# Descripción: Tenemos una lista de productos con sus precios y queremos quedarnos solo con aquellos productos
# que valen menos de 20 euros. El formato es una lista de tuplas: (producto, precio)

inventario = [
    ("Cuaderno", 3.5),
    ("USB", 15),
    ("Teclado", 22.8),
    ("Ratón", 18.2),
    ("Monitor", 120.5)
]

# TODO: Implementar la función 'filtrar_baratos'
# Debe devolver una nueva lista con los productos cuyo precio sea menor que 20 euros

def filtrar_baratos(lista):
    pass

baratos = filtrar_baratos(inventario)
print("Productos económicos:", baratos)


# Ejercicio 3: Análisis de texto
# Descripción: Dado un texto largo, queremos saber cuántas palabras tiene, cuántas letras, y el promedio
# de letras por palabra. No se deben contar signos de puntuación.

texto = "Python es un lenguaje de programación potente, claro y fácil de aprender."

# TODO: Implementar la función 'analizar_texto'
# Debe devolver una tupla: (número de palabras, número de letras, promedio letras por palabra)

def analizar_texto(texto):
    pass

resumen = analizar_texto(texto)
print("Análisis del texto:", resumen)


# Ejercicio 4: Registro de asistencia
# Descripción: Dado un listado de alumnos y una lista de nombres que asistieron, queremos mostrar
# un listado con dos grupos: 'presentes' y 'ausentes'.

alumnos = ["Lucía", "Pedro", "Ana", "Juan", "Sofía"]
asistieron = ["Pedro", "Juan", "Sofía"]

# TODO: Implementar la función 'registrar_asistencia'
# Debe devolver un diccionario con claves 'presentes' y 'ausentes', cada una con la lista correspondiente

def registrar_asistencia(total, presentes):
    pass

asistencia = registrar_asistencia(alumnos, asistieron)
print("Asistencia:", asistencia)


# Ejercicio 5: Clasificación de edades
# Descripción: Dada una lista de edades, queremos contar cuántas personas hay en los siguientes grupos:
#  - menores de edad (<18)
#  - adultos (18 a 64)
#  - mayores (65 o más)

edades = [15, 22, 34, 17, 45, 67, 80, 16, 60, 70]

# TODO: Implementar la función 'clasificar_edades'
# Debe devolver un diccionario con las claves: 'menores', 'adultos', 'mayores'

def clasificar_edades(lista):
    pass

clasificacion = clasificar_edades(edades)
print("Distribución por edad:", clasificacion)
