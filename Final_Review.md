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

## Discrete Math Study Guide: Chapter 5
### Direct and Contrapositive Proofs

This chapter is all about the "if $P$, then $Q$" structure. Remember:
* **Direct Proof:** Assume $P$, show $Q$.
* **Contrapositive Proof:** Assume $\sim Q$, show $\sim P$. (Use this if $Q$ is "negative" or if $P$ is easier to work with than $Q$).

---

### Exercise 5.15: Contrapositive Strategy
**Statement:** Suppose $x \in \mathbb{Z}$. If $x^3 - 1$ is even, then $x$ is odd.
* **Method:** Contrapositive. (Easier to start with $x$ than $x^3$).
* **Assume $\sim Q$:** Suppose $x$ is **even**.
* **Goal:** Show $x^3 - 1$ is **odd**.
* **Proof:**
    1.  Since $x$ is even, $x = 2k$ for some $k \in \mathbb{Z}$.
    2.  Substitute into the expression: $x^3 - 1 = (2k)^3 - 1 = 8k^3 - 1$.
    3.  Rewrite to show it's odd: $8k^3 - 1 = 8k^3 - 2 + 1 = 2(4k^3 - 1) + 1$.
    4.  Since $(4k^3 - 1)$ is an integer, $x^3 - 1$ is of the form $2j + 1$.
    5.  Therefore, $x^3 - 1$ is odd.
* **Conclusion:** By contrapositive, if $x^3 - 1$ is even, then $x$ is odd.

### Exercise 5.17: Direct Proof with Division
**Statement:** If $n$ is odd, then $8 \mid (n^2 - 1)$.
* **Method:** Direct.
* **Assume $P$:** Suppose $n$ is odd.
* **Proof:**
    1.  $n = 2k + 1$ for some $k \in \mathbb{Z}$.
    2.  Expand $n^2 - 1$:
        $$(2k+1)^2 - 1 = (4k^2 + 4k + 1) - 1 = 4k^2 + 4k = 4k(k+1)$$
    3.  Analyze the term $k(k+1)$: Since $k$ and $k+1$ are consecutive integers, one of them **must** be even. Thus, $k(k+1) = 2m$ for some $m \in \mathbb{Z}$.
    4.  Substitute back: $4k(k+1) = 4(2m) = 8m$.
    5.  Since $n^2 - 1 = 8m$, it is divisible by 8.

### Exercise 5.21: Direct Proof (Congruence)
**Statement:** Let $a, b \in \mathbb{Z}$ and $n \in \mathbb{N}$. If $a \equiv b \pmod n$, then $a^3 \equiv b^3 \pmod n$.
* **Method:** Direct.
* **Assume $P$:** $a \equiv b \pmod n$, which means $n \mid (a - b)$.
* **Proof:**
    1.  By definition, $a - b = nk$ for some $k \in \mathbb{Z}$.
    2.  We use the algebraic identity for the difference of cubes:
        $$a^3 - b^3 = (a - b)(a^2 + ab + b^2)$$
    3.  Substitute the assumption: $a^3 - b^3 = (nk)(a^2 + ab + b^2)$.
    4.  Let $j = k(a^2 + ab + b^2)$. Since $a, b, k \in \mathbb{Z}$, $j$ is an integer.
    5.  $a^3 - b^3 = nj$, which means $n \mid (a^3 - b^3)$.
* **Conclusion:** $a^3 \equiv b^3 \pmod n$.

### Exercise 5.27: Proof by Cases
**Statement:** If $a \equiv 0 \pmod 4$ or $a \equiv 1 \pmod 4$, then $\binom{a}{2}$ is even.
* **Method:** Direct (Cases).
* **Formula Note:** $\binom{a}{2} = \frac{a(a-1)}{2}$.
* **Case 1: $a \equiv 0 \pmod 4$**
    1.  $a = 4k$ for some $k \in \mathbb{Z}$.
    2.  $\binom{a}{2} = \frac{4k(4k-1)}{2} = 2k(4k-1)$.
    3.  This is $2 \times (\text{integer})$, so it is even.
