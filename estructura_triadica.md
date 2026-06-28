# Estructura triádica equilibrada  
## Marco general por órbitas de Venn y caso excepcional \(n=4\)

**Autor:** Sergi Garcia Mecinas  
**Versión:** V6 — reorganización en torno al teorema general  
**Ámbito:** combinatoria, geometría discreta, matrices de Hadamard, grafos de Cayley y acciones de grupos finitos.

---

## Resumen

Se estudian tríadas de vectores de signos

\[
(H_1,H_2,H_3)\in(\{-1,+1\}^{n})^3
\]

sujetas a dos restricciones locales:

1. **equilibrio** de cada bloque;
2. **ortogonalidad** entre cada par de bloques.

Identificando cada vector equilibrado con el subconjunto de posiciones positivas

\[
A\subset[n],\qquad |A|=\frac n2,
\]

la ortogonalidad entre dos vectores se convierte en una condición de intersección:

\[
H_A\perp H_B
\iff
|A\cap B|=\frac n4.
\]

Por tanto, la construcción existe únicamente cuando

\[
n\equiv0\pmod4.
\]

El resultado general es que las tríadas equilibradas y mutuamente ortogonales se descomponen en órbitas bajo la acción natural de \(S_n\), clasificadas por un único invariante:

\[
t=|A\cap B\cap C|.
\]

Si

\[
m=\frac n4,
\]

entonces las órbitas son

\[
\mathcal O_t,\qquad t=0,1,\ldots,m,
\]

y su tamaño es

\[
\boxed{
|\mathcal O_t|
=
\frac{n!}{(t!)^4((m-t)!)^4}.
}
\]

La dualidad por complemento global

\[
A\mapsto A^c=[n]\setminus A
\]

intercambia

\[
\mathcal O_t\leftrightarrow \mathcal O_{m-t}.
\]

La órbita uniforme existe si y solo si

\[
n\equiv0\pmod8.
\]

En ese caso todos los 8 átomos del diagrama de Venn tienen el mismo tamaño \(n/8\), y la órbita uniforme es el espacio homogéneo

\[
S_n/(S_{n/8})^8.
\]

El caso \(n=4\) es el primer caso no trivial y resulta excepcional: las 48 tríadas perfectas se identifican con el grupo hiperoctaédrico

\[
P_{48}\cong B_3\cong C_2^3\rtimes S_3,
\]

y su grafo natural de relaciones es el grafo de Cayley

\[
\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}.
\]

---

## 0. Idea central

El principio que organiza el trabajo es:

\[
\boxed{
\text{equilibrio}
+
\text{ortogonalidad}
\Longrightarrow
\text{órbitas simétricas}
}
\]

En dimensión 4, esa regla colapsa en una estructura especialmente rígida:

\[
48\cong B_3.
\]

En dimensión 8 aparece una órbita uniforme que es un torsor de \(S_8\).

En dimensión 12 la fórmula general se verifica por conteo independiente.

La estructura general no es una teoría física. Es un marco de combinatoria y geometría discreta basado en selección por restricciones.

---

# 1. Modelo general

Sea

\[
H_A\in\{-1,+1\}^{n}
\]

el vector asociado a un subconjunto \(A\subset[n]\), definido por

\[
H_A(i)=
\begin{cases}
+1,& i\in A,\\
-1,& i\notin A.
\end{cases}
\]

Un vector está equilibrado si

\[
|A|=\frac n2.
\]

Una tríada equilibrada es un triple ordenado

\[
(A,B,C)
\]

con

\[
|A|=|B|=|C|=\frac n2.
\]

La ortogonalidad entre dos vectores de signos es:

\[
\langle H_A,H_B\rangle=0.
\]

Como

\[
\langle H_A,H_B\rangle=n-2d(H_A,H_B),
\]

la ortogonalidad equivale a

\[
d(H_A,H_B)=\frac n2.
\]

En términos de subconjuntos,

\[
d(H_A,H_B)=2\left(\frac n2-|A\cap B|\right).
\]

Por tanto,

\[
H_A\perp H_B
\iff
|A\cap B|=\frac n4.
\]

---

# 2. Condición de existencia

La condición

\[
|A\cap B|=\frac n4
\]

solo puede tener sentido entero si

\[
n\equiv0\pmod4.
\]

