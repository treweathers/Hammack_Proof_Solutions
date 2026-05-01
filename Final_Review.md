# Finals Prep

## Discrete Math Study Guide: Chapter 2

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
## Discrete Math Study Guide: Chapter 9
### Disproof and Counterexamples

When a statement is universal (e.g., "For every $n$...") and you suspect it's false, you only need **one** specific case where it fails. This is a **counterexample**.

---

### Exercise 9.2: Is it always prime?
**Statement:** For every $n \in \mathbb{N}$, the integer $2n^2 - 4n + 31$ is prime.
* **Assessment:** **False**.
* **Strategy:** Many quadratic formulas like this look prime for small values, but eventually fail. Let's test values.
    * $n=1: 2(1)^2 - 4(1) + 31 = 29$ (Prime)
    * $n=2: 2(4) - 8 + 31 = 31$ (Prime)
    * ... Skip ahead to see if we can make it a multiple of 31. Let $n = 31$.
* **Disproof (Counterexample):** Let $n = 31$.
    * $2(31)^2 - 4(31) + 31 = 31(2 \cdot 31 - 4 + 1) = 31(62 - 4 + 1) = 31(59)$.
    * Since this is a product of two integers greater than 1 ($31 \times 59 = 1829$), the result is composite.
    * **Result:** Disproven.

### Exercise 9.5: Cartesian Product Union
**Statement:** If $A, B, C$ and $D$ are sets, then $(A \times B) \cup (C \times D) = (A \cup C) \times (B \cup D)$.
* **Assessment:** **False**.
* **Visualization:** Think of rectangles on a coordinate plane. The left side is two separate "boxes." The right side is one giant "box" that contains both, plus some extra corners.

* **Disproof (Counterexample):** Let $A=\{1\}, B=\{1\}, C=\{2\}, D=\{2\}$.
    * Left Side: $(A \times B) \cup (C \times D) = \{(1,1)\} \cup \{(2,2)\} = \{(1,1), (2,2)\}$.
    * Right Side: $(A \cup C) \times (B \cup D) = \{1,2\} \times \{1,2\} = \{(1,1), (1,2), (2,1), (2,2)\}$.
    * The pairs $(1,2)$ and $(2,1)$ are in the right side but not the left.
    * **Result:** Disproven.

### Exercise 9.9: Power Sets and Differences
**Statement:** If $A$ and $B$ are sets, then $\mathcal{P}(A) - \mathcal{P}(B) \subseteq \mathcal{P}(A - B)$.
* **Assessment:** **False**.
* **Disproof (Counterexample):** Let $A = \{1, 2\}$ and $B = \{2\}$.
    * $A - B = \{1\}$.
    * $\mathcal{P}(A) = \{\emptyset, \{1\}, \{2\}, \{1, 2\}\}$
    * $\mathcal{P}(B) = \{\emptyset, \{2\}\}$
    * $\mathcal{P}(A) - \mathcal{P}(B) = \{\{1\}, \{1, 2\}\}$.
    * $\mathcal{P}(A - B) = \mathcal{P}(\{1\}) = \{\emptyset, \{1\}\}$.
    * Note that $\{1, 2\} \in (\mathcal{P}(A) - \mathcal{P}(B))$ but $\{1, 2\} \notin \mathcal{P}(A - B)$.
    * **Result:** Disproven.

### Exercise 9.11: Additive vs Multiplicative Growth
**Statement:** If $a, b \in \mathbb{N}$, then $a + b < ab$.
* **Assessment:** **False**.
* **Disproof (Counterexample):** Let $a = 1$ and $b = 1$.
    * $1 + 1 = 2$.
    * $1 \times 1 = 1$.
    * $2 < 1$ is false. (Similarly, if $a=2, b=2$, then $2+2=4$ and $2\times 2=4$. $4 < 4$ is false).
    * **Result:** Disproven.

---

## Discrete Math Study Guide: Chapter 10
### Proof by Induction

Induction is like knocking over a line of dominoes. You prove the first one falls (**Base Case**), and then you prove that if any one domino falls, it will definitely knock over the next one (**Inductive Step**).



---

### Exercise 10.1: Sum of First $n$ Integers
**Statement:** $1 + 2 + 3 + \dots + n = \frac{n^2 + n}{2}$ for every $n \in \mathbb{N}$.
* **Base Case ($n=1$):**
    * LHS: $1$
    * RHS: $\frac{1^2 + 1}{2} = \frac{2}{2} = 1$. Matches.
