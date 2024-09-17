# Quiz 05

![Captura de tela 2024-09-16 224057](https://github.com/user-attachments/assets/d4752ed4-4c80-4260-af12-0347f6997948)


## Paper Work

![IMG_3133 (1)](https://github.com/user-attachments/assets/80588ad7-8bd8-4c47-9532-1a88627db39c)


## Code for SL

```py
word = input("Enter a word: ")

sum = 0

for i in word:
    code = ord(i.lower())
    if code<91:
        sum = sum + (code - 90)
    if code>96:
        sum = sum + (code - 96)
print(f"{sum}")
```

## Proof of Work

![Captura de tela 2024-09-17 034701](https://github.com/user-attachments/assets/33314ace-b5f8-41db-844b-ed0813088160)


## Code For HL

```py
word = input("Enter a word: ")

sum = 0

for i in word:
    code = ord(i)
    
    if 'A' <= i <= 'Z':  
        sum += (code - ord('A') + 1) 
    elif 'a' <= i <= 'z':  
        sum += (code - ord('a') + 1)  
print(f"{sum}")

```

## Proof of Work

![Captura de tela 2024-09-17 034939](https://github.com/user-attachments/assets/745a794a-af3d-4be4-8254-83c1ff942a1d)


## Flow Diagram

![IMG_3134](https://github.com/user-attachments/assets/aa267e8a-5694-4d22-8411-eb5a07d94e50)

