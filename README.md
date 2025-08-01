# Onto4
[For the Russian version of this README, see](README-RU.md).

**Onto4** is a four-valued logic in which the logical status of a statement depends not only on its truth or falsity but also on whether it is meaningful within a given context.

The name **Onto4** comes from **"ontology"**—the study of what exists, in what sense, and under what conditions a statement can mean anything.

> Not every assertion has meaning.
> Before discussing whether it is true or false, we must ask:
> **"Can it even be meaningfully formulated?"**

In classical logic any statement is considered either true (`T`) or false (`F`). Yet that system does not distinguish cases where a statement cannot be meaningfully formulated at all or where the logical categories of truth and falsity do not apply.

**Onto4** introduces a more precise classification by adding two additional statuses:

- `U` — **uncertain**: the statement is meaningful but cannot be logically evaluated as true or false;
- `Ø` — **nonsense**: the statement has no meaning in the given context and cannot take part in logical reasoning.

Thus Onto4 extends classical logic by introducing the concept of **ontological admissibility** as a preliminary condition for analysis. Each statement is first checked for meaning and evaluability and receives one of four values:

- `T` — **true**: meaningful and true;
- `F` — **false**: meaningful and false;
- `U` — **uncertain**: meaningful but not subject to binary evaluation;
- `Ø` — **nonsense**: meaningless and excluded from the logic.

### Formal structure of Onto4

Each value in Onto4 is described by a triple of binary features:

| Feature      | Label          | Values        | Description |
|--------------|---------------|---------------|-------------|
| Sense        | `S` (Sensible) | `1` / `0`     | Whether the statement makes sense in this context |
| Evaluability | `E` (Evaluable)| `1` / `0`     | Whether it can be logically judged as true or false |
| Truth value  | `V` (Value)    | `1` / `0` / `–` | True, false or not applicable (if `E = 0`) |

Onto4 feature table:

| Onto4 | `S` | `E` | `V` | Comment |
|-------|-----|-----|-----|------------------------------|
| `T`   | 1   | 1   | 1   | Makes sense, evaluable, and true |
| `F`   | 1   | 1   | 0   | Makes sense, evaluable, and false |
| `U`   | 1   | 0   | –   | Makes sense, but logical evaluation does not apply |
| `Ø`   | 0   | 0   | –   | Statement lacks meaning; evaluation is impossible |

> Thus every logical value in Onto4 is not merely a label (`True`/`False`) but a **combination of ontological and logical conditions**.

---

### Relation to classical logic

Onto4 **does not abolish binary logic**, but extends it with an **ontological layer**:

- If `S = 1` and `E = 1`, logic reduces to the classical case;
- If `S = 1` but `E = 0` — logical indeterminacy (`U`);
- If `S = 0` — nonsense (`Ø`), and reasoning cannot start.

This separation enables **context-sensitive reasoning** where a statement may be rejected not because it is false but because it is inexpressible within the system of concepts.

### Overcoming the observer paradox

Classical logic implicitly relies on a metaphysical assumption of an external, universal observer for whom any statement:

- has a fixed, unambiguous meaning,
- can be formulated in any context,
- and is subject to logical evaluation as true or false.

Such an observer:

- is **outside time** — knowing past, present and future as a whole;
- **outside language and culture** — concepts are always defined;
- **outside the system itself** — merely "looking from the side".

This is not a logically derived entity but a **projection of the subjective feeling "I, observing everything"**, built into thinking by default. In reality such an observer is a **metaphysical fiction** that ignores the limitations of context, language and concepts.

**Onto4** rejects this fiction.

> ❓ *"Is it even possible to formulate this statement meaningfully within the given system—in its language, time, culture?"*

If the answer is no, the statement receives status `Ø` — **ontologically inadmissible**, and is excluded from logical analysis.

Thus Onto4 allows reasoning **from within the system itself**, acknowledging:

- the limitedness of language,
- the impossibility of a universal context,
- and the dependence of meaning on the participant's viewpoint.

### Examples

```
"2 + 2 = 4"                               → T (meaningful and true)
"An elephant is smaller than an ant"      → F (meaningful and false)
"It will rain tomorrow"                   → U (meaningful but truth not yet determined)
"The Internet existed in the year 0 AD"  → Ø (meaningless in the context of the 1st century)
```

Onto4 is a logic in which truth is secondary:
first comes meaning, then applicability, and only after that—truth or falsity.

### Context and the meaning of a statement

In Onto4 any statement is considered **within a context** that defines:

- which concepts exist at all,
- what language is used,
- what rules are allowed,
- and in what time, culture or mental model the judgment occurs.

Unlike classical logic, Onto4 **does not evaluate a statement "by itself"**—it must first be meaningful within the given context.

This is reflected in the signature of the meaning function:

```text
meaning : Statement × Context → Onto4Value
```

A context `Context` can be represented as a set of parameters:

```text
C = {
  Language = Russian,
  Time = 2025,
  Concepts = {internet, computer, falsehood, truth},
  ReferenceMode = SelfReferenceAllowed,
  EvaluationPolicy = StrictMeaningCheck,
  ...
}
```

A context may include any parameters necessary for interpretation, and depending on them the same statement may have different meaning—or none at all.

Example:

```text
S = "The Internet exists"

C₁ = {
  Time = 0,
  Language = Latin,
  Concepts = {aqua, gladius, imperium}
}

C₂ = {
  Time = 2025,
  Language = Russian,
  Concepts = {интернет, компьютер, сеть}
}

meaning(S, C₁) = Ø   // nonsense — the concept "internet" is absent
meaning(S, C₂) = T   // meaningful and true
```

This allows Onto4 to abandon the abstract observer for whom all statements always have sense and value.

---

## Comparison of Onto4 with other logics

| Logic | Values | Support for meaningless expressions | Indeterminacy | Self-reference | Features |
|-------|--------|------------------------------------|---------------|----------------|----------|
| **Classical logic** | T, F | ❌ | ❌ | 💥 paradox | Simple but inflexible. Everything is meaningful and evaluable. |
| **Three-valued (Łukasiewicz, Kleene)** | T, F, U | ❌ | ✅ | 💥 paradox | Introduces "unknown" but still requires meaning |
| **FDE / paraconsistent logic** | T, F, {T∧F} | ❌ | ✅ | 💥 paradox | Allows contradictions without collapse |
| **Modal logic** | T, F across worlds | ❌ | ◼ | 💥 paradox | Extends classical logic via modalities |
| **Onto4** | T, F, U, Ø | ✅ | ✅ | ✅ → Ø | Takes ontological admissibility into account, separates meaning from truth |

### Examples and philosophical analyses

Onto4 is a tool for analyzing philosophical and linguistic paradoxes that are hard to express in classical systems.

The project includes discussions of cases such as:

- **The liar paradox** — why the phrase *"This statement is false"* has no meaning in Onto4:
  📄 [docs/examples/liar-paradox.md](docs/examples/liar-paradox.md)

---

### Tables of logical operators

Onto4 extends the classical truth table by adding the additional states `U` (undefined) and `Ø` (nonsense).

For details, see the tables of logical operators:

📄 [docs/truth-tables.md](docs/truth-tables.md)