Además, la distancia Hamming entre dos vectores equilibrados siempre es par:

\[
d(H_A,H_B)=2\left(\frac n2-|A\cap B|\right).
\]

La ortogonalidad exige

\[
d(H_A,H_B)=\frac n2.
\]

Por tanto, \(\frac n2\) debe ser par, lo cual equivale a

\[
\boxed{
n\equiv0\pmod4.
}
\]

Ejemplo de obstrucción:

\[
n=6.
\]

Los vectores equilibrados tienen peso 3. Las distancias Hamming posibles entre ellos son

\[
0,2,4,6.
\]

La ortogonalidad exigiría distancia

\[
\frac62=3,
\]

imposible. Por eso en \(n=6\) no existe ni siquiera un par ortogonal equilibrado.

---

# 3. Teorema general de órbitas por átomos de Venn

Sea

\[
n=4m.
\]

Sea \((A,B,C)\) una tríada equilibrada y mutuamente ortogonal:

\[
|A|=|B|=|C|=2m,
\]

\[
|A\cap B|=|A\cap C|=|B\cap C|=m.
\]

Definimos

\[
t=|A\cap B\cap C|.
\]

Los 8 átomos del diagrama de Venn quedan completamente determinados por \(t\):

| Átomo | Tamaño |
|---|---:|
| \(A\cap B\cap C\) | \(t\) |
| \((A\cap B)\setminus C\) | \(m-t\) |
| \((A\cap C)\setminus B\) | \(m-t\) |
| \((B\cap C)\setminus A\) | \(m-t\) |
| \(A\setminus(B\cup C)\) | \(t\) |
| \(B\setminus(A\cup C)\) | \(t\) |
| \(C\setminus(A\cup B)\) | \(t\) |
| \([n]\setminus(A\cup B\cup C)\) | \(m-t\) |

Por tanto, el invariante

\[
t=0,1,\ldots,m
\]

clasifica las órbitas bajo la acción natural de \(S_n\).

---

## Teorema

Las tríadas equilibradas y mutuamente ortogonales de dimensión \(n=4m\) se dividen bajo \(S_n\) en exactamente

\[
m+1=\frac n4+1
\]

órbitas:

\[
\mathcal O_0,\mathcal O_1,\ldots,\mathcal O_m.
\]

La órbita de parámetro \(t\) tiene tamaño

\[
\boxed{
|\mathcal O_t|
=
\frac{n!}{(t!)^4((m-t)!)^4}.
}
\]

---

## Demostración

Una tríada de tipo \(t\) divide \([n]\) en 8 átomos de Venn: cuatro de tamaño \(t\) y cuatro de tamaño \(m-t\).

El estabilizador de la tríada en \(S_n\) está formado por las permutaciones que preservan cada átomo. Por tanto,

\[
\operatorname{Stab}(\mathcal O_t)
\cong
(S_t)^4\times(S_{m-t})^4.
\]

Su orden es

\[
(t!)^4((m-t)!)^4.
\]

Por el teorema órbita-estabilizador,

\[
|\mathcal O_t|
=
\frac{|S_n|}{|\operatorname{Stab}(\mathcal O_t)|}
=
\frac{n!}{(t!)^4((m-t)!)^4}.
\]

---

# 4. Dualidad por complemento

El complemento global

\[
A\mapsto A^c=[n]\setminus A
\]

envía una tríada

\[
(A,B,C)
\]

a

\[
(A^c,B^c,C^c).
\]

Si

\[
t=|A\cap B\cap C|,
\]

entonces el complemento envía

\[
t\mapsto m-t.
\]

Así,

\[
\boxed{
\mathcal O_t
\leftrightarrow
\mathcal O_{m-t}.
}
\]

La órbita fija del complemento existe si y solo si

\[
t=m-t,
\]

es decir,

\[
t=\frac m2.
\]

Esto exige que \(m\) sea par:

\[
m=\frac n4\equiv0\pmod2.
\]

Por tanto,

\[
\boxed{
n\equiv0\pmod8.
}
\]

---

# 5. Órbita uniforme

Una órbita es uniforme cuando los 8 átomos de Venn tienen el mismo tamaño.

Esto ocurre si

\[
t=m-t,
\]

es decir,

\[
t=\frac m2=\frac n8.
\]

Por tanto, la órbita uniforme existe exactamente cuando

