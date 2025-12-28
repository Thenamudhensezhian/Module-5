# # Constructors in Python: Welcome Message with Student Name

## 🎯 Aim
To write a Python program that creates a **Student** class with a **default constructor** and a method to display a welcome message along with the student’s name provided by the user.

## 🧠 Algorithm
1. **Get user input**: Accept the student's name from the user.
2. **Define the class**: Create a class `Student` with a default constructor (`__init__`).
3. **Default Constructor**: In the constructor, assign the user input (student name) to an instance variable `self.a`.
4. **Display Message**: Define a method `show` that prints "This is non-parameterized constructor" and a welcome message with the student’s name.
5. **Execute the Program**: Instantiate the `Student` class and call the `show` method.

## 🧾 Program

```

class student:
    def __init__(self):
        print("This is non parametrized constructor")
    def display_welcome(self,name):
        print(f"Hello {name}")
name=input()
studentinstance=student()
studentinstance.display_welcome(name)


```

## Output
<img width="838" height="220" alt="486522636-45adc714-ae27-4e3a-bb64-85338bbb11c5" src="https://github.com/user-attachments/assets/80367812-ef01-4740-b05c-2777fe1f7c11" />

## Result
Thus the output is Verified.

# Destructor in Python

This project demonstrates how to implement a **destructor** in Python using a simple class.

## 🚀 Overview

The program defines a class `Demo` with:

- A **constructor** `__init__` that initializes an instance variable and prints a message.
- A **destructor** `__del__` that prints a message when the object is destroyed.

## 🧠 Algorithm

1. Define a class named `Demo`.
2. Inside the class, define the `__init__` method:
   - Initialize an instance variable `status` with the value `"Alive"`.
   - Print the value of `status`.
3. Define the `__del__` method:
   - Print a message indicating the object is being destroyed.
4. Outside the class:
   - Create an instance of the `Demo` class.
   - Delete the object using the `del` keyword.
## Program
~~~
class Demo:
    def __init__(self, value):
        self.value = value 
    def display(self):
        print(f"The value of this instance is: {self.value}")


demo_instance = Demo(10)

print(demo_instance.value)  

demo_instance.display()   
~~~
## 🧪 Output
<img width="994" height="865" alt="image" src="https://github.com/user-attachments/assets/78d069cf-b544-4fee-8722-11985ad89165" />


## Result
hence the code is written and executed

# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```
    def __init__(self):
        self.name = ""
        self.age = 0

    def getName(self):
        self.name = input("Enter name: ")

    def getAge(self):
        self.age = int(input("Enter age: "))

class Employee(Details):
    def __init__(self):
        super().__init__()
        self.employee_id = ""
        self.department = ""

    def getEmployeeDetails(self):
        self.employee_id = input("Enter Employee ID: ")
        self.department = input("Enter Department: ")
    
    def displayEmployee(self):
        print("\nEmployee Details:")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)


class Patient(Details):
    def __init__(self):
        super().__init__()
        self.patient_id = ""
        self.disease = ""

    def getPatientDetails(self):
        self.patient_id = input("Enter Patient ID: ")
        self.disease = input("Enter Disease: ")
    
    def displayPatient(self):
        print("\nPatient Details:")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)

emp = Employee()
print("\nEnter Employee Information:")
emp.getName()
emp.getAge()
emp.getEmployeeDetails()
emp.displayEmployee()


pat = Patient()
print("\nEnter Patient Information:")
pat.getName()
pat.getAge()
pat.getPatientDetails()
pat.displayPatient()
```
## Sample Output
```
Enter Employee Information:
Enter name: Ananya
Enter age: 25
Enter Employee ID: E101
Enter Department: HR

Employee Details:
Name: Ananya
Age: 25
Employee ID: E101
Department: HR

Enter Patient Information:
Enter name: Rohan
Enter age: 30
Enter Patient ID: P202
Enter Disease: Flu

Patient Details:
Name: Rohan
Age: 30
Patient ID: P202
Disease: Flu
```

# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **location** of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program
```

class Person:
    def __init__(self, name):
        self.name = name

    def getName(self):
        return self.name


class Child(Person):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

    def getAge(self):
        return self.age

class Grandchild(Child):
    def __init__(self, name, age, location):
        super().__init__(name, age)
        self.location = location

    def getLocation(self):
        return self.location

name = input("Enter name: ")
age = int(input("Enter age: "))
location = input("Enter location: ")


person = Grandchild(name, age, location)


print("\nPerson Details:")
print("Name:", person.getName())
print("Age:", person.getAge())
print("Location:", person.getLocation())
```

## Sample Output
```
Enter name: Ananya
Enter age: 22
Enter location: Chennai

Person Details:
Name: Ananya
Age: 22
Location: Chennai
```

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