* **Case 2: $a \equiv 1 \pmod 4$**
    1.  $a = 4k + 1$ for some $k \in \mathbb{Z}$.
    2.  $\binom{a}{2} = \frac{(4k+1)(4k+1-1)}{2} = \frac{(4k+1)(4k)}{2} = (4k+1)(2k)$.
    3.  This is $2 \times (k(4k+1))$, which is even.
* **Conclusion:** In both possible cases, $\binom{a}{2}$ is even.

---

## Discrete Math Study Guide: Chapter 6
### Proof by Contradiction

The logic here is: Assume the statement is **false**, then show this leads to a logical disaster (a contradiction like $0=1$ or a number being both even and odd).

---

## 1. Landmark Proofs

### Proof: $\sqrt{2}$ is Irrational
* **Assume False:** Suppose $\sqrt{2}$ is **rational**. This means $\sqrt{2} = \frac{a}{b}$ for some $a, b \in \mathbb{Z}$ where the fraction is in **simplest form** (no common factors).
* **Square both sides:** $2 = \frac{a^2}{b^2} \implies a^2 = 2b^2$.
* **Deduce parity:** This means $a^2$ is even, so **$a$ must be even** ($a = 2k$).
* **Substitute:** $(2k)^2 = 2b^2 \implies 4k^2 = 2b^2 \implies 2k^2 = b^2$.
* **The Contradiction:** This means $b^2$ is even, so **$b$ must be even**.
* **Result:** If $a$ and $b$ are both even, the fraction $\frac{a}{b}$ was not in simplest form. **Contradiction.**

### Proof: Infinitude of Primes (Euclid)
* **Assume False:** Suppose there is a finite set of primes $P = \{p_1, p_2, \dots, p_n\}$.
* **Construct a new number:** Let $Q = (p_1 \times p_2 \times \dots \times p_n) + 1$.
* **Analyze $Q$:**
    * $Q$ is an integer greater than 1, so it must have a prime divisor.
    * However, if you divide $Q$ by any prime in our "complete" list $P$, you get a remainder of **1**.
    * Therefore, $Q$ is either prime itself or divisible by a prime not in our list.
* **The Contradiction:** We found a prime not in our "complete" list. **Contradiction.**

---

## 2. Exercises

**Exercise 6.7: Parity of Squares**
* **Statement:** If $a, b \in \mathbb{Z}$, then $a^2 - 4b - 3 \neq 0$.
* **Assume False:** Suppose $a^2 - 4b - 3 = 0$.
* **Rearrange:** $a^2 = 4b + 3$.
* **Analyze Modulo 4:** This says $a^2 \equiv 3 \pmod 4$.
* **Check all cases for $a^2 \pmod 4$:**
    * If $a$ is even ($4k$ or $4k+2$), $a^2$ is $0 \pmod 4$ or $4 \pmod 4 \equiv 0$.
    * If $a$ is odd ($4k+1$ or $4k+3$), $a^2$ is $1 \pmod 4$ or $9 \pmod 4 \equiv 1$.
* **The Contradiction:** A square can only be $0$ or $1 \pmod 4$. It can **never** be $3 \pmod 4$. **Contradiction.**

**Exercise 6.16: AM-GM Inequality (Basic)**
* **Statement:** If $a, b \in \mathbb{R}^+$, then $a + b \geq 2\sqrt{ab}$.
* **Assume False:** Suppose $a + b < 2\sqrt{ab}$.
* **Algebra:** Since $a, b > 0$, we can square both sides:
    * $(a+b)^2 < 4ab$
    * $a^2 + 2ab + b^2 < 4ab$
    * $a^2 - 2ab + b^2 < 0$
    * $(a - b)^2 < 0$
* **The Contradiction:** The square of any real number must be $\geq 0$. It is impossible for $(a-b)^2 < 0$. **Contradiction.**

**Exercise 6.17: Divisibility**
* **Statement:** For every $n \in \mathbb{Z}$, $4 \nmid (n^2 + 2)$.
* **Assume False:** Suppose $4 \mid (n^2 + 2)$ for some $n$.
* **Algebra:** This means $n^2 + 2 = 4k$, or $n^2 = 4k - 2$.
* **Analyze Modulo 4:** $n^2 \equiv -2 \equiv 2 \pmod 4$.
* **The Contradiction:** As shown in Exercise 6.7, $n^2 \pmod 4$ can only be $0$ or $1$. It can never be $2$. **Contradiction.**

