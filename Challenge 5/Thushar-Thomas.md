# Code
```python
'''
Documentation
Program to convert a word to ceaser cipher (Only Alphabets)

Name   : Thushar Thomas
Branch : AI & DS
'''
def ceaser(t,s):    # Function to covert word to ceaser cipher
    encry=""
    if s>25:
        print("Cannot shift more than 25")
        return "None"
    if len(t)==0:    # Checking whether user entered any word
        print("\nNo text entered")
        return "None"
    for i in range(len(t)):
        char = t[i]
        if 64<ord(char)<91:    # Converting upper case letters to cipher
            if (ord(char)+s)>90:
                char=chr(ord(char)-26)
            encry = encry + chr(ord(char) + s )
        elif 96<ord(char)<123:    # Converting lower case letters to cipher
            if (ord(char)+s)>122:
                char=chr(ord(char)-26)
            encry = encry + chr(ord(char) + s )
        else:    # If non-alphabet characters are entered
            print("\n Only characters are suported in this program.\n Please try again.")
            return "None"  
    return encry

text=input("Enter the word to be encrypted: ")
shift=int(input("Enter the shift: "))
print("\nEncrypted Text: " + ceaser(text,shift))    # Calling Function
```

# Explanation
####In this program, user can enter a word and convert to ceasar cipher upto 25 shift.
<p> <br/>The word is converted into letters. Each letter is then converted to it's ASCII value and the shift is added to it.
    <br/>Then the ASCII value with shift is converted back to letter. Then those letters are converted to a word.
   <br/>**Error fixed**: If the shift results in exceeding of ASCII value from the alphabet range to symbol range, it violates the ceasar cipher.
  <br/>The program ensures that the ASCII value do not exceed the alphabet range
   
<br/>Thank you
