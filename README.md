# Barendregt Numerals in Lambda Shell

## Samuel Correa Velasquez

---

## Environment and Tools Used

- **Operating System:** Debian 12.10 (via WSL on Windows 11)
- **Interpreter:** Lambda Shell
- **Haskell Compiler:** GHC 9.4.8

---
3. **Detailed instructions for running the code:**
   - Now you can evaluate the behavior of the implemented operations by using the eval command followed by the expression you want to evaluate.
   - Here are some examples:

     - **Successor (S+) Examples:**
       
       eval S+ n0
       eval S+ (S+ n0)
       
       *(Expected output: n1, n2 respectively)*

     - **Predecessor (P-) Examples:**
       
       eval P- n1
       eval P- n0
       
       *(Expected output: n0, false respectively)*

     - **Zero Test (Zero) Examples:**
       
       eval Zero n0
       eval Zero n1
       
       *(Expected output: true, false respectively)*

   - Observe the output of each command to verify the correct behavior of the Barendregt numeral operations.

---

---

## References

1. **videos**
   -  How to install WSL for windows 11 (https://youtu.be/lt4UtlUzx9w?si=M2_yQ7ypWq0F5V4c)
2. **PDF**
   - Guidelines for Lambda Shell  (https://asr.github.io/courses/programs-installations-tips-and-tricks.pdf.)
3. **AI Tools:**
   - ChatGPT and DeepSeek for code organization, explanation of lambdaShell and documentation guidance.




