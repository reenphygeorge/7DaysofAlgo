# CODE
```python
def to_hex(choice):
    if choice==1:
           num = int(input("ENTER THE BINAY VALUE: "))
           return hex(num)[2:].upper()
    elif choice==2:
           num = int(input("ENTER THE DECIMAL VALUE: "))
           return hex(num)[2:].upper()
    else:
           return "ENTER A VALID CHOICE"
print("1.BINARY\t 2.DECIMAL")  
print(to_hex(int(input("ENTER YOUR CHOICE:"))))
```

# EXPLANATION
  *In the main function user inputs a choice of eigther binary or decimal number
  *The choice is passed to the to_hex function where choices are selected by if else conditon
  *User inputs the neccessary number in each which is converted into hexadecimal by built in function hex()
  *The hex() function returns lower case characters which is convereted to upper case using .upper()
