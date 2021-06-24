# Code
```
#Python Code
#Problem Statement : Implement a pure function that takes a whole number in either base 2 or base 10 format and converts it to base 16.
#Author : Akshara Raju

def to_hex(number):
    if number < 0:
        return("Please enter a Whole Number")
    hex_num = hex(number)
    hex_num = hex_num.replace("0x","")
    return(hex_num.upper())

print("CONVERT TO HEXADECIMAL\n1. Whole number with base 2 (Binary)\n2. Whole number with base 10 (Decimal)")
choice = int(input("Choose your Option: "))
if choice == 1:
    number = (input("Enter your Binary Number: "))
    number = int(number,2)
    print (to_hex(number))
if choice == 2:
    number = int(input("Enter your Decimal Number: "))
    print (to_hex(number))   
elif choice>2 or choice<1:
    print("Please Choose the Correct Option")     


```

# Explanation
The user is asked to choose one of the option and if chosen 1-Binary number is the input, if chosen 2-Decimal number is the input. The input is assigned to a variable called **number** which is passed to the function **to_hex()**. There the number is converted to hexadecimal value by using the function **hex()** and is assigned to variable **hex_num**.
Finally the hexadecimal value is retured.