---
## Discrete Math Study Guide: Chapter 7
### Proofs of "If and Only If" ($P \iff Q$)

To prove an "if and only if" statement, you must prove two directions:
1.  **Forward ($\Rightarrow$):** If $P$, then $Q$.
2.  **Backward ($\Leftarrow$):** If $Q$, then $P$.

---

### Exercise 7.3: Parity of a Polynomial
**Statement:** $a^3 + a^2 + a$ is even if and only if $a$ is even.
* **Forward ($\Rightarrow$):** Assume $a^3 + a^2 + a$ is even. We use **contrapositive**.
    * Suppose $a$ is odd. Then $a = 2k+1$.
    * $a^3 + a^2 + a = (\text{odd})^3 + (\text{odd})^2 + (\text{odd}) = \text{odd} + \text{odd} + \text{odd} = \text{odd}$.
    * Since the result is odd, the contrapositive is proven.
* **Backward ($\Leftarrow$):** Assume $a$ is even. Then $a = 2k$.
    * $a^3 + a^2 + a = (2k)^3 + (2k)^2 + 2k = 8k^3 + 4k^2 + 2k = 2(4k^3 + 2k^2 + k)$.
    * This is clearly even.

### Exercise 7.5: Cubic Parity
**Statement:** $a$ is odd if and only if $a^3$ is odd.
* **Forward ($\Rightarrow$):** Assume $a$ is odd ($a = 2k+1$).
    * $a^3 = (2k+1)^3 = 8k^3 + 12k^2 + 6k + 1 = 2(4k^3 + 6k^2 + 3k) + 1$.
    * Thus, $a^3$ is odd.
* **Backward ($\Leftarrow$):** Assume $a^3$ is odd. We use **contrapositive**.
    * Suppose $a$ is even ($a = 2k$).
    * $a^3 = (2k)^3 = 8k^3 = 2(4k^3)$.
    * Thus, $a^3$ is even. Contrapositive proven.

### Exercise 7.9: Divisibility by 14
**Statement:** $14 \mid a$ iff $7 \mid a$ and $2 \mid a$.
* **Forward ($\Rightarrow$):** Assume $14 \mid a$.
    * Then $a = 14k$ for some $k \in \mathbb{Z}$.
    * Since $a = 7(2k)$, $7 \mid a$. Since $a = 2(7k)$, $2 \mid a$.
* **Backward ($\Leftarrow$):** Assume $7 \mid a$ and $2 \mid a$.
    * Since $2 \mid a$, $a$ is even, so $a = 2m$.
    * Substitute this into the other condition: $7 \mid 2m$.
    * By **Euclid's Lemma**, since $7$ is prime and $7 \nmid 2$, it must be that $7 \mid m$.
    * So $m = 7j$.
    * Substitute back: $a = 2(7j) = 14j$. Thus $14 \mid a$.

### Exercise 7.11: Product Parity
**Statement:** $(a-3)b^2$ is even if and only if $a$ is odd or $b$ is even.
* **Forward ($\Rightarrow$):** Assume $(a-3)b^2$ is even. Use **contrapositive**.
    * Negate "($a$ is odd or $b$ is even)": Assume $a$ is even **and** $b$ is odd.
    * If $a$ is even, $(a-3)$ is (even - odd) = **odd**.
    * If $b$ is odd, $b^2$ is **odd**.
    * The product of two odds is **odd**. So $(a-3)b^2$ is odd. Contrapositive proven.
* **Backward ($\Leftarrow$):** Assume $a$ is odd or $b$ is even.
    * **Case 1:** $a$ is odd. Then $(a-3)$ is (odd - odd) = **even**. A product involving an even factor is even.
    * **Case 2:** $b$ is even. Then $b^2$ is **even**. A product involving an even factor is even.

---

## Discrete Math Study Guide: Chapter 8
### Proofs Involving Sets

