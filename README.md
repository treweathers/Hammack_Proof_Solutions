# Hammack_Proof_Solutions

### "Cram" Tips:
* **Contradiction:** Use it when the statement says "There are no..." or "$\sqrt{x}$ is irrational."
* **Contrapositive:** Use it when the "Then" part is simpler than the "If" part (like $x^2 \in \text{Even} \implies x \in \text{Even}$).
* **Induction:** Use it for sums ($\sum$), factorials ($n!$), or $a^n - b^n$ divisibility.
* **Direct:** Use it for straightforward definitions (Even/Odd/Divisibility).

## Chapter 4: Direct Proof

### 3. If $a$ is an odd integer, then $a^2 + 3a + 5$ is odd.
**Proof.** Assume $a$ is an odd integer. By definition, $a = 2k + 1$ for some integer $k$. Substituting this into the expression:
$$a^2 + 3a + 5 = (2k + 1)^2 + 3(2k + 1) + 5$$
$$= (4k^2 + 4k + 1) + (6k + 3) + 5$$
$$= 4k^2 + 10k + 9$$
$$= 4k^2 + 10k + 8 + 1 = 2(2k^2 + 5k + 4) + 1$$
Since $2k^2 + 5k + 4$ is an integer, $a^2 + 3a + 5$ is odd by definition. $\square$

---

### 7. Suppose $a, b \in \mathbb{Z}$. If $a | b$, then $a^2 | b^2$.
**Proof.** Suppose $a | b$. By definition of divisibility, there exists an integer $k$ such that $b = ak$. Squaring both sides of this equation, we get:
$$b^2 = (ak)^2 = a^2k^2$$
Since $k^2$ is an integer, it follows from the definition of divisibility that $a^2 | b^2$. $\square$

---

### 11. Suppose $a, b, c, d \in \mathbb{Z}$. If $a | b$ and $c | d$, then $ac | bd$.
**Proof.** Suppose $a | b$ and $c | d$. Then there exist integers $k$ and $m$ such that $b = ak$ and $d = cm$. Multiplying these two equations together:
$$bd = (ak)(cm) = (ac)(km)$$
Since $km$ is an integer, the product $ac$ divides $bd$ by definition. $\square$

---

### 15. If $n \in \mathbb{Z}$, then $n^2 + 3n + 4$ is even.
**Proof.** We consider two cases based on the parity of $n$.

* **Case 1:** $n$ is even. Then $n = 2k$ for some $k \in \mathbb{Z}$.
    $$n^2 + 3n + 4 = (2k)^2 + 3(2k) + 4 = 4k^2 + 6k + 4 = 2(2k^2 + 3k + 2)$$
    This is even.
* **Case 2:** $n$ is odd. Then $n = 2k + 1$ for some $k \in \mathbb{Z}$.
    $$n^2 + 3n + 4 = (2k+1)^2 + 3(2k+1) + 4 = (4k^2+4k+1) + (6k+3) + 4$$
    $$= 4k^2 + 10k + 8 = 2(2k^2 + 5k + 4)$$
    This is also even.
In both cases, the expression is even. $\square$

---

### 17. If two integers have opposite parity, then their product is even.
**Proof.** Let the two integers be $a$ and $b$. Without loss of generality, assume $a$ is even and $b$ is odd. By definition, $a = 2k$ and $b = 2m + 1$ for some integers $k, m$. Their product is:
$$ab = (2k)(2m + 1) = 2(k(2m + 1))$$
Because $k(2m + 1)$ is an integer, the product $ab$ is even. $\square$

---


## Chapter 5: Contrapositive Proof

### 3. Suppose $a, b \in \mathbb{Z}$. If $a^2(b^2 - 2b)$ is odd, then $a$ and $b$ are odd.
**Proof.** (By contrapositive) Suppose it is not the case that $a$ and $b$ are both odd. Then $a$ is even or $b$ is even.
* **Case 1:** $a$ is even. Then $a = 2k$ for some $k \in \mathbb{Z}$. Substituting this:
    $$a^2(b^2 - 2b) = (2k)^2(b^2 - 2b) = 4k^2(b^2 - 2b) = 2(2k^2(b^2 - 2b))$$
    Since $2k^2(b^2 - 2b)$ is an integer, $a^2(b^2 - 2b)$ is even.
