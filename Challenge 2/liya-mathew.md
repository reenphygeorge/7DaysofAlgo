# Code
```
def spell_it(n):
    assert (n>=0)
    digits_and_exceptions = {0: "zero", 1: "one", 2: "two", 3: "three", 4: "four", 5: "five", 6: "six", 7: "seven", 8: "eight", 9: "nine",
                             10: "ten", 11: "eleven", 12: "twelve", 13: "thirteen", 14: "fourteen", 15: "fifteen",
                             16: "sixteen", 17: "seventeen", 18: "eighteen", 19: "nineteen",
                             20: "twenty", 30: "thirty", 40: "forty", 50: "fifty", 60: "sixty", 70: "seventy",
                             80: "eighty", 90: "ninety"}
    if n in digits_and_exceptions.keys():
        return digits_and_exceptions[n]
    elif (len(str(n)) == 2):
        return digits_and_exceptions[n // 10 * 10] +" "+ digits_and_exceptions[n % 10]
    elif (len(str(n)) == 3):
        if (n % 100 == 0):
            return digits_and_exceptions[n // 100] + ' hundred'
        else:
            return digits_and_exceptions[n // 100] + ' hundred and ' + spell_it(n % 100)
    elif(len(str(n))<=5 ):
        if n % 1000 == 0:
            return spell_it(n // 1000) + ' thousand'
        else:
            return spell_it(n // 1000) + ' thousand' +" "+ spell_it(n % 1000)
    elif(len(str(n))<=7):
        if (n % 100000) == 0:
            return spell_it(n // 100000) + ' lakh'
        else:
            return spell_it(n // 100000) + ' lakh, ' + spell_it(n % 100000)
    elif (len(str(n)) <= 13):
        if (n % 10000000) == 0:
            return spell_it(n // 10000000) + ' crore'
        else:
            return spell_it(n // 10000000) + ' crore, ' + spell_it(n % 10000000)




print(spell_it(7))

```

# Explanation
Whole numbers can be expressed as ones,tens,hundreds,thousands,lakhs and crores.In our approarch we first ensure that the input is a whole number ,otherwise an assertionError would be raised.All the digits from 0 to 9 and exceptions (11 to 19 and 10,20,30,40 ,..) are intialized into a dictionary with its integer form as the key and word format as its value. The numbers from 11 to 19 as well as 20,30 etc are considered as exceptions because these numbers form their words in a different manner.
We check whether the input is in the already created dictionary if it is,the value corresponding to that is returned and the function terminates.Else, we check the integers according to their lengths and follow an recursive approach inorder to reduce complexity.
Integers of different length need to be handled in different ways.if length=2 (simplest base case ),we employ a mathematical formula to extract  the required value from the dictionary(digits) and transform the number into the desired output(words) and return it.
We have seperate else parts for hundreds,thousands,lakhs and crores.For all other cases, we first examine the number by dividing it with the smallest possible number of that range,if it is divisible then we recursevely call the function for the next digits(to left) of that number and transform it into the desired  output or else ,we employee a recursive formula extracting numbers  from right to left , inorder to transform our input number into its corresponding word.