\[
n\equiv0\pmod8.
\]

Cuando existe, su tamaño es

\[
\boxed{
|\mathcal O_{\mathrm{unif}}|
=
\frac{n!}{((n/8)!)^8}.
}
\]

Estructuralmente,

\[
\mathcal O_{\mathrm{unif}}
\cong
S_n/(S_{n/8})^8.
\]

En \(n=8\), como \(n/8=1\), se obtiene

\[
|\mathcal O_{\mathrm{unif}}|=8!,
\]

y el estabilizador es trivial. Por tanto, la órbita uniforme de \(n=8\) es un torsor libre de \(S_8\).

En \(n=16\),

\[
|\mathcal O_{\mathrm{unif}}|
=
\frac{16!}{(2!)^8},
\]

y el estabilizador es

\[
(S_2)^8.
\]

Por tanto, ya no es un torsor libre, sino un espacio homogéneo.

---

# 6. Tabla de casos

| \(n\) | \(m=n/4\) | Órbitas bajo \(S_n\) | Órbita uniforme | Total tríadas ordenadas |
|---:|---:|---:|---|---:|
| 4 | 1 | 2 | No | 48 |
| 6 | — | 0 | No existe ortogonalidad | 0 |
| 8 | 2 | 3 | \(t=1\), tamaño \(8!\) | 45360 |
| 12 | 3 | 4 | No | 60614400 |
| 16 | 4 | 5 | \(t=2\), tamaño \(16!/2^8\) | 114144030000 |

---

# 7. Caso \(n=4\): el caso excepcional

En \(n=4\),

\[
m=1.
\]

La teoría general predice dos órbitas bajo \(S_4\):

\[
t=0,\qquad t=1.
\]

Cada una tiene tamaño

\[
\frac{4!}{(t!)^4((1-t)!)^4}=24.
\]

Por tanto,

\[
24+24=48.
\]

El complemento global intercambia ambas órbitas:

\[
0\leftrightarrow1.
\]

Bajo el grupo ampliado

\[
S_4\times C_2,
\]

las dos órbitas se fusionan en una única estructura de 48 tríadas.

Esta fusión explica por qué el caso \(n=4\) parece más compacto que los casos superiores.

---

## 7.1 Equivalencia Hadamard

Sea

\[
u=(1,1,1,1).
\]

Dada una tríada

\[
(H_1,H_2,H_3)\in(\{-1,+1\}^4)^3,
\]

definimos

\[
M=
\begin{pmatrix}
u\\
H_1\\
H_2\\
H_3
\end{pmatrix}.
\]

Entonces

\[
(H_1,H_2,H_3)
\]

es perfecta si y solo si

\[
\boxed{
MM^T=4I_4.
}
\]

Esto equivale a decir que \(M\) es una matriz de Hadamard de orden 4.

La condición Hadamard contiene simultáneamente:

- equilibrio de cada \(H_i\);
- ortogonalidad entre cada par \(H_i,H_j\);
- distancia Hamming \(2\) entre cada par.

Por tanto, en \(n=4\), la definición puede condensarse en una sola ecuación matricial.

---

## 7.2 Octaedro \(\Delta(4,2)\)

Los vectores equilibrados de longitud 4 son exactamente

\[
u^\perp\cap\{-1,+1\}^4.
\]

Hay

\[
\binom42=6
\]

vectores equilibrados.

Estos 6 puntos forman el hipersímplice

\[
\Delta(4,2),
\]

que en este caso es un octaedro regular.

Así,

\[
\Delta(4,2)\cong\text{octaedro}.
\]

---

## 7.3 Ocho bases ortogonales

Dentro del octaedro, una tríada perfecta es una base ortogonal de tres vectores.

Hay 8 bases ortogonales no ordenadas.

Cada una admite

\[
3!=6
\]

ordenaciones.

Por tanto,

\[
8\cdot6=48.
\]

---

## 7.4 Identificación con \(B_3\)

El octaedro tiene tres ejes antipodales.

Una tríada perfecta ordenada equivale a:

1. escoger la orientación de cada uno de los 3 ejes:

\[
2^3;
\]

2. ordenar los 3 ejes:

\[
3!.
\]

Por tanto,

\[
48=2^3\cdot3!.
\]

Esta es exactamente la cardinalidad del grupo hiperoctaédrico de dimensión 3:

