# Code
```python3
def encrypt(text):
    print("Enter the number of shifts:")
    shifts = int(input())
    encrypted_text = ""
    alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    for i in range(len(text)):
        char = text[i]
        index = alphabet.find(char.upper())
        if index == -1:
            encrypted_text = encrypted_text + char
        elif char.islower():
            char_index = ord(char) - ord("a")
            new_index = (char_index + shifts) % 26
            new_char = chr(new_index + ord("a"))
            encrypted_text = encrypted_text + new_char
        else:
            char_index = ord(char) - ord("A")
            new_index = (char_index + shifts) % 26
            new_char = chr(new_index + ord("A"))
            encrypted_text = encrypted_text + new_char

    return encrypted_text


print("Enter the text to be encrypted:")
print(encrypt(input()))


```

# Explanation
We need to implement a pure function that takes a string as an argument and encodes it using the ceaser’s cipher and returns the encoded string.
* For this we first ask the user to enter the text to be encrypted and the user input is passed as an argument for the function encrypt.
* Within the function ,the user is asked about the number of shifts he/she wants to perform. We intialize an empty string called encrypted_string to hold the result and another string alphabet intializing all the alphabets in uppercase
* The string may contain numbers,special symbols etc as its characters .but ceaser's cipher algorithm is concerned only about alphabets both in its upper and lower cases.
* So we check for every character in the string ,whether it is present in the string alphabet by converting it using upper() and implementing the python find().If it is not present the find() function returns a value -1 and in that case the character is concatinated to the encrypted_string
* else if the character is in lowercase,we calculate the position of character whin the range(26 alphabets) and perform the shift using modulo operation.We find the new character  and  concatinate it with the encrypted_text.
*  else if the character is in uppercase,we perform the same function as of lowercase and the only difference is that we are considering the unicode values of uppercase alphabets.
*  Two main python functions that are used for the implementation are ord() and chr()
*  * ord() accepts a single character string and return its unicode value.
*  * chr() returns the string corresponding to the unicode that is pointing to an integer.
*  Finally after the entire string has been processed ,the encrypted_text is returned and is printed.