To prove $X \subseteq Y$, we use the **Element Method**: pick an arbitrary element $x \in X$ and show that it must also be in $Y$. To prove $X = Y$, show $X \subseteq Y$ and $Y \subseteq X$.

---

### Exercise 8.1: Multiples and Intersections
**Statement:** $\{12n : n \in \mathbb{Z}\} \subseteq \{2n : n \in \mathbb{Z}\} \cap \{3n : n \in \mathbb{Z}\}$
* **Proof:** 1.  Let $x \in \{12n : n \in \mathbb{Z}\}$. This means $x = 12k$ for some integer $k$.
    2.  We can write $x = 2(6k)$. Since $6k \in \mathbb{Z}$, $x$ is a multiple of 2, so $x \in \{2n : n \in \mathbb{Z}\}$.
    3.  We can also write $x = 3(4k)$. Since $4k \in \mathbb{Z}$, $x$ is a multiple of 3, so $x \in \{3n : n \in \mathbb{Z}\}$.
    4.  Since $x$ is in both sets, $x \in \{2n : n \in \mathbb{Z}\} \cap \{3n : n \in \mathbb{Z}\}$.
* **Conclusion:** The subset relation holds.

### Exercise 8.3: Divisor Sets
**Statement:** If $k \in \mathbb{Z}$, then $\{n \in \mathbb{Z} : n \mid k\} \subseteq \{n \in \mathbb{Z} : n \mid k^2\}$
* **Proof:**
    1.  Let $x$ be an arbitrary element in the set of divisors of $k$. This means $x \mid k$.
    2.  By definition of divisibility, $k = xj$ for some integer $j$.
    3.  Square both sides: $k^2 = (xj)^2 = x^2 j^2 = x(xj^2)$.
    4.  Since $xj^2$ is an integer, $x \mid k^2$.
    5.  Therefore, $x \in \{n \in \mathbb{Z} : n \mid k^2\}$.

### Exercise 8.13: DeMorgan’s Law for Sets
**Statement:** $A - (B \cup C) = (A - B) \cap (A - C)$

* **Proof ($\subseteq$):**
    1.  Let $x \in A - (B \cup C)$. By definition, $x \in A$ and $x \notin (B \cup C)$.
    2.  $x \notin (B \cup C)$ means $x$ is not in $B$ **and** $x$ is not in $C$.
    3.  Since $x \in A$ and $x \notin B$, then $x \in (A - B)$.
    4.  Since $x \in A$ and $x \notin C$, then $x \in (A - C)$.
    5.  Therefore, $x \in (A - B) \cap (A - C)$.
* **Proof ($\supseteq$):**
    1.  Let $x \in (A - B) \cap (A - C)$.
    2.  This means $x \in (A - B)$ (so $x \in A$ and $x \notin B$) and $x \in (A - C)$ (so $x \in A$ and $x \notin C$).
    3.  Since $x \notin B$ and $x \notin C$, then $x \notin (B \cup C)$.
    4.  Combined with $x \in A$, we have $x \in A - (B \cup C)$.

### Exercise 8.15: Distribution of Difference over Intersection
**Statement:** $(A \cap B) - C = (A - C) \cap (B - C)$
* **Proof ($\subseteq$):**
    1.  Let $x \in (A \cap B) - C$. Then $x \in (A \cap B)$ and $x \notin C$.
    2.  This means $x \in A, x \in B$, and $x \notin C$.
    3.  Since $x \in A$ and $x \notin C$, $x \in (A - C)$.
    4.  Since $x \in B$ and $x \notin C$, $x \in (B - C)$.
    5.  Thus, $x \in (A - C) \cap (B - C)$.
* **Proof ($\supseteq$):**
    1.  Let $x \in (A - C) \cap (B - C)$.
    2.  Then $x \in (A - C)$ (so $x \in A, x \notin C$) and $x \in (B - C)$ (so $x \in B, x \notin C$).
    3.  Since $x \in A$ and $x \in B$, $x \in (A \cap B)$.
    4.  Since $x \notin C$, we conclude $x \in (A \cap B) - C$.

---

