<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Toward a Two-Class Foundation of Mathematical Objects</title>

  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['\\(', '\\)']],
        displayMath: [['\\[', '\\]']],
        processEscapes: true
      },
      svg: {
        fontCache: 'global'
      }
    };
  </script>
  <script async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js"></script>

  <style>
    :root {
      --bg: #f6f5f2;
      --paper: #ffffff;
      --text: #1d1d1f;
      --muted: #66666a;
      --line: #d9d7d2;
      --accent: #1f4f8a;
      --soft: #eef3f8;
      --shadow: 0 18px 60px rgba(0, 0, 0, 0.08);
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      background:
        radial-gradient(circle at top left, rgba(31, 79, 138, 0.08), transparent 34rem),
        var(--bg);
      color: var(--text);
      font-family: Georgia, "Times New Roman", serif;
      line-height: 1.65;
    }

    .page {
      width: min(980px, calc(100% - 32px));
      margin: 48px auto;
      background: var(--paper);
      box-shadow: var(--shadow);
      border: 1px solid rgba(0, 0, 0, 0.05);
    }

    header {
      padding: 64px 72px 42px;
      border-bottom: 1px solid var(--line);
      background: linear-gradient(180deg, #fff 0%, #fbfbfa 100%);
    }

    .eyebrow {
      margin: 0 0 14px;
      font-family: Arial, Helvetica, sans-serif;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      font-size: 0.76rem;
      color: var(--accent);
      font-weight: 700;
    }

    h1 {
      margin: 0;
      font-size: clamp(2.2rem, 5vw, 4.4rem);
      line-height: 1.05;
      letter-spacing: -0.04em;
      max-width: 820px;
    }

    .subtitle {
      margin: 22px 0 0;
      max-width: 720px;
      color: var(--muted);
      font-size: 1.08rem;
    }

    main {
      padding: 48px 72px 72px;
    }

    nav {
      margin-bottom: 46px;
      padding: 22px 24px;
      background: var(--soft);
      border-left: 4px solid var(--accent);
      font-family: Arial, Helvetica, sans-serif;
    }

    nav strong {
      display: block;
      margin-bottom: 8px;
    }

    nav a {
      color: var(--accent);
      text-decoration: none;
      margin-right: 14px;
      white-space: nowrap;
    }

    nav a:hover {
      text-decoration: underline;
    }

    section {
      margin-top: 46px;
      scroll-margin-top: 24px;
    }

    h2 {
      margin: 0 0 16px;
      font-size: 1.8rem;
      line-height: 1.2;
      letter-spacing: -0.02em;
    }

    h3 {
      margin: 0 0 10px;
      font-size: 1.28rem;
    }

    p {
      margin: 12px 0;
    }

    ul, ol {
      padding-left: 1.4rem;
    }

    .statement {
      margin: 24px 0;
      padding: 24px 26px;
      border: 1px solid var(--line);
      border-radius: 10px;
      background: #fff;
    }

    .statement.axiom {
      border-left: 5px solid #1f4f8a;
    }

    .statement.definition {
      border-left: 5px solid #6d4c8e;
    }

    .statement.corollary {
      border-left: 5px solid #2d7a56;
    }

    .statement.principle {
      border-left: 5px solid #9a6b16;
    }

    .statement.conjecture {
      border-left: 5px solid #9b3b3b;
    }

    .label {
      display: inline-block;
      margin-bottom: 8px;
      font-family: Arial, Helvetica, sans-serif;
      font-weight: 700;
      letter-spacing: 0.02em;
    }

    .math-block {
      overflow-x: auto;
      padding: 8px 0;
    }

    .note {
      margin-top: 50px;
      padding: 24px 26px;
      background: #fbf7ed;
      border: 1px solid #e7dcc0;
      border-radius: 10px;
    }

    footer {
      padding: 24px 72px 34px;
      border-top: 1px solid var(--line);
      color: var(--muted);
      font-family: Arial, Helvetica, sans-serif;
      font-size: 0.9rem;
    }

    @media (max-width: 700px) {
      .page {
        width: 100%;
        margin: 0;
        border: none;
      }

      header,
      main,
      footer {
        padding-left: 24px;
        padding-right: 24px;
      }

      header {
        padding-top: 42px;
      }

      main {
        padding-top: 32px;
      }

      .statement {
        padding: 20px;
      }
    }

    @media print {
      body {
        background: #fff;
      }

      .page {
        width: 100%;
        margin: 0;
        box-shadow: none;
        border: none;
      }

      nav {
        display: none;
      }

      .statement {
        break-inside: avoid;
      }
    }
  </style>
</head>

<body>
  <article class="page">
    <header>
      <p class="eyebrow">Foundational Mathematics Note</p>
      <h1>Toward a Two-Class Foundation of Mathematical Objects</h1>
      <p class="subtitle">
        A formal presentation of the proposed distinction between surfaces and laws as mutually exclusive primitive classes.
      </p>
    </header>

    <main>
      <nav aria-label="Table of contents">
        <strong>Contents</strong>
        <a href="#symbols">Primitive Symbols</a>
        <a href="#axioms">Axioms</a>
        <a href="#definitions">Definitions</a>
        <a href="#principle">Principle</a>
        <a href="#conjectures">Conjectures</a>
      </nav>

      <section id="symbols">
        <h2>Primitive Symbols</h2>
        <ul>
          <li>\(\mathcal{S}\) denotes the class of surfaces.</li>
          <li>\(\mathcal{L}\) denotes the class of laws.</li>
          <li>\(\mathcal{U}\) denotes the universe of mathematical objects.</li>
        </ul>
      </section>

      <section id="axioms">
        <h2>Axioms</h2>

        <div class="statement axiom">
          <div class="label">Axiom 1 — Completeness</div>
          <p>Every primitive mathematical object belongs to exactly one class.</p>
          <div class="math-block">
            \[
            \forall x \in \mathcal{U},
            \quad
            x \in \mathcal{S}
            \;\lor\;
            x \in \mathcal{L}.
            \]
          </div>
        </div>

        <div class="statement axiom">
          <div class="label">Axiom 2 — Mutual Exclusivity</div>
          <p>No primitive object is simultaneously a surface and a law.</p>
          <div class="math-block">
            \[
            \forall x \in \mathcal{U},
            \quad
            \neg\left(
            x \in \mathcal{S}
            \land
            x \in \mathcal{L}
            \right).
            \]
          </div>
        </div>

        <div class="statement corollary">
          <div class="label">Corollary 2.1</div>
          <p>The two classes form a disjoint partition of the universe.</p>
          <div class="math-block">
            \[
            \mathcal{U}
            =
            \mathcal{S}
            \sqcup
            \mathcal{L}.
            \]
          </div>
        </div>

        <div class="statement axiom">
          <div class="label">Axiom 3 — Transformation</div>
          <p>Every admissible transformation between surfaces is induced by at least one law.</p>
          <div class="math-block">
            \[
            S_1,S_2 \in \mathcal{S},
            \qquad
            S_1 \rightarrow S_2
            \Longrightarrow
            \exists L \in \mathcal{L}.
            \]
          </div>
        </div>

        <div class="statement axiom">
          <div class="label">Axiom 4 — No Self-Evolution</div>
          <p>No surface evolves independently of a law.</p>
          <div class="math-block">
            \[
            S_1 \rightarrow S_2
            \Longrightarrow
            \exists L \in \mathcal{L}
            \text{ such that }
            L(S_1)=S_2.
            \]
          </div>
        </div>

        <div class="statement axiom">
          <div class="label">Axiom 5 — Irreducibility</div>
          <p>No law is identical to any surface.</p>
          <div class="math-block">
            \[
            \forall L \in \mathcal{L},
            \forall S \in \mathcal{S},
            \quad
            L \neq S.
            \]
          </div>
        </div>

        <div class="statement axiom">
          <div class="label">Axiom 6 — Representation</div>
          <p>A surface may encode a law without becoming identical to that law.</p>
          <div class="math-block">
            \[
            R(L)\in\mathcal{S},
            \qquad
            L\in\mathcal{L},
            \qquad
            R(L)\neq L.
            \]
          </div>
        </div>
      </section>

      <section id="definitions">
        <h2>Definitions</h2>

        <div class="statement definition">
          <div class="label">Definition 1 — Surface</div>
          <p>
            A <em>surface</em> is an object whose identity is completely determined by its intrinsic state.
            A surface possesses no primitive notion of transformation.
          </p>
        </div>

        <div class="statement definition">
          <div class="label">Definition 2 — Law</div>
          <p>
            A <em>law</em> is an object whose identity is completely determined by the admissible transformations it defines between surfaces.
            A law is not itself a surface.
          </p>
        </div>
      </section>

      <section id="principle">
        <h2>Foundational Principle</h2>

        <div class="statement principle">
          <div class="label">Principle 1</div>
          <p>The ontology of mathematics consists of two primitive classes:</p>
          <ol>
            <li>state-bearing objects,</li>
            <li>transformation-bearing objects.</li>
          </ol>
          <p>No third primitive class is assumed.</p>
        </div>
      </section>

      <section id="conjectures">
        <h2>Conjectures</h2>

        <div class="statement conjecture">
          <div class="label">Conjecture 1</div>
          <p>Every mathematical theory admits a canonical decomposition</p>
          <div class="math-block">
            \[
            (\mathcal{S},\mathcal{L}).
            \]
          </div>
        </div>

        <div class="statement conjecture">
          <div class="label">Conjecture 2</div>
          <p>
            Every physical theory admits a unique decomposition into a family of surfaces and a family of laws.
          </p>
        </div>

        <div class="statement conjecture">
          <div class="label">Conjecture 3</div>
          <p>No faithful isomorphism exists between the class of surfaces and the class of laws.</p>
          <div class="math-block">
            \[
            \mathcal{S}
            \not\cong
            \mathcal{L}.
            \]
          </div>
        </div>

        <div class="statement conjecture">
          <div class="label">Conjecture 4</div>
          <p>
            Every computable process can be expressed as repeated application of elements of
            \(\mathcal{L}\) acting upon elements of \(\mathcal{S}\).
          </p>
        </div>

        <div class="statement conjecture">
          <div class="label">Conjecture 5</div>
          <p>The partition</p>
          <div class="math-block">
            \[
            \mathcal{U}
            =
            \mathcal{S}
            \sqcup
            \mathcal{L}
            \]
          </div>
          <p>
            is more fundamental than distinctions such as state versus dynamics,
            object versus morphism, data versus algorithm, manifold versus vector field,
            and configuration versus evolution.
          </p>
        </div>
      </section>

      <aside class="note">
        <strong>Formalization note.</strong>
        The framework becomes substantially stronger once the meanings of
        “primitive,” “intrinsic state,” “admissible transformation,” “representation,”
        and “faithful isomorphism” are specified inside a chosen foundational system,
        such as category theory, dependent type theory, or a two-sorted logical language.
      </aside>
    </main>

    <footer>
      Standalone HTML document rendered with MathJax 3.
    </footer>
  </article>
</body>
</html>
