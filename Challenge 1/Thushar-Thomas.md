# Code
```python
'''
Documentation
Program to check whether the given number is prime or not

Name  : Thushar Thomas
Branch: AI & DS
'''

def is_prime(num): 
    fact=2
    if num==1:
            fact=fact-1
    for i in range(2,int(num/2)+1):
        if num%i==0:
            fact=fact+1
    if (fact==2):
        return True
    else:
        return False
        
n = int(input("Enter a number: ")) #Getting a number from user
print("Is the given number prime?")

is_prime(n)
```

# Explanation
The program above checks whether the number from the user is a prime number or not. 
<p>Prime number is a number that has only 2 factors. In this progam we check the number of factors for a number using for loop and if condition.
If the number only has 2 factors, 'if else condition' returns 'True'. If not 'False'.

    I avioded "num+1" in the 'for' loop instead of "(num/2)+1" inorder to optimize the program.</p>

<p>Thank you</p>
