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
3. If the user enters the secret code ("53176"), the program will change modes and act as a password manager.
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
    else:
        return num1 / num2

def calculator():
    # Ask user to input the math expression
    expression = input("Sorry, please enter again: ")

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

# Define a secret code and the corresponding password manager logic
secretcode = "53176"
pssfile = 'patientpasswords.txt'

# Change characters to opposite Function
def oppositecharacters(char):
    if 'a' <= char <= 'z':  # letters
        return chr(219 - ord(char))  # Opposite letters
    elif '0' <= char <= '9':  # Numbers
        return chr(105 - ord(char))  # Opposite Numbers
    else:
        return char  # Return any other character

# Hide or reveal (reverse password) Function
def hrpassword(password):
    result = ""
    for char in password[::-1]:
        result += oppositecharacters(char)
    return result

# Load passwords Function
def lpasswords():
    passwords = {}
    try:
        with open(pssfile, 'r') as file:
            for line in file:
                patientlogin, password = line.split(':')
                passwords[patientlogin] = password.strip()  # Strip newline characters
    except FileNotFoundError:
        print("File not found. Starting an empty list.")
    return passwords

# Save passwords Function
def spasswords(passwords):
    with open(pssfile, 'w') as file:
        for patientlogin, password in passwords.items():
            file.write(f"{patientlogin}:{password}\n")

# Masked Form Function
def mpassword(password):
    if len(password) > 2:
        return password[0] + "*" * (len(password) - 2) + password[-1]
    return password

# View passwords Function
def vpasswords(passwords):
    print("\nStored Passwords:")
    for patientlogin, password in passwords.items():
        hidden = hrpassword(password)
        maskedformpassword = mpassword(hidden)
        print(f"{patientlogin}: {maskedformpassword}")
    print()

# Add a new password Function
def apassword(passwords):
    patientlogin = input("Enter the full patient name: ")
    password = input("Enter the password: ")
    revealed = hrpassword(password)
    passwords[patientlogin] = revealed
    spasswords(passwords)
    print(f"Password for {patientlogin} added successfully.\n")

# Update password Function
def upassword(passwords):
    patientlogin = input("Enter the full patient name to update: ")
    if patientlogin in passwords:
        newpassword = input("Enter the new password: ")
        hidden = hrpassword(newpassword)
        passwords[patientlogin] = hidden
        spasswords(passwords)
        print(f"Password for {patientlogin} updated successfully.\n")
    else:
        print(f"Patient not registered.\n")

# Delete password Function
def dpassword(passwords):
    patientlogin = input("Enter the account name to delete: ")
    if patientlogin in passwords:
        del passwords[patientlogin]
        spasswords(passwords)
        print(f"Password for {patientlogin} deleted successfully.\n")
    else:
        print(f"Patient not registered.\n")

# Password Manager 
def password_manager():
    passwords = lpasswords()
    while True:
        print("\nPassword Manager:")
        print("1. Add a password")
        print("2. View all passwords")
        print("3. Update a password")
        print("4. Delete a password")
        print("5. Exit")
        
        choice = input("Choose one of the options: ")
        if choice == '1':
            apassword(passwords)
        elif choice == '2':
            code = input("Enter the secret code to view passwords: ")
            if code == secretcode:
                vpasswords(passwords)
            else:
                print("Access denied.\n")
        elif choice == '3':
            upassword(passwords)
        elif choice == '4':
            dpassword(passwords)
        elif choice == '5':
            print("Exiting password manager.")
            break
        else:
            print("Please choose an option between 1 and 5")

# Entry point of the program
expression = input("Enter an expression (example: 2 + 2 or 4 * 3, etc): ")

if expression == "53176":
    print("Welcome to Smile Password Manager!")
    password_manager()
else:
    # Run the calculator
    print(calculator())

```


# Sources

1. W3schools.com. W3Schools Online Web Tutorials. (n.d.). https://www.w3schools.com/python/default.asp 
2. GeeksforGeeks. (2024, September 6). Python program to make a simple calculator. https://www.geeksforgeeks.org/make-simple-calculator-using-python/ 
3. GeeksforGeeks. (2024, March 18). How to build a password manager in python. https://www.geeksforgeeks.org/how-to-build-a-password-manager-in-python/ 
4. ASCII TABLE
