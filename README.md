# Triadic Structure 4D

**A discrete structural construction connecting Hadamard matrices, the
hyperoctahedral group (B_3), and the Cayley graph (Q_3
`\square `{=tex}K\_{3,3}).**

------------------------------------------------------------------------

## Overview

This project studies the discrete space

\[ ({-1,+1}^{4})^{3}, \]

containing **4096** possible states.

Applying only two local constraints:

-   balanced blocks (two `+1` and two `−1`)
-   pairwise Hamming distance equal to 2

selects exactly **48 perfect states**.

These states generate the structural chain:

``` text
2/2 balance
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

------------------------------------------------------------------------

# Main result

The perfect triads satisfy

\[ MM\^{T}=4I_4. \]

This single matrix condition is equivalent to the original balance and
Hamming conditions.

Furthermore,

\[ P\_{48}`\cong `{=tex}B_3 \]

and

\[ `\mathrm{Cay}`{=tex}(B_3,S)`\cong `{=tex}Q_3`\square `{=tex}K\_{3,3}.
\]

------------------------------------------------------------------------

# Relational formulation

The same structure can be reconstructed from

\[ C(A,B)=A\^{-1}B \]

plus a reference state.

From this formulation it is possible to reconstruct:

-   the 48 perfect states
-   the group (B_3)
-   the Cayley graph
-   the Hadamard structure

------------------------------------------------------------------------

# Verified results

-   ✅ 48 perfect states
-   ✅ Hadamard equivalence
-   ✅ (P\_{48}`\cong `{=tex}B_3)
-   ✅ (Q_3`\square `{=tex}K\_{3,3})
-   ✅ 144 edges
-   ✅ 3456 automorphisms
-   ✅ Walsh--Hadamard peak (58.5% at order 6)
-   ✅ Monte Carlo significance (z = 39.84)
-   ✅ Relational reconstruction using (A\^{-1}B)

------------------------------------------------------------------------

# Repository structure

``` text
README.md

estructura_triadica_4D.md
    Complete mathematical document

triadic_structure_3d.html
    Interactive visualizer

python/
    Enumeration
    Verification
    Spectral analysis
    Group tests
    Relational reconstruction
```

------------------------------------------------------------------------

# Interactive visualizer

The HTML visualizer follows the complete construction:

1.  Balance 2/2
2.  Octahedron
3.  Hadamard
4.  Dual tetrahedra
5.  Cube (Q_3)
6.  Cayley graph
7.  Spectral evidence
8.  Relational formulation
9.  Comparison operator (A\^{-1}B)
10. Final synthesis

------------------------------------------------------------------------

# Scope

The project connects several known mathematical objects through a single
discrete construction.

The claim is **not** that these mathematical objects are individually
new, but that they emerge together from the same minimal rule and can be
reproduced computationally.

------------------------------------------------------------------------

# Author

**Sergi Garcia Mecinas**
