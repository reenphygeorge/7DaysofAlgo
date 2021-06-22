# Code
```
def is_prime(number):
    count = 2
    flag = 0
    if number < 1: 
        return ("Invalid!")
    if number == 1:
        return ("Sorry!1 is not prime.")
    if number == 2:
        return(True)
    while count < number:
        if number%count == 0:
            return(false)

        else:
            flag = 1
            count = count+1


    if flag == 1:
        return(True)
            
number = int(input("Enter a Natural Number:"))
print (is_prime(number))
```

# Explanation
**Prime number** is a number which is not divisible by any other number.
Here the user is asked to input a **Natural Number**.
The Natural number assigned to the variable **number** is passed to the function **is_prime**.
Inside the function there is a **count** variable and **flag** variable.
If number is:
**=>** less than 1, it returns **Invalid**. 
**=>** equals 1, then returns **Sorry!1 is not prime**.
**=>** equals 2, then returns **True**.
**=>** while count is less than number, the while loop executes and returns **false** if the number is divisible by count.
        else the the flag is set to 1, also count increaments and the process is repeated. Finally as the loop is executed and the flag value is 1,then returns **True** indicating given number is a prime number.