* **Case 2:** $b$ is even. Then $b = 2k$ for some $k \in \mathbb{Z}$. Substituting this:
    $$a^2(b^2 - 2b) = a^2((2k)^2 - 2(2k)) = a^2(4k^2 - 4k) = 2(a^2(2k^2 - 2k))$$
    Since $a^2(2k^2 - 2k)$ is an integer, $a^2(b^2 - 2b)$ is even.
In both cases, $a^2(b^2 - 2b)$ is even. Thus, if $a^2(b^2 - 2b)$ is odd, $a$ and $b$ must both be odd. $\square$

---

### 7. Suppose $a, b \in \mathbb{Z}$. If both $ab$ and $a + b$ are even, then both $a$ and $b$ are even.
**Proof.** (By contrapositive) Suppose it is not the case that both $a$ and $b$ are even. This means at least one of $a$ or $b$ is odd.
* **Case 1:** $a$ is odd and $b$ is even. Then $a+b$ is odd.
* **Case 2:** $a$ is even and $b$ is odd. Then $a+b$ is odd.
* **Case 3:** $a$ is odd and $b$ is odd. Then $ab$ is odd (product of two odds is odd).
In all possible cases where $a$ and $b$ are not both even, the statement "both $ab$ and $a+b$ are even" is false. Therefore, if both are even, $a$ and $b$ must both be even. $\square$

---

### 17. If $n$ is odd, then $8 \mid (n^2 - 1)$.
**Proof.** (Direct proof is actually cleaner here) If $n$ is odd, then $n = 2k + 1$ for some $k \in \mathbb{Z}$. Then:
$$n^2 - 1 = (2k + 1)^2 - 1 = (4k^2 + 4k + 1) - 1 = 4k^2 + 4k = 4k(k + 1)$$
Note that $k$ and $k+1$ are consecutive integers, so one of them must be even. Thus, $k(k + 1) = 2m$ for some integer $m$. Substituting this back:
$$4k(k + 1) = 4(2m) = 8m$$
Since $8m$ is a multiple of 8, $8 \mid (n^2 - 1)$. $\square$

---

### 23. Let $a, b \in \mathbb{Z}$ and $n \in \mathbb{N}$. If $a \equiv b \pmod n$, then $a^2 \equiv ab \pmod n$.
**Proof.** Suppose $a \equiv b \pmod n$. By definition of congruence, $n \mid (a - b)$. This means $a - b = nk$ for some integer $k$. Multiplying both sides by $a$:
$$a(a - b) = a(nk)$$
$$a^2 - ab = n(ak)$$
Since $ak$ is an integer, $n \mid (a^2 - ab)$. By definition of congruence, $a^2 \equiv ab \pmod n$. $\square$

---

### 25. Let $n \in \mathbb{N}$. If $2^n - 1$ is prime, then $n$ is prime.
**Proof.** (By contrapositive) Suppose $n$ is composite. Then $n = ab$ for some integers $a, b > 1$. Substituting this into the expression:
$$2^n - 1 = 2^{ab} - 1 = (2^a)^b - 1$$
Using the algebraic identity $x^b - 1 = (x - 1)(x^{b-1} + x^{b-2} + \dots + x + 1)$, let $x = 2^a$:
$$2^n - 1 = (2^a - 1)( (2^a)^{b-1} + (2^a)^{b-2} + \dots + 2^a + 1)$$
Since $a > 1$, $(2^a - 1) > 1$. Since $b > 1$, the second factor is also greater than 1. Thus, $2^n - 1$ is the product of two integers greater than 1, so it is composite. Therefore, if $2^n - 1$ is prime, $n$ must be prime. $\square$

---


## Chapter 6: Proof by Contradiction

### 3. Prove that $\sqrt[3]{2}$ is irrational.
**Proof.** Suppose for the sake of contradiction that $\sqrt[3]{2}$ is rational. Then there exist integers $a$ and $b$ ($b \neq 0$) such that $\sqrt[3]{2} = \frac{a}{b}$. We assume this fraction is in simplest form, meaning $\gcd(a, b) = 1$. 

