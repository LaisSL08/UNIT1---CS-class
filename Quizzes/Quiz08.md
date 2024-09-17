# Quiz 008

![Captura de tela 2024-09-16 224150](https://github.com/user-attachments/assets/536dc908-ca2a-4c90-9800-3a98a666c34d)

## Paper Work

![IMG_3144](https://github.com/user-attachments/assets/d3140b9a-9486-4e04-88b1-5b96aa441ce6)

## Code

```py

floor = 0
room = 00

for i in range (1,11,1):
    floor += 1
    for x in range (1,11,1):
        room += 1

        print(f"{floor}F{room}")
       
num = int(input("which room would you like to locate?: "))

room_num = 00
floor_num = 0

if num < 101:
    room_num += int(num)%10
    floor_num = int(num)//10
    print(f"{floor_num}F0{room_num}")
else:
    print("Room available until 100")

```

## Proof of Work

![Captura de tela 2024-09-17 104135](https://github.com/user-attachments/assets/16f5352f-a71f-40f4-85ff-0221bdc3ccb8)


## Flow Diagram

![IMG_3145](https://github.com/user-attachments/assets/953535ef-a65d-45bd-9995-c415fbfd4d0e)

