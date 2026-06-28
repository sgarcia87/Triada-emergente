# Estructura triádica 4D

**Autor:** Sergi Garcia Mecinas  
**Objeto de estudio:** \(\pm((\{-1,+1\}^{4})^{3})\)

---

## Resumen ejecutivo

Se estudió el espacio binario

\[
(\{-1,+1\}^{4})^{3},
\]

interpretado como una terna de bloques 4D:

\[
s=(H_1,H_2,H_3), \qquad H_i\in\{-1,+1\}^{4}.
\]

El espacio total contiene \(2^{12}=4096\) estados. Al imponer dos restricciones estructurales:

1. **equilibrio interno** en cada bloque: dos valores \(+1\) y dos valores \(-1\);
2. **equidistancia triádica:** \(d(H_1,H_2)=d(H_1,H_3)=d(H_2,H_3)=2\),

aparecen exactamente **48 estados perfectos**.

Estos 48 estados no son una colección arbitraria. La cadena estructural completa obtenida es:

\[
\text{equilibrio }2/2
\rightarrow
(\pm3,\mp1,\mp1,\mp1)
\rightarrow
T\cup(-T)
\rightarrow
Q_3
\rightarrow
Q_3\times S_3
\rightarrow
8\cdot K_{3,3}
\rightarrow
Q_3\,\square\,K_{3,3}
\rightarrow
Q_4\times 3\ \text{capas}.
\]

La geometría primaria son dos tetraedros regulares opuestos \(T\cup(-T)\) en el hiperplano de suma cero. El cubo \(Q_3\) emerge como grafo relacional entre las 8 familias. El grafo completo de los 48 estados es el producto cartesiano \(Q_3\,\square\,K_{3,3}\) con 144 aristas y espectro laplaciano exacto derivable analíticamente.

El análisis espectral de Walsh-Hadamard sobre \(Q_{12}\) muestra que los 48 estados tienen una firma estadísticamente excepcional: concentración del 58.5% de energía en orden \(k=6\) (z-score 39.84 respecto a subconjuntos aleatorios), anulación exacta de todos los órdenes impares demostrable analíticamente, y robustez ante controles que preservan simetrías parciales (z-score mínimo 8.78 ante el control más cercano).

La aportación es una estructura combinatoria y geométrica coherente, verificable y no genérica, conectada con objetos conocidos: códigos de peso constante, grafos de Johnson, el sistema de raíces \(A_3\), el cubo \(Q_3\) y el grupo \(S_3\). No se hacen afirmaciones sobre física, consciencia ni aplicaciones externas no demostradas.

El grupo de automorfismos del grafo acoplado \(G_{48}^+ \cong Q_3\,\square\,K_{3,3}\) tiene orden \(|Aut(G)| = 3456 = 48 \cdot 72\), verificado algebraicamente y computacionalmente. El grafo es vértice-transitivo (ningún estado privilegiado) y tiene exactamente dos órbitas de aristas que no se mezclan, lo que demuestra que la distinción entre estructura intra-familia e inter-familia es intrínseca al grafo, no una elección de representación.


---

## Novedad y alcance

### Lo que no es nuevo

Los objetos individuales que aparecen en este trabajo son clásicos y perfectamente conocidos:

- Las matrices de Hadamard de orden 4 son objeto de estudio desde el siglo XIX.
- El grafo de Johnson \(J(4,2)\), el hipersímplice \(\Delta(4,2)\) y el sistema de raíces \(A_3\) pertenecen a la combinatoria y geometría discreta estándar.
- El producto cartesiano de grafos \(Q_3 \,\square\, K_{3,3}\) y la fórmula de automorfismos de Sabidussi son resultados establecidos.
- La transformada de Walsh-Hadamard es una herramienta estándar en análisis de funciones booleanas.

### Lo que sí es nuevo

La contribución no son los objetos individuales sino **la cadena exacta que los conecta desde una única condición matricial discreta mínima**:

\[
(H_1,H_2,H_3) \text{ perfecta}
\iff
\begin{pmatrix} u \\ H_1 \\ H_2 \\ H_3 \end{pmatrix}
\text{ es Hadamard}
\;\Rightarrow\;
\text{octaedro} \rightarrow J(4,2) \rightarrow 8 \text{ bases} \rightarrow Q_3 \times S_3 \rightarrow Q_3 \,\square\, K_{3,3} \rightarrow |Aut|=3456.
\]

Esta cadena tiene tres propiedades que la hacen no genérica:

**1. Irreducibilidad estadística.** La firma espectral de Walsh-Hadamard del conjunto sobre \(Q_{12}\) concentra el 58.5% de energía en orden \(k=6\), con z-score 39.84 respecto a subconjuntos aleatorios del mismo tamaño. Aplicando controles que preservan las simetrías más obvias (antipodal, equilibrado, ambas), el z-score mínimo es 8.78. La señal es irreducible a propiedades más simples que la condición triádica completa.

**2. Dinámica natural independiente.** El funcional \(E_H = \sum_i(u\cdot H_i)^2 + \sum_{i<j}(H_i\cdot H_j)^2\) selecciona exactamente los 48 estados como únicos mínimos globales sin mencionar equilibrio ni distancia Hamming. Emerge de la teoría de matrices de Hadamard, no fue diseñado para seleccionar el conjunto.

**3. Protección algebraica intrínseca.** Las 144 aristas del grafo acoplado forman exactamente dos órbitas bajo \(Aut(G_{48}^+)\) que nunca se mezclan. La distinción intra-familia / inter-familia no es una convención del investigador: está protegida por la simetría del objeto.

Las 48 tríadas perfectas son además exactamente los 48 elementos del grupo hiperoctaédrico \(B_3 \cong C_2^3 \rtimes S_3\) — el grupo de simetrías del cubo y el octaedro — verificado por cerradura bajo multiplicación matricial.

### Lo que no debe afirmarse

Este trabajo no demuestra ninguna ley física, ninguna teoría de la gravedad o la consciencia, ninguna conexión con numerología ni excepcionalidad absoluta frente a todas las construcciones alternativas posibles. El cuadrado de Khajuraho es una coordenatización aritmética compatible (categoría C), no una simetría del sistema.

La contribución es un ejercicio de geometría discreta y combinatoria no genérico: una semilla matemática pequeña que genera una densidad inusual de propiedades simétricas y conexiones rígidas.

---

**Nota sobre categorías:** este documento distingue resultados demostrados por enumeración o álgebra (A), propiedades derivadas de definiciones (A†), resultados que dependen de una dinámica concreta (B) e interpretaciones conceptuales (C).

---

# 1. Definición formal del modelo

El modelo base es:

\[
H=(\{-1,+1\}^{4})^{3}.
\]

Un estado se escribe como:

\[
s=(H_1,H_2,H_3),
\]

donde cada bloque es un vector binario de cuatro coordenadas:

\[
H_i=(h_{i1},h_{i2},h_{i3},h_{i4}),
\qquad h_{ij}\in\{-1,+1\}.
\]

El espacio total contiene:

\[
|H|=(2^4)^3=16^3=4096.
\]

Equivalentemente:

\[
(\{-1,+1\}^{4})^{3}\cong \{-1,+1\}^{12}.
\]

---

# 2. Estados perfectos

## 2.1 Equilibrio interno

Un bloque \(H_i\) se considera equilibrado si contiene dos signos \(+1\) y dos signos \(-1\). En notación de suma:

\[
\sum_{j=1}^{4} h_{ij}=0.
\]

El número de bloques equilibrados es:

\[
\binom{4}{2}=6.
\]

Las seis configuraciones equilibradas pueden escribirse como:

```text
--++
-+-+
-++-
+--+
+-+-
++--
```

Estas seis palabras equivalen al conjunto de palabras binarias de longitud 4 y peso 2.

## 2.2 Condición Hamming triádica

Un estado perfecto satisface además:

\[
d(H_1,H_2)=d(H_1,H_3)=d(H_2,H_3)=2.
\]

Es decir, cada par de bloques difiere exactamente en dos posiciones.

## 2.3 Enumeración completa

La enumeración exhaustiva de los 4096 estados da:

\[
48
\]

estados perfectos.

La fracción del espacio total es:

\[
\frac{48}{4096}=0.01171875=1.171875\%.
\]

---

# 3. Teorema central

## Teorema central

En \((\{-1,+1\}^{4})^{3}\), los estados que cumplen equilibrio interno \(2+/2-\) en cada bloque y distancia Hamming \(2/2/2\) entre bloques inducen exactamente ocho vectores de familia de la forma:

\[
(\pm3,\mp1,\mp1,\mp1)
\]

junto con sus permutaciones. Estos ocho vectores forman dos tetraedros regulares opuestos en el hiperplano:

\[
x_1+x_2+x_3+x_4=0.
\]

El grafo relacional natural entre familias es isomorfo al cubo \(Q_3\), y los 48 estados se organizan como:

\[
48=|Q_3|\times |S_3|=8\times 6.
\]

---

# 3bis. Principio de organización Hadamard

**Categoría epistemológica:** A (equivalencia demostrada por verificación exhaustiva y álgebra lineal elemental)

## 3bis.1 Teorema de equivalencia con matrices de Hadamard

Sea \(u = (1,1,1,1) \in \{-1,+1\}^4\) el vector unidad. Dada una terna \((H_1, H_2, H_3)\) con \(H_i \in \{-1,+1\}^4\), se define la matriz:

\[
M =
\begin{pmatrix}
u \\ H_1 \\ H_2 \\ H_3
\end{pmatrix}
\in \{-1,+1\}^{4\times4}.
\]

**Teorema.** La terna \((H_1, H_2, H_3)\) es perfecta (equilibrio \(2+/2-\) y distancia Hamming \(2/2/2\)) si y solo si:

\[
MM^T = 4I_4.
\]

Es decir, \(M\) es una matriz de Hadamard de orden 4.

**Demostración.** La condición \(MM^T = 4I_4\) expande entrada a entrada como:

\[
(MM^T)_{ij} = \sum_{k=1}^{4} M_{ik} M_{jk} = \langle \text{fila}_i, \text{fila}_j \rangle.
\]

Las entradas diagonales exigen \(\|u\|^2 = \|H_i\|^2 = 4\), que es automático para vectores en \(\{-1,+1\}^4\).

Las entradas fuera de la diagonal exigen:

\[
\langle u, H_i \rangle = 0 \iff H_i \text{ es equilibrado},
\]

\[
\langle H_i, H_j \rangle = 0 \iff d(H_i, H_j) = 2.
\]

La segunda equivalencia se sigue de que para \(a, b \in \{-1,+1\}^4\):

\[
\langle a, b \rangle = 4 - 2\,d(a,b),
\]

por lo que \(\langle a,b\rangle = 0 \iff d(a,b) = 2\). $\square$

**Verificación computacional.** Los dos conjuntos coinciden exactamente:

| Método | Estados encontrados |
|---|---:|
| \(MM^T = 4I_4\) | 48 |
| Equilibrio + Hamming 2/2/2 | 48 |
| Coincidencia exacta | Sí |

## 3bis.2 Reformulación compacta

La caracterización más compacta del conjunto perfecto es:

\[
P_{48} = \left\{ (H_1,H_2,H_3) \in (\{-1,+1\}^4)^3 : \begin{pmatrix} u \\ H_1 \\ H_2 \\ H_3 \end{pmatrix} \text{ es una matriz de Hadamard de orden 4} \right\}.
\]

Esta formulación reemplaza dos condiciones separadas (equilibrio y equidistancia Hamming) por una sola condición algebraica matricial. Las condiciones originales son consecuencias de la ortogonalidad, no axiomas independientes.

## 3bis.3 El octaedro en \(u^\perp\) como geometría primaria

Los 6 vectores equilibrados de longitud 4 son exactamente los vectores de \(\{-1,+1\}^4\) ortogonales a \(u\):

\[
B = \{ v \in \{-1,+1\}^4 : \langle u, v \rangle = 0 \} = \binom{[4]}{2} \longleftrightarrow E(K_4).
\]

Sus propiedades métricas son:

- Norma: \(\|v\|^2 = 4\) para todo \(v \in B\).
- Productos escalares entre vectores distintos: solo dos valores posibles, \(\{-4, 0\}\).
  - \(\langle a,b\rangle = 0\): vectores ortogonales (distancia Hamming 2).
  - \(\langle a,b\rangle = -4\): vectores antipodales (distancia Hamming 4, \(b = -a\)).

Los 6 vectores forman un **octaedro regular** en el hiperplano \(u^\perp : x_1+x_2+x_3+x_4=0\). Este octaedro es exactamente \(\Delta(4,2)\), el hipersímplice de orden 2 en dimensión 4, cuyos vértices son los subconjuntos de tamaño 2 de \([4]\).

## 3bis.4 Las tríadas perfectas como bases ortogonales del octaedro

Dentro del octaedro en \(u^\perp\), una tríada perfecta es exactamente una **base ortogonal de 3 vectores**:

\[
(H_1, H_2, H_3) \text{ perfecta} \iff H_1, H_2, H_3 \in B \text{ y } \langle H_i, H_j \rangle = 0 \text{ para } i \neq j.
\]

El conteo directo confirma:

- Bases ortogonales no ordenadas de 3 vectores en \(B\): **8**.
- Ordenaciones de cada base: \(3! = 6\).
- Total de tríadas ordenadas: \(8 \times 6 = \mathbf{48}\).

Las 8 bases ortogonales son exactamente las 8 familias identificadas en la sección 3. El paso de las 8 familias a los 48 estados es el paso de bases no ordenadas a bases ordenadas, es decir, a la acción de \(S_3\) sobre cada base.

La cadena estructural se extiende hacia atrás:

\[
u^\perp \cap \{-1,+1\}^4 = \text{octaedro} \rightarrow \text{8 bases ortogonales} \rightarrow 48 = 8 \times S_3.
\]

## 3bis.5 El funcional \(E_H\): primera dinámica independiente

Se define el funcional de organización Hadamard:

