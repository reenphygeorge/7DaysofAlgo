##### Challenge 5: Caeser Cypher.
##### Problem Statement: Implement a pure function that takes a string as an argument and encodes it using the caeser’s cipher and returns the encoded string.
##### Author: Dona Maria Sunny (S6, CSE)
##### Language used: Python 3
# Code
```python
def caesarCipher(shift,userInput):
    length=len(userInput)
    output=""
    flag=0
    for x in range(0,length):
        singleChar=userInput[x]
        if(singleChar.isupper()):
            unicodeEquivalence=ord(singleChar)
            value=unicodeEquivalence+shift-65
            output=output+chr((value)%26+65)
        else:
            unicodeEquivalence=ord(singleChar)
            value=unicodeEquivalence+shift-97
            output=output+chr((value)%26+97)
    return(output)


shift=int(input("Enter shift:"))
userInput=input("Enter text for encryption:")
print("\nEncrypted value:")
print(caesarCipher(shift,userInput))


```
# Explanation
1. User enters the ```shift``` and the string need to be encrypted. String is stored in ```userInput```.
2. Now the function **caesarCipher()** is called. ```shift``` and ```userInput``` is passed to it.
3. Inside the function the following happens:
   * Length of string needed is found and is stored in ```length```.
   * Each character in the string is taken.
   * If the character is in capital, it's Unicode equivalence is found using **ord()**. Then to it ```shift``` is added and **65** is subtracted and the result is stored in **value**. 
     Here **65** is used because ascii value of ‘A’ is **65**.
     Encoded value of the character obtained by doing **chr((value)%26+65)**
   * If the character is not in captital, same process as given for capital character is done. Except that, here **97** is used because ascii value of ‘a’ is **97**.
   * After concatenation of all the characters in the input string **encoded string** is returned.
