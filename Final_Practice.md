# Set 1

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

### **(1) Section 1: Truth Tables**
**Problem:** Use a truth table to determine if $[P \wedge (P \implies Q)] \implies Q$ is a tautology.

| $P$ | $Q$ | $P \implies Q$ | $P \wedge (P \implies Q)$ | $[P \wedge (P \implies Q)] \implies Q$ |
| :--- | :--- | :--- | :--- | :--- |
| T | T | T | T | **T** |
| T | F | F | F | **T** |
| F | T | T | F | **T** |
| F | F | T | F | **T** |

**Conclusion:** Since the final column is all True, the statement is a tautology.

---

### **(2) Section 2: Negating Statements**
**Problem:** Negate: For every integer $n$, if $n$ is prime, then $n$ is odd or $n = 2$.
**Symbolic Form:** $\forall n \in \mathbb{Z}, P(n) \implies (O(n) \vee (n=2))$
**Negation Steps:**
1. $\forall n$ becomes $\exists n$.
2. Keep the antecedent ($P(n)$).
3. Negate the consequent: $\sim(O(n) \vee n=2)$ becomes $(\sim O(n) \wedge n \neq 2)$.
**Answer:** There exists an integer $n$ such that $n$ is prime, and $n$ is even and $n \neq 2$.

---

### **(3) Section 3: Counting Problems**
**Problem:** A club has 20 members. How many ways can they choose a President, a Vice President, and a Treasurer?
**Logic:** Order matters because the roles are distinct (President $\neq$ Treasurer).
**Solution:** $P(20, 3) = \frac{20!}{(20-3)!} = 20 \times 19 \times 18$.
**Result:** $6,840$.

---

### **(4) Section 4: Pascal / Binomial**
**Problem:** Show that $\binom{n}{k} = \frac{n}{k} \binom{n-1}{k-1}$ for $1 \le k \le n$.
**Proof:** LHS: $\frac{n!}{k!(n-k)!}$
RHS: $\frac{n}{k} \cdot \frac{(n-1)!}{(k-1)!( (n-1)-(k-1) )!} = \frac{n(n-1)!}{k(k-1)!(n-k)!}$
Since $n(n-1)! = n!$ and $k(k-1)! = k!$, the RHS becomes $\frac{n!}{k!(n-k)!}$.
**Conclusion:** LHS = RHS.

---

### **(5) Section 5: Direct / Contrapositive**
**Problem:** If $n^2$ is a multiple of 3, then $n$ is a multiple of 3.
**Method:** Contrapositive. Suppose $n$ is **not** a multiple of 3.
**Case 1:** $n = 3k + 1 \implies n^2 = 9k^2 + 6k + 1 = 3(3k^2 + 2k) + 1$. (Not a multiple of 3).
**Case 2:** $n = 3k + 2 \implies n^2 = 9k^2 + 12k + 4 = 3(3k^2 + 4k + 1) + 1$. (Not a multiple of 3).
**Conclusion:** Since $n^2$ is not a multiple of 3 in either case, the contrapositive is proven.

---

### **(6) Section 6: Proof by Contradiction**
**Problem:** If $a \in \mathbb{Q}$ and $b \notin \mathbb{Q}$, then $a + b \notin \mathbb{Q}$.
**Assume False:** Suppose $a + b = c$ where $c \in \mathbb{Q}$.
**Proof:** $b = c - a$. Since $c$ and $a$ are both rational, their difference $c - a$ must be rational (rationals are closed under subtraction).
**Contradiction:** This implies $b \in \mathbb{Q}$, but the problem states $b$ is irrational.
**Conclusion:** The sum must be irrational.

---

### **(7) Section 7: IFF Statements**
**Problem:** $6 \mid a$ iff $2 \mid a$ and $3 \mid a$.
**($\implies$):** If $6 \mid a$, then $a = 6k = 2(3k)$ and $a = 3(2k)$. Thus $2 \mid a$ and $3 \mid a$.
**($\impliedby$):** If $2 \mid a$ and $3 \mid a$, then $a = 2m$. Since $3 \mid 2m$ and $\text{gcd}(3,2)=1$, by Euclid's Lemma, $3 \mid m$. So $m = 3k$. Substituting back, $a = 2(3k) = 6k$. Thus $6 \mid a$.

---

### **(8) Section 8: Proofs Involving Sets**
**Problem:** $(A \cup B) - C = (A - C) \cup (B - C)$.
**Element Method:** $x \in (A \cup B) - C \iff x \in (A \cup B) \wedge x \notin C$
$\iff (x \in A \vee x \in B) \wedge x \notin C$
$\iff (x \in A \wedge x \notin C) \vee (x \in B \wedge x \notin C)$
$\iff (x \in A - C) \vee (x \in B - C) \iff x \in (A - C) \cup (B - C)$.