* **Inductive Step:**
    * Assume $1 + 2 + \dots + k = \frac{k^2 + k}{2}$ for some $k \in \mathbb{N}$.
    * We want to show the formula holds for $k+1$: $(1 + 2 + \dots + k) + (k+1)$.
    * Substitute our assumption: $\frac{k^2 + k}{2} + (k+1)$.
    * Get a common denominator: $\frac{k^2 + k + 2(k+1)}{2} = \frac{k^2 + 3k + 2}{2}$.
    * Factor the numerator: $\frac{(k+1)(k+2)}{2}$.
    * Check target: $\frac{(k+1)^2 + (k+1)}{2} = \frac{k^2 + 2k + 1 + k + 1}{2} = \frac{k^2 + 3k + 2}{2}$.
* **Conclusion:** By induction, the statement is true for all $n \in \mathbb{N}$.

---

### Exercise 10.5: Sum of Powers of 2
**Statement:** $2^1 + 2^2 + \dots + 2^n = 2^{n+1} - 2$.
* **Base Case ($n=1$):**
    * LHS: $2^1 = 2$.
    * RHS: $2^{1+1} - 2 = 4 - 2 = 2$. Matches.
* **Inductive Step:**
    * Assume $\sum_{i=1}^k 2^i = 2^{k+1} - 2$.
    * For $k+1$: $(2^1 + \dots + 2^k) + 2^{k+1}$.
    * Substitute assumption: $(2^{k+1} - 2) + 2^{k+1}$.
    * Combine like terms: $2(2^{k+1}) - 2 = 2^{k+2} - 2$.
    * This matches the formula for $n = k+1$.

---

### Exercise 10.7: Sum of $n(n+2)$
**Statement:** $\sum_{i=1}^n i(i+2) = \frac{n(n+1)(2n+7)}{6}$.
* **Base Case ($n=1$):**
    * LHS: $1(1+2) = 3$.
    * RHS: $\frac{1(2)(9)}{6} = \frac{18}{6} = 3$. Matches.
* **Inductive Step:**
    * Assume $\sum_{i=1}^k i(i+2) = \frac{k(k+1)(2k+7)}{6}$.
    * Add the $(k+1)$ term: $\frac{k(k+1)(2k+7)}{6} + (k+1)(k+3)$.
    * Factor out $(k+1)$: $(k+1) \left[ \frac{2k^2 + 7k + 6k + 18}{6} \right] = (k+1) \left[ \frac{2k^2 + 13k + 18}{6} \right]$.
    * Factor the quadratic: $\frac{(k+1)(k+2)(2k+9)}{6}$.
    * This matches the formula for $n=k+1$ because $2(k+1)+7 = 2k+9$.

---

### Proof of the Binomial Theorem (by Induction)
**Identity:** $(x+y)^n = \sum_{k=0}^n \binom{n}{k} x^{n-k}y^k$.
* **Base Case ($n=1$):** $(x+y)^1 = \binom{1}{0}x^1 y^0 + \binom{1}{1}x^0 y^1 = x+y$. True.
* **Inductive Step:** Assume $(x+y)^k = \sum_{j=0}^k \binom{k}{j} x^{k-j}y^j$.
    * Multiply both sides by $(x+y)$:
    * $(x+y)^{k+1} = x \sum \binom{k}{j} x^{k-j}y^j + y \sum \binom{k}{j} x^{k-j}y^j$.
    * Distribute: $\sum \binom{k}{j} x^{k+1-j}y^j + \sum \binom{k}{j} x^{k-j}y^{j+1}$.
    * After shifting the index on the second sum and grouping terms with the same powers ($x^{k+1-j}y^j$), the coefficients become $\binom{k}{j} + \binom{k}{j-1}$.
    * By **Pascal’s Rule**, $\binom{k}{j} + \binom{k}{j-1} = \binom{k+1}{j}$.
* **Result:** This results exactly in the expansion for $(x+y)^{k+1}$.

---

Don't let the "scary" labels get to you! Relations are just a way of pairing things up. Think of a relation $R$ on a set $A$ as a collection of arrows pointing from one element to another. 

To master these, you just need to check three "pass/fail" tests:
1.  **Reflexive:** Does every element point to itself? ($aRa$ for all $a$)
2.  **Symmetric:** If $a \to b$, is there a $b \to a$?
3.  **Transitive:** If $a \to b$ and $b \to c$, is there a shortcut $a \to c$?

---

## Discrete Math Study Guide: Chapter 11

## Section 11.2: Relations

### Exercise 11.2.3: Small Finite Set
**Relation:** $R = \{(a, b), (a, c), (c, b), (b, c)\}$ on $A = \{a, b, c\}$.
* **Reflexive?** **No.** For $R$ to be reflexive, it must contain $(a, a), (b, b),$ and $(c, c)$. It contains none of these.
* **Symmetric?** **No.** While it has $(c, b)$ and $(b, c)$, it has $(a, b)$ but **not** $(b, a)$.
* **Transitive?** **No.** We have $(a, b)$ and $(b, c)$. For it to be transitive, we need the "shortcut" $(a, c)$. While $(a, c)$ is actually there, let's check another: we have $(a, c)$ and $(c, b)$. We need $(a, b)$, which is also there. Wait, check $(b, c)$ and $(c, b)$—we would need $(b, b)$, which is **missing**.
* **Result:** None of the three.

