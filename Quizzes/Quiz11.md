# Quiz 011

![Captura de tela 2024-10-20 054654](https://github.com/user-attachments/assets/e01f914e-569a-4c56-8005-37bdcf39613b)

## Paper Work

![IMG_3532](https://github.com/user-attachments/assets/412667e8-16df-495f-8d5d-0e329d5b3fa1)

## Code

```py
import calendar 

def birthMonth():
    month = int(input("Enter your birth month (1 for January, 12 for December): "))
    
    year = 2024
    
    calen = calendar.monthcalendar(year, month)
    
    print(f"\nCalendar for {calendar.month_name[month]} {year}:\n")
    print("Mo Tu We Th Fr Sa Su")
    for week in calen:
        for day in week:
            if day == 0:
                print("  ", end=" ") 
            else:
                print(f"{day:2}", end=" ")  
        print() 
birthMonth()


```

## Proof of Work

![Captura de tela 2024-10-20 072523](https://github.com/user-attachments/assets/9b733320-a690-4904-8f5c-27b07179b9ee)

## Flow Diagram

![IMG_3533](https://github.com/user-attachments/assets/a2e518bb-2df2-4e99-af2e-b00e0eca0ebc)



