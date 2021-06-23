# Code
```python
def hexadecimal(choice):
    if choice==1:
           n=int(input("Enter binary value: "),2)
           print((hex(n)[2:]).upper())
    elif choice==2:
           n=int(input("Enter decimal value: "))
           print((hex(n)[2:]).upper())
    else:
           print("wrong choice")
print("1.Binary\n2.Decimal")           
hexadecimal(int(input("Enter your choice:")))
```
# Explanation
1. Input the choise Binary/Decimal, and pass the choice to `hexadecimal()` function as parameters
2. If user choice is binary(1):
   * Input the binary number,and convert it to decimal
   * Convert the decimal value to hexadecimal using `hex()` and print it
3. If user choice is decimal(2):
   * Convert the decimal value to hexadecimal using `hex()` and print it
