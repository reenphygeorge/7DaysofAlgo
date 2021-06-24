# Code
```
def decimal(n):
	hexa = ['0'] * 100
	i = 0
	while(n != 0):
		temp = 0
		temp = n % 16
		if(temp < 10):
			hexa[i] = chr(temp + 48)
			i = i + 1
		else:
			hexa[i] = chr(temp + 55)
			i = i + 1
		n = int(n / 16)
	j = i - 1
	while(j >= 0):
		print("The hexadecimal number from decimal number is:",hexa[j])
		j = j - 1
n=int(input("Enter the decimal number:"))
decimal(n)

def binary(s):
    j = len(s)
    temp = 0
    n = 0
    sum = 0
    m = 1
    hexa = []
    i = j - 1
    while (i >= 0):
        sum += (ord(s[i]) - ord('0')) * m
        m *= 2
        temp += 1
        if (temp == 4 or i == 0):
            if (sum <= 9):
                hexa.append(chr(sum + ord('0')))
            else:
                hexa.append(chr(sum + 55));
            temp = 0
            sum = 0
            m = 1
        i -= 1
    j = len(hexa)
    i = j - 1
    while (i >= 0):
        print("The Hexadecimal from binary number",s,"is:",hexa[i])
        i -= 1
if __name__ == '__main__':
    s = input("Enter the binary number:")
    binary(s)

```

# Explanation
  Challenge 3
  the function decimal : converts the decimal number into hexadecimal number,in here hexa=['0']*100
     while(n != 0):
		temp = 0
		temp = n % 16
		if(temp < 10):
			hexa[i] = chr(temp + 48)
			i = i + 1
		else:
			hexa[i] = chr(temp + 55)
			i = i + 1
		n = int(n / 16)
	j = i - 1
     while j>=0 print the result
  the function binary:converts the binary number into hexadecimal number, in here length of the entered number is checked,then
      while (i >= 0):
        sum += (ord(s[i]) - ord('0')) * m
        m *= 2
        temp += 1
        if (temp == 4 or i == 0):
            if (sum <= 9):
                hexa.append(chr(sum + ord('0')))
            else:
                hexa.append(chr(sum + 55));
            temp = 0
            sum = 0
            m = 1
        i -= 1
    j = len(hexa)
    i = j - 1
  while i>=0 print the result 
