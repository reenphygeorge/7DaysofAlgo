# Code
```
def spell_it():
    n=int(input('Enter an integer between 1 and 10000: '))
    
    one = ["","one", "two", "three", "four", "five", "six", "seven", "eight","nine", "ten"]
    ten1 = ["","eleven", "twelve", "thirteen", "fourteen", "fifteen","sixteen","seventeen","eighteen", "nineteen"]
    ten2 = ["","", "twenty","thirty", "fourty", "fifty", "sixty", "seventy", "eighty", "ninety"]
    a = int(n / 1000)
    b = int((n-a*1000)/100)
    c = int((n % 100)/10)
    d = n % 10
    
    if a > 0:
        print(one[a], "thousand ",end="")
    else:
        print("", end="")
    if b > 0:
        print(one[b], "hundred ",end="")
    else:
        print("", end="")
    if c == 0:
        print(one[d], end="")
    elif c >= 2:
        print(ten2[c], one[d],end="")
    elif 0 < c < 2:
        print(ten1[d],end="")
spell_it()
```

# Explanation
The program takes a whole number as an input and returns the number in words.  
- In the function, we accept a whole number between 0 and 10000 as input from the user.
- We defined 3 String arrays[one,ten,ten1] to hold place values.
- we defined variables a,b and c to identify the range of the integer and  
- conditionals converts the number into word format and output is printed.

Implemented a **Pure function** which returns   
> the number in words  
> Range :0 to 10000 

******************************
Language used: Python3  