### Exercise 11.2.5: The Small Coordinate Set
**Relation:** $R = \{(0, 0), (\sqrt{2}, 0), (0, \sqrt{2}), (\sqrt{2}, \sqrt{2})\}$ on $\mathbb{R}$.
* **Reflexive?** **No.** To be reflexive on $\mathbb{R}$, every real number $x$ must satisfy $xRx$ (e.g., $(1, 1)$ must be there). This relation only has loops for $0$ and $\sqrt{2}$.
* **Symmetric?** **Yes.** * $(0, 0)$ and $(\sqrt{2}, \sqrt{2})$ are their own reverses.
    * The pair $(\sqrt{2}, 0)$ has its reverse $(0, \sqrt{2})$ present.
* **Transitive?** **Yes.** All paths like $(\sqrt{2} \to 0 \to \sqrt{2})$ have their shortcuts $(\sqrt{2} \to \sqrt{2})$ present.
* **Result:** Symmetric and Transitive only.

### Exercise 11.2.9: Parity Relation
**Relation:** $xRy$ iff $x$ and $y$ have the same parity (both even or both odd) on $\mathbb{Z}$.
* **Reflexive?** **Yes.** Any integer $x$ has the same parity as itself.
* **Symmetric?** **Yes.** If $x$ and $y$ have the same parity, then $y$ and $x$ have the same parity.
* **Transitive?** **Yes.** If $x, y$ are both even and $y, z$ are both even, then $x, z$ are both even. (Same works for odd).
* **What familiar relation is this?** This is **Congruence Modulo 2** ($x \equiv y \pmod 2$).

### Exercise 11.2.13: Difference is an Integer
**Relation:** $R = \{(x, y) \in \mathbb{R} \times \mathbb{R} : x - y \in \mathbb{Z}\}$ on $\mathbb{R}$.

* **Reflexive:** Let $x \in \mathbb{R}$. Then $x - x = 0$. Since $0 \in \mathbb{Z}$, $xRx$ is true.
* **Symmetric:** Suppose $xRy$. Then $x - y = k$ for some $k \in \mathbb{Z}$.
    * Then $y - x = -(x - y) = -k$.
    * Since $k$ is an integer, $-k$ is also an integer. Thus $yRx$.
* **Transitive:** Suppose $xRy$ and $yRz$.
    * Then $x - y = k$ and $y - z = m$ for some $k, m \in \mathbb{Z}$.
    * Add the equations: $(x - y) + (y - z) = k + m$.
    * $x - z = k + m$.
    * Since the sum of two integers is an integer, $xRz$.
* **Result:** It is an **Equivalence Relation** (it passed all three tests!).

---

Equivalence classes are basically "clubs" where every member is related to every other member. If a relation is an **Equivalence Relation** (Reflexive, Symmetric, and Transitive), it partitions the set into these disjoint clubs.

---

## Section 11.3: Equivalence Relations & Classes

### Exercise 11.3.5: Relations on $A = \{a, b\}$
There are two ways to group $\{a, b\}$ such that the rules of equivalence are followed:
1.  **The Identity Relation:** Each element is only in a club with itself.
    * $R_1 = \{(a, a), (b, b)\}$.
    * Classes: $[a] = \{a\}$, $[b] = \{b\}$.
2.  **The Universal Relation:** Everyone is related to everyone.
    * $R_2 = \{(a, a), (b, b), (a, b), (b, a)\}$.
    * Class: $[a] = \{a, b\}$.



---

### Exercise 11.3.7: $3x - 5y$ is even
**Relation:** $xRy \iff 3x - 5y = 2k$ for some $k \in \mathbb{Z}$.
* **Reflexive:** $3x - 5x = -2x = 2(-x)$. Since $-x \in \mathbb{Z}$, $xRx$.
* **Symmetric:** Suppose $3x - 5y = 2k$. We want to see if $3y - 5x$ is even.
    * $(3y - 5x) + (3x - 5y) = -2x - 2y = 2(-x - y)$.
    * Since the sum and one term are even, the other term $(3y - 5x)$ must be even.
* **Transitive:** Suppose $3x - 5y = 2k$ and $3y - 5z = 2m$.
    * Add them: $3x - 2y - 5z = 2k + 2m$.
    * $3x - 5z = 2k + 2m + 2y = 2(k + m + y)$. Even!
* **Equivalence Classes:** * If $x$ is even, $3(\text{even}) - 5y = \text{even} \implies y$ must be even.
    * If $x$ is odd, $3(\text{odd}) - 5y = \text{even} \implies y$ must be odd.
    * **Classes:** The set of even integers $\mathbb{E}$ and the set of odd integers $\mathbb{O}$.

