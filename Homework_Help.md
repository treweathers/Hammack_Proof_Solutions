# SUMMARIES
This summary covers the foundational concepts of functions from Sections 12.1 and 12.2 of Hammack's *Book of Proof*. It is formatted for easy use in a GitHub repository or Markdown-based study guide.

---

# Hammack's Book of Proof: Chapter 12 Summary

## 12.1 Functions

In higher-level mathematics, a function is formally defined through the lens of **set theory** rather than just an algebraic "rule."

### Formal Definition
Suppose $A$ and $B$ are sets. A **function** $f$ from $A$ to $B$ (denoted $f: A \to B$) is a **relation** $f \subseteq A \times B$ satisfying the property that for each $a \in A$, the relation contains **exactly one** ordered pair of the form $(a, b)$.
* The statement $(a, b) \in f$ is abbreviated as $f(a) = b$.
* **Vertical Line Test:** This set-theoretic definition is the rigorous version of the vertical line test; every input $a$ has exactly one output $b$.

### Components of a Function
* **Domain:** The set $A$ (the set of all possible "input values").
* **Codomain:** The set $B$ (the "target" set for the outputs).
* **Range:** The subset of the codomain consisting of all actual outputs:
    $$\{f(a) : a \in A\} = \{b : (a, b) \in f\}$$

> **Crucial Note:** The codomain is not intrinsic to the function’s values; it is a choice of context. Any set containing the range can serve as the codomain. However, changing the codomain can change whether a function is considered "surjective."



### Function Equality
Two functions $f: A \to B$ and $g: C \to D$ are **equal** ($f = g$) if:
1.  They are equal as sets of ordered pairs.
2.  Equivalently: They have the same domain ($A = C$) and $f(x) = g(x)$ for every $x \in A$.

---

## 12.2 Injective and Surjective Functions

These properties describe how elements of the domain map to the codomain, determining if a function is "invertible."

### 1. Injective (One-to-One)
A function $f: A \to B$ is **injective** if unequal inputs always result in unequal outputs.
* **Formal Logic:** $\forall a, a' \in A, a \neq a' \implies f(a) \neq f(a')$
* **Proof Strategy (Contrapositive):** Assume $f(a) = f(a')$ and show that it implies $a = a'$. This is usually easier algebraically.



### 2. Surjective (Onto)
A function $f: A \to B$ is **surjective** if every element in the codomain is "hit" by at least one element from the domain.
* **Formal Logic:** $\forall b \in B, \exists a \in A$ such that $f(a) = b$.
* **Condition:** A function is surjective if and only if its **Range = Codomain**.
* **Proof Strategy:** Pick an arbitrary $b \in B$ and solve for $a$ in terms of $b$ to show such an $a$ always exists within the domain $A$.

### 3. Bijective
A function is **bijective** if it is both injective and surjective. A bijection represents a "perfect pairing" between the elements of $A$ and $B$.

---

## Summary of Proof Techniques

| Property | How to Prove It | How to Disprove It |
| :--- | :--- | :--- |
| **Injective** | Assume $f(a) = f(a')$ and algebraically derive $a = a'$. | Find two distinct inputs $a, a'$ such that $f(a) = f(a')$. |
| **Surjective** | Take an arbitrary $b \in B$ and show there exists $a \in A$ where $f(a) = b$. | Find an element $b \in B$ that has no corresponding $a \in A$. |

### Examples from the Text
* **Example 12.4:** $f: \mathbb{R}-\{0\} \to \mathbb{R}$ where $f(x) = \frac{1}{x} + 1$.
    * **Injective:** Yes. If $\frac{1}{a}+1 = \frac{1}{a'}+1$, then $a = a'$.
    * **Surjective:** No. There is no $x$ such that $f(x) = 1$ (since $\frac{1}{x}$ can never be $0$).
* **Example 12.6:** $g: \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z} \times \mathbb{Z}$ where $g(m, n) = (m+n, m+2n)$.
    * This is **bijective**. You prove injectivity by solving the system of equations for equality, and surjectivity by finding the "pre-image" $(x, y)$ for any target $(b, c)$.

---

## Tips for Exercises
* **Ordered Pairs:** Remember that if the domain is $A \times B$, an input is an ordered pair $(m, n)$.
* **Discrete Sets:** For small finite sets, drawing arrow diagrams is often the best way to list all possible functions.
* **Range of Multiples:** In functions like $f(m, n) = 6m - 9n$, the range is related to the greatest common divisor. Here, $GCD(6, 9) = 3$, so the range is all multiples of 3.
Transitivity is often the "boss battle" of relation properties because it involves three elements ($x, y, z$) and two separate assumptions. While Symmetry is about a "flip," Transitivity is about a **"chain."**

### The Logical Template
To prove Transitivity, you must show: **If $xRy$ and $yRz$, then $xRz$.**

1.  **The Setup:** Assume $xRy$ AND $yRz$ are both true.
2.  **The Unpacking:** Write out what the relation means for both pairs using algebra.
3.  **The Substitution/Bridge:** This is the hard part. You must combine the two algebraic statements to eliminate the "middleman" ($y$).
4.  **The Conclusion:** Show that the resulting relationship between $x$ and $z$ fits the original rule.


### Why Transitivity Fails (The Visual Check)
In a diagram, Transitivity means: **If there is an arrow from $x$ to $y$ and an arrow from $y$ to $z$, there MUST be a direct shortcut arrow from $x$ to $z$.**

If you can find a "path" of two arrows ($x \to y \to z$) but no shortcut exists ($x \to z$), the relation is **not** transitive.

### The "5-Minute Professor" Tip
When working on Transitivity for the Hammack problems, look for the "Middleman" ($y$).
* In **Equality/Congruence:** $y$ is usually substituted out.
* In **Divisibility ($a|b$):** $y$ is usually eliminated by multiplying the two equations.
* In **Parity/Summation:** $y$ is usually eliminated by adding or subtracting the equations (like we did above).



