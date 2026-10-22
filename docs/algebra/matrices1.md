Para que $A$ sea invertible, su determinante debe ser distinto de cero:

$$\det(A) = \begin{vmatrix} 1 & 0 \\ 2 & 1 \end{vmatrix} = (1 \cdot 1) - (0 \cdot 2) = 1 \neq 0$$

Como $\det(A) = 1$, la matriz es invertible. Calculamos la adjunta traspuesta:

$$\text{Adj}(A) = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} \implies (\text{Adj}(A))^T = \begin{pmatrix} 1 & 0 \\ -2 & 1 \end{pmatrix}$$

$$A^{-1} = \frac{1}{\det(A)} (\text{Adj}(A))^T = \begin{pmatrix} 1 & 0 \\ -2 & 1 \end{pmatrix}$$

---

**Paso 2: Resolución de la ecuación matricial**

Despejamos la matriz incógnita $X$:

$$A \cdot X + B = C \implies A \cdot X = C - B$$

Multiplicamos por $A^{-1}$ por la izquierda en ambos miembros:

$$A^{-1} \cdot (A \cdot X) = A^{-1} \cdot (C - B) \implies X = A^{-1} \cdot (C - B)$$

Calculamos primero $(C - B)$:

$$C - B = \begin{pmatrix} 3 & 1 \\ 1 & 0 \end{pmatrix} - \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 1 & 1 \end{pmatrix}$$

Multiplicamos por $A^{-1}$:

$$X = \begin{pmatrix} 1 & 0 \\ -2 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 & 0 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} (1\cdot 1 + 0\cdot 1) & (1\cdot 0 + 0\cdot 1) \\ (-2\cdot 1 + 1\cdot 1) & (-2\cdot 0 + 1\cdot 1) \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ -1 & 1 \end{pmatrix}$$