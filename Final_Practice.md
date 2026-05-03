# Set 1
That’s the spirit! Let's get these graded. Below are the step-by-step solutions for the 16 problems, using the exact logic and "Conclusion" phrasing your professor provided in the guide.

---

### **(1) Section 1: Truth Tables**
**Problem:** Use a truth table to determine if $(P \implies Q) \equiv (\sim Q \implies \sim P)$.

| $P$ | $Q$ | $\sim P$ | $\sim Q$ | $P \implies Q$ | $\sim Q \implies \sim P$ |
| :--- | :--- | :--- | :--- | :--- | :--- |
| T | T | F | F | **T** | **T** |
| T | F | F | T | **F** | **F** |
| F | T | T | F | **T** | **T** |
| F | F | T | T | **T** | **T** |

**Conclusion:** The columns match exactly. The statement is logically equivalent. (This is the Law of Contrapositive).

---

### **(2) Section 2: Negating Statements**
**Problem:** Negate: For every positive number $a$, there exists a positive number $b$ such that $x^2 < b$ whenever $|x| < a$.
**Symbolic Form:** $\forall a > 0, \exists b > 0, (|x| < a) \implies (x^2 < b)$
**Negation Steps:**
1. Flip $\forall a$ to $\exists a$.
2. Flip $\exists b$ to $\forall b$.
3. Negate the implication $(P \implies Q)$ to $(P \wedge \sim Q)$.
**Answer:** There exists a positive number $a$ such that for every positive number $b$, $|x| < a$ and $x^2 \ge b$.

---

### **(3) Section 3: Counting Problems**
**Problem:** How many permutations of the letters $\{A, B, C, D, E, F, G, H\}$ contain the consecutive block $“BDE”$?
**Strategy:** Treat $[BDE]$ as a single super-letter.
**Solution:** Instead of 8 letters, we have the set: $\{[BDE], A, C, F, G, H\}$. This set has 6 items.
**Result:** $6! = 720$.

---

### **(4) Section 4: Binomial Theorem**
**Problem:** Show that $\binom{n}{0} + \binom{n}{1} + \dots + \binom{n}{n} = 2^n$ using the Binomial Theorem.
**Solution:** The Binomial Theorem states $(1 + x)^n = \sum_{k=0}^{n} \binom{n}{k} x^k$.
Let $x = 1$.
$(1 + 1)^n = \binom{n}{0}(1)^0 + \binom{n}{1}(1)^1 + \dots + \binom{n}{n}(1)^n$.
**Result:** $2^n = \binom{n}{0} + \binom{n}{1} + \dots + \binom{n}{n}$.

---

### **(5) Section 5: Direct / Contrapositive Proofs**
**Problem:** Suppose $x \in \mathbb{Z}$. If $x^2 - 1$ is odd, then $x$ is even.
**Method:** Contrapositive.
**Assume $\sim Q$:** Suppose $x$ is odd. Then $x = 2k + 1$ for some $k \in \mathbb{Z}$.
**Proof:** $x^2 - 1 = (2k + 1)^2 - 1 = (4k^2 + 4k + 1) - 1 = 4k^2 + 4k = 2(2k^2 + 2k)$.
**Conclusion:** Since $x^2 - 1 = 2j$, it is even. By contrapositive, if $x^2 - 1$ is odd, then $x$ is even.

---

### **(6) Section 6: Proof by Contradiction**
**Problem:** Prove for every $n \in \mathbb{Z}$, $4 \nmid (n^2 + 1)$.
**Assume False:** Suppose $4 \mid (n^2 + 1)$. Then $n^2 + 1 = 4k$, so $n^2 = 4k - 1$.
**Analyze Modulo 4:** $n^2 \equiv -1 \equiv 3 \pmod 4$.
**Contradiction:** A square $n^2 \pmod 4$ can only be $0$ or $1$. It can never be $3$. Contradiction.

---