Cubing both sides of the equation gives:
$$2 = \frac{a^3}{b^3} \implies 2b^3 = a^3$$
This implies that $a^3$ is even. By the properties of integers, if $a^3$ is even, then $a$ must also be even. Thus, $a = 2k$ for some integer $k$. Substituting this back into our equation:
$$2b^3 = (2k)^3 \implies 2b^3 = 8k^3$$
Dividing by 2, we get:
$$b^3 = 4k^3 = 2(2k^3)$$
This implies that $b^3$ is even, and therefore $b$ must be even. 

If both $a$ and $b$ are even, they share a common factor of 2, which contradicts our assumption that $\gcd(a, b) = 1$. Therefore, $\sqrt[3]{2}$ must be irrational. $\square$

---

### 5. Prove that $\sqrt{3}$ is irrational.
**Proof.** Suppose $\sqrt{3}$ is rational. Then $\sqrt{3} = \frac{a}{b}$ for some $a, b \in \mathbb{Z}$ where the fraction is in simplest form ($\gcd(a, b) = 1$). Squaring both sides:
$$3 = \frac{a^2}{b^2} \implies 3b^2 = a^2$$
This implies $3 \mid a^2$. Since 3 is prime, if $3 \mid a^2$, then $3 \mid a$. So $a = 3k$ for some $k \in \mathbb{Z}$. Substituting this back:
$$3b^2 = (3k)^2 = 9k^2 \implies b^2 = 3k^2$$
This implies $3 \mid b^2$, and thus $3 \mid b$. Since both $a$ and $b$ are divisible by 3, $\gcd(a, b) \geq 3$, which contradicts our assumption that the fraction was in simplest form. Thus, $\sqrt{3}$ is irrational. $\square$

---

### 11. There exist no integers $a$ and $b$ for which $18a + 6b = 1$.
**Proof.** Suppose there exist integers $a$ and $b$ such that $18a + 6b = 1$. We can factor out a 6 from the left side:
$$6(3a + b) = 1$$
Since $a$ and $b$ are integers, $3a + b$ is an integer. Let $k = 3a + b$. Then $6k = 1$. Solving for $k$, we get $k = 1/6$. But $1/6$ is not an integer. This is a contradiction. Therefore, no such integers $a$ and $b$ exist. $\square$

---

### 15. If $b \in \mathbb{Z}$ and $b \nmid k$ for every $k \in \mathbb{N}$, then $b = 0$.

**Proof.** (By Contradiction) 
Suppose $b \in \mathbb{Z}$ and $b \nmid k$ for every $k \in \mathbb{N}$, but assume for the sake of contradiction that $b \neq 0$.

If $b \neq 0$, then either $b > 0$ or $b < 0$. We consider the absolute value $|b|$. Since $b$ is a non-zero integer, $|b|$ is a positive integer, so $|b| \in \mathbb{N}$.

By the definition of divisibility, any non-zero integer $b$ divides itself ($b \cdot 1 = b$) and its negation ($b \cdot -1 = -b$). Therefore, $b$ must divide $|b|$. 

Since $|b|$ is a natural number, this contradicts our initial statement that $b$ does not divide *any* $k \in \mathbb{N}$. 

Thus, our assumption that $b \neq 0$ must be false. Therefore, $b = 0$. $\square$

---

### 19. The product of any five consecutive integers is divisible by 120.
**Proof.** Let the five consecutive integers be $n, n+1, n+2, n+3, n+4$. Their product is $P = \frac{(n+4)!}{(n-1)!}$.
In any $k$ consecutive integers, one is divisible by $k$.
1. One of these must be divisible by 5.
2. One must be divisible by 4, and another (distinct) one must be even, so the product is divisible by 8.
3. One must be divisible by 3.
Since 3, 5, and 8 are pairwise relatively prime, the product is divisible by $3 \times 5 \times 8 = 120$. $\square$

---


## Chapter 7: Proving Non-Conditional Statements

### 5. An integer $a$ is odd if and only if $a^3$ is odd.
**Proof.**
$(\Rightarrow)$ Suppose $a$ is odd. Then $a = 2k + 1$ for some $k \in \mathbb{Z}$.
$a^3 = (2k+1)^3 = 8k^3 + 12k^2 + 6k + 1 = 2(4k^3 + 6k^2 + 3k) + 1$.
Since $(4k^3 + 6k^2 + 3k) \in \mathbb{Z}$, $a^3$ is odd.
$(\Leftarrow)$ We prove the contrapositive: If $a$ is even, then $a^3$ is even.
Suppose $a$ is even, so $a = 2k$.
$a^3 = (2k)^3 = 8k^3 = 2(4k^3)$.
Since $4k^3 \in \mathbb{Z}$, $a^3$ is even. $\square$

