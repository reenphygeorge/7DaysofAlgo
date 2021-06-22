# CODE
```python
  def is_prime(num):
     flag=1
     if num>1:
         for i in range(2,num):
             if(num%i)==0:
                 flag=flag+1
         if flag==1:
             return True
         else:
             return False
num=int(input())
result=is_prime(num)
print(result)
```

# Explanation

 1. Prime numbers are numbers that have only 2 factors: 1 and themselves.
 2. I have defined a flag variable and initilazed with 1(which is used to store the count of factors of that number).
 
    2.1  if its value = 1 , there is no factors for that number and it is a prime number and return boolean value True.
    
    2.2  else,it is not a prime number and return boolean value False.
