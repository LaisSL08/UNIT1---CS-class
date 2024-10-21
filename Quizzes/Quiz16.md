# Quiz 016

![Captura de tela 2024-10-20 210711](https://github.com/user-attachments/assets/67f9244c-5209-46e1-86d4-2541752bd670)


## Paper Work

![IMG_3543](https://github.com/user-attachments/assets/d27b1f63-95fe-4d02-9a3d-1830fd709d4d)

## Code

```py
msginput = input("")
def get_l3tt3r(msg):
    replacements = {
        'a': '4',
        'e': '3',
        'i': '1',
        'o': '0',
        'A': '4',
        'E': '3',
        'I': '1',
        'O': '0',
        ' ': '_'
    }
    
    new_msg = ""
    for char in msg:
        if char in replacements:
            new_msg += replacements[char]
        else:

            new_msg += char
    
    return new_msg

case1 = get_l3tt3r(msginput)
print(case1)

```

## Proof of Work

![Captura de tela 2024-10-20 213151](https://github.com/user-attachments/assets/c14e2428-38f2-4103-9661-b84adad92ba5)

## Flow Diagram

![IMG_3544](https://github.com/user-attachments/assets/2ca97fef-fd13-4b69-aeb5-a0becf6e1850)

## Boolean Circuit
