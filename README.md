
# Estructuras triádicas discretas

**El caso \(n=4\): matrices de Hadamard, el grupo hiperoctaédrico \(B_3\) y el grafo de Cayley \(Q_3 \square K_{3,3}\).**

---

## Resumen

Este trabajo estudia una familia de estructuras discretas obtenidas al imponer **equilibrio** y **ortogonalidad** sobre tríadas de vectores binarios.

Para \(n\equiv0\pmod4\), las tríadas perfectas se organizan en órbitas bajo la acción del grupo simétrico \(S_n\), clasificadas completamente por el tamaño de la triple intersección de sus átomos de Venn.

El caso \(n=4\) constituye el primer miembro no trivial de esta familia y conduce de forma natural a matrices de Hadamard de orden 4, al grupo hiperoctaédrico \(B_3\) y al grafo de Cayley \(Q_3\square K_{3,3}\).

---

## Cadena estructural

```text
Espacio discreto
      ↓
Equilibrio
      ↓
Ortogonalidad
      ↓
Órbitas de Sₙ  ←  clasificadas completamente por t = |A∩B∩C|
      ↓
Dualidad por complemento
      ↓
Caso especial n=4
      ↓
Hadamard
      ↓
B₃
      ↓
Q₃ □ K₃,₃
```

---

## Teoría general

Para \(n=4m\):

- las tríadas perfectas se dividen en \(m+1=n/4+1\) órbitas bajo \(S_n\);
- el invariante \(t=|A\cap B\cap C|\) es **completo**: dos tríadas pertenecen a la misma órbita si y solo si tienen el mismo \(t\);
- cada órbita tiene tamaño

\[
|\mathcal O_t|=
\frac{n!}{(t!)^4((m-t)!)^4};
\]

- el complemento induce la dualidad

\[
\mathcal O_t\leftrightarrow\mathcal O_{m-t};
\]

- existe una órbita completamente uniforme **si y solo si**

\[
n\equiv0\pmod8.
\]

### Tabla de casos

| \(n\) | Órbitas | Tríadas ordenadas | Órbita uniforme |
|---:|---:|---:|---|
| 4 | 2 | 48 | No |
| 8 | 3 | 45360 | \(\mathcal{O}_1\), tamaño \(8!\), torsor de \(S_8\) |
| 12 | 4 | 60614400 | No |
| 16 | 5 | 114144030000 | \(\mathcal{O}_2\), tamaño \(16!/(2!)^8\) |

---

## Caso \(n=4\)

En el espacio

\[
(\{-1,+1\}^{4})^{3},
\]

las restricciones de equilibrio interno y ortogonalidad seleccionan exactamente **48 estados perfectos**.

Estos satisfacen

\[
MM^T=4I_4,
\]

son equivalentes a matrices de Hadamard de orden 4,

\[
P_{48}\cong B_3,
\]

y su grafo natural verifica

\[
\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}.
\]

---

## Resultados verificados

- ✔ Equivalencia exacta con matrices de Hadamard de orden 4.
- ✔ \(P_{48}\cong B_3\).
- ✔ \(\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}\).
- ✔ Grupo de automorfismos de orden 3456.
- ✔ Concentración espectral Walsh-Hadamard del 58.5 % (z-score 39.84).
- ✔ Clasificación completa por órbitas de \(S_n\): el invariante \(t\) es completo.
- ✔ Dualidad \(\mathcal O_t\leftrightarrow\mathcal O_{m-t}\).
- ✔ Verificación independiente para \(n=4,8,12\).
- ✔ Órbita uniforme únicamente cuando \(n\equiv0\pmod8\).
- ✔ \(\mathcal O_1(n=8)\) es un \(S_8\)-torsor.
- ✔ Reconstrucción relacional mediante \(C(A,B)=A^{-1}B\).

---

## Alcance

Este trabajo **no propone nuevos objetos matemáticos individuales**. Los objetos implicados (Hadamard, Johnson, \(A_3\), \(B_3\), grafos de Cayley, etc.) son clásicos.

La aportación consiste en mostrar cómo todos ellos emergen de una misma construcción discreta basada en equilibrio y ortogonalidad, y en desarrollar una clasificación completa mediante órbitas de \(S_n\), dualidad por complemento y estructuras relacionales.

---

## Autor

**Sergi Garcia Mecinas**
