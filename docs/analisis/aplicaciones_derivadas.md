# Aplicaciones de las Derivadas

El estudio de las derivadas permite analizar el comportamiento cualitativo de una función $f(x)$: su crecimiento, sus extremos relativos (máximos y mínimos), la forma de su curva (concavidad y convexidad) y los puntos donde cambia dicha forma (puntos de inflexión).

---

## 1. Monotonía: Crecimiento y Decrecimiento

La primera derivada $f'(x)$ indica la pendiente de la recta tangente a la función en cada punto. Su signo determina la monotonía de $f(x)$:

* **Estrictamente Creciente:** Si $f'(x) > 0$ en un intervalo $(a, b)$.
* **Estrictamente Decreciente:** Si $f'(x) < 0$ en un intervalo $(a, b)$.

!!! tip "Procedimiento para estudiar la Monotonía"
    1. Calcula la primera derivada $f'(x)$.
    2. Iguala a cero para hallar los **puntos críticos** o candidatos: $f'(x) = 0$.
    3. Añade los puntos donde la función $f(x)$ **no existe** (puntos fuera del dominio).
    4. Divide el dominio en intervalos con estos puntos y evalúa el signo de $f'(x)$ en un punto probador de cada intervalo.

---

## 2. Máximos y Mínimos Relativos (Extremos)

Los extremos relativos ocurren en los puntos donde la función pasa de crecer a decrecer o viceversa.

=== "Criterio de la Primera Derivada"
    Sea $x_0$ un punto crítico tal que $f'(x_0) = 0$:

    * **Máximo Relativo:** La función pasa de crecer a decrecer en $x_0$.  
      $\text{Signo de } f'(x): \quad + \quad \xrightarrow{\quad x_0 \quad} \quad -$
    * **Mínimo Relativo:** La función pasa de decrecer a crecer en $x_0$.  
      $\text{Signo de } f'(x): \quad - \quad \xrightarrow{\quad x_0 \quad} \quad +$

