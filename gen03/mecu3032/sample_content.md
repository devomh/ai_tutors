# Tema 2: Límite de una Función

## 2.1 Acercamiento Intuitivo al Límite

El concepto de **límite** es fundamental en el cálculo. Describe el comportamiento de una función a medida que su variable de entrada se acerca a un número particular.

> **Definición Intuitiva: Límite**
> 
> Decimos que el límite de $f(x)$ cuando $x$ se acerca a $c$ es $L$, y lo escribimos como:
> $$ \lim_{x \to c} f(x) = L $$
> si podemos hacer que los valores de $f(x)$ estén arbitrariamente cerca de $L$ tomando valores de $x$ suficientemente cerca de $c$, pero no iguales a $c$.

> **Ejemplo: Un Límite que Existe**
> 
> Considere la función $f(x) = \frac{x^2 - 9}{x - 3}$. No podemos evaluar la función en $x=3$ porque resultaría en una división por cero. Sin embargo, podemos analizar qué valor aproxima la función cuando $x$ se acerca a 3.
> 
> Factorizando el numerador, obtenemos:
> $$ f(x) = \frac{(x-3)(x+3)}{x-3} = x+3, \quad \text{para } x \neq 3 $$
> A medida que $x$ se acerca a 3, $f(x)$ se acerca a $3+3=6$. Por lo tanto:
> $$ \lim_{x \to 3} \frac{x^2 - 9}{x - 3} = 6 $$

---

## 2.2 Límites Laterales

En ocasiones, el comportamiento de una función es diferente si nos acercamos por la izquierda o por la derecha.

> **Definición: Límites Laterales**
> 
> - **Límite por la Derecha:** $\lim_{x \to c^+} f(x)$ describe el comportamiento de $f(x)$ cuando $x$ se acerca a $c$ con valores mayores que $c$.
> - **Límite por la Izquierda:** $\lim_{x \to c^-} f(x)$ describe el comportamiento de $f(x)$ cuando $x$ se acerca a $c$ con valores menores que $c$.

> **Teorema de Existencia de un Límite**
> 
> El límite $\lim_{x \to c} f(x)$ existe y es igual a $L$ si y solo si ambos límites laterales existen y son iguales a $L$.
> $$ \lim_{x \to c} f(x) = L \iff \lim_{x \to c^-} f(x) = L \quad \text{y} \quad \lim_{x \to c^+} f(x) = L $$

---

## 2.3 Propiedades de los Límites

Para calcular límites de forma algebraica, usamos las siguientes propiedades.

> **Propiedades Básicas**
> 
> Si $\lim_{x \to c} f(x) = L$ y $\lim_{x \to c} g(x) = M$, entonces:
> 1.  **Suma y Resta:** $\lim_{x \to c} [f(x) \pm g(x)] = L \pm M$
> 2.  **Producto:** $\lim_{x \to c} [f(x) \cdot g(x)] = L \cdot M$
> 3.  **Cociente:** $\lim_{x \to c} \frac{f(x)}{g(x)} = \frac{L}{M}$, siempre que $M \neq 0$.
> 4.  **Constante por Función:** $\lim_{x \to c} [k \cdot f(x)] = k \cdot L$
> 5.  **Potencia:** $\lim_{x \to c} [f(x)]^n = L^n$

> **Ejemplo: Uso de las Propiedades**
> 
> Calcular $\lim_{x \to 2} (3x^2 - 5x + 1)$.
> 
> Usando las propiedades de suma, resta, constante y potencia:
> $$ \lim_{x \to 2} (3x^2 - 5x + 1) = 3(\lim_{x \to 2} x)^2 - 5(\lim_{x \to 2} x) + \lim_{x \to 2} 1 $$
> $$ = 3(2)^2 - 5(2) + 1 = 3(4) - 10 + 1 = 12 - 10 + 1 = 3 $$
