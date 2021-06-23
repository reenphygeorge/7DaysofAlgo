#code
def isPrime(n):
    if n <= 1:
        return False
    for i in range(2, n):
        if n % i == 0:
            return False;
  
    return True
n=int(input("enter a number"))
print(isPrime(n))

#EXPLANATION

*if the number entered is less than or equal to  1 then we get FALSE as output
*if the remainder of the number entered is equal to 0 we get false as output
else return true