---

### 11. Suppose $a, b \in \mathbb{Z}$. Prove $(a-3)b^2$ is even iff $a$ is odd or $b$ is even.
**Proof.**
$(\Leftarrow)$ Suppose $a$ is odd or $b$ is even.
* **Case 1:** $a$ is odd. Then $a = 2k+1$. Thus $(a-3) = (2k+1-3) = 2k-2 = 2(k-1)$. This is even, so the whole product $(a-3)b^2$ is even.
* **Case 2:** $b$ is even. Then $b = 2k$, so $b^2 = 4k^2$. Thus $(a-3)b^2 = (a-3)(4k^2) = 2(2k^2(a-3))$, which is even.
$(\Rightarrow)$ We prove the contrapositive: If $a$ is even and $b$ is odd, then $(a-3)b^2$ is odd.
If $a$ is even and $b$ is odd, then $(a-3)$ is (even - odd) = odd. Also, $b^2$ is (odd $\times$ odd) = odd.
The product of two odd integers is odd, so $(a-3)b^2$ is odd. $\square$

---

### 13. Suppose $a, b \in \mathbb{Z}$. If $a + b$ is odd, then $a^2 + b^2$ is odd.
**Proof.** Suppose $a+b$ is odd. This implies $a$ and $b$ have opposite parity (one is even, one is odd).
Without loss of generality, let $a = 2k$ and $b = 2m + 1$.
$a^2 + b^2 = (2k)^2 + (2m+1)^2 = 4k^2 + 4m^2 + 4m + 1 = 2(2k^2 + 2m^2 + 2m) + 1$.
Since the term in parentheses is an integer, $a^2 + b^2$ is odd. $\square$

---

### 22. If $n \in \mathbb{Z}$, then $4 \mid n^2$ or $4 \mid (n^2 - 1)$.
**Proof.** We use cases based on the parity of $n$.
* **Case 1:** $n$ is even. Then $n = 2k$.
  $n^2 = (2k)^2 = 4k^2$. Thus $4 \mid n^2$.
* **Case 2:** $n$ is odd. Then $n = 2k + 1$.
  $n^2 - 1 = (2k+1)^2 - 1 = (4k^2 + 4k + 1) - 1 = 4k^2 + 4k = 4(k^2 + k)$.
  Thus $4 \mid (n^2 - 1)$.
In all cases, the statement holds. $\square$

---

### 23. Suppose $a, b, c \in \mathbb{Z}$. If $a \mid b$ and $a \mid (b^2 - c)$, then $a \mid c$.
**Proof.** Assume $a \mid b$ and $a \mid (b^2 - c)$.
By definition, $b = ak$ and $b^2 - c = am$ for some $k, m \in \mathbb{Z}$.
Substitute $b = ak$ into the second equation:
$(ak)^2 - c = am \implies a^2k^2 - c = am$.
Solving for $c$: $c = a^2k^2 - am = a(ak^2 - m)$.
Since $(ak^2 - m)$ is an integer, $a \mid c$ by definition. $\square$

---


## Chapter 8: Proofs Involving Sets

### 1. Prove that $\{12n : n \in \mathbb{Z}\} \subseteq \{2n : n \in \mathbb{Z}\} \cap \{3n : n \in \mathbb{Z}\}$.
**Proof.** Let $x \in \{12n : n \in \mathbb{Z}\}$. By definition, $x = 12k$ for some integer $k$.
* Since $x = 2(6k)$ and $6k \in \mathbb{Z}$, $x \in \{2n : n \in \mathbb{Z}\}$.
* Since $x = 3(4k)$ and $4k \in \mathbb{Z}$, $x \in \{3n : n \in \mathbb{Z}\}$.
Because $x$ is in both sets, $x \in \{2n : n \in \mathbb{Z}\} \cap \{3n : n \in \mathbb{Z}\}$. 
Thus, the inclusion holds. $\square$

---

