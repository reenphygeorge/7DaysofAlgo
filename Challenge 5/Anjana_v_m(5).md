#code
```python
def encryption(text,s):

    c="ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    u="abcdefghijklmnopqrstuvwxyz"
    for i in text:
        if i in c:
            ind=c.index(i)
            final=(ind+s)%26
            print (c[final],end="")
        elif i in u:
            ind=u.index(i)
            final=(ind+s)%26
            print (u[final],end="")
        else:
            print ("Oops!something went wrong")
                    
        
text=input("Enter your Text\n")
s=int(input("Enter your shift\n"))
encryption(text,s)
```

# Explanation
CaesarCipher is used for encryption.The function takes text to be encrypted and Number of shifts has to be done as parameters.We use the concept of (x+n)%26 where 'x' is the position
of that alphabet in alphabetic order and 's' is the shift to be performed.Consider the first letter of our input,(x+n)%26 can lead you to a new number and this will be the position of our encrypted
letter.We continue this for all letters in our input using a for loop.If you entered something wrong,program leads you to else loop indicating something error has occured.