\[
B_3\cong C_2^3\rtimes S_3.
\]

Las 48 tríadas perfectas se identifican con las 48 matrices monomiales firmadas \(3\times3\). Por tanto,

\[
\boxed{
P_{48}\cong B_3.
}
\]

---

## 7.5 Grafo de Cayley

Con los generadores naturales:

\[
S=
\{
\text{flip}_X,
\text{flip}_Y,
\text{flip}_Z,
\text{swap}_{XY},
\text{swap}_{XZ},
\text{swap}_{YZ}
\},
\]

el grafo de Cayley de \(B_3\) es:

\[
\mathrm{Cay}(B_3,S).
\]

Computacional y algebraicamente se verifica que

\[
\boxed{
\mathrm{Cay}(B_3,S)
\cong
Q_3\square K_{3,3}.
}
\]

Este grafo tiene:

- 48 vértices;
- 144 aristas;
- grado 6;
- diámetro 5;
- dos órbitas de aristas: flips y swaps.

---

## 7.6 Automorfismos

Como

\[
Q_3\not\cong K_{3,3},
\]

el grupo de automorfismos del producto cartesiano factoriza:

\[
Aut(Q_3\square K_{3,3})
\cong
Aut(Q_3)\times Aut(K_{3,3}).
\]

Los órdenes son:

\[
|Aut(Q_3)|=48,
\]

\[
|Aut(K_{3,3})|=72.
\]

Por tanto,

\[
\boxed{
|Aut(Q_3\square K_{3,3})|
=
48\cdot72
=
3456.
}
\]

Las aristas internas y externas forman dos órbitas distintas bajo el grupo de automorfismos. Esta distinción es intrínseca al grafo.

---

## 7.7 Firma espectral de Walsh-Hadamard

La transformada de Walsh-Hadamard de la función indicadora de \(P_{48}\) sobre \(Q_{12}=\{-1,+1\}^{12}\) tiene tres propiedades exactas:

**E1** (Anulación de órdenes impares). Todos los coeficientes de Walsh de orden impar son exactamente cero. *Demostración*: \(P_{48}\) es cerrado bajo inversión global \(s\mapsto -s\), que multiplica los coeficientes de orden \(k\) por \((-1)^k\). \(\square\)

**E2** (Simetría especular). La energía en orden \(k\) iguala la energía en orden \(12-k\).

**E3** (Uniformidad de módulo). Todos los coeficientes de Walsh no nulos de órdenes 4, 6, 8 tienen valor absoluto exactamente \(3/256\).

Distribución de energía por orden:

| Orden \(k\) | Energía |
|---:|---:|
| 2 | 2.37% |
| 4 | 17.79% |
| **6** | **58.50%** |
| 8 | 17.79% |
| 10 | 2.37% |
| 12 | 1.19% |

**No genericidad estadística.** Un test de Monte Carlo con 10.000 subconjuntos aleatorios de 48 elementos de \(Q_{12}\) da \(z\text{-score}=39.84\). Con controles que preservan equilibrio y/o antipodalidad, el \(z\)-score mínimo es 8.78. La concentración espectral es irreducible a propiedades más simples que la condición triádica completa.

---

# 8. Caso \(n=8\): tres órbitas y torsor de \(S_8\)

En \(n=8\),

\[
m=2.
\]

La teoría general predice tres órbitas:

\[
t=0,1,2.
\]

| Tipo | Átomos de Venn | Tríadas ordenadas |
|---:|---|---:|
| \(t=0\) | \((0,2,2,2,0,0,0,2)\) | 2520 |
| \(t=1\) | \((1,1,1,1,1,1,1,1)\) | 40320 |
| \(t=2\) | \((2,0,0,0,2,2,2,0)\) | 2520 |

Así,

\[
45360=2520+40320+2520.
\]

La órbita central

\[
\mathcal O_1
\]

es uniforme.

Todos los 8 átomos del diagrama de Venn tienen tamaño 1.

Por tanto,

\[
|\mathcal O_1|=8!.
\]

La acción de \(S_8\) sobre \(\mathcal O_1\) es libre y transitiva. En consecuencia,

\[
\boxed{
\mathcal O_1
\text{ es un }S_8\text{-torsor}.
}
\]

Tras elegir una tríada base, se obtiene una identificación

