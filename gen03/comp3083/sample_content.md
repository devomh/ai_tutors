# Tema 3: Variables y Tipos de Datos en Python

## 3.1 ¿Qué son las Variables?

Una **variable** es un contenedor que almacena valores de datos. En Python, las variables se crean automáticamente cuando les asignas un valor por primera vez.

> **Concepto Clave: Variables**
> 
> Una variable es como una "etiqueta" que le ponemos a un valor para poder referirnos a él más tarde en nuestro programa. Es una forma de almacenar información que podemos usar y modificar.

> **Ejemplo: Creando Variables**
> 
> ```python
> # Crear variables de diferentes tipos
> nombre = "Ana"           # String (cadena de texto)
> edad = 20               # Integer (número entero)
> promedio = 85.5         # Float (número decimal)
> es_estudiante = True    # Boolean (verdadero/falso)
> ```
> 
> En este ejemplo, hemos creado cuatro variables diferentes, cada una almacenando un tipo de dato distinto.

---

## 3.2 Tipos de Datos Fundamentales

Python tiene varios tipos de datos básicos que necesitas conocer:

> **Los Cuatro Tipos Básicos**
> 
> 1. **String (str):** Texto rodeado de comillas
> 2. **Integer (int):** Números enteros sin decimales
> 3. **Float (float):** Números con decimales
> 4. **Boolean (bool):** Valores True o False

> **Ejemplo Práctico: Sistema de Calificaciones**
> 
> ```python
> # Información del estudiante
> nombre_estudiante = "Carlos Rodríguez"
> numero_creditos = 18
> calificacion_parcial = 78.5
> aprobado = True
> 
> # Mostrar información
> print(f"Estudiante: {nombre_estudiante}")
> print(f"Créditos: {numero_creditos}")
> print(f"Calificación: {calificacion_parcial}")
> print(f"¿Aprobado?: {aprobado}")
> ```
> 
> **Salida:**
> ```
> Estudiante: Carlos Rodríguez
> Créditos: 18
> Calificación: 78.5
> ¿Aprobado?: True
> ```

---

## 3.3 Operaciones con Variables

Puedes realizar operaciones matemáticas y de manipulación con las variables:

> **Operaciones Matemáticas Básicas**
> 
> ```python
> # Variables numéricas
> x = 10
> y = 3
> 
> suma = x + y        # 13
> resta = x - y       # 7
> multiplicacion = x * y  # 30
> division = x / y    # 3.333...
> division_entera = x // y  # 3
> modulo = x % y      # 1
> potencia = x ** y   # 1000
> ```

> **Manipulación de Strings**
> 
> ```python
> nombre = "María"
> apellido = "González"
> 
> # Concatenación
> nombre_completo = nombre + " " + apellido
> print(nombre_completo)  # María González
> 
> # Métodos útiles de strings
> print(nombre.upper())      # MARÍA
> print(apellido.lower())    # gonzález
> print(len(nombre))         # 5
> ```

---

## 3.4 Verificación de Tipos de Datos

Python proporciona la función `type()` para verificar el tipo de una variable:

> **Ejemplo: Verificando Tipos**
> 
> ```python
> edad = 21
> altura = 1.75
> nombre = "Luis"
> activo = False
> 
> print(type(edad))      # <class 'int'>
> print(type(altura))    # <class 'float'>
> print(type(nombre))    # <class 'str'>
> print(type(activo))    # <class 'bool'>
> 
> # Verificar si una variable es de un tipo específico
> print(isinstance(edad, int))     # True
> print(isinstance(altura, str))   # False
> ```

---

## 3.5 Conversión de Tipos de Datos

A menudo necesitarás convertir entre diferentes tipos de datos:

> **Funciones de Conversión**
> 
> ```python
> # Conversión de string a número
> numero_como_texto = "25"
> numero_entero = int(numero_como_texto)    # 25
> numero_decimal = float(numero_como_texto) # 25.0
> 
> # Conversión de número a string
> edad = 20
> edad_como_texto = str(edad)  # "20"
> 
> # Conversión a boolean
> print(bool(1))      # True
> print(bool(0))      # False
> print(bool(""))     # False
> print(bool("hola")) # True
> ```

> **Proyecto Práctico: Calculadora de Notas**
> 
> ```python
> # Solicitar información del estudiante
> nombre = input("Ingresa tu nombre: ")
>
> # Solicitar calificaciones (convertir de string a float)
> examen1 = float(input("Calificación examen 1: "))
> examen2 = float(input("Calificación examen 2: "))
> tareas = float(input("Promedio de tareas: "))
> 
> # Calcular promedio final
> promedio_final = (examen1 * 0.4 + examen2 * 0.4 + tareas * 0.2)
> 
> # Determinar si aprobó
> aprobado = promedio_final >= 70
> 
> # Mostrar resultados
> print(f"\n--- Reporte de Calificaciones ---")
> print(f"Estudiante: {nombre}")
> print(f"Promedio final: {promedio_final:.2f}")
> print(f"Estado: {'APROBADO' if aprobado else 'REPROBADO'}")
> ```