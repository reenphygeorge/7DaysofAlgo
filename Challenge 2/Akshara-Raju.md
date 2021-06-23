# Code
```
#Python Code

def spell_it(number):
    length = len(number)
    number = int(number)
    num_digit = ['Zero','One','Two','Three','Four','Five','Six','Seven','Eight','Nine','Ten','Eleven','Twelve','Thirteen','Fourteen','Fifteen','Sixteen','Seventeen','Eighteen','Nineteen']
    tens_digit = ['','','Twenty','Thirty','Fourty','Fifty','Sixty','Seventy','Eighty','Ninety']
    if number == 100:
        return('One Hundred')

    if number < 20:
        return(num_digit[number])
    elif number< 1000:
        if length == 2:
            return(tens_digit[number//10]+' '+num_digit[number%10])
        if length == 3:
            copy1 = number//100
            copy2 = number//10
            new_num = number%100
            if new_num < 20:
                return(num_digit[copy1]+' '+'Hundred'+' '+num_digit[new_num])
            else:
                return(num_digit[number//100]+' '+'Hundred'+' '+tens_digit[copy2%10]+' '+num_digit[number%10])
    elif number>999:
        return("Enter a number less than 1000")        


number = input('Enter a whole number (0-999):')
print(spell_it(number))



  


```

# Explanation
**number** is passed to the function. 2 lists of Numbers are made with proper index value to help in converting numbers to words. If the entered number is less than twenty, then we can use the number as the index and return the output from the **num_digit**.
If number is less than 999, it checks the length of the number and corresponding actions are performed. If number is greater than 999 then it returns **Enter a number less than 1000**.