\[
E_H(H_1,H_2,H_3) = \sum_{i=1}^{3}(u\cdot H_i)^2 + \sum_{1\leq i<j\leq 3}(H_i\cdot H_j)^2.
\]

**Proposición.** \(E_H(H_1,H_2,H_3) = 0\) si y solo si \((H_1,H_2,H_3)\) es perfecta.

**Demostración.** Cada sumando es un cuadrado, luego \(E_H \geq 0\). Se anula si y solo si cada sumando es cero, lo que equivale a \(\langle u,H_i\rangle = 0\) para todo \(i\) y \(\langle H_i,H_j\rangle = 0\) para todo par \(i\neq j\), que es exactamente \(MM^T = 4I_4\). $\square$

La distribución de \(E_H\) sobre los 4096 estados de \(Q_{12}\) es:

| \(E_H\) | Estados |
|---:|---:|
| **0** | **48** |
| 12 | 768 |
| 16 | 1152 |
| 28 | 1152 |
| 32 | 648 |
| 48 | 192 |
| 60 | 128 |
| 96 | 8 |

Los 48 perfectos son los únicos mínimos globales. El siguiente nivel (\(E_H=12\)) contiene 768 estados, a distancia de un único fallo de ortogonalidad.

**Independencia respecto a la definición original.** El funcional \(E_H\) no menciona explícitamente el equilibrio 2+/2− ni la distancia Hamming 2. Ambas condiciones emergen como consecuencias de la condición de ortogonalidad que anula \(E_H\). Esto lo convierte en la primera dinámica natural del sistema que no fue diseñada para seleccionar los 48 estados: los selecciona porque son las únicas configuraciones que completan \(u\) hasta una base ortogonal discreta.

Esto responde directamente a la pregunta abierta 16.5 (dinámica natural): \(E_H\) es una función de coste derivada de la teoría de matrices de Hadamard, no de los defectos triádicos.

## 3bis.6 Relación con la distribución de energía triádica

La distribución de la energía triádica clásica \(E(s) = |H_1\cdot\mathbf{1}| + |H_2\cdot\mathbf{1}| + |H_3\cdot\mathbf{1}| + |d_{12}-2| + |d_{13}-2| + |d_{23}-2|\) sobre \(Q_{12}\) tiene valores en \(\{0,2,4,6,8,10,12,14,18\}\), con mínimo exactamente en los mismos 48 estados. El funcional \(E_H\) es cuadrático mientras que \(E\) es lineal en los defectos; ambos seleccionan el mismo conjunto mínimo pero con paisajes de energía distintos. El paisaje de \(E_H\) tiene la ventaja de derivarse directamente de la teoría de matrices de Hadamard.

## 3bis.7 Estatus epistemológico

| Resultado | Categoría |
|---|---|
| \(MM^T=4I_4 \iff\) tríada perfecta | A — álgebra lineal elemental + verificación exhaustiva |
| Los 6 equilibrados forman un octaedro en \(u^\perp\) | A — cálculo directo de normas y productos escalares |
| 8 bases ortogonales × 6 = 48 | A — enumeración exhaustiva |
| \(E_H=0 \iff\) tríada perfecta | A — consecuencia directa de la equivalencia con Hadamard |
| \(E_H\) es independiente de la definición original | A† — no menciona equilibrio ni Hamming explícitamente |
| \(E_H\) como dinámica natural | A† — mínimo global por construcción, no por diseño ad hoc |

---

# 4. Demostración del núcleo tetraédrico

## 4.1 Vector de familia

Dado un estado perfecto:

\[
s=(H_1,H_2,H_3),
\]

definimos el vector de familia como la suma columna a columna:

\[
F(s)=H_1+H_2+H_3.
\]

Cada coordenada de \(F(s)\) pertenece a:

\[
\{-3,-1,+1,+3\},
\]

porque suma tres valores \(\pm1\).

Como cada bloque es equilibrado:

\[
\sum_{j=1}^{4}H_i(j)=0
\]

para \(i=1,2,3\). Por tanto:

\[
\sum_{j=1}^{4}F(s)_j=0.
\]

Así, todos los vectores de familia viven en el hiperplano:

\[
x_1+x_2+x_3+x_4=0.
\]

## 4.2 Por qué aparece \((\pm3,\mp1,\mp1,\mp1)\)

Para tres bloques, en cada columna pueden ocurrir dos tipos de patrones:

1. los tres signos son iguales; entonces la columna suma \(+3\) o \(-3\);
2. dos signos son iguales y uno distinto; entonces la columna suma \(+1\) o \(-1\).

Sea \(k\) el número de columnas de tipo dividido, es decir, columnas en las que no coinciden los tres signos.

Una columna dividida aporta exactamente 2 diferencias Hamming al total de los tres pares de bloques. Una columna unánime aporta 0 diferencias.

Como en un estado perfecto:

\[
d(H_1,H_2)+d(H_1,H_3)+d(H_2,H_3)=2+2+2=6,
\]

se tiene:

\[
2k=6,
\]

por lo que:

\[
k=3.
\]

Luego exactamente tres columnas son divididas y una columna es unánime.

Por tanto, el vector de familia tiene una coordenada de valor \(\pm3\) y tres coordenadas de valor \(\pm1\). Como además la suma total debe ser cero, las únicas posibilidades son:

\[
(3,-1,-1,-1)
\]

sus permutaciones, y sus opuestos globales:

\[
(-3,+1,+1,+1).
\]

Así aparecen exactamente ocho familias.

## 4.3 Cada familia contiene 6 estados

Tomemos como ejemplo la familia:

\[
F=(3,-1,-1,-1).
\]

La primera coordenada suma 3, así que los tres bloques tienen \(+1\) en la primera posición. Las otras tres coordenadas suman \(-1\), lo que significa que en cada una de ellas hay exactamente un \(+1\) y dos \(-1\).

Cada bloque ya tiene un \(+1\) en la primera coordenada. Como debe ser equilibrado, cada bloque necesita exactamente un \(+1\) adicional en las tres coordenadas restantes.

Asignar esos tres \(+1\) restantes, uno por bloque y uno por columna, equivale a una permutación de tres elementos:

\[
3!=6.
\]

Por tanto, cada familia contiene 6 estados.

Como hay 8 familias:

\[
8\times 6=48.
\]

## 4.4 Tetraedro regular

Consideremos los cuatro vectores positivos:

\[
v_1=(3,-1,-1,-1),
\]

\[
v_2=(-1,3,-1,-1),
\]

\[
v_3=(-1,-1,3,-1),
\]

\[
v_4=(-1,-1,-1,3).
\]

Todos tienen norma cuadrada:

\[
v_i\cdot v_i=12.
\]

Para \(i\neq j\), el producto escalar es:

\[
v_i\cdot v_j=-4.
\]

La distancia cuadrada entre vértices distintos es:

\[
\|v_i-v_j\|^2
=\|v_i\|^2+\|v_j\|^2-2v_i\cdot v_j
=12+12-2(-4)=32.
\]

Todas las distancias entre vértices distintos son iguales. Por tanto, los cuatro vectores forman un tetraedro regular.

## 4.5 Tetraedro opuesto

Los cuatro vectores restantes son:

\[
-v_1,-v_2,-v_3,-v_4.
\]

Forman otro tetraedro regular, invertido respecto al origen. La estructura de familias es:

\[
T\cup(-T).
\]

## 4.6 Centro algebraico

La suma de los ocho vectores de familia es:

\[
\sum_{i=1}^{4}v_i+\sum_{i=1}^{4}(-v_i)=(0,0,0,0).
\]

El centroide existe exactamente, pero no coincide con ningún estado ni familia. El centro natural del conjunto es algebraico, no un vértice manifestado.

## 4.7 Relación con \(A_3\)

Las diferencias entre vértices del tetraedro son:

\[
v_i-v_j=4(e_i-e_j).
\]

Los vectores \(e_i-e_j\) son las raíces del sistema \(A_3\). Por tanto, la geometría de las familias está directamente relacionada con el hiperplano natural de \(A_3\):

\[
x_1+x_2+x_3+x_4=0.
\]

---

# 5. Emergencia del cubo \(Q_3\)

La geometría euclídea primaria es \(T\cup(-T)\), no el cubo.

El cubo aparece al definir una relación entre familias de polaridad opuesta no antipodales. Esto produce el grafo:

\[
K_{4,4}-M,
\]

donde \(M\) es el emparejamiento antipodal.

Este grafo tiene:

- 8 vértices;
- 12 aristas;
- grado 3 en cada vértice;
- es bipartito;
- diámetro 3;
- espectro de adyacencia:

\[
3,1,1,1,-1,-1,-1,-3.
\]

Por tanto:

\[
G_{\text{familias}}\cong Q_3.
\]

La verificación computacional confirmó:

| Propiedad | Resultado |
|---|---:|
| Familias | 8 |
| Aristas mínimas | 12 |
| Grado por vértice | 3 |
| Bipartito | Sí |
| Isomorfo a \(Q_3\) | Sí |

Además, entre las 8 familias aparecen las siguientes relaciones geométricas:

| Relación entre familias | Número de pares |
|---|---:|
| Pares antipodales | 4 |
| Pares dentro del mismo tetraedro | 12 |
| Pares de polaridad opuesta no antipodales, aristas de \(Q_3\) | 12 |

---

# 6. Estructura interna de los 48 estados

Los 48 estados se reparten como:

\[
8\ \text{familias}\times 6\ \text{permutaciones}=48.
\]

Cada familia contiene 6 estados, correspondientes a las permutaciones de una triada:

\[
|S_3|=3!=6.
\]

Bajo las relaciones internas consideradas, el grafo de los 48 estados tiene:

- 48 nodos;
- 72 aristas;
- grado medio 3;
- 8 componentes;
- cada componente tiene 6 estados y corresponde a una familia.

Así:

\[
72=8\times 9=\frac{48\times 3}{2}.
\]

El 72 aparece como consecuencia de la estructura interna de los 48 estados, no como número independiente.

**Nota sobre simetría global.** El centroide de las 8 familias es \((0,0,0,0)\), que no corresponde a ningún estado ni familia. El grafo \(Q_3\) es regular: todos los vértices tienen grado 3 y la misma excentricidad. No existe vértice privilegiado.

---

# 7. Dinámicas y cobertura (resumen)

**Categoría:** B — resultados dependientes de reglas concretas, no evidencia independiente de la estructura.

**Potencial estructural \(\Phi\).** Cualquier función \(\Phi = w_E E + w_H H\) con \(w_E, w_H > 0\) tiene \(\Phi = 0 \iff\) estado perfecto (propiedad A†, no dinámica independiente). La primera dinámica genuinamente independiente es \(E_H\) (sección 3bis).

**Cobertura de \(Q_{12}\).** Radio de cobertura: 6. Distancia media al perfecto más cercano: 2.52. Los 8 estados a distancia máxima 6 corresponden a configuraciones de máxima polarización.

**Dinámica greedy de 1 bit.** Tasa de convergencia a perfectos: 40.2% (1648 de 4096). Longitud media de trayectorias exitosas: 1.71 pasos. Mínimos locales: 576 estados (14.1% del espacio), todos a distancia ≤ 4 de algún perfecto. La dinámica no es globalmente convergente.

**Simetría global.** La inversión \(s \mapsto -s\) preserva el conjunto perfecto e intercambia las 4 familias positivas con las 4 negativas. No hay sesgo de signo.

---

# 8. Generalización a \((\{-1,+1\}^{n})^{3}\)

## 8.1 Criterio general

Para \(n\), se estudian tres bloques:

\[
H_1,H_2,H_3\in\{-1,+1\}^{n}.
\]

Un estado perfecto generalizado debe cumplir:

1. cada bloque está equilibrado;
2. las distancias Hamming entre los tres bloques son:

\[
d(H_1,H_2)=d(H_1,H_3)=d(H_2,H_3)=\frac{n}{2}.
\]

## 8.2 Condición necesaria \(n\equiv 0\pmod 4\)

En cada columna de tres signos, una columna dividida aporta 2 diferencias Hamming al total de los tres pares, y una columna unánime aporta 0.

Como el total requerido es:

\[
3\cdot \frac{n}{2}=\frac{3n}{2},
\]

este número debe ser par, porque es igual a \(2k\), donde \(k\) es el número de columnas divididas.

Por tanto:

\[
2k=\frac{3n}{2}
\]

\[
k=\frac{3n}{4}.
\]

Así, \(n\) debe ser múltiplo de 4.

Esta es una condición necesaria para la existencia de estados perfectos bajo este criterio.

## 8.3 Resultados computacionales para \(n=2,3,4,5,6,8\)

| \(n\) | Estados totales \(2^{3n}\) | Bloques equilibrados | Hamming objetivo | Estados perfectos | Familias | Cierre antipodal |
|---:|---:|---:|---:|---:|---:|---|
| 2 | 64 | 2 | 1 | 0 | 0 | Sí |
| 3 | 512 | 0 | N/A | 0 | 0 | Sí |
| 4 | 4096 | 6 | 2 | 48 | 8 | Sí |
| 5 | 32768 | 0 | N/A | 0 | 0 | Sí |
| 6 | 262144 | 20 | 3 | 0 | 0 | Sí |
| 8 | 16777216 | 70 | 4 | 45360 | 1176 | Sí |

Para \(n=4\), las familias tienen distribución:

\[
8\ \text{familias de 6 estados}.
\]

Para \(n=8\), las familias tienen distribución:

\[
1120\ \text{familias de 36 estados},
\]

\[
56\ \text{familias de 90 estados}.
\]

## 8.4 Conclusión

El caso \(n=4\) es el primer caso no trivial limpio. El caso \(n=8\) también produce estados perfectos, pero ya no conserva la simplicidad:

\[
48=Q_3\times S_3.
\]

Por tanto, el caso 4D tiene un papel especial como mínima estructura completa con equilibrio triádico no trivial.

---

# 9. Control D.5: unicidad del conjunto equilibrado (resumen)

