# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```
class Calculation1:
    def Summation(self, a, b):
        return a + b


class Calculation2:
    def Subtraction(self, a, b):
        return a - b


class Derived(Calculation1, Calculation2):
    def Division(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Division by zero is not allowed"

num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

calc = Derived()


sum_result = calc.Summation(num1, num2)
sub_result = calc.Subtraction(num1, num2)
div_result = calc.Division(num1, num2)


print("\nResults:")
print("Addition:", sum_result)
print("Subtraction:", sub_result)
print("Division:", div_result)
```
## Output Example
```
Enter first number: 10
Enter second number: 5

Results:
Addition: 15.0
Subtraction: 5.0
Division: 2.0
```


