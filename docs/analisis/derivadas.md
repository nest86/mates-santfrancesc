# Reglas y Fórmulas de Derivación

La **derivada** de una función $f(x)$ mide la tasa de variación instantánea de dicha función respecto a la variable independiente $x$.

---

## 1. Reglas Básicas de Operación

Sean $u(x)$ y $v(x)$ dos funciones derivables, y $k$ una constante real ($k \in \mathbb{R}$):

| Operación | Regla en LaTeX |
| :--- | :--- |
| **Constante por función** | $(k \cdot u)' = k \cdot u'$ |
| **Suma y Resta** | $(u \pm v)' = u' \pm v'$ |
| **Producto** | $(u \cdot v)' = u' \cdot v + u \cdot v'$ |
| **Cociente** | $\left(\frac{u}{v}\right)' = \frac{u' \cdot v - u \cdot v'}{v^2}$ |
| **Regla de la Cadena (Composición)** | $(f(g(x)))' = f'(g(x)) \cdot g'(x)$ |
!!! note "Fórmula clave"
    La derivada de una potencia $u^n$ siempre requiere multiplicar por la derivada interna $u'$.
!!! warning "¡Ojo en la PAU!"
    Un error muy habitual es olvidar simplificar el numerador tras aplicar la regla del cociente.
---

## 2. Tabla de Derivadas de Funciones Elementales

A continuación se presentan las fórmulas para funciones simples $x$ y para funciones compuestas $u(x)$.

### 2.1. Funciones Polinómicas y Potenciales

* **Constante:** $(k)' = 0$
* **Identidad:** $(x)' = 1$
* **Potencia simple:** $(x^n)' = n \cdot x^{n-1}$
* **Potencia compuesta:** $(u^n)' = n \cdot u^{n-1} \cdot u'$
* **Raíz cuadrada simple:** $\left(\sqrt{x}\right)' = \frac{1}{2\sqrt{x}}$
* **Raíz cuadrada compuesta:** $\left(\sqrt{u}\right)' = \frac{u'}{2\sqrt{u}}$
!!! tip "Truco de cálculo"
    Antes de derivar una raíz, a veces conviene pasarla a forma de potencia de exponente fraccionario: $\sqrt[n]{x^m} = x^{\frac{m}{n}}$.
---

### 2.2. Funciones Exponenciales

* **Exponencial de base $e$ (Simple):** $(e^x)' = e^x$
* **Exponencial de base $e$ (Compuesta):** $(e^u)' = e^u \cdot u'$
* **Exponencial de base $a$ ($a > 0, a \neq 1$):** $(a^x)' = a^x \cdot \ln(a)$
* **Exponencial de base $a$ compuesta:** $(a^u)' = a^u \cdot u' \cdot \ln(a)$

---

### 2.3. Funciones Logarítmicas

* **Logaritmo Neperiano (Simple):** $(\ln(x))' = \frac{1}{x}$
* **Logaritmo Neperiano (Compuesto):** $(\ln(u))' = \frac{u'}{u}$
* **Logaritmo en base $a$ ($a > 0, a \neq 1$):** $(\log_a(x))' = \frac{1}{x \cdot \ln(a)}$
* **Logaritmo en base $a$ compuesto:** $(\log_a(u))' = \frac{u'}{u \cdot \ln(a)}$

---
### 2.4. Funciones Trigonométricas

A continuación se presentan las fórmulas de derivación para las funciones trigonométricas directas ($x$ e $u(x)$):

#### Función Seno
* **Simple:**
  $\big(\sin(x)\big)' = \cos(x)$
* **Compuesta:**
  $\big(\sin(u)\big)' = \cos(u) \cdot u'$

---

#### Función Coseno
* **Simple:**
  $\big(\cos(x)\big)' = -\sin(x)$
* **Compuesta:**
  $\big(\cos(u)\big)' = -\sin(u) \cdot u'$

---

#### Función Tangente
La derivada de la tangente admite tres formas equivalentes (puedes usar la que más te convenga según la simplificación):

* **Simple:**
  $\big(\tan(x)\big)' = 1 + \tan^2(x) = \frac{1}{\cos^2(x)} = \sec^2(x)$
* **Compuesta:**
  $\big(\tan(u)\big)' = (1 + \tan^2(u)) \cdot u' = \frac{u'}{\cos^2(u)}$

---
## 3. Ejemplos Resueltos de Derivación

### Ejemplo 1: Derivada de un Polinomio
Calcula la derivada de $f(x) = 3x^4 - 5x^2 + 7x - 2$.

??? success "Ver Solución"
    Aplicamos las reglas del producto por constante y suma/resta:
    
    $$f'(x) = 3 \cdot (4x^3) - 5 \cdot (2x) + 7 \cdot (1) - 0$$
    
    $$f'(x) = 12x^3 - 10x + 7$$

---

### Ejemplo 2: Regla del Cociente
Calcula la derivada de $f(x) = \frac{2x + 1}{x^2 + 3}$.

??? success "Ver Solución"
    Identificamos $u = 2x + 1 \implies u' = 2$ y $v = x^2 + 3 \implies v' = 2x$:
    
    $$f'(x) = \frac{2 \cdot (x^2 + 3) - (2x + 1) \cdot (2x)}{(x^2 + 3)^2}$$

    $$f'(x) = \frac{2x^2 + 6 - (4x^2 + 2x)}{(x^2 + 3)^2} = \frac{-2x^2 - 2x + 6}{(x^2 + 3)^2}$$

---

### Ejemplo 3: Regla de la Cadena con Logaritmo
Calcula la derivada de $f(x) = \ln(3x^2 - 5x)$.

??? success "Ver Solución"
    Aplicamos la fórmula de la derivada del logaritmo compuesto $(\ln(u))' = \frac{u'}{u}$, con $u = 3x^2 - 5x \implies u' = 6x - 5$:
    
    $$f'(x) = \frac{6x - 5}{3x^2 - 5x}$$
---
### Ejemplo 4: Regla de la cadena con Seno
Calcula la derivada de $f(x) = \sin(3x^2 - 5)$.

??? success "Ver Solución Paso a Paso"
    Aplicamos la fórmula compuesta $\big(\sin(u)\big)' = \cos(u) \cdot u'$, donde $u = 3x^2 - 5 \implies u' = 6x$:
    
    $$f'(x) = \cos(3x^2 - 5) \cdot 6x = 6x \cdot \cos(3x^2 - 5)$$

---
### Ejemplo 5: Producto con Coseno
Calcula la derivada de $f(x) = x^2 \cdot \cos(x)$.

??? success "Ver Solución Paso a Paso"
    Aplicamos la regla del producto $(u \cdot v)' = u' \cdot v + u \cdot v'$, con $u = x^2 \implies u' = 2x$ y $v = \cos(x) \implies v' = -\sin(x)$:
    
    $$f'(x) = 2x \cdot \cos(x) + x^2 \cdot (-\sin(x)) = 2x \cos(x) - x^2 \sin(x)$$
## 4.Presentación de la unidad
<div style="position: relative; width: 100%; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe 
    src="https://docs.google.com/presentation/d/e/2PACX-1vRVEBOj38-ANx7r3WwcwAHcaeqc7KQXOQ2pA-7IdilBgOPdNZc7fkVBlfgHrVJOrT-3vtf_pfPWGTAq/pubembed?start=false&loop=false&delayms=3000" 
    frameborder="0" 
    width="960" 
    height="569" 
    allowfullscreen="true" 
    mozallowfullscreen="true" 
    webkitallowfullscreen="true"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>