---

### Exercise 11.3.9: $4 \mid (x + 3y)$
**Relation:** $xRy \iff x + 3y = 4k$.
* **Reflexive:** $x + 3x = 4x$. Clearly $4 \mid 4x$.
* **Symmetric:** Suppose $x + 3y = 4k$. Then $x = 4k - 3y$.
    * Check $y + 3x$: $y + 3(4k - 3y) = y + 12k - 9y = 12k - 8y = 4(3k - 2y)$.
    * Divisible by 4. $yRx$.
* **Transitive:** Suppose $x + 3y = 4k$ and $y + 3z = 4m$.
    * Add them: $x + 4y + 3z = 4(k + m)$.
    * $x + 3z = 4(k + m - y)$. Divisible by 4.
* **Equivalence Classes:** This is actually just **Congruence Modulo 4**.
    * $x + 3y \equiv 0 \pmod 4 \implies x \equiv -3y \equiv y \pmod 4$.
    * **Classes:** $\{ [0], [1], [2], [3] \}$ (remainders when divided by 4).

---

### Exercise 11.3.11: Infinite set, Infinite classes?
**Statement:** If $R$ is an equivalence relation on an infinite set $A$, then $R$ has infinitely many equivalence classes.
* **Assessment:** **False.**
* **Disproof (Counterexample):** Let $A = \mathbb{Z}$ (an infinite set). Define $xRy$ if $x$ and $y$ have the same parity (Exercise 11.2.9).
    * $A$ is infinite.
    * $R$ is an equivalence relation.
    * However, there are only **two** equivalence classes: $[0]$ (evens) and $[1]$ (odds).
    * Two is not infinite.

---

Equivalence classes are basically "clubs" where every member is related to every other member. If a relation is an **Equivalence Relation** (Reflexive, Symmetric, and Transitive), it partitions the set into these disjoint clubs.

---

## Section 11.3: Equivalence Relations & Classes

### Exercise 11.3.5: Relations on $A = \{a, b\}$
There are two ways to group $\{a, b\}$ such that the rules of equivalence are followed:
1.  **The Identity Relation:** Each element is only in a club with itself.
    * $R_1 = \{(a, a), (b, b)\}$.
    * Classes: $[a] = \{a\}$, $[b] = \{b\}$.
2.  **The Universal Relation:** Everyone is related to everyone.
    * $R_2 = \{(a, a), (b, b), (a, b), (b, a)\}$.
    * Class: $[a] = \{a, b\}$.



---

### Exercise 11.3.7: $3x - 5y$ is even
**Relation:** $xRy \iff 3x - 5y = 2k$ for some $k \in \mathbb{Z}$.
* **Reflexive:** $3x - 5x = -2x = 2(-x)$. Since $-x \in \mathbb{Z}$, $xRx$.
* **Symmetric:** Suppose $3x - 5y = 2k$. We want to see if $3y - 5x$ is even.
    * $(3y - 5x) + (3x - 5y) = -2x - 2y = 2(-x - y)$.
    * Since the sum and one term are even, the other term $(3y - 5x)$ must be even.
* **Transitive:** Suppose $3x - 5y = 2k$ and $3y - 5z = 2m$.
    * Add them: $3x - 2y - 5z = 2k + 2m$.
    * $3x - 5z = 2k + 2m + 2y = 2(k + m + y)$. Even!
* **Equivalence Classes:** * If $x$ is even, $3(\text{even}) - 5y = \text{even} \implies y$ must be even.
    * If $x$ is odd, $3(\text{odd}) - 5y = \text{even} \implies y$ must be odd.
    * **Classes:** The set of even integers $\mathbb{E}$ and the set of odd integers $\mathbb{O}$.

---

### Exercise 11.3.9: $4 \mid (x + 3y)$
**Relation:** $xRy \iff x + 3y = 4k$.
* **Reflexive:** $x + 3x = 4x$. Clearly $4 \mid 4x$.
* **Symmetric:** Suppose $x + 3y = 4k$. Then $x = 4k - 3y$.
    * Check $y + 3x$: $y + 3(4k - 3y) = y + 12k - 9y = 12k - 8y = 4(3k - 2y)$.
    * Divisible by 4. $yRx$.
* **Transitive:** Suppose $x + 3y = 4k$ and $y + 3z = 4m$.
    * Add them: $x + 4y + 3z = 4(k + m)$.
    * $x + 3z = 4(k + m - y)$. Divisible by 4.
* **Equivalence Classes:** This is actually just **Congruence Modulo 4**.
    * $x + 3y \equiv 0 \pmod 4 \implies x \equiv -3y \equiv y \pmod 4$.
    * **Classes:** $\{ [0], [1], [2], [3] \}$ (remainders when divided by 4).

---

