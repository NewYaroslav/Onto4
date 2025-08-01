# Truth Tables for Onto4 Logic Operators

## Onto4 States

| Symbol | Name | Meaning |
|--------|----------------------------|------------------------------------------------|
| **T**  | True                       | Standard truth |
| **F**  | False                      | Standard falsity |
| **U**  | Undefined                  | No data / not derived |
| **C**  | Nonsense / Category error  | The concept is fictive; the statement has no ontological meaning |

---

## Negation (¬)

Idea:

- ¬T = F
- ¬F = T
- ¬U = U
- ¬C = C ← you cannot turn nonsense into sense

| A | ¬A |
|---|----|
| T | F  |
| F | T  |
| U | U  |
| C | C  |

---

## Conjunction (A ∧ B)

Idea:

- If both parts are **T**, then T.
- If at least one is **F**, then F.
- If both are **U**, then U.
- If one is **C**, the result is **C** (a category failure infects the whole construction).

| A | B | A ∧ B |
|---|---|-------|
| T | T | T     |
| T | F | F     |
| F | F | F     |
| T | U | U     |
| F | U | F     |
| U | U | U     |
| T | C | C     |
| F | C | C     |
| U | C | C     |
| C | C | C     |

**Rule:** if there is **C** → the result is **C**, even if the other part is **F**, because the conjunction is semantically invalid.

---

## Disjunction (A ∨ B)

Idea:

- If at least one **T**, then T.
- If both are **F**, then F.
- If at least one **C**, the result is C unless there is T (see below).

| A | B | A ∨ B |
|---|---|-------|
| T | T | T     |
| T | F | T     |
| F | F | F     |
| T | U | T     |
| F | U | U     |
| U | U | U     |
| T | C | T     |
| F | C | C     |
| U | C | C     |
| C | C | C     |

**Rule:** if at least one argument is **categorically meaningless**, and there is no **T**, the disjunction is also **meaningless (C)**.

---

## Implication (A → B)

Implication is tricky:

- In classical logic: false A → anything = true
- In Onto4: **if A or B = C → the result is also C**, because the statement is logically inadmissible.

| A | B | A → B |
|---|---|-------|
| T | T | T     |
| T | F | F     |
| F | T | T     |
| F | F | T     |
| T | U | U     |
| U | T | T     |
| U | U | U     |
| T | C | C     |
| C | T | C     |
| F | C | C     |
| C | F | C     |
| C | U | C     |
| U | C | C     |
| C | C | C     |

---

## Equivalence (A ↔ B)

| A | B | A ↔ B |
|---|---|-------|
| T | T | T     |
| F | F | T     |
| T | F | F     |
| F | T | F     |
| U | U | U     |
| T | U | U     |
| F | U | U     |
| T | C | C     |
| F | C | C     |
| U | C | C     |
| C | C | C     |

---
