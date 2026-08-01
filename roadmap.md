# Roadmap

## Toward a Two-Class Foundation of Mathematical Objects

This roadmap outlines the development of the proposed distinction between **surfaces** and **laws** as mutually exclusive primitive classes of mathematical objects.

The project begins as a foundational note and progresses toward a formally specified, testable, and mechanically verifiable mathematical framework.

---

## Project Goal

Develop a rigorous mathematical system in which every primitive mathematical object belongs to exactly one of two classes:

[
\mathcal{S} = \text{state-bearing objects}
]

[
\mathcal{L} = \text{transformation-bearing objects}
]

The long-term objective is to determine whether this partition can:

* describe existing mathematical theories,
* classify physical theories,
* formalize computable processes,
* produce nontrivial theorems,
* reveal useful structural distinctions,
* and support a distinct research program.

---

# Phase 0 — Initial Proposal

## Status: Complete

Establish the conceptual foundation of the project.

### Completed

* [x] Define the primitive class of surfaces, (\mathcal{S}).
* [x] Define the primitive class of laws, (\mathcal{L}).
* [x] Introduce the universe of mathematical objects, (\mathcal{U}).
* [x] State the completeness axiom.
* [x] State the mutual-exclusivity axiom.
* [x] State the transformation axiom.
* [x] State the no-self-evolution axiom.
* [x] State the irreducibility axiom.
* [x] State the representation axiom.
* [x] Formulate the foundational principle.
* [x] Record the initial conjectures.
* [x] Publish the framework as HTML and PDF.
* [x] Create a public GitHub repository.

---

# Phase 1 — Terminology and Logical Precision

## Goal

Replace intuitive terms with precise definitions that can be evaluated mathematically.

### Tasks

* [ ] Define a **primitive mathematical object**.
* [ ] Define **intrinsic state**.
* [ ] Define an **admissible transformation**.
* [ ] Define what it means for a law to **induce** a transformation.
* [ ] Define **representation**.
* [ ] Define **evolution**.
* [ ] Define **identity** for surfaces and laws.
* [ ] Define a **faithful isomorphism** between classes.
* [ ] Distinguish primitive objects from derived or composite objects.
* [ ] Explain whether (\mathcal{U}) is a set, class, type, category, or metatheoretic universe.
* [ ] Determine whether “surface” should remain the formal term or be replaced by “state,” “configuration,” or “structure.”
* [ ] Create a glossary of all technical terms.
* [ ] Create a notation reference.

### Deliverables

* `docs/glossary.md`
* `docs/notation.md`
* `theory/definitions.md`
* Revised foundational note, version `0.2`

---

# Phase 2 — Choose a Formal Language

## Goal

Express the two-class framework inside a recognized foundational system.

### Candidate approaches

#### Two-sorted first-order logic

Use separate sorts for surfaces and laws.

Possible predicates and operations:

[
\operatorname{Surface}(x)
]

[
\operatorname{Law}(x)
]

[
\operatorname{ActsOn}(\ell,s)
]

[
\operatorname{Transforms}(\ell,s_1,s_2)
]

#### Category theory

Interpret:

* surfaces as objects,
* laws as morphisms, functors, or transformation-generating structures,
* transformations as arrows between objects.

This approach must address whether every morphism should count as a law and whether laws can themselves be objects in higher categories.

#### Dependent type theory

Represent surfaces and laws as distinct types, with law application encoded through typed functions or relations.

#### Set-theoretic formalization

Represent both classes as disjoint tagged structures while preserving the claim that their primitive roles are distinct.

### Tasks

* [ ] Compare the candidate systems.
* [ ] Select an initial formal language.
* [ ] State the syntax of the theory.
* [ ] State the semantics of the theory.
* [ ] Translate all six axioms into the selected language.
* [ ] Identify whether any axioms are redundant.
* [ ] Identify whether any definitions are circular.
* [ ] Separate axioms from definitions and interpretive principles.
* [ ] Specify the metatheory in which the framework is formulated.

