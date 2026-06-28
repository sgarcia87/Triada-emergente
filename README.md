# Estructuras triádicas discretas

**Una familia de estructuras discretas generadas por equilibrio, ortogonalidad y simetría.**  
El caso \(n=4\) produce matrices de Hadamard de orden 4, el grupo hiperoctaédrico \(B_3\) y el grafo de Cayley \(Q_3 \square K_{3,3}\).

---

## Resumen

Este proyecto estudia tríadas de vectores binarios sometidas a dos restricciones simples:

1. **equilibrio**;
2. **ortogonalidad por pares**.

Para \(n \equiv 0 \pmod 4\), estas restricciones generan una familia de espacios triádicos discretos \(\mathcal T_n\).  
Las órbitas de \(\mathcal T_n\) bajo la acción del grupo simétrico \(S_n\) quedan completamente clasificadas por un único invariante:

\[
t=|A\cap B\cap C|.
\]

El caso \(n=4\) es el primer caso no trivial y resulta excepcionalmente simétrico:

\[
P_{48}\cong B_3,
\]

con grafo natural

\[
\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}.
\]

---

## Idea central

El objeto general del proyecto es

\[
\mathcal T_n=
\left\{
(A,B,C):
|A|=|B|=|C|=\frac n2,\;
|A\cap B|=|A\cap C|=|B\cap C|=\frac n4
\right\},
\]

donde \(A,B,C\subseteq[n]\).

Esta formulación equivale a estudiar tríadas de vectores de signos

\[
H_1,H_2,H_3\in\{-1,+1\}^{n}
\]

con equilibrio interno y ortogonalidad mutua.

La cadena conceptual es:

```text
Espacio discreto
      ↓
Equilibrio
      ↓
Ortogonalidad
      ↓
Átomos de Venn
      ↓
Órbitas de Sₙ
      ↓
Dualidad por complemento
      ↓
Caso excepcional n=4
      ↓
Hadamard → B₃ → Q₃ □ K₃,₃
```

---

## Teorema general de órbitas

Sea

\[
n=4m.
\]

Entonces las tríadas de \(\mathcal T_n\) se dividen en

\[
m+1=\frac n4+1
\]

órbitas bajo \(S_n\).

Cada órbita está determinada por

\[
t=|A\cap B\cap C|,
\qquad
t\in\{0,1,\ldots,m\}.
\]

El tamaño de la órbita correspondiente a \(t\) es

\[
|\mathcal O_t|
=
\frac{n!}{(t!)^4((m-t)!)^4}.
\]

---

## Completitud del invariante \(t\)

El invariante

\[
t=|A\cap B\cap C|
\]

no solo distingue órbitas: las clasifica completamente.

Es decir,

\[
(A,B,C)\sim_{S_n}(A',B',C')
\iff
|A\cap B\cap C|
=
|A'\cap B'\cap C'|.
\]

Por tanto,

\[
\mathcal T_n/S_n
=
\{0,1,\ldots,m\}.
\]

No hay invariantes ocultos bajo la acción de \(S_n\).

---

## Dualidad por complemento

El complemento global

\[
A\mapsto A^c=[n]\setminus A
\]

actúa sobre las órbitas como

\[
\mathcal O_t
\longleftrightarrow
\mathcal O_{m-t}.
\]

La órbita uniforme aparece exactamente cuando esta dualidad tiene punto fijo:

\[
t=m-t.
\]

Esto ocurre si y solo si

\[
n\equiv0\pmod8.
\]

Cuando existe, la órbita uniforme tiene tamaño

\[
|\mathcal O_{\mathrm{unif}}|
=
\frac{n!}{((n/8)!)^8}.
\]

---

## Casos principales

| \(n\) | \(m=n/4\) | Órbitas | Tríadas ordenadas | Estructura destacada |
|---:|---:|---:|---:|---|
| 4 | 1 | 2 | 48 | \(P_{48}\cong B_3\) |
| 8 | 2 | 3 | 45360 | \(\mathcal O_1\) es un \(S_8\)-torsor |
| 12 | 3 | 4 | 60614400 | verificación independiente completa |
| 16 | 4 | 5 | 114144030000 | órbita uniforme \(S_{16}/(S_2)^8\) |

---

## El caso \(n=4\)

En

\[
(\{-1,+1\}^{4})^3
\]

hay \(4096\) estados posibles.

La condición de equilibrio y ortogonalidad selecciona exactamente

\[
48
\]

estados perfectos.

Estos estados cumplen

\[
MM^T=4I_4,
\]

por lo que son equivalentes a completaciones de matrices de Hadamard de orden 4.

Además,

\[
P_{48}\cong B_3,
\]

donde

\[
B_3\cong C_2^3\rtimes S_3
\]

es el grupo hiperoctaédrico de dimensión 3.

El grafo natural de los 48 estados es

\[
\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}.
\]

