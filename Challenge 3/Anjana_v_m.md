# code
```python
def to_hex(choice):
    if (choice==1):
           num = int(input("Enter the BINARY number:\n "),2)
           x= (hex(num).replace("0x"," "))
           return x.upper() + ' is the hexadecimal value of given binary number'
    elif (choice==2):
           num = int(input("Enter the DECIMAL number:\n"))
           x= (hex(num).replace("0x"," "))
           return x.upper()+ ' is the hexadecimal value of given decimal number'
    else:
           return ("Select either 1 OR 2")
print("CHOICE 1:BINARY NUMBER\t\t CHOICE 2:DECIMAL NUMBER")      
     
print(to_hex(int(input("Your choice:\n"))))
```

# Explanation
Here we can input either binary or decimal number.This brings the idea of choices in the code.so,In function, as parameter we are poviding choice. Python have many in-built function.hex() is one of it to convert given number to hexadecimal value.bin() helps to convert number to binary and so on.When we want to convert a decimal
number to it's hexagonal value, we can use hex(number), but the output will contain "0x" which represents it's a hexagonal number. To remove "0x", we have used replace("0x," ")which
replaces "0x" with space. upper() is used to convert letters to uppercase letters.According to our choice we enter to the loop and execute remaining statements.If choice is out of range
we ask them to select choice of given range.
