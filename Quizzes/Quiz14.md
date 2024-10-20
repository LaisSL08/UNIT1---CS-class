# Quiz 014

![Captura de tela 2024-10-20 105216](https://github.com/user-attachments/assets/de12b680-a478-49a7-ac0b-d1ec0bf1982f)

## Paper Work

![IMG_3539](https://github.com/user-attachments/assets/13ca1edd-7900-4e21-85ac-42ed72ea8ebe)

## Code

```py
num_students = int(input(""))

def open_doors(num_students):
    
    open_count = 0
    for i in range(1, num_students + 1):
        if i * i <= num_students:
            open_count += 1
        else:
            break  #
    return open_count


open_count = open_doors(num_students)
print(f"{open_count}")

```

## Proof of Work

![Captura de tela 2024-10-20 203344](https://github.com/user-attachments/assets/a4129529-63bf-491f-915e-48ae51e9a797)

## Flow Diagram

![IMG_3540](https://github.com/user-attachments/assets/7d3175f1-c781-4ce0-8400-1a3612816d9d)

