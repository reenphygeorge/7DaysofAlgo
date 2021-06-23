# Code
```python
'''
Documentation
Program to convert Base 10 or Base 2 number to Base 16

Name   : Thushar Thomas
Branch : AI & DS
'''
def to_hex(num,choice):    # Function to convert Binary or Decimal number to Hexadecimal number
    bin_to_dec=0
    pos=0
    if choice==1:    # Directly converts Decimal number to Hexadecimal number
        print("\nYour Decimal number:",num,"\nHexadecimal number :",hex(int(num)))
    elif choice==2:    # Coverts Binary number to Hexadecimal number
        if len(num)>8:    # Checks if the given Binary number is more than 8 bits
            print("\nThe binary number you entered is more than 8 bits.\nPlease try again.")
            return
        if {'0'}==set(num) or {'1'}==set(num) or {'0','1'}==set(num):    # Checks if numbers other than '0' or '1' is in given number
            temp=int(num);
            while(temp!=0):    # Converts Binary to Decimal number
                if temp%10==1:
                    bin_to_dec = bin_to_dec + pow(2, pos)
                pos+=1
                temp=int(temp/10)
            print("\nYour Binary number:",num,"\nHexadecimal number :",hex(int(bin_to_dec)))
        else:
            print("\nThe entered number is not binary. \nPlease try again.")
            
print("Enter '1' to covert Decimal(Base 10) to Hexadecimal(Base 16)")
print("Enter '2' to covert Binary(Base 2) to Hexadecimal(Base 16) upto 8 bits")
c=int(input("Enter your choice: "))
if c==1 or c==2:    # Checks if user entered invalid choice
    n=input("Enter the number: ")    # Recieves a number from user
    to_hex(n,c)  
else:
    print("\nInvalid choice.\nPlease try again.") 
```

# Explanation
In this program, user can convert a base 2 or base 10 number to base 16 number.
<p> <br/>This program has 2 choices
   <br/>* Decimal to Hexadecimal
   <br/>* Binary to Hexadecimal
  <br/><br/>In case of Decimal, the number is directly converted to Hexadecimal using hex() function.
 <br/>In case of Binary, the number is converted to Decimal and then to Hexadecimal using hex() function.</p>
  <br/>Thank you

