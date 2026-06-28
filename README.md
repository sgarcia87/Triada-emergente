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

por lo que son equivalentes a matrices de Hadamard de orden 4.

Además,

\[
P_{48}\cong B_3,
\]

y su grafo natural es

\[
\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}.
\]

---

## Cadena estructural

```text
Equilibrio 2/2
      ↓
Δ(4,2)
      ↓
Hadamard
      ↓
P48
      ↓
B3
      ↓
Cay(B3,S)
      ↓
Q3 □ K3,3
```

---

## Formulación relacional

La misma estructura puede reconstruirse utilizando únicamente comparaciones entre estados.

La operación

\[
C(A,B)=A^{-1}B
\]

permite reconstruir:

- el grupo \(B_3\),
- los 48 estados,
- el grafo de Cayley,
- la estructura de Hadamard,

una vez fijada una referencia.

---

## Resultados verificados

- 48 estados perfectos.
- Equivalencia con matrices de Hadamard de orden 4.
- \(P_{48}\cong B_3\).
- \(\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}\).
- 144 aristas.
- 3456 automorfismos.
- Concentración espectral Walsh-Hadamard del 58.5 % en orden 6.
- z-score 39.84 frente a conjuntos aleatorios.
- Reconstrucción relacional mediante \(A^{-1}B\).

---

## Contenido del repositorio

```text
README.md
estructura_triadica_4D.md
triadic_structure_3d.html
python/
results/
```

- **estructura_triadica_4D.md**: desarrollo matemático completo.
- **triadic_structure_3d.html**: visualizador interactivo.
- **python/**: scripts de enumeración, verificación y análisis.
- **results/**: resultados reproducibles de los experimentos.

---

## Alcance

El trabajo no propone nuevos objetos matemáticos individuales.

La aportación consiste en mostrar que una única condición discreta genera de forma conjunta una cadena de estructuras conocidas y verificables, reproducible mediante enumeración y cálculo algebraico.

---

## Autor

**Sergi Garcia Mecinas**