---

### **(9) Section 9: Disproof / Counterexamples**
**Problem:** Disprove: $n^2 + n + 41$ is always prime for $n \in \mathbb{N}$.
**Counterexample:** Let $n = 41$.
**Calculation:** $41^2 + 41 + 41 = 41(41 + 1 + 1) = 41(43)$.
**Conclusion:** This number is divisible by 41 and 43, so it is composite. The statement is false.

---

### **(10) Section 10: Induction**
**Problem:** $\sum_{i=1}^n \frac{1}{i(i+1)} = \frac{n}{n+1}$.
**Base Case ($n=1$):** $\frac{1}{1(2)} = 1/2$. Formula: $\frac{1}{1+1} = 1/2$. Matches.
**Inductive Step:** Assume $P(k) = \frac{k}{k+1}$. For $k+1$:
$\frac{k}{k+1} + \frac{1}{(k+1)(k+2)} = \frac{k(k+2) + 1}{(k+1)(k+2)} = \frac{k^2 + 2k + 1}{(k+1)(k+2)} = \frac{(k+1)^2}{(k+1)(k+2)} = \frac{k+1}{k+2}$.
**Conclusion:** Matches target formula for $n=k+1$.

---

### **(11) Section 11: Relations**
**Problem:** $A = \{1, 2, 3\}$, $R = \{(1,1), (2,2), (1,2), (2,1)\}$.
**Reflexive?** No. $(3,3)$ is missing.
**Transitive?** Yes. Checking pairs: $(1,2)$ and $(2,1)$ exists, and $(1,1)$ is there. $(2,1)$ and $(1,2)$ exists, and $(2,2)$ is there.

---

### **(12) Section 12: Equivalence Classes**
**Problem:** $xRy \iff x^2 + y^2$ is even.
**Logic:** $x^2 + y^2$ is even only if $x^2$ and $y^2$ have the same parity. This means $x$ and $y$ must both be even or both be odd.
**Classes:** $[0] = \{ \dots, -2, 0, 2, \dots \}$ and $[1] = \{ \dots, -1, 1, 3, \dots \}$.

---

### **(13) Section 13: Inj / Surj**
**Problem:** $f: \mathbb{R} \to \mathbb{R}, f(x) = x^2$.
**Injective?** No. $f(-2) = 4$ and $f(2) = 4$.
**Surjective?** No. There is no $x$ such that $x^2 = -1$.

---

### **(14) Section 14: Inverses**
**Problem:** $f(x) = \sqrt[3]{x - 5}$.
**Step:** $y = \sqrt[3]{x - 5} \implies y^3 = x - 5 \implies x = y^3 + 5$.
**Result:** $f^{-1}(x) = x^3 + 5$.

---

### **(15) Section 15: Equal Cardinalities**
**Problem:** $| \mathbb{E} | = | \mathbb{O} |$.
**Bijection:** $f: \mathbb{E} \to \mathbb{O}$ defined by $f(n) = n + 1$.
**Check:** Every even number $n$ maps to a unique odd number $n+1$. The inverse $f^{-1}(y) = y - 1$ maps every odd number back to a unique even number.

---

### **(16) Section 16: Countable Sets**
**Problem:** $\{2^n : n \in \mathbb{N}\}$ is countably infinite.
**Proof:** Define $f: \mathbb{N} \to A$ by $f(n) = 2^n$.
1. **Injective:** If $2^{n_1} = 2^{n_2}$, then $n_1 = n_2$ (by log properties).
2. **Surjective:** Any element in the set is $2^k$ for some $k \in \mathbb{N}$, which is $f(k)$.
**Conclusion:** Since a bijection exists, it is countably infinite.

---

# Set 3

### **(1) Section 1: Truth Tables (2.6.9)**
**Problem:** Show $(P \iff Q) \equiv (P \wedge Q) \vee (\sim P \wedge \sim Q)$ using a truth table.

| $P$ | $Q$ | $P \iff Q$ | $P \wedge Q$ | $\sim P \wedge \sim Q$ | $(P \wedge Q) \vee (\sim P \wedge \sim Q)$ |
| :--- | :--- | :--- | :--- | :--- | :--- |
| T | T | **T** | T | F | **T** |
| T | F | **F** | F | F | **F** |
| F | T | **F** | F | F | **F** |
| F | F | **T** | F | T | **T** |

