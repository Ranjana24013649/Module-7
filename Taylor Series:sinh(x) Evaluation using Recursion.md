# 📐 Taylor Series:sinh(x) Evaluation using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate the value of **sinh(x)** for **n terms** using recursion.

---

## 🧠 ALGORITHM:

1. **Start**
2. Read input for variable `x` (angle or number)
3. Read input for variable `n` (number of terms)
4. Define a function `fact(n)`:
   - If `n <= 1`, return 1
   - Else, return `n * fact(n - 1)` (recursive factorial)
5. Define a function `sinh(x, n)`:
   - If `n == 0`, return `x`
   - Else, return `(pow(x, 2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)`
6. Call the `sinh(x, n)` function and print the result
7. **Stop**

---

## 💻 PROGRAM:

ADD CODE HERE

power = 1

fact = 1

def taylor_series(x, n):

    global power, fact

    if n == 0:
    
        return 1
        
    result = taylor_series(x, n - 1)
    
    power *= x
    
    fact *= n
    
    return result + (power / fact)
    
x = float(input("Enter the value of x: "))

n = int(input("Enter the number of terms (n): "))

result = taylor_series(x, n)

print(f"\nThe value of e^{x} using Taylor series (n={n} terms) is: {result:.5f}")

## OUTPUT

![442486706-5bd2a165-53c6-448e-8297-2774f150dd10](https://github.com/user-attachments/assets/0a033ef5-5361-4241-9656-b1af63e3df35)

## RESULT

Thus the program has been executed successfully.