\[
\mathcal O_1\cong S_8.
\]

Sin elegir base, no hay elemento neutro canónico.

---

# 9. Caso \(n=12\): verificación independiente

En \(n=12\),

\[
m=3.
\]

La teoría general predice cuatro órbitas:

| \(t\) | Átomos de Venn | Tríadas ordenadas |
|---:|---|---:|
| 0 | \((0,3,3,3,0,0,0,3)\) | 369600 |
| 1 | \((1,2,2,2,1,1,1,2)\) | 29937600 |
| 2 | \((2,1,1,1,2,2,2,1)\) | 29937600 |
| 3 | \((3,0,0,0,3,3,3,0)\) | 369600 |

Total:

\[
60614400.
\]

Este resultado fue verificado por conteo directo de triángulos en el grafo de ortogonalidad de los \(924=\binom{12}{6}\) vectores equilibrados.

Datos del grafo de ortogonalidad de \(n=12\):

| Propiedad | Valor |
|---|---:|
| Vértices (vectores equilibrados) | 924 |
| Aristas (pares ortogonales) | 184800 |
| Grado regular | 400 |
| Tríadas ordenadas totales | 60614400 |
| Tiempo de verificación | 6.19 s |

La verificación directa coincide exactamente con la fórmula general en las cuatro órbitas.

---

# 10. Lectura relacional

En el caso \(n=4\), como \(P_{48}\cong B_3\), hay una operación de comparación natural:

\[
C(A,B)=A^{-1}B.
\]

**Unicidad axiomática.** Entre las siete operaciones binarias naturales sobre \(B_3\), solo \(C(A,B)=A^{-1}B\) satisface simultáneamente los seis axiomas relacionales:

| Axioma | Expresión |
|---|---|
| 1. Identidad diagonal | \(C(A,A)=e\) |
| 2. Identidad implica igualdad | \(C(A,B)=e\Rightarrow A=B\) |
| 3. Simetría inversa | \(C(B,A)=C(A,B)^{-1}\) |
| 4. Reconstrucción de distancias | \(d(e,C(A,B))=d(A,B)\) |
| 5. Ley de cociclo | \(C(A,B)\cdot C(B,D)=C(A,D)\) |
| 6. Invariancia izquierda | \(C(LA,LB)=C(A,B)\) |

La alternativa más cercana (\(B^{-1}A\)) falla la ley de cociclo (20.8% de satisfacción). Verificado sobre los \(48^2=2304\) pares.

La ley de cociclo permite reconstruir toda la estructura desde comparaciones y una raíz: dado el grafo de Cayley etiquetado y cualquier vértice base, los 48 estados, la ley de grupo y la condición de Hadamard son recuperables con cero errores.

En \(n=8\), la órbita uniforme no es un grupo sino un torsor. La comparación relacional entre tríadas es:

\[
C(T,U)=p_U p_T^{-1},
\]

donde \(p_T,p_U\in S_8\) son las permutaciones asociadas. Satisface \(C(U,V)C(T,U)=C(T,V)\) (verificado computacionalmente). El patrón es común a ambos casos:

\[
\boxed{
\text{comparaciones coherentes}
\Longrightarrow
\text{estructura reconstruible hasta elección de raíz}.
}
\]

---

# 11. Alcance y cautelas

## Lo demostrado

- La condición de existencia \(n\equiv0\pmod4\).
- La clasificación de órbitas por \(t=|A\cap B\cap C|\).
- La fórmula de tamaño de órbitas.
- La dualidad por complemento.
- La existencia de órbita uniforme si y solo si \(n\equiv0\pmod8\).
- La identificación \(P_{48}\cong B_3\) en \(n=4\).
- El isomorfismo

\[
\mathrm{Cay}(B_3,S)\cong Q_3\square K_{3,3}.
\]

- El torsor de \(S_8\) en la órbita uniforme de \(n=8\).
- La verificación independiente de \(n=12\).

El trabajo se sitúa en combinatoria, geometría discreta, teoría de grafos y acciones de grupos.

La posible novedad no está en \(B_3\), \(S_n\), Hadamard, Johnson o Cayley por separado, sino en la cadena exacta que los conecta a partir de la selección triádica equilibrada.

---

# 12. Preguntas abiertas

## 12.1 Búsqueda bibliográfica

Determinar si la cadena

