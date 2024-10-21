# Quiz 015

![Captura de tela 2024-10-20 204157](https://github.com/user-attachments/assets/46b1f451-5284-4fc1-9810-cd45070763a5)

## Paper Work

![IMG_3541](https://github.com/user-attachments/assets/741c3b13-ca0b-465d-8009-8102fc96f8eb)

## Code

```py
wordsinput = input("Enter a list of words: ")

wordslist = wordsinput.replace(",", " ").split()

def averagelength(words):
    totallength = 0  
    for word in words:
        removespace = "" 
        for char in word:
            if char != " " and char != ",":  
                removespace += char
        
        totallength += len(removespace)  
    
    
    average = totallength / len(words)
    
    return float(average)  
out = averagelength(wordslist)
print(out)

```

## Proof of Work

![Captura de tela 2024-10-20 205902](https://github.com/user-attachments/assets/0f4ea17f-79ea-4a0c-836a-db40ce0010c9)

## Flow Diagram

![IMG_3542](https://github.com/user-attachments/assets/7b6675bc-6807-416c-9053-792cb4eba3fa)