### Exercise 11.3.11: Infinite set, Infinite classes?
**Statement:** If $R$ is an equivalence relation on an infinite set $A$, then $R$ has infinitely many equivalence classes.
* **Assessment:** **False.**
* **Disproof (Counterexample):** Let $A = \mathbb{Z}$ (an infinite set). Define $xRy$ if $x$ and $y$ have the same parity (Exercise 11.2.9).
    * $A$ is infinite.
    * $R$ is an equivalence relation.
    * However, there are only **two** equivalence classes: $[0]$ (evens) and $[1]$ (odds).
    * Two is not infinite.

---
No problem! Let’s hit the reset button on Section 12.2 and use these specific problems. This is a critical section because "bijective" is the gold standard for comparing the sizes of infinite sets later (Chapter 14).

---

## Discrete Math Study Guide: Chapter 12
### Injective, Surjective, and Bijective Functions

**The Cheat Sheet:**
* **Injective (1-to-1):** Every input has a *unique* output. 
    * *Test:* Assume $f(x) = f(y)$. If you can prove $x = y$, it’s injective.
* **Surjective (Onto):** Every element in the codomain (target set) is "hit" by at least one input.
    * *Test:* Pick an arbitrary $y$ in the codomain. Can you find an $x$ in the domain such that $f(x) = y$?
* **Bijective:** Both Injective AND Surjective.

---

### Exercise 12.2.5: The Linear Integer Function
**Function:** $f: \mathbb{Z} \to \mathbb{Z}$ defined by $f(n) = 2n + 1$.

* **Injective?** **Yes.**
    * Assume $f(n_1) = f(n_2)$.
    * $2n_1 + 1 = 2n_2 + 1$.
    * Subtract 1: $2n_1 = 2n_2$.
    * Divide by 2: $n_1 = n_2$.
* **Surjective?** **No.**
    * The codomain is $\mathbb{Z}$ (all integers).
    * However, $2n+1$ is the definition of an **odd** integer.
    * There is no integer $n$ that will output an even number (like $2$). 
    * *Example:* If $2n+1 = 2$, then $2n = 1$, so $n = 0.5$, which is not in the domain $\mathbb{Z}$.

---

### Exercise 12.2.7: Mapping Pairs to Integers
**Function:** $f: \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}$ defined by $f(m, n) = 2n - 4m$.

* **Injective?** **No.**
    * We need two different pairs $(m, n)$ that give the same result.
    * Let $(m, n) = (1, 2) \implies f(1, 2) = 2(2) - 4(1) = 0$.
    * Let $(m, n) = (2, 4) \implies f(2, 4) = 2(4) - 4(2) = 0$.
    * Since $(1, 2) \neq (2, 4)$ but $f(1, 2) = f(2, 4)$, it is not injective.
* **Surjective?** **No.**
    * Notice $2n - 4m = 2(n - 2m)$.
    * This result is always **even** because it's a multiple of 2.
    * You can never get an odd integer (like $1$) as an output.

---

### Exercise 12.2.9: Proving a Bijection (Rational Function)
**Function:** $f: \mathbb{R} - \{2\} \to \mathbb{R} - \{5\}$ defined by $f(x) = \frac{5x+1}{x-2}$.

* **Proof of Injective:**
    * Assume $f(a) = f(b)$: $\frac{5a+1}{a-2} = \frac{5b+1}{b-2}$.
    * Cross-multiply: $(5a+1)(b-2) = (5b+1)(a-2)$.
    * Expand: $5ab - 10a + b - 2 = 5ab - 10b + a - 2$.
    * Cancel $5ab$ and $-2$: $-10a + b = -10b + a$.
    * Rearrange: $11b = 11a \implies a = b$. **Injective!**
* **Proof of Surjective:**
    * Let $y \in \mathbb{R} - \{5\}$. Solve $y = \frac{5x+1}{x-2}$ for $x$.
    * $y(x-2) = 5x + 1 \implies yx - 2y = 5x + 1$.
    * $yx - 5x = 2y + 1 \implies x(y-5) = 2y + 1$.
    * $x = \frac{2y+1}{y-5}$.
    * Since $y \neq 5$, this fraction is always defined. Since $x$ is a real number (and you can check $x \neq 2$), every $y$ has an $x$. **Surjective!**
* **Conclusion:** Since it is both, it is **bijective**.



---

### Exercise 12.2.11: The Signed Natural Numbers
**Function:** $\theta: \{0, 1\} \times \mathbb{N} \to \mathbb{Z}$ defined by $\theta(a, b) = (-1)^a b$.
*Note: The domain is pairs where the first item is 0 or 1, and the second is a positive integer $\{1, 2, 3, \dots\}$.*

* **Injective?** **Yes.**
    * If $a=0$, the output is $(1)b = b$ (positive integers).
    * If $a=1$, the output is $(-1)b = -b$ (negative integers).
    * Since positive and negative integers never overlap, and each $b$ is unique, no two pairs $(a, b)$ can produce the same result.
