# Code
```
def encode(Text):
    step=int(input("Enter the shift required : "))
    outText=[]
    uppercase=['A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z']
    lowercase=['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
    for letter in Text:
        if letter in uppercase:
            ind=uppercase.index(letter)
            val=(ind+step)%26
            new_letter=uppercase[val]
            outText.append(new_letter)
        elif letter in lowercase:
            ind=lowercase.index(letter)
            val=(ind+step)%26
            new_letter=lowercase[val]
            outText.append(new_letter)
    return("".join(outText))

string=input("Enter the string to be encoded : ")
print(encode(string))
```

# Explanation
encode is a function in which the string encoding operation is performed. For this the string to be encoded is passed to the function. In the function we ask the user the shift no
 required. In the for loop, we extract each letter from the Text to be decoded and checks whether it is in uppercase list or lowercase list. If it is uppercase then we find the index of 
 the letter in uppercase list. To find the index of the encoding letter, we need to take the sum of the index value of the letter and the step value that you have already fixed .This 
 sum has to be divided by 26 and its remainder gives the index value of the encoding letter. The encoding letter is placed in new_letter which is the added to list outText.
 If it is lowercase then we find the index of 
 the letter in lowercase list. To find the index of the encoding letter, we need to take the sum of the index value of the letter and the step value that you have already fixed .This 
 sum has to be divided by 26 and its remainder gives the index value of the encoding letter. The encoding letter is placed in new_letter which is the added to list outText.
 After the loop, the function returns the string obtained by joining the list outText
