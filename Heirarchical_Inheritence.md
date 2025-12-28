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

