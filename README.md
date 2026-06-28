# Estructura Triádica 4D

**Una construcción discreta que conecta matrices de Hadamard, el grupo hiperoctaédrico \(B_3\) y el grafo de Cayley \(Q_3 \square K_{3,3}\).**

---

## Resumen

Este proyecto estudia el espacio discreto

\[
(\{-1,+1\}^{4})^{3},
\]

formado por tres bloques binarios de cuatro componentes.

Al imponer únicamente dos restricciones:

- equilibrio interno (dos `+1` y dos `−1` por bloque),
- distancia de Hamming igual a 2 entre cada par de bloques,

aparecen exactamente **48 estados perfectos**.

---

## Resultado principal

Las tríadas perfectas cumplen

\[
MM^T=4I_4,
\]

por lo que son equivalentes a matrices de Hadamard de orden 4. Los 6 vectores equilibrados forman el octaedro \(\Delta(4,2)\) en \(u^\perp\), y las 8 bases ortogonales de ese octaedro generan los 48 estados.

Además,

\[
P_{48}\cong B_3,
\]

y su grafo natural es

\[
\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}.
\]

Las 144 aristas se dividen en dos órbitas algebraicamente protegidas bajo \(\mathrm{Aut}(G)\): 72 aristas de flip (generadores de cambio de signo, estructura intra-familia \(K_{3,3}\)) y 72 aristas de swap (generadores de transposición, estructura inter-familia \(Q_3\)).

---

## Cadena estructural

```
Equilibrio 2/2
      ↓
Δ(4,2) = octaedro en u⊥
      ↓
Hadamard: MM^T = 4I
      ↓
P₄₈ ≅ B₃
      ↓
Cay(B₃, S) ≅ Q₃ □ K₃,₃
      ↓
|Aut| = 3456 = 48 · 72
```

---

## Generalización

La construcción funciona para todo \(n \equiv 0 \pmod{4}\). Las tríadas perfectas de dimensión \(n\) se clasifican en \(n/4 + 1\) órbitas bajo \(S_n\), determinadas por el invariante \(t = |A \cap B \cap C|\), con tamaño:

\[
|\mathcal{O}_t| = \frac{n!}{(t!)^4\,((m-t)!)^4}, \qquad m = \frac{n}{4}.
\]

| \(n\) | Órbitas | Tríadas ordenadas | Órbita uniforme |
|---:|---:|---:|---|
| 4 | 2 | 48 | No |
| 8 | 3 | 45360 | \(\mathcal{O}_1 \cong S_8\text{-torsor}\) |
| 12 | 4 | 60614400 | No |
| 16 | 5 | 114144030000 | \(S_{16}/(S_2)^8\) |

La órbita uniforme (todos los átomos de Venn de igual tamaño) existe exactamente cuando \(n \equiv 0 \pmod{8}\).

---

## Formulación relacional

La estructura completa puede reconstruirse desde comparaciones entre estados. La operación

\[
C(A,B)=A^{-1}B
\]

es la única operación binaria sobre \(B_3\) que satisface simultáneamente los seis axiomas de comparación relacional (identidad, simetría inversa, cociclo, distancias, invariancia izquierda, uniformidad). Permite reconstruir el grupo, los 48 estados, el grafo de Cayley y la condición de Hadamard desde una referencia arbitraria.

---

## Resultados verificados

- 48 estados perfectos — equivalencia exacta con matrices de Hadamard de orden 4.
- \(P_{48} \cong B_3\) — verificado por cerradura bajo multiplicación matricial.
- \(\mathrm{Cay}(B_3,S) \cong Q_3 \square K_{3,3}\) — isomorfismo verificado computacionalmente.
- 144 aristas en dos órbitas algebraicas disjuntas bajo \(|\mathrm{Aut}| = 3456\).
- Concentración espectral Walsh-Hadamard del 58.5 % en orden \(k=6\).
- Z-score 39.84 frente a conjuntos aleatorios; z-score mínimo 8.78 ante controles con simetrías parciales.
- Teorema de órbitas \(|\mathcal{O}_t| = n!/((t!)^4((m-t)!)^4)\) verificado para \(n=4,8\); predicciones para \(n=12,16\).
- \(\mathcal{O}_1(n=8)\) es un \(S_8\)-torsor — verificado por acción libre y transitiva.
- Reconstrucción relacional biyectiva desde comparaciones \(A^{-1}B\).

---

## Contenido del repositorio

```
README.md
estructura_triadica_4D.md       — desarrollo matemático completo
nota_triadica_paper.md          — versión corta tipo paper
triadic_structure_3d_v3.html    — visualizador interactivo 3D
python/                         — scripts de enumeración y verificación
results/                        — resultados reproducibles
```

---

## Alcance

El trabajo no propone nuevos objetos matemáticos individuales. Las matrices de Hadamard de orden 4, el grafo \(J(4,2)\), el sistema de raíces \(A_3\) y el producto cartesiano \(Q_3 \square K_{3,3}\) son objetos conocidos.

La aportación es la cadena exacta que los conecta desde una única condición discreta mínima, verificada mediante enumeración exhaustiva y cálculo algebraico.

---

## Autor

**Sergi Garcia Mecinas**
