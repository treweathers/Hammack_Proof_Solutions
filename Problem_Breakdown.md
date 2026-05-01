# Chapter 11
### 11.2.9
This is a perfect problem to "anchor" your understanding of relations because it connects simple number properties (even/odd) to the abstract rules of equivalence.

Let’s tear this apart step-by-step.

---

### The Setup
* **The Set:** $\mathbb{Z}$ (all integers: $\{\dots, -2, -1, 0, 1, 2, \dots\}$).
* **The Condition:** $xRy \iff x$ and $y$ have the **same parity**. 
    * This means they are either **both even** or **both odd**.

---

### 1. Is $R$ Reflexive?
**The Test:** For every integer $a$, is it true that $aRa$? 
* **Logic:** Does $a$ always have the same parity as $a$? 
* **Proof:** Take any integer $a$. If $a$ is even, then $a$ is even. If $a$ is odd, then $a$ is odd. In either case, $a$ has the same parity as itself.
* **Verdict:** **Yes, $R$ is reflexive.**

### 2. Is $R$ Symmetric?
**The Test:** If $xRy$, must it be true that $yRx$?
* **Logic:** If $x$ and $y$ have the same parity, do $y$ and $x$ have the same parity?
* **Proof:** Assume $xRy$. This means $x$ and $y$ are both even or both odd. If $x$ and $y$ are both even, then $y$ and $x$ are both even. If they are both odd, then $y$ and $x$ are both odd. In either case, $y$ has the same parity as $x$.
* **Verdict:** **Yes, $R$ is symmetric.**

### 3. Is $R$ Transitive?
**The Test:** If $xRy$ and $yRz$, must it be true that $xRz$?
* **Logic:** If $x$ matches $y$, and $y$ matches $z$, does $x$ match $z$?
* **Proof:** Assume $xRy$ and $yRz$. 
    * **Case 1:** $y$ is even. Since $xRy$, $x$ must be even. Since $yRz$, $z$ must be even. Therefore, $x$ and $z$ are both even ($xRz$).
    * **Case 2:** $y$ is odd. Since $xRy$, $x$ must be odd. Since $yRz$, $z$ must be odd. Therefore, $x$ and $z$ are both odd ($xRz$).
* **Verdict:** **Yes, $R$ is transitive.**

---

### What "Familiar Relation" is this?
Since $R$ is reflexive, symmetric, and transitive, it is an **Equivalence Relation**. But it has a more specific name in number theory:

**Congruence Modulo 2 ($x \equiv y \pmod 2$)**



**Why?** * Two numbers have the same parity if and only if their **difference is even**.
* If $x$ and $y$ are both even: $x - y = \text{even}$.
* If $x$ and $y$ are both odd: $x - y = \text{even}$ (e.g., $7 - 3 = 4$).
* If one is even and one is odd: $x - y = \text{odd}$ (they are *not* related).

This relation splits the entire universe of integers into exactly two "clubs" (Equivalence Classes):
1.  **$[0]$**: The set of all even integers.
2.  **$[1]$**: The set of all odd integers.

### Summary for the Exam:
If you see a "parity" problem, remember it's just a fancy way of saying "Are they in the same Even/Odd group?" Since every number stays in its own group, it's always going to be an **equivalence relation**.

**Does that help visualize the "tests" better? Which section should we dive into next—maybe a tricky Induction or a Set Proof?**

### 11.2.13
I totally get that. In math, sometimes the more "obvious" a thing seems, the harder it is to write down because you feel like you’re just stating the same thing over and over.

The trick to **11.2.13** is to realize that the "rule" for the relation is a **membership test**. To see if $x$ is related to $y$, you subtract them. If the result is an integer (no decimals), they pass.

Here is the "Layered" setup you can use for almost any relation proof on the final.

---

### The Setup
* **The Set:** $\mathbb{R}$ (all real numbers, including $3.14$, $\sqrt{2}$, etc.)
* **The Rule:** $xRy \iff x - y \in \mathbb{Z}$ (the difference is a "whole" number)

---

### Layer 1: Reflexive
**Goal:** Show $xRx$ for every $x \in \mathbb{R}$.
* **Step 1:** Pick an arbitrary element: "Let $x \in \mathbb{R}$."
* **Step 2:** Test the rule: "Consider $x - x$."
* **Step 3:** Calculate: "$x - x = 0$."
* **Step 4:** Connect to the condition: "Since $0$ is an integer ($0 \in \mathbb{Z}$), the condition $x - x \in \mathbb{Z}$ is satisfied."
* **Conclusion:** "Therefore, $R$ is reflexive."

### Layer 2: Symmetric
**Goal:** Show that if $xRy$, then $yRx$.
* **Step 1:** Start with the assumption: "Suppose $xRy$ for some $x, y \in \mathbb{R}$."
* **Step 2:** Unpack what that means: "This means $x - y = k$ for some integer $k \in \mathbb{Z}$."
* **Step 3:** Manipulate to look like the target ($y - x$): "Then $y - x = -(x - y) = -k$."
* **Step 4:** Logic check: "Since $k$ is an integer, its negative $-k$ is also an integer."
* **Step 5:** Link back: "Since $y - x \in \mathbb{Z}$, it follows that $yRx$."
* **Conclusion:** "Therefore, $R$ is symmetric."

### Layer 3: Transitive
**Goal:** Show that if $xRy$ and $yRz$, then $xRz$.
* **Step 1:** Start with the assumption: "Suppose $xRy$ and $yRz$ for some $x, y, z \in \mathbb{R}$."
* **Step 2:** Unpack both:
    * "$x - y = k$ for some integer $k \in \mathbb{Z}$."
    * "$y - z = m$ for some integer $m \in \mathbb{Z}$."
* **Step 3:** Use algebra to get $x$ and $z$ together. (Hint: Add the equations to cancel out $y$):
    * "$(x - y) + (y - z) = k + m$"
    * "$x - z = k + m$"
* **Step 4:** Logic check: "Since $k$ and $m$ are integers, their sum $k + m$ is also an integer ($k+m \in \mathbb{Z}$)."
* **Step 5:** Link back: "Since $x - z$ is an integer, $xRz$."
* **Conclusion:** "Therefore, $R$ is transitive."

---

### Why this is an Equivalence Relation (The "Vibe")
Think about what this relation is actually doing. If $x - y$ is an integer, it means $x$ and $y$ have the **exact same decimal part**.



* **Example:** $0.5, 1.5, 2.5, 10.5$ are all related to each other because subtracting any two gives a clean integer ($1.5 - 0.5 = 1$).
* **Example:** $\pi$ and $\pi - 3$ are related.

On the final, if you get stuck, remember this "Unpack $\to$ Manipulate $\to$ Re-pack" flow:
1.  **Unpack:** Turn the symbol $xRy$ into an equation ($x - y = k$).
2.  **Manipulate:** Do algebra to get the equation to look like the property you need.
3.  **Re-pack:** Turn the equation back into the symbol ($yRx$ or $xRz$).

**Does that "Layered" template make the setup feel a bit more manageable? Want to try applying it to a Set Proof (Chapter 8) or move to Induction?**

