```markdown
# Toward a Two-Class Foundation of Mathematical Objects

*A proposal for a foundational distinction between surfaces and laws.*

---

# Primitive Symbols

Let

- $\mathcal{S}$ denote the class of **surfaces**.
- $\mathcal{L}$ denote the class of **laws**.
- $\mathcal{U}$ denote the universe of mathematical objects.

---

# Axiom 1 — Completeness

Every primitive mathematical object belongs to exactly one class.

$$
\forall x\in\mathcal U,\qquad
x\in\mathcal S
\;\lor\;
x\in\mathcal L.
$$

---

# Axiom 2 — Mutual Exclusivity

No primitive object belongs simultaneously to both classes.

$$
\forall x\in\mathcal U,\qquad
\neg\left(
x\in\mathcal S
\land
x\in\mathcal L
\right).
$$

---

# Corollary 2.1

The universe is partitioned into surfaces and laws.

$$
\mathcal U
=
\mathcal S
\sqcup
\mathcal L.
$$

---

# Definition 1 — Surface

A **surface** is an object whose identity is completely determined by its intrinsic state.

A surface possesses no primitive notion of transformation.

---

# Definition 2 — Law

A **law** is an object whose identity is determined by the admissible transformations it defines between surfaces.

A law is not itself a surface.

---

# Axiom 3 — Transformation

Every admissible transformation between surfaces is induced by at least one law.

If

$$
S_1,S_2\in\mathcal S,
$$

then

$$
S_1
\rightarrow
S_2
\Longrightarrow
\exists L\in\mathcal L.
$$

---

# Axiom 4 — No Self-Evolution

No surface evolves independently.

If

$$
S_1
\rightarrow
S_2,
$$

then

$$
\exists L\in\mathcal L
\text{ such that }
L(S_1)=S_2.
$$

---

# Axiom 5 — Irreducibility

No law is identical to any surface.

$$
\forall L\in\mathcal L,
\forall S\in\mathcal S,
\qquad
L\neq S.
$$

---

# Axiom 6 — Representation

A surface may encode a law without becoming that law.

If $R(L)$ denotes a representation of the law $L$, then

$$
R(L)\in\mathcal S,
$$

while

$$
L\in\mathcal L,
$$

and therefore

$$
R(L)\neq L.
$$

---

# Principle 1

The ontology of mathematics consists of two primitive classes:

1. State-bearing objects.
2. Transformation-bearing objects.

No third primitive class is assumed.

---

# Conjecture 1

Every mathematical theory admits a canonical decomposition

$$
(\mathcal S,\mathcal L).
$$

---

# Conjecture 2

Every physical theory admits a unique decomposition into

- a family of surfaces, and
- a family of laws.

---

# Conjecture 3

No faithful isomorphism exists between the class of surfaces and the class of laws.

$$
\mathcal S
\not\cong
\mathcal L.
$$

---

# Conjecture 4

Every computable process can be expressed as repeated application of elements of

$$
\mathcal L
$$

acting upon elements of

$$
\mathcal S.
$$

---

# Conjecture 5

The partition

$$
\mathcal U
=
\mathcal S
\sqcup
\mathcal L
$$

is more fundamental than distinctions such as

- state versus dynamics,
- object versus morphism,
- data versus algorithm,
- manifold versus vector field,
- configuration versus evolution.

---

# Future Work

Potential directions include:

- Formalizing surfaces and laws within first-order logic.
- Developing an algebra of laws.
- Defining morphisms between surfaces.
- Investigating categorical formulations.
- Determining whether existing physical theories admit a canonical $(\mathcal S,\mathcal L)$ decomposition.
- Exploring applications to computation, artificial intelligence, and information theory.

---

# Summary

The central proposal is that all primitive mathematical objects belong to exactly one of two disjoint classes:

- **Surfaces**, which represent intrinsic states.
- **Laws**, which define admissible transformations.

The hypothesis is that this distinction is foundational and that many existing mathematical frameworks arise as specializations of this more primitive decomposition.
```
