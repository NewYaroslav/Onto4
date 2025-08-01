# Analysis of the Liar Paradox in Onto4

## 1. Context of Reasoning

Consider a context `C₀` in which the following basic ontological assumption holds:

> **(Axiom 1: Distinction as a condition of truth)**
> Any logical state (`true` or `false`) is possible **only when two different objects are distinguished** during comparison.

Formally:

```text
Let V ∈ {T, F}  // logical values
Let compare : Object × Object → V

compare(a, b) is meaningful ⇔ a ≠ b
```

If an object is compared with itself (`a = a`), then according to this principle the logical evaluation `V` is **meaningless**, because no distinction takes place. This defines the basic boundary of applicability of logic inside Onto4.

## 2. Formalizing the liar statement

The liar paradox:

```text
L := "This statement is false."
```

In more explicit form:

```text
L ≡ "L is false"
```

Here `L` makes a logical judgment about itself, that is `compare(L, L)`.

## 3. Applying the axiom of distinction

The comparison `compare(L, L)` compares **an object with itself**:

```text
compare(L, L) ⇒ meaningless (by Axiom 1)
```

Therefore the logical operation `L is false` **has no foundation**, as it violates the basic criterion of distinction. As a result, the whole statement `L` cannot be logically evaluated.

## 4. Derivation via Onto4

Check the features:

| Feature | Value | Justification |
|---------|-------|---------------|
| `S` (sensible) | `0` | Self-reference destroys distinction → no meaning |
| `E` (evaluable) | `0` | Evaluation impossible when `S = 0` |
| `V` (value) | `–` | Not applicable |

Result:

```text
meaning(L, C₀) = Ø
```

## 5. Conclusion

In Onto4 the liar paradox is not a paradox in the logical sense. It **does not produce a contradiction** because it **fails the ontological admissibility test**: the statement has no meaning as an object of reasoning.

Onto4 allows a clear separation between:

* grammatically correct but ontologically meaningless constructions;
* and truly comparable statements that can be analyzed logically.

Thus the liar paradox in Onto4 receives the value `Ø`—**outside of logic**, not within its bounds.
