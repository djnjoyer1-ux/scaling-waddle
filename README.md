# Foundational Mathematics Note

## Toward a Two-Class Foundation of Mathematical Objects

A formal presentation of the proposed distinction between
SURFACES and LAWS as mutually exclusive primitive classes.

------------------------------------------------------------
Contents
------------------------------------------------------------

1. Primitive Symbols
2. Axioms
3. Definitions
4. Foundational Principle
5. Conjectures

------------------------------------------------------------
Primitive Symbols
------------------------------------------------------------

S = class of surfaces

L = class of laws

U = universe of mathematical objects

------------------------------------------------------------
Axioms
------------------------------------------------------------

Axiom 1 -- Completeness

Every primitive mathematical object belongs to exactly one class.

    forall x in U,
        x in S XOR x in L


Axiom 2 -- Mutual Exclusivity

No primitive object is simultaneously a surface and a law.

    S ∩ L = empty set


Corollary 2.1

The two classes form a disjoint partition of the universe.

    U = S U L
    S ∩ L = empty


Axiom 3 -- Transformation

Every admissible transformation between surfaces is induced
by at least one law.


Axiom 4 -- No Self-Evolution

No surface evolves independently of a law.


Axiom 5 -- Irreducibility

No law is identical to any surface.


Axiom 6 -- Representation

A surface may encode a law without becoming identical to that
law.

------------------------------------------------------------
Definitions
------------------------------------------------------------

Definition 1 -- Surface

A surface is an object whose identity is completely determined
by its intrinsic state.

A surface possesses no primitive notion of transformation.


Definition 2 -- Law

A law is an object whose identity is completely determined by
the admissible transformations it defines between surfaces.

A law is not itself a surface.

------------------------------------------------------------
Foundational Principle
------------------------------------------------------------

Principle 1

The ontology of mathematics consists of exactly two primitive
classes:

    • state-bearing objects
    • transformation-bearing objects

No third primitive class is assumed.

------------------------------------------------------------
Conjectures
------------------------------------------------------------

Conjecture 1

Every mathematical theory admits a canonical decomposition
into surfaces and laws.


Conjecture 2

Every physical theory admits a unique decomposition into a
family of surfaces and a family of laws.


Conjecture 3

No faithful isomorphism exists between the class of surfaces
and the class of laws.


Conjecture 4

Every computable process can be expressed as repeated
application of elements of L acting upon elements of S.


Conjecture 5

The partition

    (S, L)

is more fundamental than distinctions such as

    • state vs dynamics
    • object vs morphism
    • data vs algorithm
    • manifold vs vector field
    • configuration vs evolution

------------------------------------------------------------
Formalization Note
------------------------------------------------------------

The framework becomes substantially stronger once the meanings
of

    • primitive
    • intrinsic state
    • admissible transformation
    • representation
    • faithful isomorphism

are specified within a chosen foundational system, such as

    • category theory
    • dependent type theory
    • two-sorted first-order logic

------------------------------------------------------------
Summary
------------------------------------------------------------

The proposal is that every primitive mathematical object
belongs to exactly one of two fundamentally different kinds:

    SURFACES = things that possess state

    LAWS = things that generate transformations

Everything else is built from these two primitive classes.
