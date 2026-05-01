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
## Discrete Math Study Guide: Chapter 3
### Counting, Pascal’s Rule, and the Binomial Theorem

---

## 1. Section 3.4: Permutations and Factorials

**Exercise 3.4.9: Strings with Consecutive Blocks**
* **Problem:** How many permutations of $\{A, B, C, D, E, F, G\}$ contain "ABC" consecutively in that order?
* **Strategy:** Treat the block $[ABC]$ as a **single super-letter**.
* **Solution:** * Instead of 7 individual letters, we now have the set: $\{[ABC], D, E, F, G\}$.
    * This set has **5 items**.
    * The number of ways to arrange 5 items is $5!$.
    * **Result:** $5! = 120$.

**Exercise 3.4.15: Picking Officers**
* **Problem:** Choose a President, VP, Secretary, and Treasurer from 15 people.
* **Strategy:** Order matters here because the roles are distinct (it's a permutation).
* **Solution:** * We are picking 4 people out of 15 where order is important.
    * $P(15, 4) = 15 \times 14 \times 13 \times 12$.
    * **Result:** $32,760$.

---

## 2. Section 3.5: Combinations and List Counting

**Exercise 3.5.9: Relative Order in Lists**
* **Problem:** Lists of length 6 from $\{A, B, C, D, E, F\}$ (no repetition). How many have $D$ occurring before $A$?
* **Strategy:** Symmetry. 
* **Solution:** * Total permutations of the 6 letters is $6! = 720$.
    * In any specific permutation, there are only two possibilities for $A$ and $D$: either $D$ comes before $A$, or $A$ comes before $D$.
    * Since the letters are distinct, these two cases are perfectly symmetric and split the total exactly in half.
    * **Result:** $\frac{6!}{2} = \frac{720}{2} = 360$.

**Exercise 3.5.19: Poker Hands (Flushes)**
* **Problem:** How many 5-card flushes are there? (All cards same suit).
* **Strategy:** Pick a suit, then pick the cards.
* **Solution:** * Step 1: Choose 1 suit out of 4: $\binom{4}{1} = 4$.
    * Step 2: Choose 5 cards out of the 13 available in that suit: $\binom{13}{5}$.
    * Calculation: $4 \times \frac{13 \times 12 \times 11 \times 10 \times 9}{5 \times 4 \times 3 \times 2 \times 1} = 4 \times 1,287$.
    * **Result:** $5,148$.

---

## 3. Essential Proofs: Pascal & Binomial

### Pascal’s Rule Proof
**Identity:** $\binom{n}{r} = \binom{n-1}{r} + \binom{n-1}{r-1}$
* **Combinatorial Proof:**
    * Suppose you have a set of $n$ people, including one person named "Zoe."
    * We want to choose a committee of $r$ people. Total ways = $\binom{n}{r}$.
    * **Case 1:** Zoe is NOT on the committee. We must choose all $r$ people from the remaining $n-1$. Ways = $\binom{n-1}{r}$.
    * **Case 2:** Zoe IS on the committee. We only need to choose $r-1$ more people from the remaining $n-1$. Ways = $\binom{n-1}{r-1}$.
    * Since these cases are mutually exclusive, their sum equals the total.

### Binomial Theorem Proof (by Induction)
**Theorem:** $(1+x)^n = \sum_{k=0}^{n} \binom{n}{k} x^k$
1.  **Base Case ($n=1$):** $(1+x)^1 = 1+x$. Sum gives $\binom{1}{0}x^0 + \binom{1}{1}x^1 = 1 + x$. Matches.
2.  **Inductive Step:** Assume true for $n$. Look at $n+1$:
    * $(1+x)^{n+1} = (1+x)(1+x)^n = (1+x) \sum \binom{n}{k} x^k$
    * $= \sum \binom{n}{k} x^k + \sum \binom{n}{k} x^{k+1}$
    * After shifting indices and combining terms, the coefficient of $x^k$ becomes $\binom{n}{k} + \binom{n}{k-1}$.
    * By **Pascal's Rule**, this equals $\binom{n+1}{k}$.

---

## 4. Section 3.6: Binomial Applications

**Exercise 3.6.9: Alternating Sum of Binomial Coefficients**
* **Problem:** Show $\binom{n}{0} - \binom{n}{1} + \binom{n}{2} - \dots + (-1)^n \binom{n}{n} = 0$.
* **Solution:** * The Binomial Theorem states: $(1+x)^n = \sum_{k=0}^{n} \binom{n}{k} x^k$.
    * Let $x = -1$.
    * $(1 + (-1))^n = \sum_{k=0}^{n} \binom{n}{k} (-1)^k$.
    * $0^n = \binom{n}{0}(-1)^0 + \binom{n}{1}(-1)^1 + \dots$
    * **Result:** $0 = \binom{n}{0} - \binom{n}{1} + \binom{n}{2} \dots$

**Exercise 3.6.13: Hockey-Stick Identity Lite**
* **Problem:** Show $\binom{n}{3} = \binom{2}{2} + \binom{3}{2} + \binom{4}{2} + \dots + \binom{n-1}{2}$.
* **Solution:** * Use Pascal’s Rule repeatedly: $\binom{n}{r} - \binom{n-1}{r} = \binom{n-1}{r-1}$.
    * $\binom{n}{3} = \binom{n-1}{3} + \binom{n-1}{2}$
    * $\binom{n-1}{3} = \binom{n-2}{3} + \binom{n-2}{2}$
    * Keep expanding the "3" term until you reach the bottom: $\binom{3}{3} = \binom{2}{2} = 1$.
    * **Result:** Summing them all up yields the right-hand side.

---
