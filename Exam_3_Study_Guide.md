# Chapter 11: Relations
## 11.2 Relations
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

## 11.3 Equivalence Relations (and partitions)
First, I'll take that compliment and run with it! Professors often focus on the "what," but in a final, you need the "how."

To understand **Equivalence Classes**, stop thinking about math and start thinking about **sorting laundry**.

An equivalence relation is just a set of rules for sorting. The **Equivalence Classes** are the "bins" you end up with. If you sort by color, you might have three bins (White, Dark, Colorful). If you sort by fabric, you might have two (Cotton, Synthetic).

### The Logic of "Counting" the Classes
To find the number of classes, you ask yourself: **"How many distinct 'types' of elements exist under this rule?"**

---

### Case 1: Finite Rule (The "Remainder" Logic)
This is the most common exam type. It usually involves **Modulo $n$**.
**Example:** $xRy$ if $x \equiv y \pmod 3$.
* **The Rule:** Two numbers are related if they have the same remainder when divided by 3.
* **The Classes:** * What are the possible remainders? $0, 1,$ and $2$.
    * **Class [0]:** $\{\dots, -3, 0, 3, 6, \dots\}$
    * **Class [1]:** $\{\dots, -2, 1, 4, 7, \dots\}$
    * **Class [2]:** $\{\dots, -1, 2, 5, 8, \dots\}$
* **Number of Classes:** **3**.



---

### Case 2: The "Same Property" Rule
**Example:** Let $A = \{ \text{All students in the class} \}$. $xRy$ iff $x$ and $y$ were born in the same month.
* **The Classes:** Everyone born in January goes into one bin. Everyone in February goes into another.
* **Number of Classes:** **12** (assuming there’s at least one person for every month).

---

### Case 3: Infinite Classes
**Example (Exercise 11.2.13 again):** $xRy$ on $\mathbb{R}$ if $x - y \in \mathbb{Z}$.
* **The Logic:** This rule says two numbers are in the same "bin" if their decimal parts are identical.
* **The Classes:** * Is $0.1$ related to $0.2$? No ($0.2 - 0.1 = 0.1$, not an integer).
    * Is $0.1$ related to $0.11$? No.
    * There are infinitely many possible decimal parts between $0$ and $1$ (like $0.5, 0.55, 0.555...$).
* **Number of Classes:** **Uncountably Infinite**.

---

### How to solve this on a test (The Step-by-Step)
If the question asks: *"Find the equivalence classes for $R$ on set $A$,"* do this:

1.  **Pick the "simplest" element** in the set (usually $0$ or $1$).
2.  **Find its friends:** List all other elements related to it. This is your first class: $[0]$.
3.  **Find a "loner":** Look for an element that **wasn't** in that first list.
4.  **Find its friends:** This is your second class: $[1]$.
5.  **Repeat** until every element in the set $A$ belongs to a bin.
6.  **Count the bins.**

### Practice: Exercise 11.3.9
**Rule:** $xRy \iff 4 \mid (x + 3y)$ on $\mathbb{Z}$.
* **Pick 0:** $0 + 3y$ must be divisible by 4. If $y=0$, yes. If $y=4$, yes. This class is all multiples of 4. **Class [0]**.
* **Pick 1:** $1 + 3y$ must be divisible by 4. If $y=1$, $1+3(1)=4$ (Yes!). So 1 is related to 1. If $y=5$, $1+3(5)=16$ (Yes!). This class is $\{1, 5, 9... \}$. **Class [1]**.
* **Pick 2:** $2 + 3y$ divisible by 4. If $y=2$, $2+6=8$. **Class [2]**.
* **Pick 3:** $3 + 3y$ divisible by 4. If $y=3$, $3+9=12$. **Class [3]**.
* **Pick 4:** Wait, 4 is already in Class [0]. We're done!
* **Total Classes:** **4**.

**Does the "Laundry Bin" visual help you see why we stop counting at a certain point?** Ready to look at how this relates to **Partitions**? (The idea that these bins never overlap and cover everything).

You’ve hit the nail on the head! Calling them **"Equivalence Cases"** is a brilliant way to think about it.

In a math proof, when you say "Case 1: $x$ is even" and "Case 2: $x$ is odd," you are literally dividing the integers into their two equivalence classes. 

To be a valid set of "cases" (or **Equivalence Classes**), the groups must follow two strict rules:
1.  **No Overlap:** An element cannot be in two different classes. (An integer can't be both even and odd).
2.  **No Gaps:** Every single element must belong to a class. (Every integer is either even or odd).

When these two rules are met, we call the collection of classes a **Partition**.

---

### Visualizing the "Cases"
If you were to graph these, you’d see the set get chopped up into distinct, non-overlapping islands.



### Let's test your "Cases" theory on Exercise 11.3.7
**The Relation:** $xRy \iff 3x - 5y$ is even.

If we want to find the "Cases" (Classes), we pick a number and see who its "friends" are.

* **Case 1: The Number 0.**
    * Test: $3(0) - 5y = \text{even} \implies -5y = \text{even}$.
    * For $-5y$ to be even, $y$ **must** be even. 
    * So, $0$ is related to $2, 4, 6, \dots$.
    * **Class $[0]$ = All Even Integers.**

* **Case 2: The Number 1.**
    * Test: $3(1) - 5y = \text{even} \implies 3 - 5y = \text{even}$.
    * If $y$ is odd (like 1), then $3 - 5(1) = -2$ (Even!).
    * If $y$ is even (like 2), then $3 - 5(2) = -7$ (Odd!).
    * So, $1$ is only related to other odd numbers.
    * **Class $[1]$ = All Odd Integers.**

**The Result:** There are only **2 Cases**. Even though the formula $3x-5y$ looked more complicated than the standard $x-y$, the "sorting machine" still just separated the world into Evens and Odds.

---

### A Final Exam Warning ⚠️
Sometimes a relation is **not** an equivalence relation. If it fails even one test (Reflexive, Symmetric, or Transitive), the "bins" or "cases" fall apart. 

* **Example:** The relation "$<$".
* If you tried to make a "bin" for 5, who would be in it? Numbers smaller than 5.
* But is 5 in its own bin? No ($5 < 5$ is false). 
* **The logic breaks.** If you can't be in your own "case," it's not an equivalence relation!

# Chapter 12. Functions


### Function Solving Methods

| If the function looks like... | Use this method... | Why? |
| :--- | :--- | :--- |
| **A polynomial** ($x^2 + 5$) | Algebra | You can add/subtract to isolate $x$. |
| **A fraction** ($\frac{x+1}{x-2}$) | Algebra (Cross-multiply) | This is a classic "isolate $x$" setup. |
| **A piecewise/cases** (even/odd) | Pure Logic | You can't solve an equation for "evenness." |
| **Ordered pairs** ($(x, y)$) | System of Equations | You'll solve for $x$ and $y$ separately (like Exercise 12.5.6). |