### 5. If $p$ and $q$ are positive integers, then $\{pn : n \in \mathbb{N}\} \cap \{qn : n \in \mathbb{N}\} \neq \emptyset$.
**Proof.** Consider the integer $x = pq$. 
Since $p, q \in \mathbb{N}$, their product $pq$ is also a natural number.
* Because $x = p(q)$ and $q \in \mathbb{N}$, $x \in \{pn : n \in \mathbb{N}\}$.
* Because $x = q(p)$ and $p \in \mathbb{N}$, $x \in \{qn : n \in \mathbb{N}\}$.
Since $x$ is an element of both sets, the intersection is non-empty. $\square$

---

### 9. If $A, B$ and $C$ are sets, then $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$.
**Proof.**
$(\subseteq)$ Let $x \in A \cap (B \cup C)$. Then $x \in A$ and $x \in (B \cup C)$. Since $x \in B \cup C$, then $x \in B$ or $x \in C$.
* If $x \in B$, then $x \in A \cap B$.
* If $x \in C$, then $x \in A \cap C$.
In either case, $x \in (A \cap B) \cup (A \cap C)$.
$(\supseteq)$ Let $x \in (A \cap B) \cup (A \cap C)$. Then $x \in (A \cap B)$ or $x \in (A \cap C)$.
* If $x \in A \cap B$, then $x \in A$ and $x \in B$. Since $x \in B$, then $x \in B \cup C$. Thus $x \in A \cap (B \cup C)$.
* If $x \in A \cap C$, then $x \in A$ and $x \in C$. Since $x \in C$, then $x \in B \cup C$. Thus $x \in A \cap (B \cup C)$.
In both cases, $x \in A \cap (B \cup C)$. Therefore, the sets are equal. $\square$

---

### 21. Suppose $A$ and $B$ are sets. Prove $A \subseteq B$ if and only if $A - B = \emptyset$.
**Proof.**
$(\Rightarrow)$ Suppose $A \subseteq B$. Assume for contradiction that $A - B \neq \emptyset$. Then there exists $x \in A - B$. By definition, $x \in A$ and $x \notin B$. But $A \subseteq B$ implies that if $x \in A$, then $x \in B$. This is a contradiction. Thus $A - B = \emptyset$.
$(\Leftarrow)$ Suppose $A - B = \emptyset$. Let $x \in A$. If $x \notin B$, then by definition $x \in A - B$. But $A - B$ is empty, so it contains no elements. Thus, it must be that $x \in B$. Therefore $A \subseteq B$. $\square$

---

### 27. Prove that $\{12a + 4b : a, b \in \mathbb{Z}\} = \{4c : c \in \mathbb{Z}\}$.
**Proof.** Let $S = \{12a + 4b : a, b \in \mathbb{Z}\}$ and $T = \{4c : c \in \mathbb{Z}\}$.
$(\subseteq)$ Let $x \in S$. Then $x = 12a + 4b = 4(3a + b)$ for some $a, b \in \mathbb{Z}$. Since $3a+b$ is an integer, $x \in T$.
$(\supseteq)$ Let $x \in T$. Then $x = 4c$ for some integer $c$. We can write $x = 12(0) + 4(c)$. Since $0, c \in \mathbb{Z}$, $x \in S$.
Since both inclusions hold, $S = T$. $\square$

---

## Chapter 9: Disproof

### 1. If $x, y \in \mathbb{R}$, then $|x + y| = |x| + |y|$.
**Disproof.** This statement is false. Consider the counterexample $x = 1$ and $y = -1$.
Then $|x + y| = |1 + (-1)| = |0| = 0$.
However, $|x| + |y| = |1| + |-1| = 1 + 1 = 2$.
Since $0 \neq 2$, the statement is false. (The actual rule is the Triangle Inequality: $|x+y| \leq |x| + |y|$). $\square$

---

### 3. If $n \in \mathbb{Z}$ and $n^5 - n$ is even, then $n$ is even.
**Disproof.** This statement is false. Consider the counterexample $n = 1$.
$n^5 - n = 1^5 - 1 = 0$. Since 0 is even, the hypothesis holds.
However, $n = 1$ is odd, not even. Thus the statement is false. $\square$

---