### Deliverables

* `formalization/logical-language.md`
* `formalization/syntax.md`
* `formalization/semantics.md`
* Formal specification, version `0.3`

---

# Phase 3 — Internal Consistency and Independence

## Goal

Determine whether the axioms can coexist and whether each axiom contributes independently.

### Tasks

* [ ] Construct at least one model satisfying all axioms.
* [ ] Prove that the completeness and exclusivity axioms yield a unique primitive classification.
* [ ] Test whether irreducibility follows from mutual exclusivity.
* [ ] Test whether no-self-evolution follows from the definition of surface.
* [ ] Test whether the representation axiom is independent.
* [ ] Search for contradictions involving self-reference.
* [ ] Analyze laws that transform other laws.
* [ ] Analyze surfaces that encode their own update rules.
* [ ] Analyze fixed points and identity transformations.
* [ ] Analyze constant laws.
* [ ] Analyze probabilistic laws.
* [ ] Analyze nondeterministic laws.
* [ ] Analyze partial laws.
* [ ] Analyze laws acting on multiple surfaces.
* [ ] Analyze transformations that preserve a surface unchanged.
* [ ] Produce countermodels for any independent axioms where possible.

### Initial theorem target

## Theorem — Unique Primitive Classification

For every primitive object (x \in \mathcal{U}), exactly one of the following holds:

[
x \in \mathcal{S}
]

or

[
x \in \mathcal{L}.
]

### Deliverables

* `theory/theorems.md`
* `theory/proofs.md`
* `theory/models.md`
* `theory/countermodels.md`
* Consistency report, version `0.4`

---

# Phase 4 — Canonical Examples

## Goal

Demonstrate how familiar mathematical and physical systems decompose into surfaces and laws.

Each example should specify:

1. the universe under consideration,
2. the proposed surfaces,
3. the proposed laws,
4. the transformations involved,
5. whether the decomposition is unique,
6. possible alternative decompositions,
7. ambiguous or exceptional objects.

### Mathematics examples

* [ ] Natural numbers and arithmetic operations.
* [ ] Groups and homomorphisms.
* [ ] Rings and ring homomorphisms.
* [ ] Vector spaces and linear transformations.
* [ ] Topological spaces and continuous maps.
* [ ] Manifolds and smooth maps.
* [ ] Graphs and graph transformations.
* [ ] Formal languages and rewrite rules.
* [ ] Dynamical systems.
* [ ] Probability spaces and stochastic transformations.
* [ ] Categories and functors.
* [ ] Proof systems and inference rules.

### Computation examples

* [ ] Finite-state machines.
* [ ] Turing machines.
* [ ] Lambda calculus.
* [ ] Cellular automata.
* [ ] Term-rewriting systems.
* [ ] Computer programs and memory states.
* [ ] Neural networks and update rules.

### Physics examples

* [ ] Newtonian mechanics.
* [ ] Hamiltonian mechanics.
* [ ] Lagrangian mechanics.
* [ ] Classical electromagnetism.
* [ ] Special relativity.
* [ ] General relativity.
* [ ] Quantum mechanics.
* [ ] Statistical mechanics.
* [ ] Quantum field theory.

### Deliverables

* `examples/mathematics/`
* `examples/computation/`
* `examples/physics/`
* Example catalogue, version `0.5`

---

# Phase 5 — Composition and Transformation Theory

## Goal

Develop the internal mathematics of laws acting on surfaces.

### Core questions

* When can two laws be composed?
* Does law composition produce another law?
* Can one law act on multiple classes of surfaces?
* Can different laws induce the same transformation?
* Can a law transform a surface into a law?
* Can laws act on laws?
* Can surfaces be combined into larger surfaces?
* What constitutes an inefficient or redundant transformation sequence?

### Tasks

