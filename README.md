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
# Get user input
name = input("Enter student name: ")

# Define the class
class Student:
    # Default constructor
    def __init__(self):
        self.a = name   # assign input to instance variable

    # Method to display message
    def show(self):
        print("This is non-parameterized constructor")
        print("Welcome", self.a)

# Create object
s = Student()

# Call method
s.show()
```


## Output
<img width="691" height="359" alt="image" src="https://github.com/user-attachments/assets/1df0ce4c-939a-471f-96aa-3d7ef7a90fef" />

## Result
The program was executed successfully. A Student class with a default (non-parameterized) constructor was created, and it correctly displayed a welcome message using the user-provided name.



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
```
class Demo:
    

    def __init__(self):
        self.status = "Alive"
        print(self.status)
    

    def __del__(self):
        print("Object is being destroyed")


obj = Demo()


del obj
```

## 🧪 Output
<img width="657" height="386" alt="image" src="https://github.com/user-attachments/assets/bec3a26e-d79c-46b4-aecb-3143b8fc40d8" />


## Result
The program was executed successfully. A class with a constructor and destructor was implemented, where the constructor initializes and displays the status, and the destructor is automatically invoked when the object is deleted



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
class Details:
    def getName(self):
        self.name = input("Enter name: ")
    
    def getAge(self):
        self.age = int(input("Enter age: "))


# Derived class 1
class Employee(Details):
    def getEmployeeDetails(self):
        self.getName()
        self.getAge()
        self.employee_id = input("Enter employee ID: ")
        self.department = input("Enter department: ")

    def showEmployee(self):
        print("\n--- Employee Details ---")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)


# Derived class 2
class Patient(Details):
    def getPatientDetails(self):
        self.getName()
        self.getAge()
        self.patient_id = input("Enter patient ID: ")
        self.disease = input("Enter disease: ")

    def showPatient(self):
        print("\n--- Patient Details ---")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)


# Create objects
emp = Employee()
pat = Patient()

# Get details
emp.getEmployeeDetails()
pat.getPatientDetails()

# Display details
emp.showEmployee()
pat.showPatient()
```
## Sample Output
<img width="629" height="837" alt="image" src="https://github.com/user-attachments/assets/9d5eda9e-e402-451b-9b64-44f0904509e7" />


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
class Grandchild(Child):
    def __init__(self, name, age, location):
        super().__init__(name, age)
        self.location = location

    def getLocation(self):
        return self.location


# User input
name = input("Enter name: ")
age = int(input("Enter age: "))
location = input("Enter location: ")

# Create object
obj = Grandchild(name, age, location)

# Display output
print("\n--- Person Details ---")
print("Name:", obj.getName())
print("Age:", obj.getAge())
print("Location:", obj.getLocation())
```

## Sample Output
<img width="580" height="496" alt="image" src="https://github.com/user-attachments/assets/896977df-69be-43b7-9eee-f37d4bee9ade" />

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
# Class 1
class Calculation1:
    def Summation(self, a, b):
        return a + b


# Class 2
class Calculation2:
    def Subtraction(self, a, b):
        return a - b


# Derived class (Multiple Inheritance)
class Derived(Calculation1, Calculation2):
    def Division(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Division by zero not allowed"


# Input
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

# Object creation
obj = Derived()

# Output
print("\n--- Results ---")
print("Addition:", obj.Summation(a, b))
print("Subtraction:", obj.Subtraction(a, b))
print("Division:", obj.Division(a, b))
```

## Output Example
<img width="606" height="438" alt="image" src="https://github.com/user-attachments/assets/ae268800-befd-4261-be0d-9edd4d73622f" />