**Conclusion:** The columns for $P \iff Q$ and the complex OR statement match exactly. They are equivalent.

---

### **(2) Section 2: Negating Statements (2.10.5)**
**Problem:** Negate: $\exists x \in \mathbb{R}, \forall n \in \mathbb{N}, x^n > 0$.
**Logic:** Flip the symbols and negate the final inequality.
**Answer:** $\forall x \in \mathbb{R}, \exists n \in \mathbb{N}, x^n \le 0$.

---

### **(3) Section 3: Counting Problems (3.5.19)**
**Problem:** How many 5-card hands contain at least one King?
**Strategy:** "Total hands" minus "Hands with ZERO Kings."
1. **Total:** $\binom{52}{5}$.
2. **No Kings:** There are 48 cards that aren't Kings. So, $\binom{48}{5}$.
**Answer:** $\binom{52}{5} - \binom{48}{5} = 2,598,960 - 1,712,304 = 886,656$.

---

### **(4) Section 4: Pascal’s Rule**
**Problem:** Find $\binom{5}{3}$ given $\binom{4}{3} = 4$ and $\binom{4}{2} = 6$.
**Logic:** Pascal's Rule says a cell in the triangle is the sum of the two cells directly above it.
**Calculation:** $\binom{5}{3} = \binom{4}{3} + \binom{4}{2} = 4 + 6 = 10$.

---

### **(5) Section 5: Direct/Contrapositive (5.27)**
**Problem:** If $a \equiv b \pmod n$, then $a^2 \equiv b^2 \pmod n$.
**Proof:** $a \equiv b \pmod n$ means $n \mid (a - b)$, so $a - b = nk$ for some integer $k$.
We want to show $n \mid (a^2 - b^2)$.
Factoring: $a^2 - b^2 = (a - b)(a + b)$.
Substitute $nk$ for $(a-b)$: $a^2 - b^2 = (nk)(a + b) = n[k(a + b)]$.
**Conclusion:** Since $a^2 - b^2$ is a multiple of $n$, then $a^2 \equiv b^2 \pmod n$.

---