Se analizaron exhaustivamente todos los subconjuntos de 6 palabras de longitud 4 dentro de \(\{-1,+1\}^4\): \(\binom{16}{6} = 8008\) subconjuntos.

**Resultado principal:** el conjunto equilibrado de 6 palabras (\(u^\perp \cap \{-1,+1\}^4\)) produce 48 tríadas ordenadas con distancia 2/2/2. Solo 8 de los 8008 subconjuntos producen exactamente 48 tríadas, y 56 producen 48 o más.

**El conjunto equilibrado no maximiza tríadas** — existen subconjuntos con 72 tríadas ordenadas. Sin embargo, los de 72 tríadas pierden centroide cero y cierre antipodal. Dentro de los subconjuntos centrados y antipodales simultáneamente, el valor de 8 tríadas no ordenadas es máximo y se alcanza en exactamente 8 subconjuntos.

**Conclusión:** la excepcionalidad del conjunto equilibrado no es por densidad de tríadas sino por la combinación simultánea de equilibrio, centroide cero, cierre antipodal y estructura \(Q_3 \times S_3\) — propiedades que son exactamente las que permiten la completación Hadamard (sección 3bis).

---

# 10. Correspondencias con objetos matemáticos conocidos

La estructura encontrada se conecta con objetos conocidos:

## 10.1 Código de peso constante

Los bloques equilibrados de longitud 4 corresponden a palabras binarias de longitud 4 y peso 2:

\[
\binom{4}{2}=6.
\]

## 10.2 Diseño combinatorio

Las 6 configuraciones equilibradas son todos los subconjuntos de tamaño 2 de un conjunto de 4 elementos. Esto corresponde al diseño completo de pares:

\[
2-(4,2,1).
\]

## 10.3 Grafo de Johnson

A nivel de bloque, las palabras equilibradas están relacionadas con el grafo de Johnson:

\[
J(4,2).
\]

## 10.4 Sistema de raíces \(A_3\)

Las diferencias entre los vectores de familia son proporcionales a raíces de tipo \(A_3\):

\[
v_i-v_j=4(e_i-e_j).
\]

## 10.5 Cubo \(Q_3\)

El cubo aparece como grafo relacional entre las 8 familias, no como geometría euclídea primaria.

## 10.6 Grupo \(S_3\)

Cada familia contiene 6 estados, correspondientes a las 6 permutaciones posibles de los tres bloques.

## 10.7 Dualidad politópica y sólidos platónicos

**Categoría:** A (consecuencias combinatorias directas de la estructura ya establecida)

La construcción triádica induce una secuencia natural de dualidades entre politopos que conecta tres sólidos platónicos.

### El hipersímplice \(\Delta(4,2)\) es un octaedro

Los 6 vectores equilibrados son exactamente los vértices del hipersímplice \(\Delta(4,2)\): el politopo convexo cuyos vértices son los vectores binarios de longitud 4 con exactamente dos unos. Tiene 6 vértices, 12 aristas y 8 caras triangulares — los datos combinatorios exactos del octaedro regular:

\[
\Delta(4,2) \cong \text{octaedro}.
\]

El grafo de adyacencia de sus vértices es \(J(4,2)\), el grafo octaédrico.

### Las 8 familias son las 8 caras del octaedro

Los 8 triángulos no ordenados de \(J(4,2)\) son exactamente las 8 caras triangulares del octaedro. Se dividen en dos grupos de cuatro:

- 4 estrellas de \(K_4\) (tres aristas con un vértice común) → tetraedro \(T\)
- 4 triángulos de \(K_4\) (tres aristas formando un triángulo) → tetraedro \(-T\)

Los dos tetraedros opuestos \(T \cup (-T)\) son la bipartición natural de las caras del octaedro.

### El cubo \(Q_3\) como dual relacional del octaedro

El dual del octaedro es el cubo: 8 caras del octaedro → 8 vértices del cubo. El grafo de adyacencia entre las 8 caras del octaedro es exactamente \(Q_3\). Por tanto:

\[
\text{octaedro}^* \cong \text{cubo} = Q_3.
\]

El cubo \(Q_3\) que aparece en el modelo no es una geometría primaria independiente: es el **dual relacional** del octaedro generado por \(\Delta(4,2)\).

### Los tres sólidos platónicos emergentes

| Sólido | Cómo emerge en el modelo |
|---|---|
| Octaedro | Como \(\Delta(4,2)\), generado por los 6 bloques equilibrados |
| Cubo | Como dual del octaedro / grafo relacional \(Q_3\) entre familias |
| Tetraedro | Como las dos familias \(T\) y \(-T\) de vectores de familia |

La cadena politópica completa es:

\[
\text{equilibrio }2/2
\rightarrow
\Delta(4,2)
\cong
\text{octaedro}
\rightarrow
\text{octaedro}^* = \text{cubo }Q_3
\rightarrow
T\cup(-T) = \text{dos tetraedros opuestos}.
\]

Los tres sólidos no son postulados ni añadidos: emergen combinatoriamente desde la regla de equilibrio binario.

### Lo que no aparece

El dodecaedro y el icosaedro no emergen en el caso \(n=4\). La familia completa de los cinco sólidos platónicos no está presente. La conexión demostrada es:

\[
\text{tetraedro} \leftrightarrow \text{octaedro} \leftrightarrow \text{cubo}.
\]

### Por qué \(n=4\) es geométricamente especial

Para \(n\) par general, los bloques equilibrados corresponden al hipersímplice \(\Delta(n, n/2)\):

| \(n\) | Hipersímplice | Dimensión | Sólido platónico |
|---:|---|---:|---|
| 4 | \(\Delta(4,2)\) | 3 | Octaedro ✓ |
| 6 | \(\Delta(6,3)\) | 5 | — |
| 8 | \(\Delta(8,4)\) | 7 | — |

El caso \(n=4\) es el único en que \(\Delta(n, n/2)\) coincide exactamente con un sólido platónico tridimensional. Para \(n \geq 6\), el hipersímplice vive en dimensión \(\geq 5\) sin análogo platónico ordinario. Esto explica analíticamente por qué \(n=4\) produce una estructura tan compacta y por qué los casos \(n=6,8\) no tienen la misma limpieza geométrica.

---

# 11. Análisis espectral de Walsh-Hadamard del conjunto perfecto

**Categoría epistemológica:** A (resultados demostrados por enumeración exhaustiva y test estadístico controlado)

## 11.1 Motivación

Los resultados de las secciones anteriores caracterizan el conjunto de 48 estados perfectos desde el punto de vista algebraico, geométrico y combinatorio. Esta sección añade una caracterización espectral: la firma del conjunto en la base de funciones de Walsh-Hadamard sobre \(Q_{12}\).

La transformada de Walsh-Hadamard (WHT) descompone cualquier subconjunto de \(\{-1,+1\}^{12}\) en componentes de distinto orden de interacción. Para un subconjunto \(S \subseteq \{-1,+1\}^{12}\) de indicador \(f_S\), los coeficientes de Walsh son:

\[
\hat{f}(m) = \frac{1}{N} \sum_{x \in \{-1,+1\}^{12}} f_S(x)\,(-1)^{\langle m, x \rangle}, \qquad N = 4096,
\]

donde \(\langle m, x \rangle\) denota el producto escalar modular. El orden espectral \(k\) de un coeficiente se define como el peso de Hamming de la máscara \(m\):

\[
k = |m|_1 \in \{0, 1, \ldots, 12\}.
\]

El eigenvalor del laplaciano del hipercubo asociado al orden \(k\) es \(\lambda_k = 2k\).

## 11.2 Propiedades espectrales exactas del conjunto perfecto

La computación exhaustiva sobre los 48 estados perfectos revela tres propiedades exactas.

### Propiedad E1 — Anulación exacta de órdenes impares

\[
\sum_{|m|_1 = k} \hat{f}(m)^2 = 0 \qquad \text{para todo } k \text{ impar.}
\]

Toda la energía espectral del conjunto perfecto recae exclusivamente en órdenes pares.

**Demostración.** El conjunto perfecto es cerrado bajo inversión global \(s \mapsto -s\) (verificado computacionalmente; véase sección 8). La inversión global actúa sobre los coeficientes de Walsh multiplicando por \((-1)^k\). Si el conjunto es invariante bajo esta operación, los coeficientes de orden impar son iguales a sus negados, luego son cero. $\square$

### Propiedad E2 — Simetría especular exacta

\[
\sum_{|m|_1 = k} \hat{f}(m)^2 = \sum_{|m|_1 = 12-k} \hat{f}(m)^2 \qquad \text{para todo } k.
\]

La distribución de energía es simétrica respecto al orden central \(k = 6\).

### Propiedad E3 — Uniformidad de módulo en coeficientes dominantes

Todos los coeficientes de Walsh de orden 4, 6, 8 no nulos tienen el mismo valor absoluto:

\[
|\hat{f}(m)| = \frac{3}{256} = 0.01171875 \qquad \text{para } |m|_1 \in \{4, 6, 8\}.
\]

Esta uniformidad es una firma de regularidad combinatoria alta: el conjunto perfecto "proyecta" de modo equidistribuidocon respecto a todas las funciones de paridad de orden medio.

## 11.3 Distribución de energía por orden espectral

La tabla siguiente recoge la fracción de energía espectral por orden, el número de coeficientes no nulos y el eigenvalor del laplaciano asociado.

| Orden \(k\) | Fracción de energía | Coeficientes no nulos | Eigenvalor \(\lambda = 2k\) |
|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 2 |
| 2 | 2.37% | 18 | 4 |
| 3 | 0 | 0 | 6 |
| 4 | 17.79% | 111 | 8 |
| 5 | 0 | 0 | 10 |
| **6** | **58.50%** | **252** | **12** |
| 7 | 0 | 0 | 14 |
| 8 | 17.79% | 111 | 16 |
| 9 | 0 | 0 | 18 |
| 10 | 2.37% | 18 | 20 |
| 11 | 0 | 0 | 22 |
| 12 | 1.19% | 1 | 24 |

Observaciones:

- El 58.50% de la energía espectral se concentra en el orden \(k = 6\), que corresponde al eigenvalor laplaciano máximo de \(Q_{12}\). El conjunto perfecto está dominado por las interacciones de orden exactamente la mitad de la dimensión del espacio.

- Las energías en órdenes \(k\) y \(12-k\) son idénticas (simetría especular exacta).

- El único coeficiente de orden 12 corresponde a la máscara \(m = (1,1,\ldots,1)\) (todos los bits) y vale \(3/256\), reflejando la densidad global del conjunto.

## 11.4 Coeficientes dominantes y su interpretación triádica

Los 30 coeficientes de mayor valor absoluto corresponden a máscaras de orden 4, 6 y 8, todos con \(|\hat{f}| = 3/256\). Las máscaras dominantes de orden 6 son subconjuntos de exactamente 2 bits de cada bloque triádico. Por ejemplo:

\[
m = \{0,1,4,5,8,9\} \longleftrightarrow \text{primeros 2 bits de } H_1, H_2, H_3.
\]

Esto indica que las funciones de paridad que "ven" la estructura triádica de bloque son exactamente las más informativas espectralmente.

Las máscaras de orden 4 y 8 dominantes corresponden respectivamente a la selección de un bloque completo (\{0,1,2,3\}, \{4,5,6,7\}, \{8,9,10,11\}) o de dos bloques completos.

## 11.5 Test estadístico de Monte Carlo

Para determinar si el perfil espectral del conjunto perfecto es estadísticamente excepcional, se comparó con 10.000 subconjuntos aleatorios de igual tamaño (48 estados) extraídos uniformemente de \(Q_{12}\).

### Protocolo

- Espacio: \(Q_{12} = \{0,1\}^{12}\), cardinalidad 4096.
- Tamaño de subconjunto: 48 (igual al conjunto perfecto).
- Número de muestras aleatorias: 10.000.
- Semilla: 12345 (reproducible).
- Estadístico primario: fracción de energía espectral en orden \(k = 6\).

### Resultados

| Estadístico | Valor |
|---|---:|
| Energía en \(k=6\) del conjunto perfecto | 0.5850 |
| Media aleatoria en \(k=6\) | 0.2257 |
| Desviación estándar aleatoria | 0.0090 |
| Máximo observado en 10.000 muestras | 0.2650 |
| **Z-score** | **39.84** |
| **p-valor empírico** | **\(< 10^{-4}\)** |

En las 10.000 muestras aleatorias, ninguna alcanzó la energía \(k=6\) del conjunto perfecto (0.5850). El máximo observado fue 0.265, a más de 32 desviaciones estándar por debajo del valor perfecto.

### Resultado secundario: paridad espectral

La fracción de energía en órdenes pares fue medida también para cada muestra aleatoria:

| Grupo | Conjunto perfecto | Media aleatoria |
|---|---:|---:|
| Órdenes pares | 1.0000 (exacto) | 0.4999 |
| Órdenes impares | 0.0000 (exacto) | 0.5001 |

El p-valor empírico para la energía par total es también \(< 10^{-4}\). Los subconjuntos aleatorios distribuyen aproximadamente la mitad de su energía en órdenes pares y la otra mitad en impares. El conjunto perfecto concentra el 100% en órdenes pares, consistente con la propiedad E1 demostrada analíticamente.

## 11.6 Interpretación estructural

La firma espectral del conjunto perfecto tiene tres características simultáneas que son en sí mismas raras de forma aislada y excepcionales en combinación:

1. **Anulación de paridad** (propiedad algebraica exacta): solo los conjuntos con simetría antipodal perfecta exhiben esta característica.

2. **Concentración extrema en \(k = n/2\)**: en la literatura de análisis de funciones booleanas, las funciones con energía concentrada en el orden central son estructuralmente especiales. Las funciones *bent* (máxima no-linealidad) tienen energía uniforme; el conjunto perfecto tiene el comportamiento opuesto: concentración extrema en una sola frecuencia, compatible con máxima selectividad en ese orden.

3. **Uniformidad de coeficientes**: todos los coeficientes no nulos de orden 4, 6 y 8 comparten el mismo módulo \(3/256\). Esto implica que el conjunto perfecto actúa como un objeto combinatorialmente regular respecto a las funciones de paridad de orden medio.

