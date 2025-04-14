# Barendregt Numerals in Lambda Shell

## Samuel Correa Velasquez

---

## Environment and Tools Used

- **Operating System:** Debian 12.10 (via WSL on Windows 11)
- **Interpreter:** Lambda Shell
- **Haskell Compiler:** GHC 9.4.8

---

## Combinators Specification

### 1. S+ (Successor)
- **Description:** Constructs the successor of a Barendregt numeral.
- **Definition:** S+ = λx. [false, x]
- **Input:** A numeral n.
- **Output:** A new numeral representing n + 1.
- **Examples:**
  - S+ n0 = n1
  - S+ n1 = n2

---

### 2. P− (Predecessor)
- **Description:** Retrieves the predecessor of a Barendregt numeral.
- **Definition:** P− = λx. x false
- **Input:** A numeral n.
- **Output:** A numeral representing n - 1. If n = 0, returns false.
- **Examples:**
  - P- n0 = false
  - P- n1 = n0

---

### 3. zero (Zero Test)
- **Description:** Checks whether a numeral is zero.
- **Definition:** Zero = λx. x true
- **Input:** A numeral n.
- **Output:** Returns true if n = 0, otherwise returns false.
- **Examples:**
  - Zero n0 = true
  - Zero n1 = false

---

## Lambda Definitions

```haskell
-- Booleans
let true  = \x.\y.x
let false = \x.\y.y
let I     = \x.x

-- Pairs and projections
let pair = \m.\n.\z.z m n
let fst  = \p.p true
let snd  = \p.p false

-- Numerals
let n0 = I
let n1 = pair false n0
let n2 = pair false n1
let n3 = pair false n2

-- Combinators
let S+   = \x. pair false x
let P-   = \x. x false
let Zero = \x. x true
