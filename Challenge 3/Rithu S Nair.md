//code

```python

def to_hex(choice):
    if choice==1:
           n=int(input("Enter binary value: "),2)
           print((hex(n)[2:]).upper())
    elif choice==2:
           n=int(input("Enter decimal value: "))
           print((hex(n)[2:]).upper())
    else:
           print("please enter a valid choice")
print("1.Binary\n2.Decimal")           
to_hex(int(input("Enter your choice:")))

```

//Explanation

1.to_hex is the function name and choice is passed as the parameter
2.if the choice 1 is entered then it asks for the binary value ,then hex(n) converts the binary value to hexadecimal and upper() converts it into uppercase.
3.if the choice 2 is enterd then it asks for the decimal value ,then hex(n) converts the decimal value to hexadecimal and upper() converts it into uppercase.