* [ ] Define law application.
* [ ] Define composition of laws.
* [ ] Define identity laws.
* [ ] Define inverse laws.
* [ ] Define equivalent laws.
* [ ] Define reducible and irreducible laws.
* [ ] Define law order or complexity.
* [ ] Define transformation paths.
* [ ] Define loops of transformations.
* [ ] Define when a loop may be collapsed.
* [ ] Define minimal transformation paths.
* [ ] Investigate whether law composition is associative.
* [ ] Investigate whether laws form a monoid, category, groupoid, algebra, or operad.
* [ ] Determine whether surfaces support products, sums, quotients, or limits.
* [ ] Develop diagrams for surface-law systems.

### Possible theorem targets

* Closure of law composition.
* Associativity of admissible composition.
* Existence or nonexistence of identity laws.
* Conditions for invertibility.
* Minimal-path or loop-collapse theorem.
* Uniqueness conditions for transformations.

### Deliverables

* `theory/composition.md`
* `theory/transformation-paths.md`
* `theory/equivalence.md`
* Transformation calculus, version `0.6`

---

# Phase 6 — Canonical Decomposition

## Goal

Investigate the claim that every mathematical theory admits a canonical decomposition into surfaces and laws.

### Tasks

* [ ] Define a mathematical theory formally.
* [ ] Define a decomposition of a theory.
* [ ] Define equivalence between decompositions.
* [ ] Define a canonical decomposition.
* [ ] Define uniqueness up to isomorphism.
* [ ] Identify theories with obvious decompositions.
* [ ] Identify theories with multiple plausible decompositions.
* [ ] Find counterexamples to uniqueness.
* [ ] Determine whether additional constraints restore uniqueness.
* [ ] Distinguish canonical, minimal, and convenient decompositions.
* [ ] Investigate decomposition-preserving maps between theories.

### Central conjecture

Every mathematical theory admits a canonical decomposition into a family of surfaces and a family of laws.

### Possible outcomes

* The conjecture is true as stated.
* The conjecture is true only under additional assumptions.
* The decomposition exists but is not unique.
* The decomposition is unique only up to equivalence.
* Some mathematical theories do not admit the decomposition.
* The conjecture must be replaced by a weaker classification theorem.

### Deliverables

* `research/canonical-decomposition.md`
* `research/counterexamples.md`
* `research/open-problems.md`
* Decomposition paper, version `0.7`

---

# Phase 7 — Computability

## Goal

Formalize the conjecture that every computable process can be expressed through repeated law application to surfaces.

### Tasks

* [ ] Define a computable process.
* [ ] Define an initial surface.
* [ ] Define a computational law.
* [ ] Define repeated law application.
* [ ] Represent deterministic computation.
* [ ] Represent nondeterministic computation.
* [ ] Represent probabilistic computation.
* [ ] Represent parallel computation.
* [ ] Represent reversible computation.
* [ ] Map Turing-machine configurations to surfaces.
* [ ] Map transition functions to laws.
* [ ] Prove equivalence with a standard model of computation.
* [ ] Determine whether the framework changes computational expressiveness.
* [ ] Define surface complexity.
* [ ] Define law complexity.
* [ ] Define transformation complexity.
* [ ] Compare these measures with time, space, circuit, and Kolmogorov complexity.

### Theorem target

A process is Turing-computable if and only if it can be represented as a finite or recursively generated sequence of admissible laws acting on representable surfaces.

### Deliverables

* `computation/model.md`
* `computation/turing-equivalence.md`
* `computation/complexity.md`
* Computability paper, version `0.8`

---

# Phase 8 — Physical Theories

## Goal

Test whether physical theories admit meaningful and unique surface-law decompositions.

### Tasks