Tiene:

- 48 vértices;
- 144 aristas;
- grado 6;
- dos órbitas de aristas;
- grupo de automorfismos de orden 3456.

---

## Formulación relacional

La estructura también puede reconstruirse desde comparaciones.

Para \(A,B\in B_3\), la operación natural es

\[
C(A,B)=A^{-1}B.
\]

Esta comparación permite reconstruir:

- el grupo \(B_3\);
- los 48 estados;
- el grafo de Cayley;
- las distancias;
- la condición de Hadamard;

una vez elegida una referencia.

La operación \(A^{-1}B\) es la única entre las operaciones candidatas estudiadas que satisface simultáneamente identidad, simetría inversa, cociclo, reconstrucción de distancias e invariancia bajo cambio de referencia.

---

## Resultados verificados

- Equivalencia exacta con matrices de Hadamard de orden 4.
- \(P_{48}\cong B_3\).
- \(\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}\).
- Grupo de automorfismos del grafo: \(|\mathrm{Aut}|=3456\).
- Dos órbitas de aristas: flips y swaps.
- Concentración espectral Walsh-Hadamard del 58.5 % en orden \(k=6\).
- Z-score 39.84 frente a subconjuntos aleatorios.
- Z-score mínimo 8.78 frente a controles con simetrías parciales.
- Clasificación general de \(\mathcal T_n/S_n\).
- Completitud del invariante \(t=|A\cap B\cap C|\).
- Dualidad por complemento \(\mathcal O_t\leftrightarrow\mathcal O_{m-t}\).
- Verificación independiente para \(n=4,8,12\).
- \(\mathcal O_1(n=8)\) es un \(S_8\)-torsor.
- Reconstrucción relacional mediante \(C(A,B)=A^{-1}B\).

---

## Estado del proyecto

| Área | Estado |
|---|---|
| Caso \(n=4\) | completo |
| Identificación con \(B_3\) | completa |
| Grafo de Cayley | completo |
| Teorema general de órbitas | completo |
| Completitud del invariante \(t\) | completo |
| Verificación \(n=12\) | completa |
| Visualizador interactivo | funcional |
| Revisión bibliográfica | realizada — sin precedentes directos encontrados |
| Preprint formal | en preparación |

---

## Contenido del repositorio

```text
README.md
paper_triadico.md
estructura_triadica_V6.md
index.html
LICENSE
```

- `README.md`: entrada principal al proyecto.
- `paper_triadico.md`: versión corta orientada a preprint.
- `estructura_triadica_V6.md`: desarrollo matemático completo.
- `index.html`: visualizador interactivo.
- `LICENSE`: licencia del repositorio.

---

## Alcance

Este trabajo **no afirma** haber descubierto nuevos objetos matemáticos individuales.

Los objetos implicados —matrices de Hadamard, grafos de Johnson, hipersímplices, \(B_3\), grafos de Cayley, transformada de Walsh-Hadamard— son objetos clásicos.

La aportación consiste en mostrar cómo una misma construcción discreta basada en equilibrio y ortogonalidad conecta estos objetos y genera una clasificación general mediante órbitas de \(S_n\), átomos de Venn y dualidad por complemento.

Tampoco se hacen afirmaciones físicas, cosmológicas, numerológicas ni sobre consciencia. El proyecto se presenta como una investigación de combinatoria, geometría discreta y teoría de grupos finitos.

---

## Autor

**Sergi Garcia Mecinas**

Investigación independiente en estructuras discretas, geometría combinatoria y simetrías finitas.
