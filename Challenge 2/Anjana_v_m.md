# code
```python
def spell_it(n):
    if (n >= 0 and n < 1000):
        numbers = ['zero','one','two','three','four','five','six','seven','eight','nine','ten','eleven','twelve','thirteen','fourteen','fifteen','sixteen','seventeen','eighteen','nineteen','twenty ','thirty ','fourty ','fifty ','sixty ','seventy ','eighty ','ninty ']
        if (n <= 20):
            return numbers[n]
           
        elif (n < 100):
            x=n-20
            r=x%10
            x =x//10
            if (n % 10 == 0):
                return numbers[20+x]
            else:
                return numbers[20+x]+numbers[r]
        elif (n < 1000):
            if (n%100 == 0):
                x=n//100
                return numbers[x]+' hundred'
            else:
                r=n%100
                x=n//100
                if (r <= 20):
                    return numbers[x]+' hundred'+' and '+numbers[r]
                else:
                    r=r-20
                    d=r//10
                    r=r%10
                    return numbers[x]+' hundred'+' and '+numbers[20+d]+numbers[r]
       
       

n=int(input())
print(spell_it(n))

```

# Explanation

Here we have a list  that store words of numbers from 1-20 and tenth position numbers.All other numbers can be obtained by comparing these names.In the list,index from 0-20
gives words of numbers from 0-20 respctively.So to find words of numbers from this range, we can obtain it by indexing.The remaining index represents words of tenth position.
words of number 30 is at list[21].The tenth position words begin from index 21 in order.We know that 65 can be written as 6x10+5.We use modulus and integer division to obtain remainder and quotient.
Initially we subtract 20 from our input and continue to find modulus and division and add 20 to index in return statement to get correct words of number.i.e in case of 65 , first reduce 20 from 65,i.e 
45. then we find remainder(5) and quotient(4).In return we add list[quotient+20]+list[remainder].Here list[quotient+20] is list[24],i.e sixty. and list[remainder] is five.Therefore sixty five.
In case of numbers greater than 100, we use same method.Infact word hundred is added to them by string concatenation
