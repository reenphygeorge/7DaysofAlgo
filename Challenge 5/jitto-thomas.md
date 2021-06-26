# CODE
~~~python

def encypt(text, s):  
    result = ""  
    for i in range(len(text)):  
        char = text[i]  
        if (char.isupper()):  
            result += chr((ord(char) + s - 64) % 26 + 65)  
        else:  
            result += chr((ord(char) + s - 96) % 26 + 97)  
    return result  
text = input("Enter the text:\t") 
s =int(input("Enter the value to be shifted:\t"))
print("Cipher: " + encypt(text, s))  
~~~

# EXPLANATION
  *In the main function the user inputs the string to be coded and the number of shifts to be applied
  *The values are passed to the function encrypt 
  *Here the string is traverseed and each character is encoded using the formulae (x + n) % 26
