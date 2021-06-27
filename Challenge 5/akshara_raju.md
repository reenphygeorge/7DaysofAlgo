# Code
```
#Python Code
#Problem Statement : Implement a pure function that takes a string as an argument and encodes it using the ceaser’s cipher and returns the encoded string.
#Author : Akshara Raju

def encrypt(string, shift):
    code = ''
    for i in range(len(string)):
        letter = string[i]
        if (letter.isupper()): 
            code+=chr((ord(letter)+shift-65)%26+65)
        else: 
            code+=chr((ord(letter)+shift-97)%26+97)
    return(code)

string = input("Enter the string to be encrypted: ")
shift = int(input("Shift Value: "))
print(encrypt(string,shift))



          


     



```
# Explanation

The input string is assigned to the variable **string**, the shifting value is assigned to variable **shift**. Both values are passed as an argument to the function **encrypt()**. 
For each character we apply:
* code+=chr((ord(letter)+shift-65)%26+65) (For uppercase characters).
* code+=chr((ord(letter)+shift-97)%26+97) (For lowercase character).
* Once the above rule is applied for each character in the string, the output is returned.
