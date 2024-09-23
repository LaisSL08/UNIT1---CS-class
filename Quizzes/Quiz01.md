# Quiz 01

![Captura de tela 2024-09-16 212713](https://github.com/user-attachments/assets/6834d680-0d8b-410b-9cfe-7b5eb7305712)

## Paper Work

![IMG_3094](https://github.com/user-attachments/assets/77a007b9-9b20-4c2d-87ba-638fb47a8039)

## Code

```py
text = input("Input text: ")
words = text.split()

result = ""
for word in words:
    if len(word) > 2:
        word = word[0] + str(len(word) - 2) + word[-1]
    result = result + word + " "

print(result.strip())

```

## "Advanced" Code


```py

words = input("Input text: ").split()  
result = ' '.join([word if len(word) <= 2 else word[0] + str(len(word) - 2) + word[-1] for word in words]) 
print(result) 

```

## Proof of Work

![IMG_3115](https://github.com/user-attachments/assets/04b1bc30-f728-43a1-9e70-41eada72680b)


## Flow Diagram

![IMG_3116](https://github.com/user-attachments/assets/ec269a54-1d0b-4e18-80c6-9784e9134907)