### 5. If $A, B, C$ and $D$ are sets, then $(A \times B) \cup (C \times D) = (A \cup C) \times (B \cup D)$.
**Disproof.** This statement is false. Let $A=\{1\}, B=\{1\}, C=\{2\}, D=\{2\}$.
Left Side: $(A \times B) \cup (C \times D) = \{(1,1)\} \cup \{(2,2)\} = \{(1,1), (2,2)\}$.
Right Side: $(A \cup C) \times (B \cup D) = \{1,2\} \times \{1,2\} = \{(1,1), (1,2), (2,1), (2,2)\}$.
The point $(1,2)$ is in the right set but not the left. Thus, the sets are not equal. $\square$

---

### 19. For every $r, s \in \mathbb{Q}$ with $r < s$, there is an irrational number $u$ for which $r < u < s$.
**Proof.** (This one is actually **True**).
Let $r, s \in \mathbb{Q}$ with $r < s$. Consider the number $u = r + \frac{s-r}{\sqrt{2}}$.
1. Since $\sqrt{2} > 1$, then $0 < \frac{s-r}{\sqrt{2}} < s-r$. Adding $r$ to all sides gives $r < u < s$.
2. If $u$ were rational, then $\sqrt{2} = \frac{s-r}{u-r}$ would be rational (since $r, s, u$ are rational), which is a contradiction. Thus $u$ is irrational. $\square$

---

### 25. For all $a, b, c \in \mathbb{Z}$, if $a \mid bc$, then $a \mid b$ or $a \mid c$.
**Disproof.** This statement is false. Consider $a = 6, b = 2, c = 3$.
$bc = 6$, and $6 \mid 6$ is true.
However, $6 \nmid 2$ and $6 \nmid 3$. Thus the statement is false. (This only holds if $a$ is prime). $\square$

---

## Chapter 10: Mathematical Induction

### 1. Prove $1 + 2 + \dots + n = \frac{n^2 + n}{2}$ for every $n \in \mathbb{N}$.
**Proof.** * **Base Case:** For $n=1$, $1 = \frac{1^2+1}{2} = 1$. This holds.
* **Inductive Step:** Assume $1 + \dots + k = \frac{k^2+k}{2}$. Then for $n=k+1$:
  $$(1 + \dots + k) + (k+1) = \frac{k^2+k}{2} + (k+1) = \frac{k^2+k + 2k+2}{2} = \frac{k^2+3k+2}{2}$$
  The formula for $n=k+1$ is $\frac{(k+1)^2+(k+1)}{2} = \frac{k^2+2k+1+k+1}{2} = \frac{k^2+3k+2}{2}$.
  The steps match, so the statement holds by induction. $\square$

---

### 9. Prove that $24 \mid (5^{2n} - 1)$ for every integer $n \geq 0$.
**Proof.**
* **Base Case:** For $n=0$, $5^0 - 1 = 0$. Since $24 \mid 0$, it holds.
* **Inductive Step:** Assume $24 \mid (5^{2k} - 1)$, so $5^{2k} - 1 = 24m$. Then for $n=k+1$:
  $$5^{2(k+1)} - 1 = 5^{2k} \cdot 5^2 - 1 = 25(5^{2k}) - 1$$
  From the assumption, $5^{2k} = 24m + 1$. Substitute:
  $$25(24m + 1) - 1 = 25(24m) + 25 - 1 = 25(24m) + 24 = 24(25m + 1)$$
  Since $24$ is a factor, the statement holds for $k+1$. $\square$

---


### 3. Prove $1^3 + 2^3 + \dots + n^3 = \frac{n^2(n+1)^2}{4}$ for every $n \in \mathbb{N}$.
**Proof.**
* **Base Case:** For $n=1$, $1^3 = \frac{1^2(1+1)^2}{4} = \frac{4}{4} = 1$. This holds.
* **Inductive Step:** Assume the formula holds for $n=k$. For $n=k+1$:
  $$\sum_{i=1}^{k} i^3 + (k+1)^3 = \frac{k^2(k+1)^2}{4} + (k+1)^3$$
  Factor out $(k+1)^2$:
  $$= (k+1)^2 \left[ \frac{k^2}{4} + (k+1) \right] = (k+1)^2 \left[ \frac{k^2 + 4k + 4}{4} \right] = \frac{(k+1)^2(k+2)^2}{4}$$
  This is the formula for $n=k+1$. Thus, it holds by induction. $\square$

---