* **Surjective?** **No.**
    * The codomain is $\mathbb{Z}$ (all integers, including zero).
    * Can we ever get $0$? 
    * $(-1)^a b = 0$ would require $b=0$. But $b \in \mathbb{N}$, and the set of natural numbers (in most textbooks for this course) starts at $1$. 
    * Zero is never hit.
* **Bijective?** **No**, because it failed surjectivity.

---

Inverse functions are all about "undoing" the mapping. If a function $f$ takes $x$ to $y$, the inverse $f^{-1}$ must take that $y$ right back to $x$. 

**Crucial Rule:** A function has an inverse **if and only if** it is bijective.

---

## Section 12.5: Inverse Functions

### Exercise 12.5.1: Linear Integer Inverse
**Function:** $f: \mathbb{Z} \to \mathbb{Z}, f(n) = 6 - n$.

* **Check Bijective:**
    * **Injective:** $6 - n_1 = 6 - n_2 \implies -n_1 = -n_2 \implies n_1 = n_2$. (Yes)
    * **Surjective:** Let $y \in \mathbb{Z}$. Solve $y = 6 - n$ for $n$. We get $n = 6 - y$. Since $y$ is an integer, $6-y$ is an integer. (Yes)
* **Find $f^{-1}(n)$:**
    * Set $y = 6 - n$.
    * Solve for $n$: $n = 6 - y$.
    * **Result:** $f^{-1}(n) = 6 - n$. (This function is its own inverse!)

---

### Exercise 12.5.6: Systems of Equations in $\mathbb{Z} \times \mathbb{Z}$
**Function:** $f(m, n) = (5m + 4n, 4m + 3n)$.

* **Strategy:** Set $(x, y) = (5m + 4n, 4m + 3n)$ and solve for $m$ and $n$ in terms of $x$ and $y$.
* **Equations:**
    1. $5m + 4n = x$
    2. $4m + 3n = y$
* **Solve:**
    * Multiply (1) by 3 and (2) by 4:
        * $15m + 12n = 3x$
        * $16m + 12n = 4y$
    * Subtract the first from the second: $(16m - 15m) = 4y - 3x \implies \mathbf{m = 4y - 3x}$.
    * Substitute $m$ into (2): $4(4y - 3x) + 3n = y \implies 16y - 12x + 3n = y$.
    * $3n = 12x - 15y \implies \mathbf{n = 4x - 5y}$.
* **Result:** $f^{-1}(x, y) = (4y - 3x, 4x - 5y)$.

---

### Exercise 12.5.7: Non-linear Bijection on $\mathbb{R}^2$
**Function:** $f(x, y) = ((x^2 + 1)y, x^3)$.

* **Check Bijective:**
    * If $f(x_1, y_1) = f(x_2, y_2)$, then $x_1^3 = x_2^3 \implies x_1 = x_2$.
    * Then $(x_1^2 + 1)y_1 = (x_1^2 + 1)y_2$. Since $x^2+1$ is never zero, we divide to get $y_1 = y_2$. (Injective!)
    * For any $(a, b)$, we can find $x = \sqrt[3]{b}$ and $y = \frac{a}{x^2+1}$. (Surjective!)
* **Find Inverse:**
    * $x^3 = y_{out} \implies x = \sqrt[3]{y_{out}}$.
    * $(x^2 + 1)y_{in} = x_{out} \implies y_{in} = \frac{x_{out}}{x^2 + 1} = \frac{x_{out}}{(\sqrt[3]{y_{out}})^2 + 1}$.
* **Result:** $f^{-1}(x, y) = \left( \frac{x}{\sqrt[3]{y^2} + 1}, \sqrt[3]{y} \right)$.

---

### Exercise 12.5.9: Swapping Domains
**Function:** $f: \mathbb{R} \times \mathbb{N} \to \mathbb{N} \times \mathbb{R}$ defined as $f(x, y) = (y, 3xy)$.
*Note: $y$ must be a natural number.*

* **Check Bijective:**
    * Assume $f(x_1, y_1) = f(x_2, y_2)$. Then $y_1 = y_2$.
    * Then $3x_1y_1 = 3x_2y_2$. Since $y_1 \in \mathbb{N}$ (so $y_1 \ge 1$), we can divide by $3y_1$. $x_1 = x_2$. (Injective!)
    * For any $(n, r) \in \mathbb{N} \times \mathbb{R}$, set $y = n$ and $3xn = r \implies x = \frac{r}{3n}$. (Surjective!)
* **Find Inverse:**
    * Let the output be $(a, b)$ where $a \in \mathbb{N}$ and $b \in \mathbb{R}$.
    * $y = a$.
    * $3xy = b \implies 3xa = b \implies x = \frac{b}{3a}$.
