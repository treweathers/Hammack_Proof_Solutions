# Chapter 11: Relations
That is the million-dollar question! The "proof paralysis" usually happens because a relation can be defined in so many different ways (equations, divisibility, set notation).

The secret is to look at the **verb** or **symbol** used in the definition. That tells you which "math language" to speak. 

Here is a simple field guide to help you decide your method:

---

### 1. If the definition uses an Equation ($=$)
* **Examples:** $x - y = 5k$, or $3x + y = 4k$, or $x^2 = y^2$.
* **The Method:** **Algebraic Substitution.**
* **The Mindset:** You are a lawyer looking for a specific "form." If the rule says the result must be $5k$, your only job is to manipulate your variables until a $5$ can be factored out.

### 2. If the definition uses "Same something"
* **Examples:** "Same parity," "Same age," "Same first letter."
* **The Method:** **Case Analysis or Descriptive Logic.**
* **The Mindset:** You don't need much math here. You just need to show that if $x$ is in Category A, and $x$ and $y$ match, then $y$ must also be in Category A.

### 3. If the definition uses Divisibility ($|$)
* **Examples:** $n \mid (a - b)$.
* **The Method:** **Definition Expansion.**
* **The Mindset:** Immediately rewrite $a \mid b$ as $b = ak$. Once you have it in that "linear" form, you can add, subtract, or multiply just like the algebraic method above.

### 4. If the definition uses Sets ($\in$ or $\subseteq$)
* **Examples:** $A \cap B = A$, or $x \in \mathcal{P}(A)$.
* **The Method:** **Element Chasing.**
* **The Mindset:** Pick a generic "neighbor" ($x$). If $x$ is in the first set, use the rules to "chase" it until you prove it must also be in the second set.

---

### The "Vibe Check" Table
When you read the problem, ask: **"What is the hurdle?"**

| If the rule looks like... | Use this strategy... | Why? |
| :--- | :--- | :--- |
| **A Calculation** ($x-y \in \mathbb{Z}$) | **Algebra** | You need to prove a numerical property. |
| **A Comparison** ($f(x) = f(y)$) | **Function Logic** | You are checking if two outputs land in the same spot. |
| **A Property** (Both are prime) | **Logic/Counterexample** | Properties are often "all or nothing." |

---

### A Quick Pro-Tip for the Final:
If you are asked to **disprove** a relation (show it is *not* an equivalence relation), **do not use algebra.** Use a **counterexample** with real numbers. 

> **Teacher:** "Is $xRy$ defined by $x+y$ is even transitive on $\mathbb{Z}$?"
>
> **You (Pro-mode):** "Let $x=1, y=2, z=3$. $1+2=3$ (odd), so the chain never even starts."
>
> **Wait, let's try a better one:** "Is $x \neq y$ transitive?" 
>
> **You:** "Let $x=5, y=6, z=5$. $5 \neq 6$ and $6 \neq 5$, but $5 = 5$. Boom. Not transitive."



Does seeing those categories help narrow down the "guessing game" of how to start? Which problem from your list should we apply this "Field Guide" to next? Maybe an **if and only if** from Chapter 7?