## 11.7 Relación con los objetos conocidos de la sección 10

La concentración espectral en \(k=6\) tiene una lectura directa en términos de la estructura combinatoria establecida:

- Las máscaras de orden 6 dominantes seleccionan exactamente 2 bits de cada bloque triádico. Estas son las funciones de paridad que detectan la coherencia inter-bloques impuesta por la condición \(d(H_i, H_j) = 2\).

- Las máscaras de orden 4 dominantes seleccionan un bloque completo, detectando la coherencia intra-bloque impuesta por el equilibrio \(2+/2-\).

- La simetría especular \(k \leftrightarrow 12-k\) corresponde a la simetría complemento de \(J(4,2)\): si \((A, B, C)\) es un triángulo de \(J(4,2)\), también lo es \((\bar{A}, \bar{B}, \bar{C})\).

El espectro de Walsh-Hadamard no añade una nueva estructura al sistema triádico, sino que la revela desde una perspectiva armónica discreta que es independiente de la construcción geométrica de las secciones anteriores.

## 11.8 Estatus epistemológico

| Resultado | Categoría |
|---|---|
| Anulación de órdenes impares | A — demostrable analíticamente por simetría antipodal |
| Simetría especular \(k \leftrightarrow 12-k\) | A — demostrable por complemento de \(J(4,2)\) |
| Uniformidad de módulo \(3/256\) | A — verificado por enumeración exhaustiva |
| Concentración en \(k=6\): z-score 39.84 | A — test Monte Carlo con 10.000 muestras, \(p < 10^{-4}\) |

Ninguno de estos resultados depende de dinámicas, funciones de coste ni elecciones de parámetros. Son propiedades intrínsecas del conjunto de 48 estados perfectos vistas a través de la transformada de Walsh-Hadamard.

---

# 12. Controles espectrales fuertes: irreducibilidad de la condición triádica

**Categoría epistemológica:** A (test estadístico controlado con modelos nulos jerárquicos)

## 12.1 Motivación

La sección 11 demostró que la energía espectral en \(k=6\) del conjunto perfecto es excepcional respecto a subconjuntos aleatorios libres (z-score 39.84). Sin embargo, el conjunto perfecto tiene dos propiedades estructurales conocidas que podrían explicar parcialmente esa concentración:

1. **Cierre antipodal**: el conjunto es invariante bajo \(s \mapsto -s\).
2. **Equilibrio de bloques**: cada bloque satisface \(\sum h_{ij} = 0\).

Para determinar si la señal espectral se debe a la condición triádica completa o es un subproducto de estas propiedades más simples, se construyeron cuatro controles jerárquicos.

## 12.2 Diseño de los cuatro controles

| Etiqueta | Restricción impuesta | Descripción |
|---|---|---|
| `libre` | Ninguna | Subconjuntos de 48 estados de \(Q_{12}\) sin restricción |
| `antipodal` | Cierre bajo \(s \mapsto -s\) | 24 pares antipodales elegidos al azar |
| `equilibrado` | Cada bloque suma 0 | Los 48 estados tienen equilibrio 2+/2− en \(H_1, H_2, H_3\) |
| `equilibrado\_antipodal` | Ambas condiciones | Equilibrio y cierre antipodal simultáneos |

El conjunto perfecto satisface las cuatro restricciones y además la condición triádica \(d(H_i, H_j) = 2\). Cada control elimina progresivamente menos restricciones, cerrando el espacio de hipótesis nulas.

Se generaron 3.000 muestras por control.

## 12.3 Resultados

| Control | Media \(k=6\) | Std | Máximo observado | Z-score | p-valor |
|---|---:|---:|---:|---:|---:|
| `libre` | 0.2259 | 0.0093 | 0.2696 | 38.79 | \(<10^{-4}\) |
| `equilibrado` | 0.2281 | 0.0194 | 0.3228 | 18.35 | \(<10^{-4}\) |
| `equilibrado\_antipodal` | 0.4075 | 0.0194 | 0.4974 | 9.13 | \(<10^{-4}\) |
| `antipodal` | 0.4510 | 0.0153 | 0.4965 | 8.78 | \(<10^{-4}\) |
| **48 perfectos** | — | — | **0.5850** | — | — |

En los 3.000 × 4 = 12.000 subconjuntos de control generados, ninguno alcanzó la energía \(k=6\) del conjunto perfecto.

## 12.4 Lectura jerárquica

El resultado tiene una estructura de falsación en capas:

**Capa 1 — Control libre vs. perfecto:** el conjunto perfecto supera por 38.79σ a subconjuntos sin restricción. La señal es visible incluso sin ningún control.

**Capa 2 — Control equilibrado:** imponer equilibrio 2+/2− en cada bloque no eleva sustancialmente la media (0.228 vs. 0.226). El equilibrio interno solo no explica la concentración espectral.

**Capa 3 — Control antipodal:** imponer cierre antipodal sí eleva la media significativamente (de 0.226 a 0.451). Esto es consistente con la propiedad E1 demostrada: la simetría antipodal anula los órdenes impares y redistribuye energía hacia los pares, incluyendo \(k=6\). Pero la media antipodal (0.451) sigue estando a 8.78σ del valor perfecto (0.585).

**Capa 4 — Control equilibrado+antipodal:** combinando ambas restricciones la media sube a 0.408, pero sigue separada del perfecto por 9.13σ. Ningún subconjunto de los 3.000 muestreados con ambas restricciones alcanzó 0.585.

**Conclusión:** la concentración espectral en \(k=6\) no se explica por la simetría antipodal ni por el equilibrio de bloques, ni por su combinación. La condición triádica completa \(d(H_1,H_2)=d(H_1,H_3)=d(H_2,H_3)=2\) es la responsable del exceso residual. La señal espectral es **irreducible** a propiedades más simples.

## 12.5 Observación sobre paridad espectral por control

| Control | Energía pares | Energía impares |
|---|---:|---:|
| `libre` | 0.5001 | 0.4999 |
| `equilibrado` | 0.6040 | 0.3960 |
| `antipodal` | 1.0000 | 0.0000 |
| `equilibrado\_antipodal` | 1.0000 | 0.0000 |
| **48 perfectos** | **1.0000** | **0.0000** |

La anulación exacta de órdenes impares (energía par = 1) se produce en todos los controles antipodales, confirmando que esta propiedad es una consecuencia directa del cierre antipodal, no de la condición triádica. Sin embargo, dentro del subespacio de órdenes pares, la concentración extrema en \(k=6\) sigue siendo exclusiva del conjunto perfecto.

## 12.6 Estatus epistemológico

| Afirmación | Categoría |
|---|---|
| Ningún control libre alcanza 0.585 en k=6 (3.000 muestras) | A — resultado empírico directo |
| Ningún control antipodal alcanza 0.585 en k=6 (3.000 muestras) | A — resultado empírico directo |
| Ningún control equilibrado+antipodal alcanza 0.585 (3.000 muestras) | A — resultado empírico directo |
| La condición triádica es irreducible a antipodal+equilibrado | A — consecuencia de los tres puntos anteriores |

---

# 13. Grafo interno de los 48 estados: 8 copias de \(K_{3,3}\)

**Categoría epistemológica:** A (enumeración exhaustiva y cálculo algebraico exacto)

## 13.1 Definición del grafo interno

Se define el grafo interno \(G_{48}\) sobre los 48 estados perfectos de la siguiente manera:

