# Quiz 02

![Captura de tela 2024-09-16 223953](https://github.com/user-attachments/assets/feb9e80d-21a4-4fa0-93d4-945d6bdb49c8)

## Paper Work

![IMG_3118](https://github.com/user-attachments/assets/06cec3d8-baf3-434d-9060-9fd200d80aaa)

## Code for SL

```py
num_A = int(input("Enter number A: "))
num_B = int(input("Enter number B: "))

if num_B == 20 or num_A == 20:
    sol = True
else:
    sol = False
    if num_B+num_A == 20:
        sol = True
    else:
        sol = False
print(f"The solution is {sol}")
```

## Proof of Work

![Captura de tela 2024-09-17 005423](https://github.com/user-attachments/assets/9697192c-14e1-409a-9447-6696ee447cd9)


## Code For HL

```py
listA = list(map(int, input("Enter list A (space-separated integers): ").split()))
listB = list(map(int, input("Enter list B (space-separated integers): ").split()))

if len(listA) != len(listB):
    raise ValueError("Both lists must be of the same length.")

sol = any(
    a == 20 or b == 20 or a + b == 20
    for a, b in zip(listA, listB)
)

print(sol)

```

## Proof of Work

![Captura de tela 2024-09-17 011503](https://github.com/user-attachments/assets/d10af13c-fcdc-4458-ade5-840f1629f48a)


## Flow Diagram

![IMG_3119](https://github.com/user-attachments/assets/8dded680-95a7-4a97-85da-86de88358791)

