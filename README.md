# Barendregt Numerals in Lambda Shell

## Samuel Correa Velasquez

---

## Environment and Tools Used

- **Operating System:** Debian 12.10 (via WSL on Windows 11)
- **Interpreter:** Lambda Shell
- **Haskell Compiler:** GHC  version 9.6.7

---

## Detailed instructions for running the code

To execute the Barendregt numeral operations in the Lambda Shell, follow these steps:

1. **Open Lambda Shell:**
   - Open your terminal or WSL terminal if you are using Windows.
   - Navigate to the directory where your Lambda Shell code file (Codigo.lam) is located using the "cd" command.
   - Start the Lambda Shell interpreter by typing "lambda-shell".

2. **Load the Code File:**
   - Once the Lambda Shell is running, load your code definitions using the ":load" command followed by the filename:
     
     :load Codigo.lam
     
   - The Lambda Shell will process the file, and the defined combinators 
     (like true, false, pair, fst, snd, S+, P-, Zero, and the numeral definitions n0, n1, etc.)
      will be available in the environment.
3. **Execute Test Commands:**
   - Now you can evaluate the behavior of the implemented operations.
   - Here are some examples:

     - **Successor (S+) Examples:**
       
        S zero <br>
        S (S zero)
       
       *(Expected output: one, two respectively)*

     - **Predecessor (P-) Examples:**
       
        P one <br>
        P zero
       
       *(Expected output: zero, false respectively)*

     - **Zero Test (Zero) Examples:**
       
        isZero zero <br>
        isZero one
       
       *(Expected output: true, false respectively)*

   - Observe the output of each command to verify the correct behavior of the Barendregt numeral operations.

---

## References

1. **videos**
   -  How to install WSL for windows 11 (https://youtu.be/lt4UtlUzx9w?si=M2_yQ7ypWq0F5V4c)
2. **PDF**
   - Guidelines for Lambda Shell  (https://asr.github.io/courses/programs-installations-tips-and-tricks.pdf.)
3. **AI Tools:**
   - ChatGPT and DeepSeek for code organization, explanation of lambdaShell and documentation guidance.






