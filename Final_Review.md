# Discrete Math Study Guide: Chapter 2

## 1. Section 2.6: Truth Tables & Logical Equivalence

### Exercise 2.6.1: Distributive Law
**Statement:** $P \wedge (Q \lor R) \equiv (P \wedge Q) \lor (P \wedge R)$

| $P$ | $Q$ | $R$ | $Q \lor R$ | $P \wedge (Q \lor R)$ | $P \wedge Q$ | $P \wedge R$ | $(P \wedge Q) \lor (P \wedge R)$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| T | T | T | T | **T** | T | T | **T** |
| T | T | F | T | **T** | T | F | **T** |
| T | F | T | T | **T** | F | T | **T** |
| T | F | F | F | **F** | F | F | **F** |
| F | T | T | T | **F** | F | F | **F** |
| F | T | F | T | **F** | F | F | **F** |
| F | F | T | T | **F** | F | F | **F** |
| F | F | F | F | **F** | F | F | **F** |
**Conclusion:** The columns match exactly. The statement is logically equivalent.

### Exercise 2.6.3: The "Or" Form of Implication
**Statement:** $P \implies Q \equiv (\sim P) \lor Q$

| $P$ | $Q$ | $\sim P$ | $P \implies Q$ | $(\sim P) \lor Q$ |
| :--- | :--- | :--- | :--- | :--- |
| T | T | F | **T** | **T** |
| T | F | F | **F** | **F** |
| F | T | T | **T** | **T** |
| F | F | T | **T** | **T** |
**Conclusion:** Equivalent. This is a crucial identity for negating implications later.

### Exercise 2.6.7: Reduction to Absurdity (Tautology)
**Statement:** $P \implies Q \equiv (P \wedge \sim Q) \implies (Q \wedge \sim Q)$

*Note: $(Q \wedge \sim Q)$ is a contradiction (always False).*

| $P$ | $Q$ | $\sim Q$ | $P \wedge \sim Q$ | $Q \wedge \sim Q$ | $P \implies Q$ | $(P \wedge \sim Q) \implies \text{False}$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| T | T | F | F | F | **T** | **T** |
| T | F | T | T | F | **F** | **F** |
| F | T | F | F | F | **T** | **T** |
| F | F | T | F | F | **T** | **T** |
**Conclusion:** Equivalent. This shows why "Proof by Contradiction" works.

### Exercise 2.6.9: DeMorgan’s Law Check
**Statement:** $P \wedge Q$ and $\sim(\sim P \lor \sim Q)$

| $P$ | $Q$ | $P \wedge Q$ | $\sim P$ | $\sim Q$ | $\sim P \lor \sim Q$ | $\sim(\sim P \lor \sim Q)$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| T | T | **T** | F | F | F | **T** |
| T | F | **F** | F | T | T | **F** |
| F | T | **F** | T | F | T | **F** |
| F | F | **F** | T | T | T | **F** |
**Conclusion:** Yes, they are logically equivalent.

---

## 2. Section 2.10: Negating Statements

**The Golden Rules for Negation:**
1. $\sim(\forall x, P(x)) \equiv \exists x, \sim P(x)$
2. $\sim(\exists x, P(x)) \equiv \forall x, \sim P(x)$
3. $\sim(P \implies Q) \equiv P \wedge \sim Q$

### Exercise 2.10.4: The Epsilon-Delta Limit Definition
**Original:** For every positive number $\epsilon$, there is a positive number $\delta$ such that $|x - a| < \delta$ implies $|f(x) - f(a)| < \epsilon$.
* **Symbolic:** $\forall \epsilon > 0, \exists \delta > 0, (|x - a| < \delta) \implies (|f(x) - f(a)| < \epsilon)$
* **Negation:**
    1. Flip $\forall \epsilon$ to $\exists \epsilon$.
    2. Flip $\exists \delta$ to $\forall \delta$.
    3. Negate the implication: $(P \implies Q)$ becomes $(P \wedge \sim Q)$.

**Answer:** There exists a positive number $\epsilon$ such that for every positive number $\delta$, $|x - a| < \delta$ and $|f(x) - f(a)| \ge \epsilon$.

### Exercise 2.10.5: Limit at Infinity
**Original:** For every positive number $\epsilon$, there is a positive number $M$ for which $|f(x) - b| < \epsilon$ whenever $x > M$.
* **Symbolic:** $\forall \epsilon > 0, \exists M > 0, (x > M) \implies (|f(x) - b| < \epsilon)$
* **Negation:**
    1. Flip $\forall \epsilon$ to $\exists \epsilon$.
    2. Flip $\exists M$ to $\forall M$.
    3. Negate the "whenever" (implication): Keep the condition $x > M$ true, but the result false.

**Answer:** There exists a positive number $\epsilon$ such that for every positive number $M$, there is some $x > M$ such that $|f(x) - b| \ge \epsilon$.

---
13. Show that n
3 =
2
2 + 3
2 + 4
2 + 5
2 + · · · + n−1
2.