### 7. Prove $1\cdot3 + 2\cdot4 + \dots + n(n+2) = \frac{n(n+1)(2n+7)}{6}$ for $n \in \mathbb{N}$.
**Proof.**
* **Base Case:** For $n=1$, $1(3) = 3$. Formula: $\frac{1(2)(9)}{6} = \frac{18}{6} = 3$. Holds.
* **Inductive Step:** Assume holds for $n=k$. For $n=k+1$:
  $$\frac{k(k+1)(2k+7)}{6} + (k+1)(k+3) = \frac{k+1}{6} [k(2k+7) + 6(k+3)]$$
  $$= \frac{k+1}{6} [2k^2 + 7k + 6k + 18] = \frac{k+1}{6} [2k^2 + 13k + 18]$$
  Factor the quadratic: $(k+2)(2k+9)$.
  $$= \frac{(k+1)(k+2)(2(k+1)+7)}{6}$$
  Matches the formula for $n=k+1$. $\square$

---

### 11. Prove $3 \mid (n^3 + 5n + 6)$ for every integer $n \geq 0$.
**Proof.**
* **Base Case:** $n=0$: $0+0+6 = 6$, and $3 \mid 6$. Holds.
* **Inductive Step:** Assume $3 \mid (k^3 + 5k + 6)$. For $n=k+1$:
  $$(k+1)^3 + 5(k+1) + 6 = (k^3 + 3k^2 + 3k + 1) + 5k + 5 + 6$$
  Rearrange to isolate the assumption:
  $$= (k^3 + 5k + 6) + 3k^2 + 3k + 6 = (k^3 + 5k + 6) + 3(k^2 + k + 2)$$
  The first part is divisible by 3 (assumption) and the second part is clearly a multiple of 3. Thus, the sum is divisible by 3. $\square$

---

## Chapter 3: Combinatorial Proofs & Identities

### 3. Show that $\binom{n}{2}\binom{n-2}{k-2} = \binom{n}{k}\binom{k}{2}$.
**Proof.**
Left side: $\frac{n!}{2!(n-2)!} \cdot \frac{(n-2)!}{(k-2)!(n-k)!} = \frac{n!}{2!(k-2)!(n-k)!}$.
Right side: $\frac{n!}{k!(n-k)!} \cdot \frac{k!}{2!(k-2)!} = \frac{n!}{2!(k-2)!(n-k)!}$.
Both sides simplify to the same expression. $\square$

#### Story for $\binom{n}{2}\binom{n-2}{k-2} = \binom{n}{k}\binom{k}{2}$

**The Scenario:** You have a pool of $n$ athletes. You need to pick a **Team of $k$ players**, and from that team, you need to designate **2 Co-Captains**.

* **Story 1 (Left Side): Pick the Captains First.**
    First, you look at all $n$ people and pick the 2 Co-Captains ($\binom{n}{2}$). Now that they are set aside, you still need to fill out the rest of the team. You need $k-2$ more players to reach a total of $k$. You pick them from the remaining $n-2$ people ($\binom{n-2}{k-2}$).
    
* **Story 2 (Right Side): Pick the Team First.**
    First, you pick the entire team of $k$ players from the pool of $n$ ($\binom{n}{k}$). Now that the $k$ players are standing in front of you, you choose 2 of them to be the Co-Captains ($\binom{k}{2}$).

**Conclusion:** Both stories result in a $k$-person team with 2 captains. Therefore, the number of ways to do it must be equal!

---

### 4. Show $P(n, k) = P(n-1, k) + k \cdot P(n-1, k-1)$.
**Proof.** Using $P(n,k) = \frac{n!}{(n-k)!}$:
Right side: $\frac{(n-1)!}{(n-1-k)!} + k \frac{(n-1)!}{(n-k)!}$
$$= \frac{(n-1)!(n-k)}{(n-k)!} + \frac{k(n-1)!}{(n-k)!} = \frac{(n-1)! [n-k+k]}{(n-k)!} = \frac{n!}{(n-k)!} = P(n,k)$$ $\square$

#### Story for $P(n, k) = P(n-1, k) + k \cdot P(n-1, k-1)$

**The Scenario:** You are awarding Gold, Silver, and Bronze medals (or any $k$ ranked positions) to $n$ runners. One of those runners is your best friend, **Alex**.