### **(6) Section 6: Proof by Contradiction (6.17)**
**Problem:** If $n^2$ is even, then $n$ is even.
**Assume False:** Suppose $n^2$ is even and $n$ is odd.
**Proof:** If $n$ is odd, $n = 2k + 1$.
$n^2 = (2k + 1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1$.
This means $n^2$ is odd.
**Contradiction:** We assumed $n^2$ was even, but we found it must be odd.
**Conclusion:** $n$ must be even.

---

### **(7) Section 7: IFF Statements (7.11)**
**Problem:** $xy$ is odd iff $x$ is odd and $y$ is odd.
**($\implies$):** Assume $xy$ is odd. By contrapositive, if $x$ or $y$ were even, the product would be even ($2k \cdot y = 2(ky)$). Thus, both must be odd.
**($\impliedby$):** Assume $x = 2k+1$ and $y = 2m+1$.
$xy = (2k+1)(2m+1) = 4km + 2k + 2m + 1 = 2(2km + k + m) + 1$.
**Conclusion:** $xy$ is odd.

---

### **(8) Section 8: Proofs Involving Sets (8.1)**
**Problem:** $\{x \in \mathbb{Z} : 8 \mid x\} \subseteq \{x \in \mathbb{Z} : 4 \mid x\}$.
**Proof:** Let $x \in \{8k\}$. Then $x = 8k$ for some integer $k$.
Rewrite $8k$ as $4(2k)$. Since $2k$ is an integer, $x$ is a multiple of $4$.
**Conclusion:** Every element of the first set is in the second set.

---

### **(9) Section 9: Disproof / Counterexamples (9.9)**
**Problem:** Disprove: $A \cap (B \cup C) = (A \cap B) \cup C$.
**Counterexample:** Let $A=\{1\}, B=\{1\}, C=\{2\}$.
**LHS:** $A \cap \{1, 2\} = \{1\}$.
**RHS:** $\{1\} \cup \{2\} = \{1, 2\}$.
**Conclusion:** $\{1\} \neq \{1, 2\}$. Disproven.

---

### **(10) Section 10: Induction**
**Problem:** $n < 2^n$ for all $n \in \mathbb{N}$.
**Base Case ($n=1$):** $1 < 2^1$ is true.
**Step:** Assume $k < 2^k$. Show $k+1 < 2^{k+1}$.
$2^{k+1} = 2 \cdot 2^k = 2^k + 2^k$.
Since $k < 2^k$ (hypothesis) and $1 \le 2^k$ (for all $n \ge 1$), then $k + 1 < 2^k + 2^k$.
**Conclusion:** $k+1 < 2^{k+1}$.

---

### **(11) Section 11: Relations (11.2.9)**
**Problem:** $xRy$ if $x \le y$ on $\mathbb{Z}$.
**Symmetric?** No. $1 \le 2$ but $2 \not\le 1$.
**Antisymmetric?** Yes. If $x \le y$ and $y \le x$, then $x = y$.

---

### **(12) Section 12: Equivalence Relations (11.3.11)**
**Problem:** If $a \equiv b \pmod n$ and $c \equiv d \pmod n$, prove $(a+c) \equiv (b+d) \pmod n$.
**Proof:**
1. $a - b = nk_1$
2. $c - d = nk_2$
Add the equations: $(a - b) + (c - d) = nk_1 + nk_2$.
Rearrange: $(a + c) - (b + d) = n(k_1 + k_2)$.
**Conclusion:** Since the difference is a multiple of $n$, the sums are congruent.

---

### **(13) Section 13: Injective (12.2.11)**
**Problem:** If $f$ and $g$ are injective, show $g \circ f$ is injective.
**Proof:** Assume $g(f(x_1)) = g(f(x_2))$.
Since $g$ is injective, $f(x_1) = f(x_2)$.
Since $f$ is injective, $x_1 = x_2$.
**Conclusion:** $g \circ f$ is injective.

---

### **(14) Section 14: Inverses (12.5.9)**
**Problem:** Find the inverse of $f(x) = \frac{2x}{x+1}$.
**Step:** $y = \frac{2x}{x+1} \implies y(x+1) = 2x \implies yx + y = 2x$.
$y = 2x - yx \implies y = x(2 - y) \implies x = \frac{y}{2-y}$.
**Result:** $f^{-1}(x) = \frac{x}{2-x}$.

---

### **(15) Section 15: Cardinality**
**Problem:** Prove $|\mathbb{N} \times \{0, 1\}| = |\mathbb{N}|$.
**Bijection:** Use the "Odd/Even" trick from your guide!
$f(n, 0) = 2n$ (maps to evens).
$f(n, 1) = 2n - 1$ (maps to odds).
**Result:** Every natural number is either even or odd, so this covers all of $\mathbb{N}$ perfectly.

---

### **(16) Section 16: Countable Sets**
**Problem:** The set of all finite subsets of $\mathbb{N}$ is countable.
**Proof (Sketch):** You can list subsets by their "maximum element" and their "sum." For any sum $S$, there are only finitely many subsets of $\mathbb{N}$ that add up to $S$. Since you can list finite groups of finite sets, the whole thing is countable.

---

# Section 4

### **(1) Section 3: Counting Problems (3.4.9)**
**Problem:** How many ways can 8 people be seated at a round table? (Note: Rotating the table doesn't count as a new seating).
**Logic:** In a line, there are $8!$ ways. However, at a round table, each arrangement is identical to 7 others (rotating each person one seat over).
**Solution:** To fix the "rotation" problem, we fix one person in a seat and arrange the remaining $(n-1)$ people around them.
**Result:** $(8 - 1)! = 7! = 5,040$.

---

### **(2) Section 5: Direct/Contrapositive (5.21)**
**Problem:** Let $a, b \in \mathbb{Z}$. Prove: If $a \equiv b \pmod n$, then $a-c \equiv b-c \pmod n$.
**Proof:**
1. Assume $a \equiv b \pmod n$. By definition, $n \mid (a - b)$.
2. This means $a - b = nk$ for some integer $k$.
3. We want to show $n \mid ((a - c) - (b - c))$.
4. Simplify the target: $(a - c) - (b - c) = a - c - b + c = a - b$.
5. Since we know $a - b = nk$, then $(a - c) - (b - c) = nk$.
**Conclusion:** Since the difference is a multiple of $n$, then $a-c \equiv b-c \pmod n$.

---

### **(3) Section 6: Proof by Contradiction (6.7)**
**Problem:** Prove there is no integer $n$ such that $n^2 \equiv 2 \pmod 4$.
**Assume False:** Suppose there exists an $n \in \mathbb{Z}$ such that $n^2 = 4k + 2$.
**Case 1 (n is even):** Let $n = 2m$. Then $n^2 = (2m)^2 = 4m^2$.
Setting $4m^2 = 4k + 2 \implies 4(m^2 - k) = 2 \implies 2(m^2 - k) = 1$.
This implies 1 is even, a **contradiction**.
**Case 2 (n is odd):** Let $n = 2m+1$. Then $n^2 = 4m^2 + 4m + 1 = 4(m^2 + m) + 1$.
This leaves a remainder of 1, not 2. **Contradiction**.
**Conclusion:** No such integer $n$ exists.

---

### **(4) Section 7: IFF Statements (7.5)**
**Problem:** Prove: $a^2 - 5a + 6$ is even for all $a \in \mathbb{Z}$.
**Method:** Case Analysis (Direct Proof).
**Case 1 (a is even):** Let $a = 2k$.
$(2k)^2 - 5(2k) + 6 = 4k^2 - 10k + 6 = 2(2k^2 - 5k + 3)$. This is even.
**Case 2 (a is odd):** Let $a = 2k + 1$.
$(2k+1)^2 - 5(2k+1) + 6 = (4k^2 + 4k + 1) - (10k + 5) + 6 = 4k^2 - 6k + 2 = 2(2k^2 - 3k + 1)$. This is even.
**Conclusion:** In both possible cases, the result is even.

---

### **(5) Section 11: Relations (11.2.5)**
**Problem:** Let $R = \{(x, y) \in \mathbb{R}^2 : x^2 + y^2 = 1\}$. Is $R$ reflexive? Is it symmetric?
**Reflexive?** No. For $R$ to be reflexive, $xRx$ must be true for all $x$. But $2^2 + 2^2 = 8 \neq 1$.
**Symmetric?** Yes. If $x^2 + y^2 = 1$, then $y^2 + x^2 = 1$ (by commutativity of addition). Thus if $xRy$, then $yRx$.

---

### **(6) Section 12: Equivalence Classes (11.3.5)**
**Problem:** Let $aRb$ iff $a \equiv b \pmod 5$. List three elements in the equivalence class $[2]$.
**Logic:** $[2]$ contains all integers $x$ such that $x \equiv 2 \pmod 5$, meaning $x = 5k + 2$.
**Elements:**
1. Let $k = 0 \implies x = 2$.
2. Let $k = 1 \implies x = 7$.
3. Let $k = -1 \implies x = -3$.
**Answer:** $\{ \dots, -3, 2, 7, \dots \}$.

---

### **(7) Section 13: Injective/Surjective (12.2.5)**
**Problem:** Let $f: \mathbb{R} \to \mathbb{R}$ be $f(x) = e^x$. Is $f$ injective? Is it surjective?
**Injective?** Yes. If $e^{x_1} = e^{x_2}$, taking the natural log of both sides gives $x_1 = x_2$.
**Surjective?** No. The range of $e^x$ is $(0, \infty)$. There is no $x$ such that $e^x = -1$ or $e^x = 0$.

---

### **(8) Section 14: Inverse Functions (12.5.7)**
**Problem:** Prove that if $f: A \to B$ is a bijection, then $f^{-1}$ is also a bijection.
**Proof Sketch:**
1. Since $f$ is a bijection, every $b \in B$ has exactly one $a \in A$ such that $f(a) = b$. This defines the function $f^{-1}(b) = a$.
2. **Injective:** If $f^{-1}(b_1) = f^{-1}(b_2) = a$, then $f(a) = b_1$ and $f(a) = b_2$. Since $f$ is a function, $b_1 = b_2$.
3. **Surjective:** For any $a \in A$, there is a $b \in B$ (namely $b = f(a)$) such that $f^{-1}(b) = a$.
**Conclusion:** $f^{-1}$ is both injective and surjective.

---

### **(9) Section 16: Countable Sets (14.2.3 variant)**
**Problem:** Prove the set of all polynomials with integer coefficients is countable.
**Proof (Sketch):** Every polynomial can be defined by a finite list of integer coefficients $(a_0, a_1, \dots, a_n)$.
1. We know $\mathbb{Z}$ is countable.
2. We know the Cartesian product of a finite number of countable sets ($\mathbb{Z} \times \mathbb{Z} \times \dots$) is countable.
3. The set of all polynomials is the union of all polynomials of degree 1, degree 2, degree 3, etc.
4. A countable union of countable sets is countable.
**Conclusion:** The set of polynomials is countable.

---

### **The "Deep Dive" Check-in**
You’ve officially covered every section! Before you close the books, let's look at the "big three" logic jumps one more time:

* **Modular Proofs:** Always write out $a - b = nk$ immediately. It turns a "logic" problem into a "basic algebra" problem.
* **Induction:** Always write down what your "Target" looks like (the formula for $n = k+1$). It helps you see how to manipulate your assumption.
* **Injective/Surjective:** If you can't solve for $x$ (for surjective) or the math gives you two answers like $\pm$ (for injective), it’s probably a "No."

