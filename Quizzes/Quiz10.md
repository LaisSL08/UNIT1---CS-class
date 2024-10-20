# Quiz 010

![Captura de tela 2024-10-20 041328](https://github.com/user-attachments/assets/a6d1b292-d38e-418c-a417-f5d8d7181260)

## Paper Work



## Code

```py
def powerten(input_string):
    
    words = input_string.split()  
    for word in words:
        if word.isdigit():  
            number = int(word)
            break
    else:
        print("invalid.")
        return
    
    prefixes = ['pico (10^-12)', 'nano (10^-9)', 'micro (10^-6)', 'milli (10^-3)',
                'centi (10^-2)', 'deci (10^-1)', 'base (10^0)', 'deca (10^1)',
                'hecto (10^2)', 'kilo (10^3)', 'mega (10^6)', 'giga (10^9)', 'tera (10^12)']
    exponents = [-12, -9, -6, -3, -2, -1, 0, 1, 2, 3, 6, 9, 12]
    
    print(f"Powers of ten for {number}:")
    for prefix, exponent in zip(prefixes, exponents):
        result = number * (10 ** exponent)
        print(f"{prefix}: {result}")

input_string = input("Enter a number with units : ")
powerten(input_string)

```

## Proof of Work

![Captura de tela 2024-10-20 052225](https://github.com/user-attachments/assets/1a18837f-0c5a-401c-b02f-75c14edcc9c5)

## Flow Diagram


