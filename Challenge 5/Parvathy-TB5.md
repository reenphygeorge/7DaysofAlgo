# Code
```python
def encrypt(string,s):
    result=""
    for char in string:
        if (char.isupper()):
            result+= chr((ord(char)+s-65)%26+65)
        else:
            result+=chr((ord(char)+s-97)%26+97)
    print("Encoded string: " + result)
string=input("Enter string:")
s=int(input("Shift:"))
encrypt(string,s)
```
# Explanation
1. Input the string need to be encoded(`string`)
2. Input the number of positions to be shifted(`s`)
3. Call `encrypt()` function
   * Inside the function, take each character in the string one by one and convert it to the unicode code representation
   * Alter the unicode code according to the shift value and convert it to back to charcter
   * Concatinate the new character to a new string (`result`)
   * After passing through every character, print the resultant string (result)
