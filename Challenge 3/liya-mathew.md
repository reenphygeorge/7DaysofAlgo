# Code
```
python

def to_hex(n):
    assert n >= 0
    for i in str(n):
        if i in '10':  
            binary = True
        else:
            binary = False
            break
    if(binary ==False):
        return  (hex(n)[2:]).upper()
    else:
        print("Enter your choice - BINARY (b)/DECIMAL (d):")
        value = input()
        assert value in ("d", "b")
        if (value == "b"):
            dec = int(str(n), 2)
            return hex(dec)[2:].upper()
        else:
            return((hex(n)[2:]).upper())



print (to_hex(243))
```

# Explanation
We are asked to accept a whole number either in its base10(decimal) or in its base2(binary) form and return its hexadecimal equivalent.For this we follow the  approach discussed below
* Firstly using assert we are ensuring that our input is a whole number.If it is not an assertion error will be created.
* Then we check whether the input is a decimal number or not(by checking if it is not a binary) . 
*   * If it is a decimal, we convert it into hexadecimal(base16) using hex() and return the corresponding value.
*   * Else, we ask the user to enter his choice(b,d) as 0 and 1 is present in both the number systems and cannot be distinguished. An assertion is created to ensure that only b or d is choosed
*   * * if the user enters b,then we convert the binary input to its corresponding hexadecimal output .For this, we first convert binary to decimal and then convert the decimal value to its hexadecimal equivalent.
*   * * else if the user enters d ,we convert the decimal value to its corresponding hexadecimal using hex() function.


