# Quiz 009

![Captura de tela 2024-10-07 004123](https://github.com/user-attachments/assets/643bc866-ea92-4993-9d38-52abfda7ad5a)

## Paper Work

![IMG_3522](https://github.com/user-attachments/assets/4834fa3c-9dd7-4760-9171-1c1113656eb2)


## Code

```py
input_text = input("Enter the text: ")
shift_value = int(input("Enter the shift value: "))

def cyphered(text, shift):
    result = ""
    
    for char in text:
        if 'A' <= char <= 'Z':
            new_char = ord(char) + shift
            if new_char > ord('Z'):
                new_char -= 26
            shifted_char = chr(new_char)
            result += shifted_char
        
        elif 'a' <= char <= 'z':
            new_char = ord(char) + shift
            if new_char > ord('z'):
                new_char -= 26
            shifted_char = chr(new_char)
            result += shifted_char
            
        else:
            result += char
    
    return result

ciphered_text = cyphered(input_text, shift_value)
print("\n", ciphered_text)

```

## Proof of Work

![Captura de tela 2024-10-20 034223](https://github.com/user-attachments/assets/9c018b02-1985-482a-8234-d9e3d75185b8)

## Flow Diagram




