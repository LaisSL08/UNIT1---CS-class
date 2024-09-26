# Criterion A: Planning
## Problem Definition

![Which _Mr_ Men_ Character Are You](https://github.com/user-attachments/assets/ffb4ea87-542f-4ab7-b671-e33896fc412d)

My client owns **Smile**, a small mental health clinic, where he manages a team of nurses, doctors, and secretaries who have to handle patient data every day. The clinic uses several software programs to manage patient records, appointments, and billing, all requiring some log in and, therefore, passwords. In the past, employees of the clinic have experienced a high workload which compromised the patient data in the clinic. Due to this, the employees have started using methods such as writing passwords on sticky notes, saving them in text files, notes on their phones, or even just telling each other, hoping one of them will memorize it. These actions caused a serious security concern, as they left the clinic vulnerable to data breaches and unauthorized access to patient data. This situation has been noticed by the patients, who are extremely concerned if their information will be accessed by people outside the workers, the trust in the clinic and its employees has decreased. The owner, scared by this situation, has approached me to design a tool to address both basic arithmetic operations like addition, subtraction, multiplication, and division, and the password management problems faced by the clinic employees. 

## Proposed Solution
My proposed solution is a calculator for basic arithmetic operations like addition, subtraction, multiplication, and division. However, this calculator has a secret function that is only revealed when a hidden code is entered. Once the correct secret code is typed into the calculator, it transforms into a basic password manager.The password manager will securely store and retrieve passwords, allowing staff to safely access the clinic’s digital systems without compromising sensitive information. This solution aims to enhance both the productivity and security of the clinic, providing an easy way to manage passwords.

### Plan for the solution:

1. Basic arithmetic operations function (addition, subtraction, multiplication, and division).
2. A secret code feature that transforms into a basic password manager.
3. Password database/storage.
4. Easy to understand/simple design.

### Concerns/Things to be solved:

1. Employees using bad methods (e.g., shared documents, physical notes) to manage passwords.
2. Increased risk of data breaches and unauthorized access.

## Success Criteria
1. The calculator should accept user input to perform basic operations (addition, subtraction, multiplication, division).
2. The calculator can handle typical errors (e.g., division by zero) and give appropriate feedback.
3. If the user enters the secret code ("00998877"), the program will change modes and act as a password manager.
4. In password manager mode, the user should be able to perform CRUD operations (Create, Replace, Update, Delete):
   * Add a password (for example, for a website).
   * View the stored passwords (only if they re-enter the secret code).
5. Save passwords permanently and securely.
7. Use the terminal to interact with the user.
8. Block the program if the wrong code is typed in **View the stored passwords**.


# Criterion B: Design
### System Diagram

**Fig 1** System Diagram showing the minimal requirement for the hardware and software used for
proposed solution. The lock indicates encryption.



### Flow diagrams for algorithms
![flow](https://github.com/user-attachments/assets/93f4a0fb-66b8-4993-9b3d-b0b47deaeb82)
**Fig. 1** This is the flow diagram for the algorithm used to search in the data file...
**Fig. 2** This is the flow diagram for the algorithm used to search in the data file...
**Fig. 3** This is the flow diagram for the algorithm used to search in the data file...

### Data storage

### Sketches of the application (wireframe diagrams)

### Test plan

## Record of Tasks

| Task Number | Planned Action              | Planned Outcome                                                 | Time Estimated | Target Completion Date | Criterion |
|-------------|-----------------------------|-----------------------------------------------------------------|----------------|------------------------|-----------|
| 1           | 1st Meeting with the client | Obtained a problem definition, understand what the situation is | 10 min         | Sep 7                  | A         |
|             |                             |                                                                 |                |                        |           |
|             |                             |                                                                 |                |                        |           |
|             |                             |                                                                 |                |                        |           |
|             |                             |                                                                 |                |                        |           |

# Criterion C: Development 

## Code

```py
# Sum Function
def add(num1, num2):
    return num1 + num2

# Subtraction Function
def subtract(num1, num2):
    return num1 - num2

# Multiplication Function
def multiply(num1, num2):
    return num1 * num2

# Division Function
def divide(num1, num2):
    if num2 == 0:
        return "Error! Please input another value, Division by zero is not allowed"
    else
        return num1 / num2

def calculator():
    # Ask user to input the math expression
    expression = input("Enter an expression (example: 2 + 2 or 4 * 3, etc): ")

    # Check the operator and solve the input
    if '+' in expression:
        num1, num2 = expression.split('+')
        result = add(float(num1), float(num2))
        operation = '+'
    elif '-' in expression:
        num1, num2 = expression.split('-')
        result = subtract(float(num1), float(num2))
        operation = '-'
    elif '*' in expression:
        num1, num2 = expression.split('*')
        result = multiply(float(num1), float(num2))
        operation = '*'
    elif '/' in expression:
        num1, num2 = expression.split('/')
        result = divide(float(num1), float(num2))
        operation = '/'
    else:
        return "Error! Please enter a valid expression with one of the operators (+, -, *, /)."

    # Show the result
    return f"{num1} {operation} {num2} = {result}"

# Run the calculator
print(calculator())

```
## Proof of Work

# Sources
