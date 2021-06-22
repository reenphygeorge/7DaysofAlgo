##### Challenge 2: Spell it out.
##### Problem Statement: Implement a pure function that takes a whole number as an argument and returns the number in words. For eg. 26 would return a string ‘twenty six’.
##### Author: Dona Maria Sunny (S6, CSE)
# Code
```python
def spell_it(number):
    from num2words import num2words
    words=num2words(number)
    words=words.replace(",","")
    words=words.replace("-"," ")
    return(words)
    

number=int(input("Spell it out.\n Enter the whole number whose words needed:"))
print(spell_it(number))
```
# Explanation
1. User enters the ```number``` whose words need to be displayed.
2. Entered ```number``` is passed to the function and now the function **spell_it** is called.
3. Inside the function **spell_it** the following happens :
   * The module **num2words** is imported. Module should be installed before the execution of the code for the module to work.
   * To get the output in the format as given in the question **replace()** is used. So "-" and "," is removed in the output returned. 
