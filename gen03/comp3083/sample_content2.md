# Tema 4: Estructuras de Datos Avanzadas y Manipulación en Python

## 4.1 Cadenas de Texto (Strings)

Las **cadenas de texto** (strings) son secuencias de caracteres que se utilizan para representar datos textuales. Son uno de los tipos de datos más fundamentales en Python y esenciales para procesar información textual, entrada de usuarios y formateo de datos.

> **Concepto Clave: Cadenas de Texto**
> 
> Una cadena de texto es una secuencia inmutable de caracteres. En Python, las cadenas se pueden crear usando comillas simples (''), comillas dobles ("") o comillas triples (""") para texto multilínea.

> **Ejemplo: Creando Cadenas**
> 
> ```python
> # Diferentes formas de crear cadenas
> mensaje_simple = 'Hola, Mundo!'
> mensaje_doble = "Bienvenido a Python"
> mensaje_multilinea = """Esta es una cadena
> que puede abarcar
> varias líneas"""
> 
> # Cadena vacía
> cadena_vacia = ""
> ```

### Operaciones Básicas con Cadenas

```python
mensaje = "Programación en Python"

# Longitud de la cadena
print(f"Longitud: {len(mensaje)}")

# Concatenación
nombre = "Ana"
apellido = "García"
nombre_completo = nombre + " " + apellido
print(nombre_completo)

# Repetición
separador = "-" * 25
print(separador)
```

### Indexación y Segmentación

```python
texto = "Python"

# Indexación positiva (comienza desde 0)
print(texto[0])    # P
print(texto[1])    # y
print(texto[5])    # n

# Indexación negativa (comienza desde -1)
print(texto[-1])   # n
print(texto[-2])   # o

# Segmentación [inicio:fin]
frase = "La programación en Python es divertida"
print(frase[3:15])    # programación
print(frase[19:])     # Python es divertida
print(frase[:2])      # La
print(frase[::-1])    # aditrevid se nohtyP ne nóicamargorp aL
```

### Métodos Esenciales de Cadenas

```python
texto = "Universidad Nacional"

# Conversión de mayúsculas y minúsculas
print(texto.upper())        # UNIVERSIDAD NACIONAL
print(texto.lower())        # universidad nacional
print(texto.capitalize())   # Universidad nacional
print(texto.title())        # Universidad Nacional

# Limpieza de cadenas
texto_sucio = "  Hola, Estudiante!  \n"
print(f"Original: '{texto_sucio}'")
print(f"Limpio: '{texto_sucio.strip()}'")

# Búsqueda en cadenas
email = "estudiante@universidad.edu"
print(f"Índice de '@': {email.find('@')}")
print(f"Conteo de 'e': {email.count('e')}")
print(f"Comienza con 'estudiante': {email.startswith('estudiante')}")
print(f"Termina con '.edu': {email.endswith('.edu')}")
```

### Formateo de Cadenas con F-strings

> **Concepto Clave: F-strings**
> 
> Las f-strings (Python 3.6+) son la forma más moderna y recomendada de formatear cadenas. Permiten insertar variables y expresiones directamente en la cadena usando la sintaxis `f"..."`.

> **Ejemplo: Sistema de Calificaciones**
> 
> ```python
> nombre_estudiante = "Carlos Rodríguez"
> edad = 21
> calificacion = 87.5
> aprobado = calificacion >= 70
> 
> # Formateo básico con f-strings
> reporte = f"Estudiante: {nombre_estudiante}, Edad: {edad} años"
> print(reporte)
> 
> # Formateo de números
> calif_formateada = f"Calificación final: {calificacion:.1f}%"
> print(calif_formateada)
> 
> # Formateo condicional
> estado = f"Estado: {'APROBADO' if aprobado else 'REPROBADO'}"
> print(estado)
> ```

---

## 4.2 Listas

Las **listas** son colecciones ordenadas y mutables que pueden almacenar múltiples elementos. Son una de las estructuras de datos más versátiles en Python, permitiendo almacenar diferentes tipos de datos, modificar contenido y realizar varias operaciones en colecciones de datos.

> **Concepto Clave: Listas**
> 
> Una lista es una estructura de datos mutable que puede contener elementos de diferentes tipos, ordenados por índice. Se definen usando corchetes `[]` y los elementos se separan por comas.

> **Ejemplo: Creando Listas**
> 
> ```python
> # Lista de calificaciones
> calificaciones = [85, 92, 78, 96, 88]
> 
> # Lista mixta con diferentes tipos de datos
> datos_estudiante = ["María", 20, True, 3.75]
> 
> # Lista vacía
> lista_vacia = []
> 
> # Lista anidada (lista de listas)
> cursos = [
>     ["COMP3083", "Programación I", 3],
>     ["MATH2050", "Cálculo I", 4],
>     ["ENGL1010", "Inglés I", 3]
> ]
> ```

### Operaciones con Listas

```python
frutas = ["manzana", "banana", "cereza"]

# Agregar elementos
frutas.append("dátil")           # Agregar al final
frutas.insert(1, "aguacate")     # Insertar en posición específica
frutas.extend(["elderberry", "higo"])  # Agregar múltiples elementos

print(f"Lista actualizada: {frutas}")

# Remover elementos
frutas.remove("banana")          # Remover primera ocurrencia
elemento_removido = frutas.pop(0)  # Remover por índice y retornar
print(f"Removido: {elemento_removido}")
print(f"Lista final: {frutas}")
```

### Comprensiones de Listas

> **Concepto Clave: Comprensiones de Listas**
> 
> Las comprensiones de listas proporcionan una forma concisa de crear listas. Son más legibles y eficientes que usar bucles explícitos para crear listas.

```python
# Forma tradicional
cuadrados_tradicional = []
for x in range(1, 6):
    cuadrados_tradicional.append(x ** 2)

# Comprensión de listas (más elegante)
cuadrados = [x ** 2 for x in range(1, 6)]

print(f"Cuadrados: {cuadrados}")

# Comprensión con filtro
numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
pares = [x for x in numeros if x % 2 == 0]
print(f"Números pares: {pares}")
```

> **Ejemplo: Sistema de Gestión de Calificaciones**
> 
> ```python
> estudiantes = [
>     {"nombre": "Ana", "calificaciones": [85, 92, 78, 90]},
>     {"nombre": "Luis", "calificaciones": [91, 88, 95, 87]},
>     {"nombre": "María", "calificaciones": [76, 82, 79, 85]},
>     {"nombre": "Carlos", "calificaciones": [94, 89, 97, 92]}
> ]
> 
> # Calcular promedios
> for estudiante in estudiantes:
>     califs = estudiante["calificaciones"]
>     promedio = sum(califs) / len(califs)
>     estudiante["promedio"] = round(promedio, 1)
> 
> # Ordenar por promedio (mayor a menor)
> estudiantes.sort(key=lambda e: e["promedio"], reverse=True)
> 
> print("--- Ranking de Estudiantes ---")
> for i, estudiante in enumerate(estudiantes, 1):
>     print(f"{i}. {estudiante['nombre']}: {estudiante['promedio']} promedio")
> ```

---

## 4.3 Diccionarios

Los **diccionarios** son colecciones mutables que almacenan datos en pares clave-valor. Son ideales para representar datos estructurados, crear búsquedas rápidas y organizar información donde cada pieza de datos tiene un identificador único (la clave).

> **Concepto Clave: Diccionarios**
> 
> Un diccionario es una estructura de datos mutable que almacena pares clave-valor. Las claves deben ser inmutables (strings, números, tuplas) y únicas dentro del diccionario.

> **Ejemplo: Información de Estudiante**
> 
> ```python
> estudiante = {
>     "nombre": "Ana López",
>     "edad": 20,
>     "carrera": "Ingeniería en Sistemas",
>     "semestre": 4,
>     "promedio": 3.8,
>     "activo": True,
>     "materias": ["COMP3083", "MATH2050", "PHYS1010"]
> }
> 
> print(f"Estudiante: {estudiante['nombre']}")
> print(f"Promedio: {estudiante['promedio']}")
> ```

### Operaciones con Diccionarios

```python
inventario = {"manzanas": 50, "bananas": 30}

# Agregar nueva clave-valor
inventario["naranjas"] = 25

# Actualizar valor existente
inventario["manzanas"] = 45

# Actualizar múltiples valores
inventario.update({"bananas": 35, "uvas": 20})

print(f"Inventario actualizado: {inventario}")

# Acceso seguro con get()
cantidad_peras = inventario.get("peras", 0)  # Retorna 0 si no existe
print(f"Peras disponibles: {cantidad_peras}")
```

### Iteración en Diccionarios

```python
calificaciones_estudiantes = {"Ana": 95, "Luis": 87, "María": 92}

# Iterar sobre claves y valores
print("\nIterando sobre elementos:")
for estudiante, calificacion in calificaciones_estudiantes.items():
    print(f"  {estudiante}: {calificacion}")

# Comprensión de diccionarios
estudiantes_destacados = {
    nombre: calif for nombre, calif in calificaciones_estudiantes.items() 
    if calif >= 90
}
print(f"Estudiantes destacados: {estudiantes_destacados}")
```

> **Ejemplo: Sistema de Registro Académico**
> 
> ```python
> registro_academico = {
>     "COMP3083": {
>         "nombre_materia": "Programación I",
>         "profesor": "Dr. González",
>         "creditos": 3,
>         "estudiantes": {
>             "12345": {"nombre": "Ana", "calificaciones": [85, 92, 78]},
>             "67890": {"nombre": "Luis", "calificaciones": [91, 88, 95]},
>             "54321": {"nombre": "María", "calificaciones": [76, 82, 79]}
>         }
>     }
> }
> 
> # Calcular promedios para cada estudiante
> materia = registro_academico["COMP3083"]
> for id_estudiante, datos in materia["estudiantes"].items():
>     califs = datos["calificaciones"]
>     promedio = sum(califs) / len(califs)
>     datos["promedio"] = round(promedio, 1)
> 
> # Generar reporte
> print(f"\n--- Reporte de {materia['nombre_materia']} ---")
> print(f"Profesor: {materia['profesor']}")
> for id_est, datos in materia["estudiantes"].items():
>     print(f"  {datos['nombre']} (ID: {id_est}): {datos['promedio']}%")
> ```

---

## 4.4 Bucles (Loops)

Los **bucles** son estructuras de control que permiten ejecutar un bloque de código repetidamente. Python proporciona dos tipos principales: bucles `for` (para iterar sobre secuencias) y bucles `while` (para repetir basándose en una condición).

> **Concepto Clave: Bucles**
> 
> Los bucles permiten automatizar tareas repetitivas. El bucle `for` es ideal para iterar sobre colecciones conocidas, mientras que `while` es mejor para repeticiones basadas en condiciones.

### Bucles For

```python
# Iterar sobre una lista
materias = ["Programación", "Matemáticas", "Física", "Química"]
for materia in materias:
    print(f"Estudiando: {materia}")

# Usar range() para números
print("\nTabla del 5:")
for i in range(1, 11):
    print(f"5 x {i} = {i * 5}")

# Enumerate para obtener índice y valor
print("\nMaterias numeradas:")
for indice, materia in enumerate(materias, 1):
    print(f"{indice}. {materia}")
```

### Bucles While

```python
# Contador simple
contador = 1
print("Contando hasta 5:")
while contador <= 5:
    print(f"Número: {contador}")
    contador += 1

# Validación de entrada (simulado)
# En un programa real, usarías input()
intentos = 0
max_intentos = 3

while intentos < max_intentos:
    print(f"Intento {intentos + 1} de validación")
    # Aquí iría la lógica de validación
    intentos += 1
    if intentos == 2:  # Simular éxito en el segundo intento
        print("¡Validación exitosa!")
        break
```

### Patrones Comunes con Bucles

> **Concepto Clave: Patrón Acumulador**
> 
> El patrón acumulador implica inicializar una variable antes del bucle y actualizarla en cada iteración para acumular un resultado.

```python
# Patrón acumulador para calcular estadísticas
calificaciones = [85, 92, 78, 96, 88, 91, 77, 89]

# Inicializar acumuladores
suma_total = 0
calificacion_mayor = 0
aprobados = 0

for calificacion in calificaciones:
    suma_total += calificacion  # Acumular suma
    if calificacion > calificacion_mayor:
        calificacion_mayor = calificacion  # Encontrar máximo
    if calificacion >= 70:
        aprobados += 1  # Contar aprobados

promedio = suma_total / len(calificaciones)

print(f"Calificaciones analizadas: {calificaciones}")
print(f"Promedio: {promedio:.1f}")
print(f"Calificación más alta: {calificacion_mayor}")
print(f"Estudiantes aprobados: {aprobados}/{len(calificaciones)}")
```

### Bucles Anidados

```python
# Crear una matriz de calificaciones
estudiantes = ["Ana", "Luis", "María"]
materias = ["Programación", "Matemáticas", "Física"]

print("Matriz de Calificaciones:")
print("Estudiante\t", end="")
for materia in materias:
    print(f"{materia}\t", end="")
print()  # Nueva línea

# Simular calificaciones (en un programa real vendrían de otra fuente)
import random
for estudiante in estudiantes:
    print(f"{estudiante}\t\t", end="")
    for materia in materias:
        calificacion = random.randint(70, 100)
        print(f"{calificacion}\t\t", end="")
    print()  # Nueva línea después de cada estudiante
```

---

## 4.5 Trabajando con JSON

**JSON** (JavaScript Object Notation) es un formato ligero de intercambio de datos que es fácil de leer para los humanos y de procesar para las máquinas. Se ha convertido en el estándar de facto para el intercambio de datos en APIs web, archivos de configuración y almacenamiento de datos.

> **Concepto Clave: JSON**
> 
> JSON almacena datos en pares clave-valor (como los diccionarios de Python) y arrays (como las listas de Python). Python incluye el módulo `json` para convertir entre objetos Python y formato JSON.

> **Ejemplo: Estructura JSON**
> 
> ```python
> import json
> 
> # Datos de estudiante en Python
> datos_estudiante = {
>     "nombre": "Ana García",
>     "id_estudiante": "12345",
>     "activo": True,
>     "materias": ["COMP3083", "MATH2050"],
>     "promedio": 3.8,
>     "tutor": None
> }
> 
> # Convertir a JSON string
> json_string = json.dumps(datos_estudiante, indent=2)
> print("Datos en formato JSON:")
> print(json_string)
> ```

### Operaciones con Archivos JSON

```python
import json

# Datos para guardar
base_datos_estudiantes = {
    "universidad": "Universidad Nacional",
    "semestre": "2024-1",
    "estudiantes": [
        {
            "id": "001",
            "nombre": "Ana García",
            "carrera": "Ingeniería en Sistemas",
            "promedio": 3.8
        },
        {
            "id": "002",
            "nombre": "Luis Martínez",
            "carrera": "Matemáticas Aplicadas",
            "promedio": 3.6
        }
    ]
}

# Guardar en archivo JSON
with open("estudiantes.json", "w", encoding='utf-8') as archivo:
    json.dump(base_datos_estudiantes, archivo, indent=2, ensure_ascii=False)

print("Datos guardados en estudiantes.json")

# Cargar desde archivo JSON
try:
    with open("estudiantes.json", "r", encoding='utf-8') as archivo:
        datos_cargados = json.load(archivo)
    
    print(f"\nDatos cargados exitosamente!")
    print(f"Universidad: {datos_cargados['universidad']}")
    print(f"Semestre: {datos_cargados['semestre']}")
    print(f"Número de estudiantes: {len(datos_cargados['estudiantes'])}")
    
except FileNotFoundError:
    print("Archivo no encontrado.")
except json.JSONDecodeError as e:
    print(f"Error al procesar JSON: {e}")
```

> **Ejemplo: Gestor de Configuración**
> 
> ```python
> import json
> 
> def cargar_configuracion(archivo_config="config_app.json"):
>     """Carga configuración desde archivo JSON."""
>     try:
>         with open(archivo_config, "r", encoding='utf-8') as f:
>             return json.load(f)
>     except FileNotFoundError:
>         print(f"Archivo '{archivo_config}' no encontrado. Usando configuración por defecto.")
>         # Configuración por defecto
>         return {
>             "nombre_app": "Sistema Académico",
>             "version": "1.0",
>             "base_datos": {
>                 "host": "localhost",
>                 "puerto": 5432
>             },
>             "modo_debug": False
>         }
> 
> # Usar configuración en la aplicación
> config = cargar_configuracion()
> print(f"Ejecutando {config['nombre_app']} v{config['version']}")
> if config.get('modo_debug', False):
>     print("Modo debug ACTIVADO")
> else:
>     print("Modo debug DESACTIVADO")
> ```

---

## Ejercicios Prácticos

### Ejercicio 1: Procesador de Texto Académico
Crea un programa que procese un texto académico:
- Cuenta palabras, oraciones y párrafos
- Genera un resumen estadístico

### Ejercicio 2: Análisis de Calificaciones
Desarrolla un analizador de calificaciones que:
- Procese listas de calificaciones por materia
- Calcule estadísticas (promedio, mediana, moda)
- Identifique estudiantes en riesgo académico

### Ejercicio 3: Gestor de Horarios
Implementa un gestor de horarios que:
- Use diccionarios para organizar materias por día/hora
- Detecte conflictos de horario
- Exporte horarios a formato JSON

### Ejercicio 4: Sistema de Biblioteca
Crea un sistema de gestión de biblioteca que combine:
- Catálogo de libros (diccionarios)
- Sistema de préstamos (listas y fechas)
- Reportes de usuarios más activos
- Persistencia en archivos JSON

---

## Conceptos Clave Aprendidos

1. **Cadenas de Texto**: Manipulación y formateo eficiente de datos textuales
2. **Listas**: Gestión de colecciones ordenadas y mutables  
3. **Diccionarios**: Organización de datos estructurados con claves únicas
4. **Bucles**: Automatización de tareas repetitivas y procesamiento de datos
5. **JSON**: Intercambio y persistencia de datos en formato estándar

Estos conceptos forman la base para el desarrollo de aplicaciones más sofisticadas y son fundamentales para cualquier programador en Python.