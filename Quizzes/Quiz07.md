# Quiz 07

![Captura de tela 2024-09-16 224129](https://github.com/user-attachments/assets/fdab09f5-a147-4d6a-9760-3d912b0c6712)


## Paper Work

![IMG_3138](https://github.com/user-attachments/assets/7d9f7771-9cf3-4c15-a78b-5ece0393323c)
![IMG_3139](https://github.com/user-attachments/assets/bb837c2b-8b7d-4237-bac9-c814c3ff5e0f)
![IMG_3140](https://github.com/user-attachments/assets/a2d7d13e-b6aa-4106-8216-e5f542167299)
![IMG_3141](https://github.com/user-attachments/assets/1cc19b36-3997-4040-9f98-7042b9b73306)

## Code

```py
def find_max(numbers):
    M = None
    for i in range(len(numbers)):
        if M is None or numbers[i] > M:
            M = numbers[i]
        
        print(f"Step {i}: Current max is {M}")
    
    return M

numbers = [3, 5, 10, 2, 15]
final_max = find_max(numbers)
print(f"The largest number is: {final_max}")

```

## Proof of Work

![Captura de tela 2024-09-17 112124](https://github.com/user-attachments/assets/41c2afdd-f9dd-4ed0-8af2-a80dbeb7fe3f)

## Flow Diagram

![IMG_2936](https://github.com/user-attachments/assets/4e7be7bc-2e22-4555-a2fe-93752bd92c86)
