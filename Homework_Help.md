# SUMMARIES

---

# 📘 Summary: Hammack's Book of Proof – Chapter 12.1

## 1. Formal Definition of a Function
In advanced mathematics, a function is not just a "rule" or "formula"; it is a specific type of **set**.

> **Definition 12.1:** A function $f$ from set $A$ to set $B$ (denoted $f: A \to B$) is a **relation** $f \subseteq A \times B$ such that for every $a \in A$, there is **exactly one** ordered pair $(a, b) \in f$.

* **Notation:** We write $f(a) = b$ as an abbreviation for $(a, b) \in f$.
* **Vertical Line Test:** In set terms, this means no two distinct pairs in the set $f$ can have the same first coordinate.



## 2. Domain, Codomain, and Range
There are three distinct sets associated with every function $f: A \to B$:

| Term | Definition | Informal Meaning |
| :--- | :--- | :--- |
| **Domain** | The set $A$. | All possible "inputs." |
| **Codomain** | The set $B$. | The "target" set or allowed types of output. |
| **Range** | $\{f(a) : a \in A\}$ | The set of values that *actually* come out. |

**Key Insight:** The **Range** is always a subset of the **Codomain** ($\text{Range} \subseteq B$), but they are not always equal. The codomain is often a matter of context (e.g., $f(n) = |n|$ could have a codomain of $\mathbb{N}$, $\mathbb{Z}$, or $\mathbb{R}$).

## 3. Function Equality
**Definition 12.3:** Two functions $f$ and $g$ are equal if:
1.  They have the same **domain**.
2.  $f(x) = g(x)$ for every $x$ in that domain.

*Note:* Functions can be equal even if they are assigned different codomains, provided the sets of ordered pairs (the relations) are identical.

## 4. Visualizing Functions
* **Traditional Graphs:** Best for functions with numerical domains/codomains (e.g., $\mathbb{R} \to \mathbb{R}$).
* **Arrow Diagrams:** Best for finite sets or abstract structures. An arrow points from $a \in A$ to $b \in B$ if $f(a) = b$.



---
*Summary based on "Book of Proof" by Richard Hammack.*


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



