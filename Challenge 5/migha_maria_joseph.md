# Code
```python
def caesarCipher(string,key):
    Encoded_string=""
    for i in string:
        char = i
        if (char.isupper()):
            Encoded_string += chr((ord(char) + key-65) % 26 + 65)
        else:
            Encoded_string += chr((ord(char) + key-97) % 26 + 97)
    return Encoded_string
string=str(input("String:"))
key=int(input("Key:"))
print("Encoded_String:",end="")
print(caesarCipher(string,key))
```
# Explanation

* In Caesar Cipher technique,each letter of a given string is replaced by a letter some fixed number of positions down the alphabet
* In this program,
    1. Traverse the given string, one character at a time 
    2. For each character, transform the given character using the rule :(x + n) % 26,where x is the actual character, and n is the number of positions we want to shift the character x by.
        We’re taking mod with 26 because there are 26 letters in the English alphabet
       *  For uppercase,the ASCII code begins with 65
       *  For lowercase,the ASCII code begins with 97
    4. Return the new string generated