* **Result:** $f^{-1}(a, b) = \left( \frac{b}{3a}, a \right)$.

---

## Discrete Math Study Guide: Chapter 14
This is where discrete math starts to feel like magic. We are moving from "counting" to "measuring the size of infinity."

**The Golden Rule of Cardinality:** Two sets have the same size ($|A| = |B|$) if and only if there exists a **bijection** between them. If you can pair every element up with no one left over, the sets are the same size—even if one seems "bigger" at first glance.

---

## 1. Landmark Proofs of Cardinality

### Proof: $|\mathbb{N}| = |\mathbb{Z}|$
* **The Problem:** $\mathbb{Z}$ looks twice as big because it has negative numbers.
* **The Solution:** We "zigzag" through the integers.
    * Map $1 \to 0$
    * Map $2 \to 1$
    * Map $3 \to -1$
    * Map $4 \to 2$
    * Map $5 \to -2$
* **The Bijection:**
    $$f(n) = \begin{cases} \frac{n}{2} & \text{if } n \text{ is even} \\ -\frac{n-1}{2} & \text{if } n \text{ is odd} \end{cases}$$
* This formula hits every integer exactly once. Thus, they are the same size.

### Proof: $|\mathbb{R}| = |(0, 1)|$
* **The Problem:** How can an infinite line be the same size as a tiny segment?
* **The Solution:** Use a tangent function. 
* **The Bijection:** $f:(0, 1) \to \mathbb{R}$ defined by $f(x) = \tan(\pi x - \frac{\pi}{2})$.
    * As $x \to 0$, $f(x) \to -\infty$.
    * As $x \to 1$, $f(x) \to \infty$.
* Since the tangent function is a bijection over this interval, the sets have equal cardinality.



### Proof: $|\mathbb{N}| \neq |\mathbb{R}|$ (Cantor's Diagonal Argument)
* **The Method:** Contradiction.
* **Assume False:** Suppose we *could* list all real numbers between 0 and 1 in a list: $r_1, r_2, r_3, \dots$
* **Construct a "Monster":** Create a new decimal $x = 0.d_1 d_2 d_3 \dots$ where $d_1$ is different from the first digit of $r_1$, $d_2$ is different from the second digit of $r_2$, and so on.
* **The Contradiction:** This new number $x$ cannot be in the list because it differs from every single $r_n$ by at least one digit. 
* **Conclusion:** $\mathbb{R}$ is "uncountably" infinite. It is a bigger level of infinity than $\mathbb{N}$.

---

## 2. Section 14.1 Exercises

**Exercise 14.1.5: Multiples of 3 vs Multiples of 7**
* **Sets:** $A = \{3k : k \in \mathbb{Z}\}$ and $B = \{7k : k \in \mathbb{Z}\}$.
* **Bijection:** To turn a $3k$ into a $7k$, we first "undo" the 3 and then "apply" the 7.
* **Formula:** $f: A \to B$ defined by $f(x) = \frac{7}{3}x$.
* **Verification:** If $x = 3k$, then $f(3k) = \frac{7}{3}(3k) = 7k$, which is in $B$. Since it's a linear function, it's a bijection.

**Exercise 14.1.9: $\{0, 1\} \times \mathbb{N}$ and $\mathbb{N}$**
* **Sets:** The domain is pairs like $(0, 1), (0, 2), \dots$ and $(1, 1), (1, 2), \dots$.
* **Strategy:** Map the $(0, n)$ pairs to odd numbers and the $(1, n)$ pairs to even numbers.
* **Formula:** $f: \{0, 1\} \times \mathbb{N} \to \mathbb{N}$ defined by:
    $$f(a, n) = 2n - a$$
    * If $a=0$: $f(0, n) = 2n$ (all even numbers).
    * If $a=1$: $f(1, n) = 2n - 1$ (all odd numbers).
* **Result:** Every natural number is covered exactly once.

**Exercise 14.1.13: $\mathcal{P}(\mathbb{N})$ and $\mathcal{P}(\mathbb{Z})$**
* **Strategy:** We already know a bijection $g: \mathbb{N} \to \mathbb{Z}$ exists (from the zigzag proof above).
* **Bijection:** To map a subset $S \subseteq \mathbb{N}$ to a subset of $\mathbb{Z}$, simply apply $g$ to every element in $S$.
* **Formula:** $f: \mathcal{P}(\mathbb{N}) \to \mathcal{P}(\mathbb{Z})$ defined by $f(S) = \{g(n) : n \in S\}$.
* **Result:** Since $g$ is a bijection, this "lifting" to power sets is also a bijection.

---

You made it to the final boss! Let’s wrap this up.


## 1. Landmark Proofs: Countability

