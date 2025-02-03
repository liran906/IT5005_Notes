# Propositional Logic

## 🔹 1. Conditional Statements

A **conditional statement** (条件语句) *p* → *q* is **false** exactly when *p* is true and *q* is false; otherwise it is true.

- *p* is called the **hypothesis (先行条件)**
- *q* is called the **conclusion (结论)**
- Formally:

$$
p → q ≡ ¬p ∨ q
$$

(Brief note: “not *p* or *q*”)

**Truth Table**

| *p* | *q* | *p* → *q* |
| --- | --- | --- |
| T | T | T |
| T | F | F |
| F | T | T |
| F | F | T |

> 💭 Note: Only when p is true and q is false does p → q become false.
> 

---

## 🔹 2. Logical Equivalences (逻辑等价)

**Common laws:**

| **Law** | **Form** |
| --- | --- |
| **Commutative** (交换律) | *p* ∧ *q* ≡ *q* ∧ *p* ｜ *p* ∨ *q* ≡ *q* ∨ *p* |
| **Associative** (结合律) | (*p* ∧ *q*) ∧ *r* ≡ *p* ∧ (*q* ∧ *r*) ｜  (*p* ∨ *q*) ∨ *r* ≡ *p* ∨ (*q* ∨ *r*) |
| **Distributive** (分配律) | *p* ∧ (*q* ∨ *r*) ≡ (*p* ∧ *q*) ∨ (*p* ∧ *r*) ｜ *p* ∨ (*q* ∧ *r*) ≡ (*p* ∨ *q*) ∧ (*p* ∨ *r*) |
| **Identity** (恒等律) | *p* ∧ true ≡ *p  ;*  *p* ∨ false ≡ *p* |
| **Negation** (否定律) | *p* ∨ ¬*p* ≡ true  |  *p* ∧ ¬*p* ≡ false |
| **Double Negation** | ¬(¬*p*) ≡ *p* |
| **De Morgan’s** (德摩根) | ¬(*p* ∧ *q*) ≡ ¬*p* ∨ ¬*q*  |  ¬(*p* ∨ *q*) ≡ ¬*p* ∧ ¬*q* |
| **Absorption** (吸收律) | *p* ∨ (*p* ∧ *q*) ≡ *p*  |  *p* ∧ (*p* ∨ *q*) ≡ *p* |

**❗️Be Careful with Mixed Operators (∧ and ∨)**

You **cannot remove parentheses** if the expression contains a mix of **AND (∧)** and **OR (∨)** without considering operator precedence.

•	**Incorrect:**  $(P \lor (Q \land R)) \neq P \lor Q \land R$

•	**Reason:**

•	**AND (∧)** has higher precedence than **OR (∨)**.

•	Removing parentheses here **changes the meaning** of the expression.

---

## 🔹 3. Contrapositives, Converses, and Inverses

| **Variant** | **Symbol** | **Equivalent?** | **Brief Meaning** |
| --- | --- | --- | --- |
| **Original** | *p* → *q* | — | “If *p*, then *q*.” |
| **Contrapositive** | ¬*q* → ¬*p* | *p* → *q* | “If not *q*, then not *p*.” |
| **Converse** | *q* → *p* | ¬*p* → ¬*q* | “If *q*, then *p*.” |
| **Inverse** | ¬*p* → ¬*q* | *q* → *p* | “If not *p*, then not *q*.” |
- **Key Points**:
    - *p* → *q* is logically equivalent to ¬*q* → ¬*p*.
    - *p* → *q* is **not** equivalent to *q* → *p*.
    - ¬*p* → ¬*q* is equivalent to *q* → *p*, but **not** to *p* → *q*.

---

## 🔹 4.  **Implication Law**

$$
p → q ≡ ¬p ∨ q
$$

**Negation of Conditional Statement：**

$$
¬(p → q) ≡ ¬(¬p ∨ q) ≡ p ∧ ¬q
$$

---

## 🔹 5. Basic Rules of Inference