* **Left Side ($P(n, k)$):** Standard way: Just award the $k$ distinct medals to $n$ people in order.

* **Right Side ($P(n-1, k) + k \cdot P(n-1, k-1)$):** We count based on whether Alex wins a medal or not.
    
    1.  **Case 1: Alex does NOT win a medal.**
        Since Alex is out, we have $n-1$ runners left to fill all $k$ ranked positions. This is $P(n-1, k)$.
        
    2.  **Case 2: Alex DOES win a medal.**
        First, decide which of the $k$ medals Alex wins (there are $k$ choices: Gold, or Silver, or...). 
        Now that Alex's spot is taken, we have $n-1$ runners left to fill the remaining $k-1$ positions. This is $k \cdot P(n-1, k-1)$.

**Conclusion:** Since Alex either wins a medal or he doesn't, adding these two cases together covers every possible way to award the medals.

### 5. Show $\binom{2n}{2} = 2\binom{n}{2} + n^2$.
**Proof.** $\binom{2n}{2} = \frac{2n(2n-1)}{2} = n(2n-1) = 2n^2 - n$.
Right side: $2\frac{n(n-1)}{2} + n^2 = n^2 - n + n^2 = 2n^2 - n$. $\square$

#### The "Descending" Shortcut
In your factorial setup, $\binom{n}{k} = \frac{n!}{k!(n-k)!}$. But when $k$ is a small, specific number like **2**, most of that factorial cancels out.

Think of $\binom{n}{k}$ as: **Start at $n$, write $k$ descending factors, then divide by $k!$.**

For **$\binom{n}{2}$**:
* Start at $n$, go down 2 factors: $n(n-1)$
* Divide by $2!$: $2 \times 1 = 2$
* Result: $\frac{n(n-1)}{2}$

For **$\binom{2n}{2}$**:
* Start at $2n$, go down 2 factors: $2n(2n-1)$
* Divide by $2!$: $2$
* Result: $\frac{2n(2n-1)}{2} = n(2n-1)$

#### Why this works (The Factorial Cancellation)
If we look at $\binom{n}{2}$ purely with factorials:
$$\binom{n}{2} = \frac{n!}{2!(n-2)!} = \frac{n \times (n-1) \times (n-2) \times \dots \times 1}{2 \times 1 \times [(n-2) \times (n-3) \times \dots \times 1]}$$
Everything from $(n-2)$ downward cancels out perfectly, leaving only $\frac{n(n-1)}{2}$.


#### The Story for $\binom{2n}{2} = 2\binom{n}{2} + n^2$

**The Scenario:** You have a group of $n$ boys and $n$ girls (total $2n$ people). You want to pick a team of 2 people.

* **Left Side ($\binom{2n}{2}$):** Just pick any 2 people from the total $2n$. Done.
* **Right Side ($2\binom{n}{2} + n^2$):** Break it down by gender:
    1.  Pick 2 boys: $\binom{n}{2}$ ways.
    2.  Pick 2 girls: $\binom{n}{2}$ ways.
    3.  Pick 1 boy AND 1 girl: $n$ choices for the boy $\times$ $n$ choices for the girl = $n^2$.
    
Add them up: $\binom{n}{2} + \binom{n}{2} + n^2 = 2\binom{n}{2} + n^2$. 


---

### 7. Show $\sum_{k=0}^{p} \binom{m}{k}\binom{n}{p-k} = \binom{m+n}{p}$ (Vandermonde's Identity).
**Proof.** (Combinatorial) Suppose you have a group of $m$ men and $n$ women. You want to choose a committee of $p$ people.
* **Right side:** Choose $p$ people from the total $m+n$.
* **Left side:** Sum up the ways to pick $k$ men and $p-k$ women for all possible values of $k$.
Since both sides count the same thing, they are equal. $\square$

### 10. Show $\sum_{k=0}^{n} k \binom{n}{k} = n 2^{n-1}$.
**Proof.** (Combinatorial) You want to choose a committee from $n$ people and designate one member as the chair.
* **Right side:** Choose the chair first ($n$ choices), then choose any subset of the remaining $n-1$ people to be on the committee ($2^{n-1}$ choices).
* **Left side:** Choose a committee of size $k$ first ($\binom{n}{k}$), then choose one of those $k$ members to be chair. Sum over all possible sizes $k$. $\square$