* [ ] Define a physical state as a surface candidate.
* [ ] Define physical dynamics as a law candidate.
* [ ] Distinguish equations of state from equations of motion.
* [ ] Analyze coordinate dependence.
* [ ] Analyze gauge freedom.
* [ ] Analyze observables.
* [ ] Analyze fields.
* [ ] Analyze spacetime.
* [ ] Analyze boundary conditions.
* [ ] Analyze constants and parameters.
* [ ] Analyze probabilistic measurement.
* [ ] Analyze whether Einstein field equations are laws, encoded surfaces, or both at different representational levels.
* [ ] Determine whether a physical law can be represented geometrically without becoming a surface.
* [ ] Test uniqueness under equivalent formulations of the same theory.

### Key challenge

The same physical theory may have several mathematically equivalent formulations. For example:

* Newtonian,
* Lagrangian,
* Hamiltonian,
* geometric,
* operator-based,
* and path-integral formulations.

The framework must determine whether these are:

* different laws acting on the same surfaces,
* different representations of one underlying law,
* or genuinely different decompositions.

### Deliverables

* `physics/classical-mechanics.md`
* `physics/relativity.md`
* `physics/quantum-mechanics.md`
* `physics/equivalent-formulations.md`
* Physical decomposition paper, version `0.9`

---

# Phase 9 — Mechanized Formalization

## Goal

Encode the framework in a proof assistant.

### Candidate systems

* Lean
* Coq
* Agda
* Isabelle
* HOL

### Tasks

* [ ] Select a proof assistant.
* [ ] Encode the two primitive sorts.
* [ ] Encode all axioms.
* [ ] Prove unique primitive classification.
* [ ] Prove basic composition results.
* [ ] Formalize at least one mathematical example.
* [ ] Formalize at least one computational example.
* [ ] Formalize at least one physical toy model.
* [ ] Add automated consistency checks where possible.
* [ ] Add continuous integration for proof verification.

### Repository structure

```text
formal/
├── SurfacesAndLaws/
│   ├── Basic.lean
│   ├── Axioms.lean
│   ├── Transformations.lean
│   ├── Composition.lean
│   ├── Computation.lean
│   └── Examples.lean
```

### Deliverables

* Machine-checked core theory.
* Automated proof-verification workflow.
* Formal release, version `1.0`.

---

# Phase 10 — Evaluation Against Existing Mathematics

## Goal

Determine whether the framework contributes something beyond existing distinctions.

### Comparisons

* [ ] Sets and functions.
* [ ] Objects and morphisms.
* [ ] States and transitions.
* [ ] Data and algorithms.
* [ ] Types and functions.
* [ ] Manifolds and vector fields.
* [ ] Configurations and dynamics.
* [ ] Syntax and inference rules.
* [ ] Coalgebras and state-transition systems.
* [ ] Dynamical systems.
* [ ] Process calculi.
* [ ] Category theory.
* [ ] Structuralism in mathematics.

### Evaluation criteria

The framework should aim to demonstrate at least one of the following:

* a theorem not naturally visible in existing language,
* a useful classification of mathematical theories,
* a new invariant,
* a simpler representation of transformations,
* a canonical decomposition result,
* a complexity measure,
* a connection between computation and physical law,
* a method for reducing redundant transformation paths,
* or a new family of open problems.

### Deliverables

* `comparisons/related-work.md`
* `comparisons/category-theory.md`
* `comparisons/type-theory.md`
* `comparisons/dynamical-systems.md`
* Related-work paper, version `1.1`

---

# Phase 11 — Research Community and Collaboration

## Goal

Make the project understandable, reviewable, and open to criticism.

### Tasks

* [ ] Add a clear `CONTRIBUTING.md`.
* [ ] Add a code of conduct.
* [ ] Add issue templates.
* [ ] Add theorem-proposal templates.
* [ ] Add counterexample-report templates.
* [ ] Label axioms, definitions, conjectures, and theorems separately.
* [ ] Track unresolved objections.
* [ ] Maintain a public bibliography.
* [ ] Invite formal-methods contributors.
* [ ] Invite mathematicians to test examples.
* [ ] Record failed definitions and disproven conjectures.
* [ ] Publish numbered releases.
* [ ] Create a project website.
* [ ] Create diagrams and explanatory notes.
* [ ] Submit mature papers for external review.

