# Code
```
def spell_it(digit):

    l=len(digit)
    if(l==0):
       print("Empty")
       return
    if(l>4):
       print('more than four digit is not supported')
       return
    ones=["zero","one","two","three","four","five","six","seven","eight","nine"]
    twos=["","ten","eleven","twelve","thirteen","fourteen","fifteen","sixteen","seventeen","eighteen","nineteen"]
    tens=["","","twenty","thirty","forty","fifty","sixty","seventy","eighty","ninety"]
    thee=["hundred","thousand"]
    print(digit,":",end=" ")
    if(l==1):
       print(ones[ord(digit[0])-48])
       return
    x=0
    while(x<len(digit)):
       if(l>=3):
         if(ord(digit[x])-48!=0):
             print(ones[ord(digit[x])-48],end=" ")
             print(thee[l-3],end=" ")
         l-=1
       else:
         if(ord(digit[x])-48==1):
             sum=(ord(digit[x])-48 + ord(digit[x+1])-48)
             print(twos[sum])
             return
         elif(ord(digit[x])-48==2 and ord(digit[x+1])-48==0):
             print("twenty")
             return
         else:
             i=ord(digit[x])-48
             if(i>0):
                print(tens[i], end=" ")
             else:
                print("",end=" ")
             x+=1
             if(ord(digit[x])-48!=0):
                print(ones[ord(digit[x])-48])
             x+=1
digit=input("enter")
print(spell_it(digit))
```

# Explanation
 Enter the digit, the code checks the length of the digit and executes the steps accordingly(if length is greater than 4 it won't
 execute,otherwise execute the code).if length is 1 it print the values in ones list. If the length greater or equal to 3 it prints the 
 values in ones list and degree .Else ,if ord(digit[x])-48==1 take the sum x and x+1 ;elif ord(digit[x])-48==2 & ord(digit[x])-48==0
 print twenty.else : i=ord(digit[x])-48 ; if i>0 print tens list;else print value. print the digit in word