=== "Criterio de la Segunda Derivada"
    Si $x_0$ cumple que $f'(x_0) = 0$, calculamos $f''(x_0)$:

    * Si $f''(x_0) < 0 \implies x_0$ es un **Máximo Relativo**.
    * Si $f''(x_0) > 0 \implies x_0$ es un **Mínimo Relativo**.
    * Si $f''(x_0) = 0 \implies$ El criterio no decide (se debe recurrir al signo de $f'$).

!!! warning "¡Ojo en la PAU!"
    Un punto crítico ($f'(x_0) = 0$) **no siempre es un máximo o un mínimo**. Si la función no cambia de signo a ambos lados de $x_0$, el punto no es un extremo relativo (puede ser un punto de inflexión con tangente horizontal).

---

## 3. Curvatura: Concavidad y Convexidad

La segunda derivada $f''(x)$ nos informa sobre la forma de la curva de la función:

* **Convexa ($\cup$):** Las tangentes quedan por debajo de la curva.  
  $f''(x) > 0 \text{ en } (a, b)$
* **Cóncava ($\cap$):** Las tangentes quedan por encima de la curva.  
  $f''(x) < 0 \text{ en } (a, b)$

---

## 4. Puntos de Inflexión

Un **punto de inflexión** es aquel punto del dominio donde la función cambia su curvatura (de cóncava a convexa o de convexa a cóncava).

### Condición Necesaria y Suficiente:
1. **Candidatos:** Se buscan resolviendo $f''(x) = 0$.
2. **Confirmación:** Un candidato $x_0$ es punto de inflexión si $f''(x)$ cambia de signo a su izquierda y a su derecha (lo que equivale a $f'''(x_0) \neq 0$).

---

## 5. Ejemplo Completo Paso a Paso

### Ejercicio
Estudia la monotonía, extremos relativos, curvatura y puntos de inflexión de la función polinómica:
$f(x) = x^3 - 3x^2 - 9x + 2$

??? success "Ver Solución Paso a Paso"
    ### Paso 1: Dominio
    Al ser una función polinómica, $\text{Dom}(f) = \mathbb{R}$.

    ### Paso 2: Monotonía y Extremos Relativos
    Calculamos la primera derivada:
    $f'(x) = 3x^2 - 6x - 9$

    Igualamos a cero para obtener los puntos críticos:
    $3x^2 - 6x - 9 = 0 \implies x^2 - 2x - 3 = 0 \implies x = \frac{2 \pm \sqrt{4 - 4(1)(-3)}}{2} \implies x_1 = 3, \; x_2 = -1$

    Estudiamos el signo de $f'(x)$ en los intervalos $(-\infty, -1)$, $(-1, 3)$ y $(3, +\infty)$:

    * En $(-\infty, -1)$, elegimos $x = -2 \implies f'(-2) = 3(-2)^2 - 6(-2) - 9 = 15 > 0 \implies$ **Creciente**
    * En $(-1, 3)$, elegimos $x = 0 \implies f'(0) = -9 < 0 \implies$ **Decreciente**
    * En $(3, +\infty)$, elegimos $x = 4 \implies f'(4) = 3(4)^2 - 6(4) - 9 = 15 > 0 \implies$ **Creciente**

    **Conclusiones:**

    * **Creciente:** $(-\infty, -1) \cup (3, +\infty)$
    * **Decreciente:** $(-1, 3)$
    * **Máximo Relativo:** En $x = -1$. Evaluando en $f(x)$: $f(-1) = (-1)^3 - 3(-1)^2 - 9(-1) + 2 = 7 \implies \mathbf{(-1, 7)}$
    * **Mínimo Relativo:** En $x = 3$. Evaluando en $f(x)$: $f(3) = 3^3 - 3(3)^2 - 9(3) + 2 = -25 \implies \mathbf{(3, -25)}$

    ---

    ### Paso 3: Curvatura y Puntos de Inflexión
    Calculamos la segunda derivada:
    $f''(x) = 6x - 6$

    Igualamos a cero para buscar candidatos a punto de inflexión:
    $6x - 6 = 0 \implies x = 1$

    Estudiamos el signo de $f''(x)$ en los intervalos $(-\infty, 1)$ y $(1, +\infty)$:

    * En $(-\infty, 1)$, elegimos $x = 0 \implies f''(0) = -6 < 0 \implies$ **Cóncava ($\cap$)**
    * En $(1, +\infty)$, elegimos $x = 2 \implies f''(2) = 6(2) - 6 = 6 > 0 \implies$ **Convexa ($\cup$)**

    **Conclusiones:**

    * **Cóncava ($\cap$):** $(-\infty, 1)$
    * **Convexa ($\cup$):** $(1, +\infty)$
    * **Punto de Inflexión:** En $x = 1$ hay cambio de curvatura. Evaluando en $f(x)$: $f(1) = 1^3 - 3(1)^2 - 9(1) + 2 = -9 \implies \mathbf{(1, -9)}$
## 6. Presentación de la unidad
<div style="position: relative; width: 100%; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe 
    src="https://docs.google.com/presentation/d/e/2PACX-1vSuIC7OfkSaFQuFNnfqoVmc3PuY42yES0S--SKGuTTYju_ozszDaaAnk_umGA-OhmW_RLk6XKMeB4Vs/pubembed?start=false&loop=false&delayms=3000" 
    frameborder="0" 
    width="960" 
    height="569" 
    allowfullscreen="true" 
    mozallowfullscreen="true" 
    webkitallowfullscreen="true"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>
## 7.Videos de la unidad
<iframe width="560" height="315" src="https://www.youtube.com/embed/Moit1lFo1D0?si=ewBIiJbEMnOQHtFf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
Resolución Junio 2019 Modelo B Baleares: 
<iframe width="560" height="315" src="https://www.youtube.com/embed/dgifzF3z6kA?si=2Emn_YQCWO20E4Q-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>