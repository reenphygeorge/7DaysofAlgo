# Code
```
def to_hex(n):
    if(choice == 1):
        hexD = 0
        num = 1
        tmp = 1
        i = 0
        value = []
        while n != 0:
            rem = n % 10
            hexD = hexD + (rem*num)
            if tmp % 4 == 0:
                if hexD < 10:
                    hexD = hexD+48
                    val = chr(hexD)
                    value.insert(i, val)
                else:
                    hexD = hexD+55
                    val = chr(hexD)
                    value.insert(i, val)
                num = 1
                hexD = 0
                tmp = 1
                i = i+1
            else:
                num = num*2
                tmp = tmp+1
            n = int(n/10)

        if tmp != 1:
            hexD = hexD+48
            val = chr(hexD)
            value.insert(i, val)
        if tmp == 1:
            i = i-1
        while i >= 0:
            print(end=value[i])
            i -= 1
    if(choice == 2):
        return print((hex(n)[2:]).upper())


print("\tConvert to Hexadecimal\n1.Binary Value\n2.Decimal Value")
choice = int(input("Enter your choice: "))
a = int(input("Enter the Number: "))
to_hex(a)
```

# Explanation
The program takes binary or decimal value and returns the Hexadecimal value.    
- The program ask the user to confirm the input.  
- If it's a binary value, conditionals evaluates to be true and the binary value is converted into its hexadecimal value.  
- If it's a decimal value, we convert the decimal value into its hexadecimal value using hex() function.  

Implemented a Function which takes **binary or decimal number** and returns   
> **Hexadecimal** value  

******************************
Language used: Python3  
