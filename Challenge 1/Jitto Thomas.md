def is_prime(num):
	# Your function implementationflag = False
	flag=0
	#Checking weather the number is greater than one
	if num > 1:
		for i in range(2, num):
		#Checking weather the number is divisible by any numbers from 2 upto the given number
			if (num % i) == 0:
				flag = 1
				break
	if flag==1:
		return False
	else:
		return True

#print(is_prime(7))
#Getting user input
number=int(input("ENTER ANY NATURAL NUMBER"))
#Passing the number to the function
print(is_prime(number))
