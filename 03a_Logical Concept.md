# Logical Concept

# Satisfiability (SAT), Validity (Tautology), Contradiction (UNSAT), and Falsifiability

## 🔹Satisfiability (SAT)

- **Definition:** A logical expression is **satisfiable (SAT)** if there exists **at least one assignment** of truth values that makes the expression **true**.
- **Key Point:** Only **one true assignment** is needed to be satisfiable.
- **Example:**
    - **( P Q )** (P OR Q)
        - If ( P = ), the expression is true.
        - If ( Q = ), the expression is also true.
        - **Therefore, it is satisfiable.**

> 注释（中文解释）： SAT 只要求在某种情况下为真即可。
> 

---

## 🔹Validity (Tautology)

- **Definition:** A logical expression is **valid (or tautology)** if it is **true in all possible cases**.
- **Key Point:** Must be **true under every possible assignment** of truth values.
- **Example:**
    - **( P P )** (P OR NOT P)
        - No matter if ( P ) is true or false, the whole expression is always true.
        - **Hence, it is a tautology.**

> 注释： Tautology 表示“永远为真”的公式，任何情况下都成立。
> 

---

## 🔹Contradiction (UNSAT)

- **Definition:** A logical expression is **unsatisfiable (UNSAT)** if it is **false in all possible cases**.
- **Key Point:** There is **no assignment** that makes the expression true.
- **Example:**
    - **( P P )** (P AND NOT P)
        - It’s impossible for ( P ) and ( P ) to be true at the same time.
        - **Therefore, it is a contradiction.**

> 注释： UNSAT 表示永远不可能为真的公式，即“矛盾式”。
> 

---

## 🔹Falsifiability (Falsifiable) 【Supplementary Concept】

- **Definition:** A logical expression is **falsifiable** if there exists **at least one assignment** that makes the expression **false**.
- **Key Point:**
    - **If you can find even one case where it’s false, it’s falsifiable.**
    - Most expressions that are **satisfiable but not tautologies** are falsifiable.
- **Example:**
    - **( P Q )** (P AND Q)
        - When ( P = , Q = ), the expression is true.
        - But if either ( P = ) or ( Q = ), the expression is false.
        - **Hence, it is falsifiable.**

> 注释： Falsifiable 只需存在一种情况下为假。Tautology 不可伪，但 SAT 的表达式通常是可伪的。
> 

---

## 🚀 Core Relationships Summary

| **Category** | **Definition** | **Truth Condition** | **Relationship with Other Concepts** |
| --- | --- | --- | --- |
| **SAT (Satisfiable)** | At least one assignment makes it true | True in at least one case | **Tautology** is a special case of SAT |
| **Tautology (Valid)** | True in all cases | **Cannot be false** | **Non-falsifiable** |
| **UNSAT (Unsatisfiable)** | No assignment makes it true | **Always false** | **Always falsifiable** |
| **Falsifiable (Falsifiable)** | At least one assignment makes it false | False in at least one case | All non-tautologies are falsifiable |

---

## 🎯 Example Summary

| **Expression** | **SAT (Satisfiable)** | **Tautology (Valid)** | **UNSAT (Contradiction)** | **Falsifiable** |
| --- | --- | --- | --- | --- |
| ( P Q ) | ✅ | ❌ | ❌ | ✅ |
| ( P P ) | ✅ | ✅ | ❌ | ❌ |
| ( P P ) | ❌ | ❌ | ✅ | ✅ |

---

## 🔑 Summary

- **Tautology:** Always true → **Non-falsifiable**.
- **Satisfiable (but not Tautology):** True in some cases, false in others → **Falsifiable**.
- **Contradiction (UNSAT):** Always false → **Falsifiable** and **Unsatisfiable**.

Understanding these relationships helps quickly determine the nature of logical expressions! 🚀