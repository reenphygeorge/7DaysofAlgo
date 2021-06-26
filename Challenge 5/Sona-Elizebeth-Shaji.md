# Code
```
def encrypt(S,n):
	res = ""
	for i in range(len(S)):
		char = S[i]
		if (char.isupper()):
			res+= chr((ord(char)+n-65)%26+65)
		else:
			res+= chr((ord(char)+n-97)%26+97)
	return res
S = input("Enter string:")
n = int(input("Enter the shift:"))
print("The entered string: "+S)
print("Shift: "+str(n))
print("Cipher: "+encrypt(S,n))

```

# Explanation
 - Enter the string to be cipher,enter the shift .
 - for a range of length of entered string:
 - char= entered string
 - if the string is uppercase:
     - the result=chr((ord(char)+n-65)%26+65)
 - else:
     - the result=chr((ord(char)+n-97)%26+97)
 - Return the cipher string 