### **(7) Section 7: IFF Statements**
**Problem:** $a$ is even iff $a^2$ is even.
**Forward ($\implies$):** Assume $a$ is even ($a=2k$). Then $a^2 = (2k)^2 = 4k^2 = 2(2k^2)$, which is even.
**Backward ($\impliedby$):** Assume $a^2$ is even. Use contrapositive: Suppose $a$ is odd ($a=2k+1$). Then $a^2 = (2k+1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1$, which is odd. Contrapositive proven.

---

### **(8) Section 8: Proofs Involving Sets**
**Problem:** Prove $A - (B \cap C) = (A - B) \cup (A - C)$.
**Proof ($\subseteq$):** Let $x \in A - (B \cap C)$. Then $x \in A$ and $x \notin (B \cap C)$. Since $x \notin (B \cap C)$, $x \notin B$ or $x \notin C$. If $x \notin B$, then $x \in A - B$. If $x \notin C$, then $x \in A - C$. Thus $x \in (A-B) \cup (A-C)$.
**Proof ($\supseteq$):** Let $x \in (A - B) \cup (A - C)$. Then ($x \in A$ and $x \notin B$) OR ($x \in A$ and $x \notin C$). In either case, $x \in A$. Also, $x$ is missing from at least one of $B$ or $C$, so $x \notin (B \cap C)$. Thus $x \in A - (B \cap C)$.

---

### **(9) Section 9: Disproof / Counterexamples**
**Problem:** Disprove $(A \times B) - (C \times D) = (A - C) \times (B - D)$.
**Counterexample:** Let $A=\{1, 2\}, B=\{1, 2\}, C=\{1\}, D=\{2\}$.
**LHS:** $(A \times B) = \{(1,1), (1,2), (2,1), (2,2)\}$. $(C \times D) = \{(1,2)\}$.
LHS = $\{(1,1), (2,1), (2,2)\}$.
**RHS:** $(A-C)=\{2\}$, $(B-D)=\{1\}$. RHS = $\{(2,1)\}$.
**Result:** LHS $\neq$ RHS. Disproven.

---

### **(10) Section 10: Proof by Induction**
**Problem:** $1^3 + 2^3 + \dots + n^3 = (\frac{n(n+1)}{2})^2$.
**Base Case ($n=1$):** LHS $= 1^3 = 1$. RHS $= (\frac{1(2)}{2})^2 = 1^2 = 1$. Matches.
**Inductive Step:** Assume $P(k)$ is true. For $k+1$:
$(\frac{k(k+1)}{2})^2 + (k+1)^3 = \frac{k^2(k+1)^2}{4} + \frac{4(k+1)^3}{4} = \frac{(k+1)^2 [k^2 + 4k + 4]}{4} = \frac{(k+1)^2(k+2)^2}{4} = (\frac{(k+1)(k+2)}{2})^2$. Matches target.

---

### **(11) Section 11: Relations**
**Problem:** $xRy \iff x - y \in \mathbb{Q}$ on $\mathbb{R}$.
**Reflexive:** $x-x=0 \in \mathbb{Q}$. Yes.
**Symmetric:** If $x-y=q$, then $y-x=-q$. Since $q \in \mathbb{Q}$, $-q \in \mathbb{Q}$. Yes.
**Transitive:** If $x-y=q_1$ and $y-z=q_2$, then $(x-y)+(y-z)=q_1+q_2$. Sum of rationals is rational. Yes.

---

### **(12) Section 12: Equivalence Classes**
**Problem:** $xRy \iff 3x - 7y$ is even on $\mathbb{Z}$.
**Equivalence Classes:** This relation simplifies to $x \equiv y \pmod 2$.
$3x - 7y \equiv x - y \pmod 2$. If $x-y$ is even, $x$ and $y$ have the same parity.
**Classes:** $[0] = \mathbb{E}$ (evens), $[1] = \mathbb{O}$ (odds).

---

### **(13) Section 13: Injective/Surjective**
**Problem:** $f: \mathbb{Z} \to \mathbb{Z}, f(n) = 3n - 1$.
**Injective:** $3n_1 - 1 = 3n_2 - 1 \implies 3n_1 = 3n_2 \implies n_1 = n_2$. Yes.
**Surjective:** Let $y = 2$. $3n - 1 = 2 \implies 3n = 3 \implies n = 1$.
Wait, let $y = 1$. $3n - 1 = 1 \implies 3n = 2 \implies n = 2/3 \notin \mathbb{Z}$.
**Result:** No, not surjective.

---

### **(14) Section 14: Inverse Functions**
**Problem:** $f(m, n) = (m + n, 2m + n)$.
**Step:** Set $x = m+n$ and $y = 2m+n$.
Subtract (1) from (2): $y - x = m$.
Substitute $m$ into (1): $x = (y-x) + n \implies n = 2x - y$.
**Result:** $f^{-1}(x, y) = (y - x, 2x - y)$.

---

### **(15) Section 15: Equal Cardinalities**
**Problem:** $| \mathbb{Z} | = | 10\mathbb{Z} |$.
**Bijection:** $f: \mathbb{Z} \to 10\mathbb{Z}$ defined by $f(n) = 10n$.
**Check:** Every multiple of 10 has a unique $n$ ($n = x/10$) and every $n$ maps to exactly one multiple. It is a bijection.

---

### **(16) Section 16: Countable Sets**
**Problem:** $A = \{(n, 3n) : n \in \mathbb{N}\}$ is countably infinite.
**Proof:** Define $f: \mathbb{N} \to A$ by $f(n) = (n, 3n)$.
1. Injective: $(n_1, 3n_1) = (n_2, 3n_2) \implies n_1 = n_2$.
2. Surjective: Any element in $A$ is of the form $(k, 3k)$, which is $f(k)$.
**Conclusion:** Since a bijection to $\mathbb{N}$ exists, $A$ is countably infinite.

---

# Set 2
