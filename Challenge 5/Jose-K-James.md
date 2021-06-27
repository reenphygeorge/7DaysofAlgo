# Code
```
def encrypt(string, shift):
 
  cipher = ''
  for char in string:
    if char == '':
      cipher = cipher + char
    elif  char.isupper():
      cipher = cipher + chr((ord(char) + shift - 65) % 26 + 65)
    else:
      cipher = cipher + chr((ord(char) + shift - 97) % 26 + 97)
  return cipher
 
text = input("Enter Word: ")
sh = int(input("Shift : "))
print("Encrypted message: ", encrypt(text, sh))
```

# Explanation
The program takes a string as an argument and encodes it using the ceaser’s cipher and returns the encoded string.  
- Each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.  

Implemented a Function that takes a string as an argument  
> encodes it using the ceaser’s cipher    
> returns the encoded string  

******************************
Language used: Python3  
