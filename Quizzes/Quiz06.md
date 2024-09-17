# Quiz 06

![Captura de tela 2024-09-16 224112](https://github.com/user-attachments/assets/3eb63ffe-4c5c-4248-b8ed-3fab8204f2f2)


## Paper Work

![IMG_3137](https://github.com/user-attachments/assets/31528056-aa1b-49d1-9417-54d13403e598)


## Code For HL/SL

```py
import random
pass_len = int(input("How long will be password be?: "))
symbol_validation = input("Would you like symbols in this? True or False: ")

if symbol_validation == ("True"):

    for i in range(10): # 10 passwords
        sequence = ""
        for x in range(pass_len):
            rand_num = random.randint(33, 122)
            while 57 < rand_num < 65 or 90 < rand_num < 97:
                rand_num = random.randint(33, 122)
            sequence += chr(rand_num)
        print(sequence)

else:
    for i in range(10): # 10 passwords
        sequence = ""
        for x in range(pass_len):
            rand_num = random.randint(48, 122)
            while 57 < rand_num < 65 or 90 < rand_num < 97:
                rand_num = random.randint(48, 122)
            sequence += chr(rand_num)
        print(sequence)
```

## Proof of Work

![Captura de tela 2024-09-17 034939](https://github.com/user-attachments/assets/b8dfc013-3715-4bdf-b298-0cfa2425eaff)


## Flow Diagram

![IMG_3135](https://github.com/user-attachments/assets/4f508926-707b-4a89-98dd-de6d5292e1df)

