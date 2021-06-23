# Code
```
def spell_it(n):
    if n in range(0,1000000000):
        ones={1:"one",2:"two",3:"three",4:"four",5:"five",6:"six",7:"seven",8:"eight",9:"nine"}
        tens={1:{1:"eleven",2:"twelve",3:"thirteen",4:"fourteen",5:"fifteen",6:"sixteen",7:"seventeen",8:"eighteen",9:"nineteen"},2:"twenty",3:"thirty",4:"forty",5:"fifty",6:"sixty",7:"seventy",8:"eighty",9:"ninty"}
        hun=["hundred","thousand","lakh","crore"]
        flag=0
        k=0
        p=0
        list1=[]
        if n==0:
            return("zero")
        else:
            while n>0:
                rem=n%10
                if flag==0:
                    if n%100==10 and p!=1:
                        val="ten"
                        list1.append(val)
                        n=n//100
                        flag=0
                        k=1
                    elif rem!=0 and p!=1:
                        val=ones[rem]
                        list1.append(val)
                        n=n//10
                        flag+=1
                        num=rem
                    elif p==1:
                        if n%10!=0:
                            val=ones[rem]
                            list1.append(val)
                            n=n//10
                            k=1
                        else:
                            k=1
                            n=n//10
                            pass
                    elif rem==0:
                        flag+=1
                        n=n//10
                        pass
                elif flag==1:
                    if rem==1:
                        val=tens[rem][num]
                        if list1!=[]:
                            list1.pop()
                        list1.append(val)
                        
                    elif rem==0:
                        pass
                    else:
                        val=tens[rem]
                        list1.append(val)
                    n=n//10
                    flag=0
                    k=1
                if k==1: 
                    if n%100>0:
                        if p==0 and n%10>0:
                            val=hun[p]
                            list1.append(val)
                        elif p!=0:
                            val=hun[p]
                            list1.append(val)
                    k=0
                    flag=0
                    p+=1
                    k=0
            new_list=list1[::-1]
            return(" ".join(new_list))
    else:
        return("")
            
print(spell_it(7))      
```

# Explanation
The function spell_it is used to spell the given positive no in the range 0 to 999999999. First we make dictionary ones,tens and hun. ones contains the words of digits and tens contains the
word of the two digit value. Here flag is used to take values alternatively from ones and tens. k is used when we want to take values from hun. p is used to index the values in hun. 
We first checks whether the given no is 0. If so we return the word zero. If the given no is not 0 then we implement a loop.
Inside the loop we enter the word of nos in reverse order ie the last no word is entered first likewise then after the loop we reverse the list and join the elements in the list with space separation and will 
return the final string.
In the loop we extract each digits and covert it into their corresponding word and will append into list.In the end we reverse this list and join it using space separation.





