# CODE
...python
def is_prime(num):
	flag=0
	if num>1:
		for i in range(2,(num//2)+1):
			if(num%i)==0:
				flag=1
				break
	if flag==1:
		return False
	else:
		return True
number=int(input("ENTER ANY NATURAL NUMBER"))
print(is_prime(number))
...

# EXPLANATION
	*Getting user input from the main function
	*Passing the value to the function is_prime
	*Checking weather the numer is greater than one
	*Checking weather the number is divisible by any numbers from 2 upto half of the given number(checking factors)
	*If factors are found flag value is changed to one
	*Checkingthe value of flag
	*Returning boolean value to the main function.
