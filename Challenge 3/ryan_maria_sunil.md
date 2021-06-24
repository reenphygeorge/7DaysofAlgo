# Code
```
def to_hex(n):
    print("From the options below choose the base of the no given to convert :")
    ch=int(input("1.Base-2  2.Base-10\n"))
    if ch==1:
        bin=["0","1"]
        if(all(cha in bin for cha in str(n))):
            n=int(n)
            count=0
            i=0
            while n>0:
                rem=n%2
                pdt=rem*(2**i)
                count+=pdt
                n=n//10
                i+=1
            n=count
            ch=2
        else:
            return("")
    if ch==2:
        if str(n).isdigit():
            n=int(n)
            hexa=["0","1","2","3","4","5","6","7","8","9","A","B","C","D","E","F"]
            list1=[]
            if n==0:
                return 0
            else:
                while n>0:
                    rem=n%16
                    n=n//16
                    list1.append(hexa[rem])
                new_list=list1[::-1]
                return("".join(new_list))
        else:
            return("")
    return("")
    
print(to_hex(243))
```

# Explanation
The function to_hex converts the no in base-2 or base-10 to its corresponding value in base-16. First we ask the user whether the given no is of base-2 or of base-10. If the no is 
of base-2 then we execute the code under first if. Where we again check whether the given value to convert is in proper binary form ie it contains only 0's and 1's.
If the no is of proper binary form then we implemet while loop. Where we extract each value of the no from the end and multiply it with 2 to the power i(starts with 0) where i increments at the end 
of the loop. After implementing the loop we get the decimal value of the binary no. Then we implement the next code under next if which converts a decimal no to hexadecimal no.
Here first we check whether the given no is a proper decimal no. If so,we check whether the given no is 0 , If true we return the value 0.Else we implement a while loop where we 
divide the no by 16 and append the list with the corresponding value of remainder in hexa. After the loop we reverse the list and join the elements in the list to make a string.
We finally return the string so obtained.