\[
\Delta(n,n/2)
+
\text{ortogonalidad}
\rightarrow
\text{órbitas de Venn}
\rightarrow
\text{caso }n=4:B_3
\]

aparece ya formulada en la literatura sobre:

- Johnson schemes;
- association schemes;
- matrices de Hadamard;
- clique complexes;
- códigos de peso constante;
- acciones de grupos simétricos sobre diagramas de Venn.

## 12.2 Relación exacta con esquemas de Johnson

En \(n=8\), los vectores equilibrados son los vértices de \(J(8,4)\) y la ortogonalidad es la relación

\[
|A\cap B|=2.
\]

Conviene formalizar la construcción como un problema de cliques en relaciones específicas del esquema de Johnson.

## 12.3 Teoría para más de tres bloques

La construcción actual usa tríadas.

Una extensión natural es estudiar \(r\)-adas:

\[
(A_1,\ldots,A_r)
\]

con equilibrio y ortogonalidad por pares.

Esto llevaría a diagramas de Venn con \(2^r\) átomos.

## 12.4 Espectro para \(n=8\) y \(n=12\)

El análisis de Walsh-Hadamard se ha desarrollado en detalle para \(n=4\). Falta estudiar la firma espectral de las órbitas \(\mathcal O_t\) en \(n=8\) y \(n=12\).

## 12.5 Publicación

El núcleo publicable debería centrarse en:

1. el teorema general de órbitas;
2. el caso excepcional \(n=4\);
3. la órbita uniforme de \(n=8\);
4. la verificación independiente de \(n=12\).

---

# 13. Conclusión

El proyecto puede formularse ahora como una teoría discreta de selección por restricciones:

\[
\boxed{
\Delta(n,n/2)
+
\text{ortogonalidad}
\Longrightarrow
\text{órbitas de }S_n
\text{ clasificadas por átomos de Venn}.
}
\]

El caso \(n=4\) no es la teoría completa, sino el primer caso excepcional, donde la estructura se cierra como

\[
P_{48}\cong B_3
\]

y el grafo relacional natural es

\[
Q_3\square K_{3,3}.
\]

El caso \(n=8\) muestra que la teoría no se agota en dimensión 4: aparece una órbita uniforme que es un torsor de \(S_8\).

El caso \(n=12\) confirma la fórmula general por conteo independiente.

La contribución principal es haber identificado un mecanismo común:

\[
\text{espacio grande}
\rightarrow
\text{restricción local}
\rightarrow
\text{órbitas}
\rightarrow
\text{simetría}.
\]

---

# Apéndice A. Fórmulas principales

\[
n=4m
\]

\[
|A|=|B|=|C|=2m
\]

\[
|A\cap B|=|A\cap C|=|B\cap C|=m
\]

\[
t=|A\cap B\cap C|
\]

\[
|\mathcal O_t|
=
\frac{n!}{(t!)^4((m-t)!)^4}
\]

\[
\mathcal O_t
\leftrightarrow
\mathcal O_{m-t}
\]

\[
\mathcal O_{\mathrm{unif}}
\text{ existe}
\iff
n\equiv0\pmod8
\]

\[
|\mathcal O_{\mathrm{unif}}|
=
\frac{n!}{((n/8)!)^8}
\]

---

# Apéndice B. Bibliografía orientativa

- Brouwer, A. E., Cohen, A. M., Neumaier, A. *Distance-Regular Graphs*. Springer, 1989.
- Cameron, P. J. *Combinatorics: Topics, Techniques, Algorithms*. Cambridge University Press, 1994.
- Delsarte, P. *An Algebraic Approach to the Association Schemes of Coding Theory*. Philips Research Reports Supplements, 1973.
- Hammack, R., Imrich, W., Klavžar, S. *Handbook of Product Graphs*. CRC Press, 2011.
- Horadam, K. J. *Hadamard Matrices and Their Applications*. Princeton University Press, 2007.
- Humphreys, J. E. *Reflection Groups and Coxeter Groups*. Cambridge University Press, 1990.
- MacWilliams, F. J., Sloane, N. J. A. *The Theory of Error-Correcting Codes*. North-Holland, 1977.
- O'Donnell, R. *Analysis of Boolean Functions*. Cambridge University Press, 2014.
- Ziegler, G. M. *Lectures on Polytopes*. Springer, 1995.