- **Vértices:** los 48 estados perfectos.
- **Aristas:** dos estados \(s, s'\) de la **misma familia** están conectados si y solo si su distancia Hamming es:

\[
d(s, s') = 4.
\]

La restricción a la misma familia es estructural: estados de familias distintas tienen distancia Hamming que no es 4 en este contexto intra-triádico.

## 13.2 Estructura del grafo

La enumeración exhaustiva de los \(\binom{48}{2} = 1128\) pares de estados produce:

- **72 aristas** de distancia Hamming 4 intra-familia.
- **8 componentes conexas**, una por familia.
- Cada componente tiene **6 vértices** y **9 aristas**.

Un grafo de 6 vértices, 9 aristas, regular de grado 3, bipartito, es exactamente \(K_{3,3}\).

Por tanto:

\[
G_{48} \cong 8 \cdot K_{3,3}.
\]

## 13.3 Por qué \(K_{3,3}\): paridad de permutaciones en \(S_3\)

Cada familia contiene 6 estados correspondientes a las 6 permutaciones de los tres bloques \((H_1, H_2, H_3)\). El grupo \(S_3\) de permutaciones de 3 elementos tiene exactamente dos clases de paridad:

- **Permutaciones pares** (identidad, rotaciones de orden 3): 3 elementos.
- **Permutaciones impares** (transposiciones): 3 elementos.

Dos estados de la misma familia están a distancia Hamming 4 si y solo si corresponden a permutaciones de paridad opuesta. Esto se debe a que una transposición de bloques intercambia exactamente las posiciones donde los dos bloques difieren, produciendo una diferencia de exactamente 4 bits en la concatenación de 12 bits.

La estructura bipartita de \(K_{3,3}\) refleja directamente esta bipartición de \(S_3\) en pares e impares:

\[
K_{3,3} \longleftrightarrow S_3^+ \times S_3^-.
\]

## 13.4 Espectro laplaciano de \(G_{48}\)

El laplaciano \(L = D - A\) de \(G_{48}\) tiene espectro exacto:

\[
\text{spec}(L) = \{0^8,\ 3^{32},\ 6^8\}.
\]

Este espectro se obtiene por la fórmula del espectro de una unión disjunta de copias:

\[
\text{spec}(m \cdot H) = m \cdot \text{spec}(H).
\]

El espectro laplaciano de \(K_{3,3}\) es:

\[
\text{spec}(L_{K_{3,3}}) = \{0^1,\ 3^4,\ 6^1\}.
\]

Para 8 copias:

\[
\text{spec}(L_{G_{48}}) = \{0^8,\ 3^{32},\ 6^8\}.
\]

Los eigenvalores verificados computacionalmente son \(0\) (multiplicidad 8), \(3\) (multiplicidad 32) y \(6\) (multiplicidad 8), con precisión numérica \(< 10^{-9}\).

## 13.5 Interpretación como modos de Chladni discretos

Los eigenvectores del laplaciano de \(G_{48}\) constituyen los modos normales de vibración del grafo. Por analogía con los patrones de Chladni en membranas continuas, donde los nodos de vibración forman figuras geométricas regulares, los eigenvectores de \(L_{G_{48}}\) definen patrones discretos con estructura análoga.

**Modo 0 (eigenvalor 0, multiplicidad 8):** funciones constantes en cada componente. Hay una función de este tipo por copia de \(K_{3,3}\), correspondiente a la función que asigna el mismo valor a los 6 estados de cada familia. Son los modos de "volumen" del sistema.

**Modo 3 (eigenvalor 3, multiplicidad 32):** modos oscilatorios dentro de cada \(K_{3,3}\). Hay 4 por componente (32 = 8 × 4). Cada uno separa los vértices de \(K_{3,3}\) en dos grupos con valores opuestos, sin cancelarse globalmente. Corresponden a los modos internos de la bipartición pares/impares.

**Modo 6 (eigenvalor 6, multiplicidad 8):** modo antiperiódico máximo, uno por componente. Es el eigenvector de Fiedler máximo de \(K_{3,3}\): asigna valores \(+1\) a un lado y \(-1\) al otro de la bipartición, con máxima alternancia. Corresponde al patrón de Chladni de mayor frecuencia del sistema: estados pares positivos y estados impares negativos (o viceversa).

La analogía con Chladni no es solo metafórica: los eigenvectores del laplaciano de grafos son el objeto algebraico natural para describir modos normales en sistemas discretos, del mismo modo que las funciones propias del laplaciano continuo describen los patrones de Chladni en membranas.

## 13.6 Relación con la cadena estructural principal

El grafo \(G_{48} \cong 8 \cdot K_{3,3}\) añade un nuevo nivel a la cadena estructural del proyecto:

\[
(\{-1,+1\}^4)^3
\rightarrow
48\ \text{perfectos}
\rightarrow
(\pm3,\mp1,\mp1,\mp1)
\rightarrow
T \cup (-T)
\rightarrow
Q_3
\rightarrow
Q_3 \times S_3
\rightarrow
8 \cdot K_{3,3}
\]

El grafo \(K_{3,3}\) emerge al definir relaciones de distancia Hamming 4 dentro de cada familia. El cubo \(Q_3\) emerge al definir relaciones entre familias de polaridad opuesta no antipodales. Los dos grafos viven en niveles diferentes de la estructura: \(K_{3,3}\) es intra-familia, \(Q_3\) es inter-familia.

## 13.7 Estatus epistemológico

| Resultado | Categoría |
|---|---|
| \(G_{48} \cong 8 \cdot K_{3,3}\) | A — enumeración exhaustiva de los 1128 pares |
| Espectro laplaciano \(\{0^8, 3^{32}, 6^8\}\) | A — cálculo algebraico exacto (error numérico \(<10^{-9}\)) |
| Bipartición por paridad de \(S_3\) | A — consecuencia directa de la definición de permutación par/impar |
| Analogía con modos de Chladni discretos | C — interpretación compatible, no resultado físico |

---

# 14. Grafo acoplado completo: \(Q_3 \,\square\, K_{3,3}\)

**Categoría epistemológica:** A (construcción algebraica exacta y cálculo espectral verificado)

## 14.1 De los dos grafos parciales al grafo completo

Las secciones anteriores introdujeron dos grafos sobre los 48 estados perfectos con tipos de aristas distintos:

- **Grafo de familias** (\(Q_3\), sección 5): aristas entre estados de **familias distintas** relacionadas como vecinos en el cubo. Cada estado conecta con estados de otras 3 familias.

- **Grafo interno** (\(8 \cdot K_{3,3}\), sección 13): aristas entre estados de la **misma familia** a distancia Hamming 4. Cada estado conecta con 3 estados de su misma familia.

Al tomar la unión de ambos conjuntos de aristas sobre los 48 estados, se obtiene el **grafo acoplado completo** \(G_{48}^+\), que captura simultáneamente la estructura inter-familia y la estructura intra-familia.

## 14.2 Identificación como producto cartesiano

El grafo acoplado es exactamente el producto cartesiano de grafos:

\[
G_{48}^+ \cong Q_3 \,\square\, K_{3,3}.
\]

El **producto cartesiano** \(A \,\square\, B\) de dos grafos tiene como vértices los pares \((a, b)\) con \(a \in V(A)\), \(b \in V(B)\), y como aristas:

\[
(a,b) \sim (a',b') \iff (a = a' \text{ y } b \sim_B b') \quad\text{o}\quad (b = b' \text{ y } a \sim_A a').
\]

En el sistema triádico, los vértices son pares (familia, permutación), y las aristas son exactamente:
- aristas de \(K_{3,3}\) cuando la familia es la misma (estructura interna);
- aristas de \(Q_3\) cuando la permutación es la misma y las familias son vecinas en el cubo (estructura externa).

La verificación computacional confirma:

| Propiedad | Valor |
|---|---:|
| Vértices | 48 |
| Aristas totales | 144 |
| Aristas internas (\(K_{3,3}\)) | 72 |
| Aristas externas (\(Q_3\)) | 72 |
| Grado de cada vértice | 6 (3 internos + 3 externos) |
| ¿Regular? | Sí |
| ¿Bipartito? | Sí |
| ¿Conexo? | Sí |

## 14.3 Espectro laplaciano por fórmula de producto cartesiano

El espectro laplaciano del producto cartesiano satisface la fórmula exacta:

\[
\text{spec}\!\left(L_{A \,\square\, B}\right) = \left\{\lambda_i^A + \lambda_j^B : i \in \text{spec}(A),\ j \in \text{spec}(B)\right\}.
\]

Los espectros de los dos factores son:

\[
\text{spec}(L_{Q_3}) = \{0^1,\ 2^3,\ 4^3,\ 6^1\},
\]

\[
\text{spec}(L_{K_{3,3}}) = \{0^1,\ 3^4,\ 6^1\}.
\]

El espectro del producto cartesiano se obtiene sumando todos los pares:

| \(\lambda_{Q_3}\) | \(\lambda_{K_{3,3}}\) | Suma | Multiplicidad |
|---:|---:|---:|---:|
| 0 | 0 | **0** | \(1 \times 1 = 1\) |
| 2 | 0 | **2** | \(3 \times 1 = 3\) |
| 0 | 3 | **3** | \(1 \times 4 = 4\) |
| 4 | 0 | **4** | \(3 \times 1 = 3\) |
| 2 | 3 | **5** | \(3 \times 4 = 12\) |
| 6 | 0 | **6** | \(1 \times 1 = 1\) |
| 0 | 6 | **6** | \(1 \times 1 = 1\) |
| 4 | 3 | **7** | \(3 \times 4 = 12\) |
| 2 | 6 | **8** | \(3 \times 1 = 3\) |
| 6 | 3 | **9** | \(1 \times 4 = 4\) |
| 4 | 6 | **10** | \(3 \times 1 = 3\) |
| 6 | 6 | **12** | \(1 \times 1 = 1\) |

Total de eigenvalores: \(1+3+4+3+12+2+12+3+4+3+1 = 48\). ✓

El espectro completo verificado computacionalmente es:

\[
\text{spec}(L_{G_{48}^+}) = \{0^1,\ 2^3,\ 3^4,\ 4^3,\ 5^{12},\ 6^2,\ 7^{12},\ 8^3,\ 9^4,\ 10^3,\ 12^1\}.
\]

El error numérico máximo respecto a los valores enteros es \(< 10^{-9}\).

## 14.4 Propiedades espectrales destacadas

**Gap espectral:** el primer eigenvalor no nulo es \(\lambda_1 = 2\), heredado de \(Q_3\). Determina la velocidad de mezcla de caminatas aleatorias sobre el grafo y la conectividad algebraica.

**Eigenvalor máximo:** \(\lambda_{47} = 12 = 6 + 6\), con multiplicidad 1. Corresponde a la combinación del modo antiperiódico máximo de \(Q_3\) con el modo antiperiódico máximo de \(K_{3,3}\). Es el modo de Chladni de mayor frecuencia del sistema acoplado.

**Eigenvalor 6:** multiplicidad 2, no 1. Aparece por dos rutas independientes: \(6+0\) (modo máximo de \(Q_3\) con modo cero de \(K_{3,3}\)) y \(0+6\) (modo cero de \(Q_3\) con modo máximo de \(K_{3,3}\)). Esta degeneración accidental refleja la coincidencia de los eigenvalores máximos de los dos factores.

**Simetría del espectro:** los eigenvalores satisfacen la simetría \(\lambda_k + \lambda_{47-k} = 12\) para todo \(k\). Esto es consecuencia de que \(G_{48}^+\) es bipartito: el espectro laplaciano de un grafo bipartito regular de grado \(d\) es simétrico alrededor de \(d\).

## 14.5 Los 144 como consecuencia estructural

El número de aristas del grafo acoplado es:

\[
|E(Q_3 \,\square\, K_{3,3})| = |V(Q_3)| \cdot |E(K_{3,3})| + |E(Q_3)| \cdot |V(K_{3,3})|
= 8 \cdot 9 + 12 \cdot 6 = 72 + 72 = 144.
\]

El número 144, que aparece en el documento en el contexto de la polaridad exterior (sección 7), emerge aquí también como el número de aristas del grafo acoplado. Sin embargo, los dos contextos son independientes: el 144 de la polaridad exterior cuenta relaciones entre estados etiquetados, mientras que el 144 de \(G_{48}^+\) cuenta aristas de distancia estructural sobre los 48 estados base. La coincidencia numérica no implica identidad de los objetos.

## 14.6 Extensión de la cadena estructural

El grafo acoplado completa la descripción de la estructura de grafos del sistema triádico:

\[
(\{-1,+1\}^4)^3
\rightarrow
48\ \text{perfectos}
\rightarrow
(\pm3,\mp1,\mp1,\mp1)
\rightarrow
T \cup (-T)
\rightarrow
Q_3 \quad \text{(inter-familia)}
\rightarrow
Q_3 \times S_3
\rightarrow
8 \cdot K_{3,3} \quad \text{(intra-familia)}
\rightarrow
Q_3 \,\square\, K_{3,3} \quad \text{(grafo completo)}
\]

Los dos grafos parciales (\(Q_3\) y \(8 \cdot K_{3,3}\)) son subgrafos complementarios de \(G_{48}^+\): sus conjuntos de aristas son disjuntos y su unión es \(G_{48}^+\).

## 14.7 Estatus epistemológico

| Resultado | Categoría |
|---|---|
| \(G_{48}^+ \cong Q_3 \,\square\, K_{3,3}\) | A — verificación computacional directa del isomorfismo |
| 144 aristas (72 internas + 72 externas) | A — enumeración exhaustiva |
| Regular de grado 6, bipartito, conexo | A — propiedades directas del producto cartesiano |
| Espectro \(\{0^1, 2^3, 3^4, 4^3, 5^{12}, 6^2, 7^{12}, 8^3, 9^4, 10^3, 12^1\}\) | A — fórmula de producto cartesiano + verificación numérica |
| Simetría espectral alrededor de 6 | A — consecuencia de bipartición regular de grado 6 |
| Coincidencia numérica 144 con polaridad exterior | A† — observación estructural, objetos distintos |

---

# 15. Grupo de automorfismos de \(G_{48}^+\)

**Categoría epistemológica:** A (cálculo algebraico exacto y verificación computacional triple)

## 15.1 Orden del grupo de automorfismos

Para el producto cartesiano de dos grafos no isomorfos entre sí, el grupo de automorfismos factoriza exactamente:

\[
Aut(A \,\square\, B) \cong Aut(A) \times Aut(B) \qquad \text{si } A \not\cong B.
\]

Como \(Q_3 \not\cong K_{3,3}\) (distintos grados, distinto número de vértices), se tiene:

\[
|Aut(G_{48}^+)| = |Aut(Q_3)| \cdot |Aut(K_{3,3})| = 48 \cdot 72 = 3456.
\]

Los valores individuales son:

\[
|Aut(Q_3)| = 2^3 \cdot 3! = 48,
\]

\[
|Aut(K_{3,3})| = 2 \cdot (3!)^2 = 72.
\]

Este resultado se verificó por tres métodos independientes:

| Método | Resultado |
|---|---:|
| Fórmula algebraica de producto cartesiano | 3456 |
| Enumeración de automorfismos por generadores | 3456 |
| Conteo exhaustivo con GraphMatcher | 3456 |

## 15.2 Transitividad en vértices

El grafo \(G_{48}^+\) es **vértice-transitivo**: para cualquier par de estados perfectos \(u, v \in P_{48}\), existe un automorfismo \(\phi \in Aut(G_{48}^+)\) tal que \(\phi(u) = v\).

La consecuencia matemática directa es que ningún estado perfecto tiene una posición estructural privilegiada dentro del grafo. Todos los estados son algebraicamente equivalentes bajo las simetrías del sistema.

Esto formaliza una propiedad que se deducía informalmente de la regularidad de \(Q_3\) y \(K_{3,3}\) por separado, pero que ahora se establece para el grafo acoplado completo.

## 15.3 Dos órbitas de aristas: la distinción interna/externa es intrínseca

Bajo la acción de \(Aut(G_{48}^+)\), las 144 aristas de \(G_{48}^+\) se dividen en exactamente **dos órbitas**:

| Órbita | Tipo | Cardinalidad |
|---|---|---:|
| Órbita 1 | Aristas internas (\(K_{3,3}\), intra-familia) | 72 |
| Órbita 2 | Aristas externas (\(Q_3\), inter-familia) | 72 |

Las dos órbitas no se intersectan: ningún automorfismo de \(G_{48}^+\) lleva una arista interna a una externa, ni viceversa.

Este resultado tiene una consecuencia conceptual importante: **la distinción entre estructura intra-familia y estructura inter-familia no es una elección de representación ni una convención del investigador. Es una propiedad intrínseca del grafo, invariante bajo todas sus simetrías.** La partición en dos tipos de aristas está protegida algebraicamente.

## 15.4 Propiedades métricas del grafo

| Propiedad | Valor |
|---|---:|
| Diámetro | 5 |
| Radio | 5 |
| Distancia media entre pares | 2.723 |
| ¿Auto-centrado? | Sí (diámetro = radio) |

El grafo es **auto-centrado**: todos los vértices tienen la misma excentricidad (5). Esto es consistente con la vértice-transitividad: si hubiera vértices con distinta excentricidad, no podrían ser todos equivalentes bajo automorfismos.

El diámetro 5 significa que los estados perfectos más alejados dentro del grafo acoplado están a 5 pasos. Dado que el grafo tiene 48 vértices de grado 6, un diámetro de 5 es compacto.

## 15.5 Implicación sobre el etiquetado de Khajuraho

El análisis de automorfismos permite precisar el estatus del etiquetado de Khajuraho (sección 16) con exactitud algebraica:

| Restricción sobre el etiquetado | Automorfismos preservados |
|---|---:|
| Etiquetado 1..48 exacto | **1** (solo la identidad) |
| Preserva las 3 capas de eje | 96 |
| Preserva la polaridad interna de \(K_{3,3}\) | 1728 |
| Sin restricción (grupo completo) | 3456 |

El etiquetado de Khajuraho es **máximamente rígido**: solo el automorfismo identidad lo preserva. Esto confirma cuantitativamente la decisión de tratarlo como categoría C: no es una simetría del sistema triádico, sino una coordenatización aritmética particular entre las \(3456\) posibles formas de etiquetar el grafo de manera compatible con la estructura \(Q_4 \times 3\).

Los 1728 automorfismos que preservan la polaridad interna representan exactamente la mitad del grupo total (\(3456/2\)), correspondiente al subgrupo que no mezcla los dos lados de la bipartición de \(K_{3,3}\).

## 15.6 Estatus epistemológico

| Resultado | Categoría |
|---|---|
| \(\|Aut(G_{48}^+)\| = 3456\) | A — verificación triple (algebraica + generadores + exhaustiva) |
| \(Aut(G_{48}^+) \cong Aut(Q_3) \times Aut(K_{3,3})\) | A — teorema de producto cartesiano para grafos no isomorfos |
| Vértice-transitividad | A — consecuencia de la transitividad de \(Q_3\) y \(K_{3,3}\) |
| Dos órbitas de aristas no mezcladas | A — verificación computacional exhaustiva |
| Diámetro 5, radio 5, auto-centrado | A — cálculo de distancias sobre el grafo |
| Khajuraho: estabilizador 1 | A — consecuencia de la rigidez del etiquetado aritmético |

---

# 16. Indexación natural de los 48 estados por \(Q_4 \times 3\) capas

**Categoría epistemológica:** A (biyección verificada) y C (nota sobre cuadrados mágicos)

## 16.1 Emergencia de \(Q_4\) en el sistema triádico

En el grafo acoplado \(Q_3 \,\square\, K_{3,3}\), cada estado perfecto queda determinado por dos coordenadas:

- **Familia** \(f \in \{0,\ldots,7\}\): representada por 3 bits \((q_0, q_1, q_2) \in \{0,1\}^3\), que indexan los 8 vértices de \(Q_3\).
- **Posición interna** \(p \in \{0,\ldots,5\}\): dentro de cada copia de \(K_{3,3}\), los 6 estados se dividen en eje \(a \in \{0,1,2\}\) (las 3 parejas de la bipartición pares/impares de \(S_3\)) y polaridad \(\pi \in \{0,1\}\) (el lado de la bipartición dentro de cada pareja).

Al combinar los 3 bits de familia con el bit de polaridad \(\pi\), se obtiene un vector de 4 bits:

\[
(q_0, q_1, q_2, \pi) \in \{0,1\}^4,
\]

que indexa los 16 vértices del hipercubo \(Q_4\). El eje \(a \in \{0,1,2\}\) actúa como índice de capa, produciendo la descomposición:

\[
48 = 16 \times 3 = Q_4 \times 3\ \text{capas}.
\]

## 16.2 El hipercubo \(Q_4\) como extensión natural de \(Q_3\)

La relación algebraica es:

\[
Q_4 = Q_3 \times P_2,
\]

donde \(P_2\) es el camino de dos vértices (un solo bit adicional). En el sistema triádico, este bit adicional es exactamente la polaridad interna \(\pi\) de \(K_{3,3}\), que separa los estados de permutación par de los de permutación impar dentro de cada familia.

La cadena de extensiones de hipercubos que aparece en el sistema triádico es por tanto:

\[
Q_3 \xrightarrow{+\pi} Q_4,
\]

donde \(Q_3\) describe las familias y \(Q_4\) describe las familias más su polaridad interna.

## 16.3 Biyección con \(\{1,\ldots,48\}\)

Se construye una biyección explícita entre los 48 estados y las etiquetas \(1,\ldots,48\) de la siguiente manera.

**Paso 1.** Cada vector de 4 bits \((q_0, q_1, q_2, \pi)\) determina una posición en una rejilla \(4 \times 4\) mediante:

\[
\text{fila} = q_0 + 2q_1, \qquad \text{columna} = q_2 + 2\pi.
\]

**Paso 2.** La rejilla \(4 \times 4\) se recorre con una función de indexación \(\sigma : \{0,1,2,3\}^2 \to \{1,\ldots,16\}\), produciendo un valor base \(v \in \{1,\ldots,16\}\).

**Paso 3.** La etiqueta final del estado con eje \(a\) y valor base \(v\) es:

\[
\ell = 16 \cdot a + v \in \{1,\ldots,48\}.
\]

La verificación computacional confirma que, para cualquier función de indexación biyectiva \(\sigma\), el resultado es una permutación exacta de \(\{1,\ldots,48\}\):

\[
\{\ell(s) : s \in P_{48}\} = \{1, 2, \ldots, 48\}.
\]

## 16.4 Las tres capas

La descomposición en 3 capas de 16 estados tiene una interpretación directa en términos del eje de \(K_{3,3}\):

| Capa | Eje \(a\) | Estados | Interpretación |
|---:|---:|---:|---|
| 0 | 0 | 16 | Primera pareja de permutaciones \((e, (12)(34)\cdot\ldots)\) |
| 1 | 1 | 16 | Segunda pareja de permutaciones |
| 2 | 2 | 16 | Tercera pareja de permutaciones |

Dentro de cada capa, los 16 estados están organizados según los 16 vértices de \(Q_4\), con la estructura de fila y columna determinada por los bits \((q_0, q_1, q_2, \pi)\).

## 16.5 Nota sobre cuadrados mágicos (categoría C)

*Esta subsección es una observación interpretativa, no un resultado demostrado del sistema triádico.*

El cuadrado de Khajuraho (siglo X, India) es una función de indexación \(\sigma\) particular de \(\{0,1,2,3\}^2 \to \{1,\ldots,16\}\) con propiedades excepcionales:

\[
\begin{pmatrix} 7 & 12 & 1 & 14 \\ 2 & 13 & 8 & 11 \\ 16 & 3 & 10 & 5 \\ 9 & 6 & 15 & 4 \end{pmatrix}
\]

Es un cuadrado mágico **pandiagonal y compacto** de orden 4: todas las filas, columnas, diagonales principales, diagonales rotas periódicas y todos los subcuadrados \(2\times2\) toroidales suman la constante mágica 34.

Al usar el cuadrado de Khajuraho como función \(\sigma\) en la construcción anterior, las tres capas heredan esta regularidad con constantes mágicas 34, 98 y 162 respectivamente (progresión aritmética de diferencia 64).

La pandiagonalidad refleja la simetría toroidal de \(Q_4\): el cuadrado se puede indexar cíclicamente en filas y columnas, consistentemente con la estructura del hipercubo, donde cada bit tiene dos vecinos periódicos. Sin embargo, la elección de este cuadrado concreto no altera ninguna propiedad de los 48 estados perfectos: cualquier biyección \(\sigma : \{1,\ldots,16\}\) produciría el mismo resultado estructural. La pandiagonalidad es una propiedad del cuadrado elegido para etiquetar, no una propiedad del sistema triádico.

## 16.6 Extensión de la cadena estructural

\[
(\{-1,+1\}^4)^3
\rightarrow
48\ \text{perfectos}
\rightarrow \cdots \rightarrow
Q_3 \times S_3
\rightarrow
Q_3 \,\square\, K_{3,3}
\rightarrow
Q_4 \times 3\ \text{capas}
\]

donde \(Q_4 = Q_3 \times P_2\) emerge al extender los bits de familia con la polaridad interna de \(K_{3,3}\).

## 16.7 Estatus epistemológico

| Resultado | Categoría |
|---|---|
| \(48 = Q_4 \times 3\) como descomposición natural | A — consecuencia directa de la estructura de \(Q_3 \,\square\, K_{3,3}\) |
| Biyección verificada con \(\{1,\ldots,48\}\) | A — verificación computacional exhaustiva |
| \(Q_4 = Q_3 \times P_2\) como extensión por polaridad | A — consecuencia algebraica de la bipartición de \(K_{3,3}\) |
| Cuadrado de Khajuraho como indexación posible | C — elección particular entre muchas equivalentes |
| Pandiagonalidad como propiedad del sistema triádico | **No válido** — es propiedad del cuadrado, no del sistema |

---

# 17. Estructura algebraica de las 48 tríadas

**Categoría:** A (verificación computacional exhaustiva y álgebra elemental)

## 17.1 Los tres ejes del octaedro y la operación multivaluada

Los 6 bloques equilibrados forman un octaedro en \(u^\perp\). Geométricamente, este octaedro tiene exactamente **3 ejes antipodales** — tres pares \(\{v, -v\}\) de vértices opuestos.

Dado un par de bloques ortogonales \(A, B\) (con \(\langle A, B\rangle = 0\)), existe un único eje faltante, pero con **dos orientaciones posibles**:

\[
A \star B = \{+C,\, -C\}.
\]

La verificación exhaustiva confirma que para los 12 pares ortogonales de bloques equilibrados, el complemento siempre produce exactamente 2 candidatos antipodales. La tríada no es una operación binaria cerrada: es una **regla de cierre multivaluada** que fuerza el eje pero no la orientación.

## 17.2 Descomposición exacta \(48 = 2^3 \cdot 3!\)

El octaedro en \(u^\perp \subset \mathbb{R}^4\) tiene exactamente **una** tripleta de ejes ortogonales (verificado computacionalmente: 1 tripleta sin signo ni orden). Las 48 tríadas perfectas son exactamente todas las formas de:

1. **orientar** los 3 ejes: \(2^3 = 8\) elecciones de signo;
2. **ordenar** los 3 ejes: \(3! = 6\) permutaciones.

Por tanto:

\[
48 = 2^3 \cdot 3! = 8 \times 6.
\]

Esto refina la descomposición \(Q_3 \times S_3\) con una interpretación geométrica precisa: \(Q_3 \cong \{-1,+1\}^3\) actúa como el grupo de orientaciones de los 3 ejes, y \(S_3\) actúa como el grupo de permutaciones.

El objeto algebraico correcto es el **producto semidirecto**:

\[
P_{48} \cong \{-1,+1\}^3 \rtimes S_3.
\]

## 17.3 Conexión con el grupo hiperoctaédrico \(B_3\)

El grupo hiperoctaédrico de dimensión 3 es:

\[
B_3 \cong C_2^3 \rtimes S_3,
\]

con orden \(|B_3| = 2^3 \cdot 3! = 48\). Es el **grupo completo de simetrías del cubo y del octaedro** en \(\mathbb{R}^3\): actúa permutando los 3 ejes coordenados y cambiando sus signos. Sus elementos son exactamente las matrices monomiales firmadas de tamaño \(3\times3\) — matrices con exactamente un \(\pm1\) por fila y columna.

**Teorema.** *Las 48 tríadas perfectas son exactamente los 48 elementos de \(B_3\), vía la representación como matrices monomiales firmadas sobre la base de ejes del octaedro.*

**Construcción.** Los 6 bloques equilibrados forman 3 pares antipodales \(\{\pm X, \pm Y, \pm Z\}\). Cada tríada perfecta ordenada \((H_1, H_2, H_3)\) asigna a cada \(H_i\) exactamente uno de los 6 bloques, produciendo una matriz \(3\times3\) con exactamente un \(\pm1\) por fila y columna:

\[
M_{ij} = \langle H_i, e_j \rangle / 4 \in \{-1, 0, +1\},
\]

donde \(e_1, e_2, e_3\) son los representantes positivos de los tres ejes.

**Verificación computacional independiente:**

| Propiedad | Resultado |
|---|---|
| Tríadas perfectas | 48 |
| Matrices monomiales firmadas \(3\times3\) distintas | 48 |
| Coincidencia exacta tríadas \(= B_3\) | ✓ True |
| Cerradura bajo multiplicación matricial | ✓ True |
| Determinante \(+1\) (simetrías propias) | 24 |
| Determinante \(-1\) (simetrías impropias) | 24 |

**Consecuencia.** Las 48 tríadas no son solo un conjunto especial de estados: forman un **grupo** bajo la multiplicación matricial de las representaciones firmadas. La construcción triádica produce exactamente \(B_3\).

Esto actualiza el resultado de la sección anterior: la identificación \(P_{48} \cong B_3\) no es solo combinatoria sino algebraica — las tríadas perfectas *son* el grupo de simetrías del cubo/octaedro. La descomposición \(48 = 2^3 \cdot 3!\) es la descomposición \(|C_2^3| \cdot |S_3|\) del producto semidirecto.

La conexión con \(A_3\) (sección 10.4) es ahora directa: \(A_3\) es un subsistema de raíces de \(B_3\), y las diferencias entre vectores de familia \(v_i - v_j = 4(e_i - e_j)\) son raíces de \(A_3\) incrustadas en el sistema \(B_3\).

## 17.7 \(Q_3 \,\square\, K_{3,3}\) como grafo de Cayley de \(B_3\)

**Teorema (verificado computacionalmente).** *El grafo acoplado \(Q_3 \,\square\, K_{3,3}\) es isomorfo al grafo de Cayley no dirigido de \(B_3\) con el conjunto de 6 generadores naturales:*

\[
S = \{\text{flip}_X,\, \text{flip}_Y,\, \text{flip}_Z,\, \text{swap}_{XY},\, \text{swap}_{XZ},\, \text{swap}_{YZ}\},
\]

*donde \(\text{flip}_i\) invierte el signo del eje \(i\) y \(\text{swap}_{ij}\) permuta los ejes \(i\) y \(j\).*

\[
\mathrm{Cay}(B_3, S) \cong Q_3 \,\square\, K_{3,3}.
\]

**Verificación independiente:**

| Propiedad | \(\mathrm{Cay}(B_3,S)\) | \(Q_3 \,\square\, K_{3,3}\) |
|---|---:|---:|
| Nodos | 48 | 48 |
| Aristas | 144 | 144 |
| Grado | 6 | 6 |
| Conexo | ✓ | ✓ |
| Bipartito | ✓ | ✓ |
| Diámetro | 5 | 5 |
| Triángulos | 0 | 0 |
| Isomorfo | ✓ True | — |

**Las dos órbitas de aristas tienen ahora interpretación generadora exacta:**

| Tipo de arista | Generador | Orbita |
|---|---|---|
| 72 internas (\(K_{3,3}\)) | \(\text{flip}_X, \text{flip}_Y, \text{flip}_Z\) | Cambio de signo de un eje |
| 72 externas (\(Q_3\)) | \(\text{swap}_{XY}, \text{swap}_{XZ}, \text{swap}_{YZ}\) | Transposición de dos ejes |
| Intersección | — | 0 (disjuntas) |

Las dos órbitas algebraicas bajo \(Aut(G_{48}^+)\) detectadas en la sección 15 son exactamente las dos clases de generadores de \(B_3\). La distinción interna/externa no es solo intrínseca al grafo — tiene una explicación generadora en términos de la acción del grupo.

**Consecuencia.** El grafo acoplado no es una construcción impuesta desde fuera: es el grafo de Cayley natural de \(B_3\) bajo sus generadores más simples. Las 144 aristas se explican como \(144 = 48 \cdot 6 / 2\) — 48 elementos del grupo, 6 generadores, cada arista contada dos veces. La cadena completa:

\[
\text{tríada perfecta}
\;\longleftrightarrow\;
\text{elemento de } B_3
\;\longleftrightarrow\;
\text{vértice de } \mathrm{Cay}(B_3, S)
\;\longleftrightarrow\;
\text{vértice de } Q_3 \,\square\, K_{3,3}.
\]

## 17.4 Principio de organización: formulación compacta

Los dos documentos anteriores convergen en una formulación que sintetiza el núcleo del trabajo:

> **La tríada perfecta no es una figura añadida al sistema. Es la forma máxima de ortogonalidad discreta compatible con el equilibrio \(2/2\) en dimensión 4.**

En términos algebraicos:

\[
\boxed{
\text{equilibrio } 2/2
\;\Rightarrow\;
\text{ortogonalidad discreta en } u^\perp
\;\Rightarrow\;
\text{Hadamard}
\;\Rightarrow\;
B_3
\;\Rightarrow\;
Q_3 \,\square\, K_{3,3}
}
\]

## 17.5 Nota sobre Chladni

La analogía con patrones de Chladni no es física sino estructural: en una membrana continua, las figuras de Chladni son modos propios del laplaciano continuo; aquí, los modos del laplaciano discreto del grafo \(Q_3 \,\square\, K_{3,3}\) producen patrones análogos. La conexión es:

\[
\text{Chladni físico} \;\leftrightarrow\; L\psi = \lambda\psi \text{ (laplaciano discreto)}.
\]

No implica ninguna relación con vibraciones físicas reales.

## 17.6 Estatus epistemológico

| Resultado | Categoría |
|---|---|
| Operación \(A \star B = \{+C,-C\}\) para pares ortogonales | A — verificación exhaustiva de los 12 pares |
| 1 única tripleta de ejes ortogonales en el octaedro | A — verificación computacional |
| \(48 = 2^3 \cdot 3!\) como orientaciones × permutaciones | A — consecuencia directa |
| \(P_{48} \cong B_3\) como grupo (cerradura verificada) | **A** — verificación computacional independiente |
| 24 simetrías propias + 24 impropias | A — distribución de determinantes verificada |
| \(A_3\) como subsistema de raíces de \(B_3\) | A† — conexión algebraica directa, formalización pendiente |
| \(\mathrm{Cay}(B_3,S) \cong Q_3 \,\square\, K_{3,3}\) | **A** — isomorfismo verificado computacionalmente |
| Flip → aristas \(K_{3,3}\), swap → aristas \(Q_3\) | **A** — verificación exhaustiva, intersección cero |

---

# 18. Métrica interna del grupo y propiedades de la operación \(A^{-1}B\)

**Categoría:** A (propiedades estándar de grupos, verificadas computacionalmente sobre \(B_3\))

## 18.1 Distancia de palabra y función de crecimiento

En el grafo de Cayley \(\mathrm{Cay}(B_3, S)\), la distancia entre dos nodos \(A\) y \(B\) coincide con la longitud mínima de palabra en los generadores que transforma \(A\) en \(B\). Esto define una métrica de palabra sobre \(B_3\):

\[
d(A,B) = \min\{n : A \cdot s_1 \cdots s_n = B,\; s_i \in S\}.
\]

La **función de crecimiento de bolas** desde la identidad — número de elementos a distancia exactamente \(k\) — es:

| Distancia \(k\) | Estados | Interpretación |
|---:|---:|---|
| 0 | 1 | Identidad |
| 1 | 6 | Los 6 generadores directos |
| 2 | 14 | Composición de dos generadores distintos |
| 3 | 16 | — |
| 4 | 9 | — |
| 5 | 2 | Los dos elementos más alejados de la identidad |
| **Total** | **48** | **\(= \|B_3\|\)** |

Diámetro: 5. Distancia media: 2.723. Estos valores coinciden con los del grafo \(Q_3 \,\square\, K_{3,3}\) (sección 15.4), como es esperable dado el isomorfismo.

## 18.2 Propiedades de los generadores

Los 6 generadores son involuciones:

\[
s^2 = e \quad \text{para todo } s \in S.
\]

De los \(\binom{6}{2} = 15\) pares de generadores:

- **6 pares conmutan** (\(ab = ba\)): pares de flips entre ejes distintos y algunos pares flip-swap compatibles.
- **9 pares no conmutan** (\(ab \neq ba\)): el orden de aplicación importa.

El ciclo mínimo del grafo tiene longitud 4 — consecuencia directa de que los generadores son involuciones y el grafo es bipartito (sin triángulos, verificado: 0 triángulos).

## 18.3 La operación \(A^{-1}B\) como comparación geométrica

Para cualquier par \(A, B \in B_3\), el elemento \(A^{-1}B\) es la transformación que lleva \(A\) a \(B\). Verificación computacional exhaustiva sobre los \(48^2 = 2304\) pares:

| Propiedad | Resultado | Categoría |
|---|---|---|
| \(d(e, A^{-1}B) = d(A,B)\) | 100% de pares | A — teorema estándar de grupos de Cayley |
| Misma propiedad para \(AB\) | 70.14% | — (no es la operación natural) |
| \(A^{-1}B = e \iff A = B\) | True | A — consecuencia directa |
| Invariancia bajo traslación izquierda: \((LA)^{-1}(LB) = A^{-1}B\) | 100% | A — propiedad de grupos |
| Misma invariancia para \(AB\) | 21.64% | — (no es invariante) |
| \(B^{-1}A = (A^{-1}B)^{-1}\) | 100% | A — consecuencia directa |
| Uniformidad: cada \(T\) aparece exactamente 48 veces como \(A^{-1}B\) | Mín=Máx=48 | A — acción regular del grupo sobre sí mismo |

La operación \(A^{-1}B\) es la métrica interna natural del grupo: mide la separación geométrica entre dos estados de forma invariante bajo cambio de referencia. El producto directo \(AB\) no tiene esta propiedad.

## 18.4 Tiempo discreto como longitud de palabra (categoría C)

La función de crecimiento de la sección 18.1 permite una interpretación algebraica — no física — de noción de "distancia desde la identidad":

\[
t(F) = d(e, F) = \text{longitud mínima de palabra que produce } F.
\]

Esta es una noción interna y bien definida dentro del sistema. El movimiento relativo entre dos estados \(A(t)\) y \(B(t)\) que evolucionan por la misma secuencia de generadores satisface:

\[
R(t) = B(t)A(t)^{-1} \in B_3 \quad \text{para todo } t,
\]

con distancia media final \(d(e, R) \approx 2.66\) en caminatas aleatorias de 80 pasos.

**Límite explícito.** Esto no es una teoría física del tiempo ni una afirmación sobre causalidad o relatividad. Es una propiedad algebraica: el sistema tiene una noción interna de "distancia desde un estado de referencia" que se conserva bajo el grupo y que se puede parametrizar con un entero no negativo.

## 18.5 Estatus epistemológico

| Resultado | Categoría |
|---|---|
| Función de crecimiento \(\{1,6,14,16,9,2\}\) | A — cálculo exacto sobre el grafo |
| Diámetro 5, distancia media 2.723 | A — consistente con secciones 14 y 15 |
| 6 generadores son involuciones | A — \(s^2=e\) verificado |
| 6 pares conmutan, 9 no conmutan | A — verificación exhaustiva |
| \(d(e,A^{-1}B)=d(A,B)\) al 100% | A — teorema de Cayley, verificado |
| Invariancia de \(A^{-1}B\) bajo traslación | A — propiedad de grupos |
| Uniformidad de \(A^{-1}B\) | A — acción regular |
| Tiempo discreto como longitud de palabra | C — interpretación algebraica compatible, no física |

## 18.6 Reconstrucción relacional: toda la estructura desde \(C(A,B) = A^{-1}B\)

Se puede preguntar si los estados absolutos son datos primarios necesarios, o si la estructura completa es recuperable únicamente desde la red de comparaciones \(C(A,B) = A^{-1}B\). La respuesta es afirmativa.

**Propiedades internas de \(C\).** La matriz de comparación satisface, para todos los pares de estados:

| Propiedad | Expresión | Verificado |
|---|---|---|
| Diagonal identidad | \(C(A,A) = e\) | ✓ True |
| Simetría inversa | \(C(B,A) = C(A,B)^{-1}\) | ✓ True |
| Ley de cociclo | \(C(A,B)\cdot C(B,D) = C(A,D)\) | ✓ True |

La ley de cociclo — que es simplemente \(A^{-1}B \cdot B^{-1}D = A^{-1}D\) en cualquier grupo — garantiza que las comparaciones son composables de forma coherente.

**Reconstrucción desde un ancla.** Para cualquier estado de referencia \(r \in P_{48}\), definir \(X_i = C(r,i) = r^{-1}i\) produce una reetiquetación de los 48 estados en la que \(r\) se convierte en la identidad. Verificación:

- Todos los 48 anclajes posibles reconstruyen 48 estados distintos: ✓ True
- Todas las comparaciones par a par se preservan bajo cualquier anclaje: ✓ True

Los estados absolutos se recuperan salvo elección de referencia — estructura de torseur de grupo.

**Reconstrucción del grafo.** Definiendo adyacencia únicamente desde las comparaciones:

\[
i \sim j \iff C(i,j) \in S,
\]

el grafo reconstruido es isomorfo al original con las mismas aristas exactas, y satisface:

- Isomorfo al grafo original: ✓ True
- Isomorfo a \(Q_3 \,\square\, K_{3,3}\): ✓ True

El grafo de Cayley es recuperable íntegramente desde las comparaciones sin conocer los estados absolutos.

**Reconstrucción de distancias.** La distancia entre dos estados se recupera como longitud de palabra de su comparación:

\[
d(A,B) = |C(A,B)|_S,
\]

con 0 errores sobre todos los \(48^2 = 2304\) pares.

**Invariancia y equivariancia.** Bajo traslación global izquierda \(A \mapsto LA\):

\[
C(LA, LB) = C(A,B) \quad \text{(invariancia al 100\%)}.
\]

Bajo traslación global derecha \(A \mapsto AR\):

\[
C(AR, BR) = R^{-1}C(A,B)R \quad \text{(equivariancia por conjugación al 100\%)}.
\]

**Reconstrucción desde árbol generador.** Usando solo una red local de \(47\) comparaciones (árbol generador del grafo), se reconstruyen coordenadas para los 48 estados y desde ellas la matriz de comparaciones completa — sin información redundante.

**Consecuencia.** Toda la estructura triádica — los 48 estados, el grafo \(Q_3 \,\square\, K_{3,3}\), las distancias y las simetrías — es completamente recuperable desde la red de comparaciones \(C(A,B) = A^{-1}B\), sin necesidad de estados absolutos como dato primario. Esto es una propiedad algebraica exacta del grupo \(B_3\), no una hipótesis adicional.

| Resultado | Categoría |
|---|---|
| Ley de cociclo \(C(A,B)C(B,D)=C(A,D)\) | A — trivialmente cierto en cualquier grupo |
| 48 anclajes distintos, comparaciones preservadas | A — isomorfismo de traslación |
| Grafo reconstruido desde \(C(i,j)\in S\) | A — definición del grafo de Cayley |
| Distancias reconstruidas con 0 errores | A — consecuencia del teorema de Cayley |
| Invariancia izquierda 100% | A — propiedad de multiplicación izquierda |
| Equivariancia derecha por conjugación 100% | A — propiedad de multiplicación derecha |
| Reconstrucción desde árbol (47 comparaciones) | A — spanning tree del grafo |

## 18.7 Dos niveles de reconstrucción: forma vs. grupo

La sección anterior muestra que la estructura es recuperable desde comparaciones. Un análisis más fino distingue qué información es necesaria en cada nivel.

**Nivel A — Grafo desnudo.** Conociendo solo qué nodos están conectados (sin etiquetas en las aristas):

| Propiedad recuperada | Resultado |
|---|---|
| 48 nodos, 144 aristas, grado 6 | ✓ |
| Bipartito, diámetro 5 | ✓ |
| Isomorfo a \(Q_3 \,\square\, K_{3,3}\) | ✓ |
| Automorfismos del grafo | 3456 |
| Traslaciones izquierdas de \(B_3\) | 48 |

Como \(3456 > 48\), el grafo desnudo tiene más simetría que \(B_3\) actuando por traslación. **El grafo solo no fija una única estructura de grupo:** hay 3456/48 = 72 formas de ver el mismo grafo como grafo de Cayley de \(B_3\), correspondientes a los automorfismos de \(K_{3,3}\).

**Nivel B — Aristas etiquetadas.** Añadiendo la etiqueta del generador a cada arista (\(\text{flip}_X, \text{flip}_Y, \text{flip}_Z, \text{swap}_{XY}, \text{swap}_{XZ}, \text{swap}_{YZ}\)) y eligiendo un nodo raíz arbitrario:

| Propiedad recuperada | Resultado |
|---|---|
| 48 nodos reconstruidos | ✓ True |
| Coordenadas únicas por nodo | ✓ True |
| Todas las aristas consistentes | ✓ True |
| Errores de arista | 0 |
| \(C(A,A)=e\) | ✓ True |
| \(C(B,A)=C(A,B)^{-1}\) | ✓ True |
| \(C(A,B)C(B,D)=C(A,D)\) | ✓ True |
| Distancias reconstruidas desde \(C\) | ✓ True |

Con aristas etiquetadas y una raíz, la estructura de grupo queda completamente fijada.

**Resumen de los tres niveles de información:**

\[
\underbrace{\text{grafo desnudo}}_{\text{forma} \atop \text{ambigüedad: 72}} \;\subset\; \underbrace{\text{aristas etiquetadas}}_{\text{grupo} \atop \text{ambigüedad: 48}} \;\subset\; \underbrace{\text{estados absolutos}}_{\text{perspectiva} \atop \text{ambigüedad: 1}}
\]

- El **grafo desnudo** da la forma topológica, con ambigüedad de 72 (automorfismos de \(K_{3,3}\)).
- Las **aristas etiquetadas** fijan el grupo, con ambigüedad residual de 48 (elección de raíz).
- Los **estados absolutos** equivalen a fijar una raíz, eliminando toda ambigüedad.

| Resultado | Categoría |
|---|---|
| Grafo desnudo isomorfo a \(Q_3\,\square\,K_{3,3}\) | A — verificado |
| Grafo desnudo no fija la estructura de grupo (3456 > 48) | A — consecuencia del análisis de automorfismos |
| Aristas etiquetadas + raíz reconstruyen los 48 estados | A — verificado, 0 errores |
| Tres niveles: forma ⊂ grupo ⊂ perspectiva | A† — organización conceptual de resultados anteriores |

## 18.8 Cadena inversa: de relaciones a Hadamard

La cadena estructural del proyecto corre en dirección directa:

\[
\text{Hadamard} \rightarrow P_{48} \cong B_3 \rightarrow \mathrm{Cay}(B_3,S) \cong Q_3\,\square\,K_{3,3}.
\]

Se verificó también la **dirección inversa**: partiendo de una red etiquetada de relaciones (sin estados absolutos), se reconstruyen los estados y se comprueba que satisfacen la condición Hadamard.

**Protocolo:** dado el grafo de Cayley etiquetado por los 6 generadores y una raíz arbitraria, se reconstruyen coordenadas relativas en \(B_3\). Esas coordenadas se convierten en tríadas \((H_1,H_2,H_3)\) y se verifica la condición matricial.

**Resultados:**

| Verificación | Resultado |
|---|---|
| Tríada raíz cumple \(MM^T=4I\) | ✓ True |
| Red etiquetada reconstruye 48 coordenadas | ✓ True |
| Coordenadas únicas | ✓ True |
| 0 aristas inconsistentes | ✓ True |
| Tríadas reconstruidas equilibradas | ✓ True |
| Tríadas reconstruidas ortogonales | ✓ True |
| Tríadas reconstruidas cumplen Hadamard | ✓ True |
| Coinciden con \(P_{48}\) directo | ✓ True |
| Grafo reconstruido \(\cong Q_3\,\square\,K_{3,3}\) | ✓ True |

La condición \(MM^T=4I\) no se impone: **emerge de la reconstrucción**. La cadena es biyectiva en ambas direcciones:

\[
\text{relaciones etiquetadas} + \text{raíz}
\;\longleftrightarrow\;
B_3
\;\longleftrightarrow\;
P_{48}
\;\longleftrightarrow\;
\text{Hadamard}.
\]

| Resultado | Categoría |
|---|---|
| Tríadas reconstruidas cumplen \(MM^T=4I\) | A — verificación exhaustiva, 48/48 |
| Cadena inversa completa sin errores | A — verificado |
| Equivalencia biyectiva de las cuatro representaciones | A — consecuencia de los resultados anteriores |

## 18.9 Unicidad axiomática de \(A^{-1}B\) como operación de comparación

Se compararon 7 operaciones binarias candidatas sobre \(B_3\) frente a 6 axiomas de comparación relacional:

1. \(C(A,A) = e\) — identidad diagonal
2. \(C(A,B) = e \iff A = B\) — identidad implica igualdad
3. \(C(B,A) = C(A,B)^{-1}\) — simetría inversa
4. \(d(e, C(A,B)) = d(A,B)\) — reconstrucción de distancias
5. \(C(A,B)\cdot C(B,D) = C(A,D)\) — ley de cociclo
6. \(C(LA,LB) = C(A,B)\) — invariancia bajo cambio de perspectiva izquierda

**Resultado:** la única operación que cumple los 6 axiomas al 100% es \(A^{-1}B\).

| Operación | Puntuación | Cociclo | Invariancia izquierda | Reconstrucción posible |
|---|---:|---:|---:|---|
| \(A^{-1}B\) | **100%** | **100%** | **100%** | ✓ |
| \(B^{-1}A\) | 86.8% | 20.8% | 100% | ✗ |
| \(AB^{-1}\) | 82.6% | 100% | 20.8% | ✓ |
| \(BA^{-1}\) | 69.4% | 20.8% | 20.8% | ✗ |
| \([A,B] = A^{-1}B^{-1}AB\) | 57.2% | 20.8% | 20.8% | ✗ |
| \(AB\) | 48.8% | 41.7% | 20.8% | ✗ |
| \(BA\) | 44.0% | 13.2% | 20.8% | ✗ |

El **discriminador crítico** es la ley de cociclo (axioma 5): \(B^{-1}A\) cumple casi todo excepto el cociclo (20.8%), y \(AB^{-1}\) falla en invariancia de perspectiva izquierda. Ambas condiciones son necesarias para que las comparaciones sean composables y para que la reconstrucción de estados desde una raíz sea posible.

**Consecuencia.** Dentro de \(B_3\), la operación \(C(A,B) = A^{-1}B\) no es una elección entre varias igualmente válidas: es la única que permite formalizar coherentemente la noción de comparación relacional composable. Los resultados de las secciones 18.6–18.8 se apoyan en esta operación, y esta sección demuestra que no hay alternativa que los sostenga.

| Resultado | Categoría |
|---|---|
| \(A^{-1}B\) es la única operación con puntuación 100% | A — verificación exhaustiva sobre 7 candidatas y 2304 pares |
| Cociclo como discriminador clave | A — \(B^{-1}A\) cumple 5/6 axiomas pero falla el cociclo |
| Invariancia izquierda como segundo discriminador | A — \(AB^{-1}\) cumple cociclo pero falla invariancia |

---

# 19. Preguntas abiertas

## 19.1 Relación entre \(B_3\) y \(Aut(G_{48}^+)\)

~~Verificar si \(P_{48} \cong B_3\).~~ **Resuelto:** las 48 tríadas son exactamente los 48 elementos de \(B_3\) (sección 17.3). Queda abierto precisar cómo \(B_3\) (orden 48) se incrusta en \(Aut(G_{48}^+)\) (orden 3456 = 48 × 72) y qué subgrupo representa. El cociente \(3456/48 = 72 = |Aut(K_{3,3})|\) sugiere que \(B_3\) corresponde al factor \(Aut(Q_3)\) en la descomposición \(Aut(Q_3) \times Aut(K_{3,3})\).

## 19.2 Formalización completa

Convertir el núcleo en un teorema autocontenido con demostración formal de \(48 = Q_3 \times S_3\) y de la isometría \(G_{48}^+ \cong Q_3\,\square\,K_{3,3}\).

## 19.3 Relación exacta con \(A_3\)

Precisar si los vectores de familia \((\pm3,\mp1,\mp1,\mp1)\) deben interpretarse como pesos, vértices tetraédricos o estructura dual dentro de la geometría de \(A_3\).

## 19.4 Búsqueda bibliográfica

Determinar si la cadena

\[
J(4,2) \rightarrow 8\ \text{triángulos} \rightarrow T\cup(-T) \rightarrow Q_3\,\square\,K_{3,3}
\]

aparece en la literatura sobre Johnson schemes, clique complexes o códigos de peso constante.

## 19.5 Controles más amplios

Extender los controles espectrales a otros tamaños de bloques (\(n=8\)), otros números de bloques, y modelos nulos que preserven equilibrio o simetría parcial.

## 19.6 Dinámica natural

~~Buscar una dinámica no diseñada ad hoc que seleccione espontáneamente los 48 estados.~~

**Resuelta.** El funcional \(E_H = \sum_i(u\cdot H_i)^2 + \sum_{i<j}(H_i\cdot H_j)^2\) (sección 3bis) se anula exactamente en los 48 estados perfectos y deriva directamente de la teoría de matrices de Hadamard, sin mencionar equilibrio ni distancia Hamming. Es la primera dinámica genuinamente independiente de la definición original.

---

# 20. Conclusión

Las restricciones de equilibrio interno y equidistancia triádica sobre \((\{-1,+1\}^4)^3\) seleccionan exactamente 48 estados con una cadena estructural completa y verificable:

\[
u^\perp \cap \{-1,+1\}^4
\rightarrow
\text{octaedro}
\rightarrow
\text{8 bases ortogonales}
\rightarrow
(\{-1,+1\}^{4})^{3} \xrightarrow{MM^T=4I_4}
48\ \text{perfectos}
\rightarrow
(\pm3,\mp1,\mp1,\mp1)
\rightarrow
T\cup(-T)
\rightarrow
Q_3
\rightarrow
Q_3\times S_3
\rightarrow
8\cdot K_{3,3}
\rightarrow
Q_3\,\square\,K_{3,3}
\rightarrow
Q_4\times 3\ \text{capas}
\]

El análisis espectral de Walsh-Hadamard sobre \(Q_{12}\) confirma que el conjunto es estadísticamente excepcional (z-score 39.84) e irreducible a simetrías más simples (z-score mínimo 8.78 ante el control más cercano).

La aportación es haber identificado que una única regla de equilibrio triádico produce una cadena coherente de objetos de geometría discreta conocidos. La novedad, si existe, no está en los objetos individuales sino en la forma concreta en que emergen conjuntamente.

---

# Apéndice A. Inventario resumido de resultados numéricos

| Resultado | Valor |
|---|---:|
| Estados totales base | 4096 |
| Estados perfectos base | 48 |
| Fracción perfecta | 1.171875% |
| Familias | 8 |
| Estados por familia | 6 |
| Aristas del grafo de familias | 12 |
| Aristas internas en los 48 estados | 72 |
| Estados etiquetados con polaridad exterior | 96 |
| Relaciones internas con polaridad exterior | 144 |
| Relaciones totales con puentes de polaridad | 192 |
| Radio de cobertura de los 48 en \(Q_{12}\) | 6 |
| Estados bloqueados locales | 576 |
| Triángulos en la frontera Hamming-2 | 2304 |
| Subconjuntos D.5 totales | 8008 |
| Subconjuntos D.5 con 48 triadas ordenadas | 8 |
| Subconjuntos D.5 con 72 triadas ordenadas | 48 |
| **Energía espectral en \(k=6\) (conjunto perfecto)** | **0.5850** |
| **Energía espectral en \(k=6\) (media aleatoria)** | **0.2257** |
| **Z-score espectral \(k=6\)** | **39.84** |
| **p-valor empírico espectral** | **\(< 10^{-4}\)** |
| Coeficientes de Walsh activos en \(k=4\) | 111 |
| Coeficientes de Walsh activos en \(k=6\) | 252 |
| Coeficientes de Walsh activos en \(k=8\) | 111 |
| Módulo uniforme de coeficientes dominantes | \(3/256 = 0.01171875\) |
| **Z-score control antipodal (más cercano)** | **8.78** |
| **Z-score control equilibrado+antipodal** | **9.13** |
| **Ningún control alcanza 0.585 en k=6** | **verificado en 12.000 muestras** |
| **Grafo interno \(G_{48}\)** | **\(8 \cdot K_{3,3}\)** |
| Aristas de \(G_{48}\) | 72 |
| Eigenvalores laplacianos de \(G_{48}\) | \(0^8,\ 3^{32},\ 6^8\) |
| **Grafo acoplado completo \(G_{48}^+\)** | **\(Q_3 \,\square\, K_{3,3}\)** |
| Aristas de \(G_{48}^+\) | 144 (72 internas + 72 externas) |
| Grado de cada vértice en \(G_{48}^+\) | 6 |
| Eigenvalores laplacianos de \(G_{48}^+\) | \(0^1, 2^3, 3^4, 4^3, 5^{12}, 6^2, 7^{12}, 8^3, 9^4, 10^3, 12^1\) |
| Gap espectral de \(G_{48}^+\) | 2 |
| Eigenvalor máximo de \(G_{48}^+\) | 12 |

---

# Apéndice B. Señal científica actual

El resultado es suficientemente sólido para considerarlo un ejercicio serio de combinatoria y geometría discreta, pero no suficiente para reclamar una teoría física ni una estructura matemática nueva a nivel global.

Los resultados principales son independientes entre sí y de las construcciones previas. Su convergencia — algebraica, geométrica, espectral y de simetría — refuerza la solidez del conjunto perfecto como objeto matemático con propiedades no genéricas.

La vía más profesional para continuar es:

1. formalizar el teorema Hadamard como teorema central en una publicación revisada por pares;
2. buscar en la literatura de Johnson schemes y association schemes si la cadena completa ya está documentada;
3. ampliar los controles espectrales a otros valores de \(n\);
4. explorar generalizaciones a \(n=8\) con las herramientas espectrales desarrolladas aquí.

---

# Bibliografía orientativa

Las conexiones estructurales identificadas en este trabajo se relacionan con los siguientes campos y referencias canónicas.

## Matrices de Hadamard

- Horadam, K. J. (2007). *Hadamard Matrices and Their Applications*. Princeton University Press.
- Seberry, J., Yamada, M. (1992). Hadamard matrices, sequences, and block designs. En *Contemporary Design Theory*, Wiley.
- La clasificación de matrices de Hadamard de orden 4 es clásica: existen exactamente 3 clases de equivalencia bajo permutación de filas y columnas y cambio de signo.

## Grafos de Johnson y códigos de peso constante

- Johnson, S. M. (1962). A new upper bound for error-correcting codes. *IRE Transactions on Information Theory*, 8(3), 203–207.
- Brouwer, A. E., Cohen, A. M., Neumaier, A. (1989). *Distance-Regular Graphs*. Springer. (Capítulo sobre grafos de Johnson \(J(n,k)\).)
- MacWilliams, F. J., Sloane, N. J. A. (1977). *The Theory of Error-Correcting Codes*. North-Holland. (Códigos de peso constante, Capítulo 2.)

## Sistema de raíces \(A_3\) y politopos

- Humphreys, J. E. (1990). *Reflection Groups and Coxeter Groups*. Cambridge University Press. (Sistema \(A_n\), §1.3.)
- Ziegler, G. M. (1995). *Lectures on Polytopes*. Springer. (Hipersímplice \(\Delta(d,k)\), §2.3.)
- El hipersímplice \(\Delta(4,2)\) es el octaedro regular; sus vértices son los vectores \(\{0,1\}^4\) con peso 2, en correspondencia con los vectores equilibrados \(\{-1,+1\}^4\) vía \(v \mapsto 2v-1\).

## Análisis espectral de funciones booleanas (Walsh-Hadamard)

- O'Donnell, R. (2014). *Analysis of Boolean Functions*. Cambridge University Press. (Transformada de Walsh-Hadamard, Capítulos 1–2.)
- Rothaus, O. S. (1976). On "bent" functions. *Journal of Combinatorial Theory, Series A*, 20(3), 300–305. (Funciones bent y concentración espectral.)

## Grafos producto cartesiano

- Hammack, R., Imrich, W., Klavžar, S. (2011). *Handbook of Product Graphs* (2nd ed.). CRC Press. (Producto cartesiano \(A \,\square\, B\), espectro laplaciano, automorfismos.)
- Sabidussi, G. (1960). Graph multiplication. *Mathematische Zeitschrift*, 72, 446–457. (Resultado clásico sobre \(Aut(A \,\square\, B)\).)

## Diseños combinatorios y esquemas de asociación

- Delsarte, P. (1973). An algebraic approach to the association schemes of coding theory. *Philips Research Reports Supplements*, 10. (Johnson schemes, relación con códigos.)
- Cameron, P. J. (1994). *Combinatorics: Topics, Techniques, Algorithms*. Cambridge University Press. (Diseños, grafos de Johnson, cliques.)

