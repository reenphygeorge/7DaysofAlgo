# Code
```python
def to_hex(choice):
    if choice==1:
           num = int(input("Input binary value: "), 2)
           return hex(num)[2:].upper()
    elif choice==2:
           num = int(input("Input decimal value: "))
           return hex(num)[2:].upper()
    else:
           return "wrong choice"
print("1.binary\n2.decimal")           
print(to_hex(int(input("choice:"))))
```
# Explanation
Here given a choice either to select binary or decimal, and get its respective input and then convert to hexadecimal equivalent using hex()function,here slicing operation done to eliminate "ox" infront of hexadecimal and upper,used to captialize the letter in hexadecimal.