| **Rule** | **Form** | **Explanation** |
| --- | --- | --- |
| **Modus Ponens** (肯定前件) | 1. *p* → *q*  2. *p*  ∴ *q* | If “*p* → *q*” **and** *p* is true, then *q* must be true. |
| **Modus Tollens** (否定后件) | 1. *p* → *q*  2. ¬*q*  ∴ ¬*p* | If “*p* → *q*” but *q* is false, then *p* must be false. |
| **Generalization** | 1. *p*  ∴ *p* ∨ *q* | From *p*, infer “*p* ∨ *q*.” |
| **Specialization** | 1. *p* ∧ *q*  ∴ *p* | From *p* ∧ *q*, infer *p*. |
| **Conjunction** | 1. *p*  2. *q*  ∴ *p* ∧ *q* | If both *p* and *q* are true individually, then *p* ∧ *q* is also true. |
| **Elimination** | 1. *p* ∨ *q*  2. ¬*p*  ∴ *q* | If “*p* ∨ *q*” is true and *p* is false, then *q* must be true (and vice versa). |
| **Transitivity** | 1. *p* → *q*  2. *q* → *r*  ∴ *p* → *r* | If *p* → *q* and *q* → *r*, then *p* → *r*. |
| **Proof by Cases** | 1. *p* ∨ *q*  2. *p* → *r*  3. *q* → *r*  ∴ *r* | If one of *p* or *q* is true, and each one implies *r*, then *r* must be true. |
| **Contradiction** | 1. ¬*p* → false  ∴ *p* | If ¬*p* leads to a contradiction, then *p* must be true. |

> 📝 Tip: These rules (规则) form the backbone of propositional logic proofs.
> 

---

## 🔹 6. Necessary vs. Sufficient Conditions

- **“*r* is a sufficient condition for *s*”** means *r* → *s*.
    
    (Sufficient: if *r* happens, *s* follows.)
    
- **“*r* is a necessary condition for *s*”** means *s* → *r* (or ¬*r* → ¬*s*).
    
    (Necessary: if *r* is missing, *s* cannot be true.)
    

---

## 🔹 7. Equivalence *p* ↔︎ *q*

By definition:
*p* ↔︎ *q* ≡ (*p* → *q*) ∧ (*q* → *p*)

This is **true** exactly when *p* and *q* share the same truth value.

| *p* | *q* | *p* ↔︎ *q* |
| --- | --- | --- |
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | T |

---

## 🔹 8. Example Equivalence: (*p* ∨ *q*) → *r*

**Claim**:
(*p* ∨ *q*) → *r* ≡ (*p* → *r*) ∧ (*q* → *r*)

**Truth Table**:

| *p* | *q* | *r* | *p* ∨ *q* | *p* → *r* | *q* → *r* | (*p* ∨ *q*) → *r* | (*p* → *r*) ∧ (*q* → *r*) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| T | T | T | T | T | T | T | T |
| T | T | F | T | F | F | F | F |
| T | F | T | T | T | T | T | T |
| T | F | F | T | F | T | F | F |
| F | T | T | T | T | T | T | T |
| F | T | F | T | T | F | F | F |
| F | F | T | F | T | T | T | T |
| F | F | F | F | T | T | T | T |

---

## 🔹 Final Takeaways 🏆

| **Point** | **Summary** |
| --- | --- |
| **1. Logical Equivalences** | Key to rewriting propositional formulas in different but equivalent forms (e.g. De Morgan’s). |
| **2. Inference Rules** | (Modus Ponens, Modus Tollens, etc.) are the backbone of proofs in propositional logic. |
| **3. Necessary vs. Sufficient** | Helps interpret statements: “*r* is necessary for *s*” vs. “*r* is sufficient for *s*.” |
| **4. Conditionals & Variants** | Contrapositive is equivalent, but converse/inverse are generally not. Check them carefully in formal proofs. |

> ✅ Tip: Practice with concrete examples to internalize these rules.
> 
> 
> **❌ Common Pitfall**: Mixing up “*p* → *q*” and “*q* → *p*,” or confusing necessary vs. sufficient conditions.
> 

[Logical Concept](Propositional%20Logic%2018d28e7162a5803e89c1d9d5706955e9/Logical%20Concept%2018d28e7162a5806ab2ade0533ec12e07.md)

[tut2](Propositional%20Logic%2018d28e7162a5803e89c1d9d5706955e9/tut2%2018d28e7162a580918404fb7602b8783d.md)
