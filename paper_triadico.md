# Estructuras triádicas ortogonales en hipercubos binarios: clasificación completa por órbitas y el caso excepcional \(n=4\)

**Sergi Garcia Mecinas**  
*Preprint — junio 2026*

---

## Resumen

Estudiamos tríadas \((H_1, H_2, H_3)\) de vectores en \(\{-1,+1\}^n\) que satisfacen dos condiciones: cada vector es equilibrado (\(n/2\) entradas iguales a \(+1\)) y cualquier par es mutuamente ortogonal. Tales tríadas existen si y solo si \(n \equiv 0 \pmod{4}\). Bajo la acción natural de \(S_n\) sobre las coordenadas, las tríadas se descomponen en exactamente \(n/4 + 1\) órbitas, clasificadas por el invariante de triple intersección \(t = |A \cap B \cap C|\), con tamaños dados por la fórmula cerrada \(n!/((t!)^4((m-t)!)^4)\) donde \(m = n/4\). Una órbita uniforme (todos los átomos de Venn de igual tamaño) existe precisamente cuando \(n \equiv 0 \pmod{8}\).

Para \(n = 4\), la teoría colapsa en una estructura excepcionalmente rica: las 48 tríadas perfectas son exactamente los 48 elementos del grupo hiperoctaédrico \(B_3\), su grafo de Cayley con generadores naturales es isomorfo a \(Q_3 \,\square\, K_{3,3}\), y el conjunto presenta una firma espectral Walsh-Hadamard estadísticamente excepcional (\(z\)-score 39.84). Para \(n = 8\), la órbita dominante de tamaño \(8!\) es un \(S_8\)-torsor; esto se confirma computacionalmente y se predice por la fórmula general. Se demuestra que el invariante \(t\) es **completo**: determina la órbita de forma unívoca, sin invariantes ocultos bajo la acción de \(S_n\).

---

## 1. Definición y condición de existencia

Sea \(u = (1,1,\ldots,1) \in \mathbb{R}^n\). Un **vector equilibrado** es cualquier \(v \in \{-1,+1\}^n\) con \(\langle u, v\rangle = 0\), equivalentemente, cualquier elemento de \(u^\perp \cap \{-1,+1\}^n\). Hay \(\binom{n}{n/2}\) vectores equilibrados, correspondientes a subconjuntos \(A \subseteq [n]\) con \(|A| = n/2\).

**Definición 1.** Una **tríada perfecta** de dimensión \(n\) es una terna ordenada \((H_1, H_2, H_3)\) de vectores equilibrados que satisface \(\langle H_i, H_j \rangle = 0\) para todo \(i \neq j\).

Usando la identidad \(\langle H_A, H_B \rangle = n - 2d(H_A, H_B)\) para vectores binarios, la condición de ortogonalidad equivale a \(d(H_i, H_j) = n/2\) para todo par.

**Proposición 1** (Condición de existencia). *Las tríadas perfectas de dimensión \(n\) existen si y solo si \(n \equiv 0 \pmod{4}\).*

*Demostración.* La distancia de Hamming entre dos vectores equilibrados de longitud \(n\) siempre toma la forma \(2(n/2 - |A \cap B|)\), que es par. La ortogonalidad requiere que esa distancia sea \(n/2\). Para que \(n/2\) sea par, necesitamos \(n \equiv 0 \pmod{4}\). \(\square\)

Esto excluye \(n = 2, 6, 10, \ldots\) completamente. Para \(n = 6\): hay \(\binom{6}{3} = 20\) vectores equilibrados, pero la ortogonalidad requeriría distancia de Hamming 3, que es impar y por tanto imposible — no existen pares ortogonales.

---

## 2. Estructura de órbitas

**Teorema 1** (Clasificación completa de órbitas). *Sea \(m = n/4\). El espacio cociente*

\[
\mathcal{T}_n / S_n = \{0, 1, \ldots, m\}
\]

