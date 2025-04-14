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
- **Definition:** S+ = \x. [false, x]
- **Input:** A numeral n.
- **Output:** A new numeral representing n + 1.
- **Examples:**
  - S+ n0 = n1
  - S+ n1 = n2

---

### 2. P− (Predecessor)

- **Description:** Retrieves the predecessor of a Barendregt numeral.
- **Definition:** P− = \x. x false
- **Input:** A numeral n.
- **Output:** A numeral representing n - 1. If n = 0, returns false.
- **Examples:**
  - P- n0 = false
  - P- n1 = n0

---

### 3. zero (Zero Test)

- **Description:** Checks whether a numeral is zero.
- **Definition:** Zero = \x. x true
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
```

---

## How to Run the Code in Lambda Shell (Detailed Instructions)

---
### **1. Open the Terminal**

Depending on your system:

- **If you're on Debian or another Linux distro:** Press Ctrl + Alt + T to open the terminal.
- **If you're using Windows with WSL (Windows Subsystem for Linux):**
  - Open the **Start Menu**.
  - Search for **"WSL"** or the name of your installed Linux distro (e.g., *Ubuntu*).
  - Click to open it.
---

### **2. Navigate to the Project Folder**

This is the folder where your code file CodigoLambdaShell.txt is saved.

Use the cd (change directory) command to move into that folder.

### **3. Launch Lambda Shell**

Once inside the folder, start the **Lambda Shell** interpreter.

### **4. Load Your File**

Now, load your file with this command:

:l CodigoLambdaShell.txt

---

### **5. Test the Functions**

You can now test the combinators you've defined.

Example tests:

bash
eval S+ n0         -- Returns: n1
eval S+ (S+ n0)    -- Returns: n2
eval P- n1         -- Returns: n0
eval P- n0         -- Returns: false
eval Zero n0       -- Returns: true
eval Zero n1       -- Returns: false

---

  ## References

1. **videos**
   -  How to install WSL for windows 11 (https://youtu.be/lt4UtlUzx9w?si=M2_yQ7ypWq0F5V4c)
2. **PDF**
   - Guidelines for Lambda Shell  (https://asr.github.io/courses/programs-installations-tips-and-tricks.pdf.)
3. **AI Tools:**
   - ChatGPT and DeepSeek for code organization, explanation of lambdaShell and documentation guidance.