### Proof: $\mathbb{Q}$ (The Rationals) is Countable
* **The Problem:** Between any two integers, there are infinitely many fractions. How can we list them?
* **The Strategy:** Arrange all fractions $\frac{a}{b}$ in a grid where the numerator increases horizontally and the denominator increases vertically.
* **The Method:** "Snake" through the grid diagonally. Start at $\frac{1}{1}$, then $\frac{2}{1}, \frac{1}{2}$, then $\frac{1}{3}, \frac{2}{2}, \frac{3}{1}$, and so on. Skip any fraction that isn't in simplest form (like $\frac{2}{2}$ or $\frac{4}{2}$).
* **Conclusion:** Since every possible fraction appears somewhere in this grid and our "snake" path eventually hits every spot, we can assign each fraction a natural number ($1, 2, 3, \dots$). Thus, $\mathbb{Q}$ is countable.


### Proof: $\mathbb{R}$ (The Reals) is Uncountable
* **The Method:** Cantor's Diagonal Argument (as summarized in the previous section).
* **Key Insight:** No matter how you try to list real numbers, you can always construct a new real number that isn't on your list by changing the diagonal digits. 
* **Conclusion:** $|\mathbb{R}| > |\mathbb{N}|$.

---

## 2. Section 14.2 Exercises

### Exercise 14.2.3: Ordered Pairs of Integers
**Statement:** Prove $A = \{(5n, -3n) : n \in \mathbb{Z}\}$ is countably infinite.
* **Proof:** 1. Define a function $f: \mathbb{Z} \to A$ by $f(n) = (5n, -3n)$.
    2. This function is clearly a bijection (each $n$ gives a unique pair, and every pair in $A$ is generated by an $n$).
    3. We already proved in Chapter 14.1 that $\mathbb{Z}$ is countably infinite (because there is a bijection $g: \mathbb{N} \to \mathbb{Z}$).
    4. Since a bijection exists from $\mathbb{N}$ to $\mathbb{Z}$, and from $\mathbb{Z}$ to $A$, the composition $f \circ g$ is a bijection from $\mathbb{N}$ to $A$.
* **Conclusion:** $A$ is countably infinite.

### Exercise 14.2.5: Subset of Irrationals
**Statement:** Prove or disprove: There exists a countably infinite subset of the set of irrational numbers.
* **Assessment:** **True.**
* **Proof:** Consider the set $S = \{\sqrt{2} \cdot n : n \in \mathbb{N}\}$. 
    * Since $\sqrt{2}$ is irrational, $\sqrt{2}, 2\sqrt{2}, 3\sqrt{2}, \dots$ are all irrational.
    * The function $f: \mathbb{N} \to S$ defined by $f(n) = \sqrt{2}n$ is a bijection.
* **Conclusion:** $S$ is a countably infinite subset of the irrationals.

### Exercise 14.2.9: $\{0, 1\} \times \mathbb{N}$
**Statement:** Prove or disprove: The set $\{0, 1\} \times \mathbb{N}$ is countably infinite.
* **Assessment:** **True.**
* **Proof:** We literally found the bijection for this in Exercise 14.1.9! 
    * The function $f(a, n) = 2n - a$ maps $\{0, 1\} \times \mathbb{N}$ to $\mathbb{N}$ bijectively.
* **Conclusion:** Since a bijection to $\mathbb{N}$ exists, it is countably infinite by definition.

### Exercise 14.2.15: The Fundamental Theorem of Arithmetic Approach
**Statement:** Show $\phi: \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ defined as $\phi(m, n) = 2^{n-1}(2m - 1)$ is bijective.
* **Proof of Injective:**
    * Assume $\phi(m_1, n_1) = \phi(m_2, n_2) \implies 2^{n_1-1}(2m_1 - 1) = 2^{n_2-1}(2m_2 - 1)$.
    * By the **Unique Factorization Theorem**, every integer has a unique representation as a power of 2 times an odd number.
    * The power of 2 must match: $n_1 - 1 = n_2 - 1 \implies n_1 = n_2$.
    * The odd part must match: $2m_1 - 1 = 2m_2 - 1 \implies m_1 = m_2$.
* **Proof of Surjective:**
    * Pick any $x \in \mathbb{N}$. Every natural number $x$ can be factored into its prime components.
    * Pull out all the 2s. Let $x = 2^k \cdot \text{odd}$.
    * Set $n - 1 = k \implies n = k + 1$.
    * Set $2m - 1 = \text{odd} \implies m = \frac{\text{odd} + 1}{2}$.
    * Since $n$ and $m$ will always be natural numbers, every $x$ is covered.
* **Conclusion:** $\phi$ is a bijection, so $\mathbb{N} \times \mathbb{N}$ is countably infinite.

---

**WE ARE FINISHED.** 57 problems, 16 chapters, and one massive master plan. You have the logic, you have the patterns, and you have the proofs. 

Go crush that final. You’ve got this! 🎓🔥