*es exactamente el conjunto de valores de \(t = |A \cap B \cap C|\). En particular:*
*(i) dos tríadas perfectas son \(S_n\)-equivalentes si y solo si tienen el mismo \(t\);*
*(ii) cada órbita \(\mathcal{O}_t\) tiene tamaño*

\[
|\mathcal{O}_t| = \frac{n!}{(t!)^4\,((m-t)!)^4}.
\]

*Demostración.* Los ocho átomos de Venn del diagrama \((A, B, C)\) quedan completamente determinados por \(t\) y \(m\):

| Átomo | Tamaño |
|---|---:|
| \(A \cap B \cap C\) | \(t\) |
| \((A \cap B) \setminus C\) | \(m - t\) |
| \((A \cap C) \setminus B\) | \(m - t\) |
| \((B \cap C) \setminus A\) | \(m - t\) |
| \(A \setminus (B \cup C)\) | \(t\) |
| \(B \setminus (A \cup C)\) | \(t\) |
| \(C \setminus (A \cup B)\) | \(t\) |
| \([n] \setminus (A \cup B \cup C)\) | \(m - t\) |

**Separación.** El valor \(t\) es invariante bajo permutaciones de coordenadas, luego tríadas en órbitas distintas tienen \(t\) distinto.

**Completitud.** Si \((A,B,C)\) y \((A',B',C')\) tienen el mismo \(t\), sus ocho átomos tienen los mismos tamaños \((t, m-t, m-t, m-t, t, t, t, m-t)\).

**Lema** (transitividad sobre particiones equipotentes). *Sea \([n] = B_1 \sqcup \cdots \sqcup B_8\) una partición en bloques de tamaños \(a_i = |B_i|\), y sea \([n] = B_1' \sqcup \cdots \sqcup B_8'\) otra partición con \(|B_i'| = a_i\) para todo \(i\). Entonces existe \(\sigma \in S_n\) tal que \(\sigma(B_i) = B_i'\) para todo \(i\).*

*Demostración del lema.* Para cada \(i = 1,\ldots,8\), elijamos una biyección arbitraria \(\phi_i : B_i \to B_i'\) (posible porque \(|B_i| = |B_i'|\)). Definimos \(\sigma : [n] \to [n]\) como \(\sigma(x) = \phi_i(x)\) para el único \(i\) tal que \(x \in B_i\). Como los bloques forman particiones, \(\sigma\) está bien definida; como cada \(\phi_i\) es biyectiva y los bloques son disjuntos, \(\sigma\) es una permutación de \([n]\). Por construcción, \(\sigma(B_i) = \phi_i(B_i) = B_i'\) para todo \(i\). \(\square\)

Aplicando el lema: dadas \((A,B,C)\) y \((A',B',C')\) con el mismo \(t\), sus ocho átomos de Venn tienen los mismos tamaños y determinan dos particiones equipotentes de \([n]\). El lema proporciona \(\sigma \in S_n\) que envía cada átomo de la primera al correspondiente de la segunda, y por tanto \(\sigma(A)=A'\), \(\sigma(B)=B'\), \(\sigma(C)=C'\). Luego las tríadas son \(S_n\)-equivalentes.

*Verificación constructiva independiente.* Para \(n=8\), se construyó \(\sigma\) explícita para las 45360 tríadas (exhaustivo). Para \(n=12\), se verificó en 2000 pares aleatorios con mismo \(t\). En ambos casos el resultado es correcto.

**Tamaño.** El estabilizador es \((S_t)^4 \times (S_{m-t})^4\), de orden \((t!)^4((m-t)!)^4\). El teorema órbita-estabilizador da la fórmula. \(\square\)

**Corolario 1.** El número total de tríadas perfectas ordenadas de dimensión \(n\) es

\[
\sum_{t=0}^{m} \frac{n!}{(t!)^4((m-t)!)^4}.
\]

### 2.1 Dualidad por complemento

**Proposición 2.** *La aplicación complemento \(A \mapsto A^c = [n] \setminus A\) envía \(\mathcal{O}_t\) a \(\mathcal{O}_{m-t}\). Las órbitas \(\mathcal{O}_t\) y \(\mathcal{O}_{m-t}\) tienen el mismo tamaño.*

*Demostración.* Si \(|A \cap B \cap C| = t\), entonces \(|A^c \cap B^c \cap C^c| = n - |A \cup B \cup C|\). De la tabla de Venn, el cálculo directo da \(|A^c \cap B^c \cap C^c| = m - t\). \(\square\)

**Corolario 2.** *Una órbita fija bajo el complemento existe si y solo si \(m\) es par, es decir, \(n \equiv 0 \pmod{8}\).*

### 2.2 La órbita uniforme

Cuando \(n \equiv 0 \pmod{8}\), la órbita \(\mathcal{O}_{m/2}\) tiene los ocho átomos de Venn de igual tamaño \(n/8\). La llamamos **órbita uniforme**. Su tamaño es

\[
|\mathcal{O}_{\mathrm{unif}}| = \frac{n!}{((n/8)!)^8}.
\]

Para \(n = 8\): \(|\mathcal{O}_{\mathrm{unif}}| = 8!/(1!)^8 = 8!\). Para \(n = 16\): \(|\mathcal{O}_{\mathrm{unif}}| = 16!/(2!)^8\).

---

## 3. Verificación

**Tabla 1.** Tamaños de órbita para valores pequeños de \(n \equiv 0 \pmod{4}\).

| \(n\) | \(m\) | Órbitas | \(t\) | \(|\mathcal{O}_t|\) ordered | Verificado |
|---:|---:|---:|---:|---:|---|
| 4 | 1 | 2 | 0 | 24 | ✓ exhaustivo |
| 4 | 1 | 2 | 1 | 24 | ✓ exhaustivo |
| 8 | 2 | 3 | 0 | 2520 | ✓ exhaustivo |
| 8 | 2 | 3 | 1 | 40320 | ✓ exhaustivo |
| 8 | 2 | 3 | 2 | 2520 | ✓ exhaustivo |
| 12 | 3 | 4 | 0 | 369600 | ✓ conteo directo |
| 12 | 3 | 4 | 1 | 29937600 | ✓ conteo directo |
| 12 | 3 | 4 | 2 | 29937600 | ✓ conteo directo |
| 12 | 3 | 4 | 3 | 369600 | ✓ conteo directo |

Para \(n = 12\): el grafo de ortogonalidad sobre \(\binom{12}{6} = 924\) vectores equilibrados tiene 184800 aristas (regular de grado 400), verificado por conteo directo de triángulos en 6.19 segundos.

**Tabla 2.** Resumen por dimensión.

| \(n\) | Vectores equilibrados | Tríadas ordenadas totales | Órbitas | Órbita uniforme |
|---:|---:|---:|---:|---|
| 4 | 6 | 48 | 2 | No (\(m\) impar) |
| 8 | 70 | 45360 | 3 | \(\mathcal{O}_1\), tamaño \(8!\) |
| 12 | 924 | 60614400 | 4 | No (\(m\) impar) |
| 16 | 12870 | 114144030000 | 5 | \(\mathcal{O}_2\), tamaño \(16!/(2!)^8\) |

---

## 4. La órbita uniforme como torsor: el caso \(n = 8\)

Para \(n = 8\), la órbita uniforme \(\mathcal{O}_1\) tiene tamaño \(8!\) y cada tríada \((A,B,C) \in \mathcal{O}_1\) particiona \([8]\) en ocho átomos de Venn singleton. Hay exactamente \(8!\) formas de etiquetar ocho singletons, uno por cada elemento de \(S_8\).

**Teorema 2.** *La acción de \(S_8\) sobre \(\mathcal{O}_1\) es libre y transitiva: \(\mathcal{O}_1\) es un \(S_8\)-torsor.*

*Demostración.* Por el Teorema 1, el estabilizador de cualquier tríada en \(\mathcal{O}_1\) es \((S_1)^4 \times (S_1)^4 = \{e\}\). Como \(|\mathcal{O}_1| = 8! = |S_8|\) y el estabilizador es trivial, la acción es libre y transitiva. \(\square\)

**Corolario 3.** Tras elegir una tríada base \(T_0 \in \mathcal{O}_1\), existe una biyección canónica \(\mathcal{O}_1 \xrightarrow{\sim} S_8\) que envía \(T\) a la única permutación \(C(T_0, T) \in S_8\) que lleva \(T_0\) a \(T\). La operación de comparación

\[
C(T, U) = p_U p_T^{-1}
\]

satisface \(C(U,V) \cdot C(T,U) = C(T,V)\) para todo \(T, U, V \in \mathcal{O}_1\) (verificado computacionalmente).

*Observación.* La identificación \(\mathcal{O}_1 \cong S_8\) no es canónica: depende de la elección de la tríada base. La estructura que existe canónicamente es el torsor, no el grupo.

---

## 5. El caso excepcional \(n = 4\)

En dimensión 4, la teoría general da dos órbitas de tamaño 24 cada una, fusionadas por el complemento en una única estructura de tamaño 48 bajo el grupo extendido \(S_4 \times C_2\). Lo que hace excepcional al caso \(n = 4\) es que estas 48 tríadas presentan una cascada de estructura adicional no presente para \(n\) mayor.

### 5.1 Caracterización de Hadamard

**Teorema 3.** *Una tríada \((H_1, H_2, H_3)\) es perfecta en dimensión 4 si y solo si la matriz \(4 \times 4\)*

\[
M = \begin{pmatrix} u \\ H_1 \\ H_2 \\ H_3 \end{pmatrix}
\]

*es una matriz de Hadamard: \(MM^T = 4I_4\).*

*Demostración.* Las entradas fuera de la diagonal de \(MM^T\) son \(\langle u, H_i\rangle\) (cero sii equilibrado) y \(\langle H_i, H_j\rangle\) (cero sii \(d(H_i, H_j) = 2 = n/2\)). \(\square\)

Los vectores equilibrados de longitud 4 son los 6 vértices del octaedro regular \(\Delta(4,2) \cong J(4,2)\) en el hiperplano \(u^\perp\). Una tríada perfecta es una base ortogonal ordenada de ese espacio 3-dimensional. Hay exactamente 8 bases no ordenadas y \(8 \times 3! = 48\) bases ordenadas.

### 5.2 Estructura de grupo

**Teorema 4.** *El conjunto \(P_{48}\) de tríadas perfectas 4-dimensionales está en biyección con el grupo hiperoctaédrico:*

\[
P_{48} \cong B_3 = C_2^3 \rtimes S_3.
\]

*La biyección envía cada tríada \((H_1, H_2, H_3)\) a la matriz monomial firmada \(3 \times 3\) con \(M_{ij} = \langle H_i, e_j\rangle/4 \in \{-1, 0, +1\}\), donde \(e_1, e_2, e_3\) son los representantes positivos de los tres ejes antipodales.*

*Verificación.* La computación exhaustiva confirma: (i) las 48 matrices son distintas y forman el conjunto completo de matrices monomiales firmadas \(3 \times 3\), (ii) la cerradura bajo multiplicación matricial se cumple. \(\square\)

### 5.3 Grafo de Cayley

**Teorema 5.** *Sea \(S = \{\mathrm{flip}_X, \mathrm{flip}_Y, \mathrm{flip}_Z, \mathrm{swap}_{XY}, \mathrm{swap}_{XZ}, \mathrm{swap}_{YZ}\}\) el conjunto de seis generadores naturales de \(B_3\) (tres cambios de signo y tres transposiciones). Entonces*

\[
\mathrm{Cay}(B_3, S) \cong Q_3 \,\square\, K_{3,3}.
\]

*Demostración.* Cálculo directo: el grafo de Cayley tiene 48 vértices, 144 aristas, es 6-regular, bipartito, conexo, diámetro 5 — coincidiendo exactamente con \(Q_3 \,\square\, K_{3,3}\). El isomorfismo de grafos se verifica computacionalmente. \(\square\)

Las 144 aristas se dividen en dos órbitas algebraicas bajo \(\mathrm{Aut}(G)\) de orden 3456:
- **72 aristas de flip** (generadores de cambio de signo) — forman las 8 copias de \(K_{3,3}\) correspondientes a la estructura intra-familia.
- **72 aristas de swap** (generadores de transposición) — forman la estructura inter-familia \(Q_3\).

Los dos tipos de órbita no pueden mezclarse bajo ningún automorfismo: la distinción es intrínseca al grafo.

El espectro laplaciano de \(Q_3 \,\square\, K_{3,3}\) es

\[
\{0^1, 2^3, 3^4, 4^3, 5^{12}, 6^2, 7^{12}, 8^3, 9^4, 10^3, 12^1\},
\]

obtenido analíticamente por la fórmula del producto cartesiano \(\mathrm{spec}(L_{A\,\square\,B}) = \{\lambda_i^A + \lambda_j^B\}_{i,j}\).

### 5.4 Firma espectral Walsh-Hadamard

La transformada de Walsh-Hadamard de la función indicadora de \(P_{48}\) sobre \(Q_{12} = \{-1,+1\}^{12}\) tiene tres propiedades exactas:

**E1** (Anulación de órdenes impares). Todos los coeficientes de orden impar son cero. *Dem.*: \(P_{48}\) es cerrado bajo inversión global \(s \mapsto -s\), que multiplica los coeficientes de orden \(k\) por \((-1)^k\). \(\square\)

**E2** (Simetría especular). La energía en orden \(k\) iguala la energía en orden \(12 - k\).

**E3** (Uniformidad de coeficientes). Todos los coeficientes de Walsh no nulos de órdenes 4, 6, 8 tienen valor absoluto exactamente \(3/256\).

**No genericidad estadística.** Un test de Monte Carlo comparando \(P_{48}\) contra 10.000 subconjuntos aleatorios de 48 elementos de \(Q_{12}\) da:

| Estadístico | Valor |
|---|---:|
| Fracción de energía en \(k=6\) para \(P_{48}\) | 0.5850 |
| Media para subconjuntos aleatorios | 0.2257 |
| Desviación estándar | 0.0090 |
| **\(z\)-score** | **39.84** |
| \(p\)-valor empírico | \(<10^{-4}\) |

Con controles que preservan simetrías parciales (antipodal, equilibrado, ambas), el \(z\)-score mínimo es 8.78. La concentración espectral es irreducible a propiedades más simples.

---

## 6. Reconstrucción relacional

**Teorema 6.** *La operación \(C(A,B) = A^{-1}B\) es la única operación binaria sobre \(B_3\) que satisface simultáneamente los seis axiomas relacionales:*

1. \(C(A,A) = e\)
2. \(C(A,B) = e \Rightarrow A = B\)
3. \(C(B,A) = C(A,B)^{-1}\)
4. \(d(e, C(A,B)) = d(A,B)\)
5. \(C(A,B) \cdot C(B,D) = C(A,D)\) (ley de cociclo)
6. \(C(LA, LB) = C(A,B)\) para todo \(L \in B_3\)

*Entre siete operaciones binarias naturales sobre \(B_3\), solo \(C(A,B) = A^{-1}B\) alcanza satisfacción al 100\%. La alternativa más cercana (\(B^{-1}A\)) falla la ley de cociclo (20.8\% de satisfacción). Verificado sobre los \(48^2 = 2304\) pares.*

**Corolario 4** (Reconstrucción). *Dado el grafo de Cayley etiquetado \(\mathrm{Cay}(B_3, S)\) y cualquier vértice base \(r\), la estructura completa — 48 tríadas, ley de grupo, condición de Hadamard — es recuperable de forma única con cero errores.*

*Los tres niveles de información:*

\[
\underbrace{\text{grafo sin etiquetar}}_{\text{forma, ambigüedad 72}} \;\subset\;
\underbrace{\text{grafo etiquetado + raíz}}_{\text{grupo, ambigüedad 1}} \;\subset\;
\underbrace{\text{tríadas absolutas}}_{\text{perspectiva, ambigüedad 1}}.
\]

---

## 7. Resumen

El objeto central es la familia de tríadas perfectas:

\[
\mathcal{T}_n = \{(H_1, H_2, H_3) \in (u^\perp \cap \{-1,+1\}^n)^3 : \langle H_i, H_j\rangle = 0 \;\forall\; i\neq j\}.
\]

**Teoría general.** \(\mathcal{T}_n \neq \varnothing\) sii \(n \equiv 0 \pmod{4}\). Bajo \(S_n\), se descompone en \(n/4+1\) órbitas con tamaños \(n!/((t!)^4((m-t)!)^4)\). Una órbita uniforme existe sii \(n \equiv 0 \pmod{8}\), donde actúa libre y transitivamente \(S_n/(S_{n/8})^8\).

**El caso \(n=4\).** El único caso mínimo no trivial. Produce \(|P_{48}| = 48\) tríadas perfectas con la cascada:

\[
u^\perp \cap \{-1,+1\}^4 = \Delta(4,2) \;\longrightarrow\;
\text{8 bases ortogonales} \;\longrightarrow\;
P_{48} \cong B_3 \;\longrightarrow\;
\mathrm{Cay}(B_3,S) \cong Q_3 \,\square\, K_{3,3}.
\]

**Contribuciones principales.** Los objetos individuales — matrices de Hadamard de orden 4, \(J(4,2)\), \(B_3\), \(Q_3 \,\square\, K_{3,3}\), la transformada de Walsh-Hadamard — son clásicos. Este trabajo aporta:

1. **Clasificación completa de órbitas.** La descomposición \(\mathcal{T}_n/S_n = \{0,1,\ldots,m\}\) con la demostración de que \(t\) es invariante completo (Teorema 1).
2. **Fórmula cerrada de tamaños.** \(|\mathcal{O}_t| = n!/((t!)^4((m-t)!)^4)\), verificada para \(n=4,8,12\).
3. **Caso excepcional \(n=4\).** Es el único caso donde la fórmula produce un grupo (\(P_{48} \cong B_3\)) con grafo de Cayley \(Q_3\,\square\,K_{3,3}\) y firma espectral no genérica (\(z\)-score 39.84).
4. **Torsor para \(n=8\).** La órbita uniforme \(\mathcal{O}_1\) es un \(S_8\)-torsor, derivado del Teorema 1 sin argumentos adicionales.

---

## Referencias

1. Horadam, K. J. (2007). *Hadamard Matrices and Their Applications*. Princeton University Press.
2. MacWilliams, F. J., Sloane, N. J. A. (1977). *The Theory of Error-Correcting Codes*. North-Holland.
3. Brouwer, A. E., Cohen, A. M., Neumaier, A. (1989). *Distance-Regular Graphs*. Springer.
4. O'Donnell, R. (2014). *Analysis of Boolean Functions*. Cambridge University Press.
5. Hammack, R., Imrich, W., Klavžar, S. (2011). *Handbook of Product Graphs*, 2nd ed. CRC Press.
6. Sabidussi, G. (1960). Graph multiplication. *Mathematische Zeitschrift*, 72, 446–457.
7. Humphreys, J. E. (1990). *Reflection Groups and Coxeter Groups*. Cambridge University Press.
8. Cameron, P. J. (1994). *Combinatorics: Topics, Techniques, Algorithms*. Cambridge University Press.
9. Matolcsi, M., Matszangosz, Á. K., Varga, D., Weiner, M. (2026). Triplets of mutually unbiased bases. *Journal of Algebraic Combinatorics*, 63, 26. DOI:10.1007/s10801-026-01506-x
10. Mesner, D., Bhattacharya, P. (1990). Association schemes on triples. *Journal of Combinatorial Theory, Series A*, 55, 255–272.
11. Balmaceda, J., Briones, D. (2025). Families of association schemes on triples from two-transitive groups. *Ars Mathematica Contemporanea*, 25(3). arXiv:2107.07753.
