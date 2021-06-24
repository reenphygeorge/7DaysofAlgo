##### Challenge 3: Base to Hex.
##### Problem Statement: Implement a pure function that takes a whole number in either base 2 or base 10 format and converts it to base 16.
##### Author: Dona Maria Sunny (S6, CSE)
##### Language used: Python 3
# Code
```python
def to_hex(number,choice):

    try:
        if(choice==1):
            binaryNumber=int(number,2)
            return(hex(binaryNumber).lstrip("0x").upper())
        elif(choice==2):
            decimalNumber=int(number)
            return(hex(decimalNumber).lstrip("0x").upper())
        else:
            return("Invalid choice entered. Please enter '1' or '2' ")
    except:
        return("Error! You entered a wrong number. Please enter a whole number in base 2 or 10.")

    
print("Base to Hex.\n OPTIONS AVAILABLE ARE:\n 1.Convert base 2 (binary) format to base 16. \n 2.Convert base 10 (decimal) format to base 16.")
choice=int(input("Enter your choice:"))
number=input("Enter the number to be converted:")
print(to_hex(number, choice))


```
# Explanation
1. User enters the ```choice```. Choices avaliable are:
   * Convert base 2 (binary) format to base 16.
   * Convert base 10 (decimal) format to base 16.
2. User enters the ```number``` to be converted.
3. Both  ```choice``` and ```number``` is passed to the function and now the function **to_hex()** is called. 
4. Following happens inside the function:
   * If ```choice``` is 1 base 16 of **binary input** is returned.
   * If ```choice``` is 2 base 16 of **decimal input** is returned.
   * If wrong choice is entered **"Invalid choice entered. Please enter '1' or '2'"** is returned.
   
   **hex()** is used to get base 16. **lstrip("0x")** is used to omit 0x in front of the output. **upper()** is used to get base 16 in capital letter. 
   Also here, **try except** is used to prevent error due to invalid entry of ```number``` and return that the number entered is not a **whole number** in the **base** chosen    by the user.