### Suggested issue labels

```text
axiom
definition
theorem
proof
counterexample
formalization
physics
computation
category-theory
open-question
needs-review
breaking-change
```

---

# Phase 12 — Long-Term Research Program

## Goal

Determine whether surfaces and laws support a durable mathematical discipline.

### Long-term questions

1. Does every mathematical theory admit a surface-law decomposition?
2. Under what conditions is the decomposition unique?
3. Can laws be classified independently of the surfaces on which they act?
4. Can surfaces be classified by the laws they admit?
5. Is there a universal law-composition structure?
6. Can redundant transformation loops always be collapsed?
7. Is there a maximum number of distinct efficient transformations among a finite family of surfaces?
8. Can transformation complexity be measured independently of representation?
9. Can physical theories be compared by their surface-law complexity?
10. Can equivalent physical formulations be reduced to a common underlying law?
11. Does the framework produce new computability or complexity results?
12. Are surfaces and laws genuinely primitive, or merely another object-morphism distinction?
13. Are there mathematical objects that cannot consistently be assigned to either class?
14. Are there objects whose classification depends on the level of abstraction?
15. Can a representation change preserve class membership while changing apparent form?

---

# Release Milestones

## Version 0.1 — Foundational Note

* Initial axioms.
* Initial definitions.
* Foundational principle.
* Initial conjectures.
* HTML and PDF publication.

## Version 0.2 — Terminology

* Formal glossary.
* Revised definitions.
* Clear notation.
* Definition of primitive object.

## Version 0.3 — Logical Specification

* Chosen formal language.
* Formal syntax.
* Formal semantics.
* Translated axioms.

## Version 0.4 — Models and Proofs

* First model.
* First theorems.
* Independence analysis.
* Initial counterexamples.

## Version 0.5 — Example Catalogue

* Mathematical examples.
* Computational examples.
* Physical examples.

## Version 0.6 — Transformation Calculus

* Law composition.
* Transformation paths.
* Loop reduction.
* Equivalence of laws.

## Version 0.7 — Decomposition Theory

* Formal decomposition definition.
* Canonical decomposition investigation.
* Uniqueness results or counterexamples.

## Version 0.8 — Computability

* Computational model.
* Turing-machine representation.
* Complexity definitions.

## Version 0.9 — Physics

* Classical and relativistic examples.
* Quantum examples.
* Equivalent-formulation analysis.

## Version 1.0 — Mechanized Core

* Proof-assistant implementation.
* Machine-checked foundational theorems.
* Stable core definitions.

## Version 1.1 and beyond

* External review.
* Expanded theorem library.
* Research papers.
* Community contributions.
* Possible textbook or monograph.

---

# Immediate Priorities

The next five concrete tasks are:

1. Define “primitive mathematical object.”
2. Choose a two-sorted formal language.
3. Construct one model satisfying all six axioms.
4. Write three complete decompositions:

   * a finite-state machine,
   * Newtonian mechanics,
   * a vector space with linear transformations.
5. Prove the first nontrivial theorem or identify the first serious counterexample.

---

# Success Criteria

The project should not be considered a mature mathematical theory merely because it has named axioms and conjectures.

It should be considered successful when it achieves several of the following:

* precise, non-circular definitions,
* at least one consistent formal model,
* nontrivial derived theorems,
* meaningful examples,
* difficult counterexamples that the theory can address,
* mechanical verification,
* explanatory advantages over existing frameworks,
* independent use by other researchers,
* and results that remain valuable even if some original conjectures are false.

The purpose of the roadmap is therefore not only to defend the two-class proposal, but to expose it to the strongest possible mathematical tests.
