# Code
```python
def spell_it(n):
    if(n==0):
        return "Zero"
    result = convert(((n // 1000) % 100),"Thousand ")
    result += convert(((n // 100) % 10),"Hundred ")
    if n > 100 and n % 100:
        result += "and "
    result += convert((n % 100), "")
    return result

def convert(n,s):
    if n ==0:
        return ""
    if n > 19:
        return Y[n // 10] + X[n % 10] + s
    else:
        return X[n] + s

X = ["", "One ", "Two ", "Three ", "Four ", "Five ", "Six ",
    "Seven ", "Eight ", "Nine ", "Ten ", "Eleven ", "Twelve ",
    "Thirteen ", "Fourteen ", "Fifteen ", "Sixteen ",
    "Seventeen ", "Eighteen ", "Nineteen "]
Y = ["", "", "Twenty ", "Thirty ", "Forty ", "Fifty ",
    "Sixty ", "Seventy ", "Eighty ", "Ninety "]
n=int(input("Enter a number:"))
print(spell_it(n))
```
# Explanation
1. User enter a number (n)
2. `spell_it()` function is called with the user entered number(n) as parameter
   * spell_it() function return "Zero" if the entered number is 0
   * Otherwise, each digit of the number and the suffix is seperated and passed to the `convert()` function
     * Inside convert() functoion digits is converted to word and it is concatinated with the suffix, then it is returned to spell_it() function
   * After visiting all digits the concatinated result value is returned to the main and print it
