# CODE
```python
one = ["","one","two","three","four","five","six","seven","eight","nine","ten","eleven","twelve","thirteen","fourteen","fifteen","sixteen","seventeen","eighteen","nineteen"]
ten = ["","","twenty","thirty","forty","fifty","sixty","seventy","eighty","ninety"]

def spell_it(number,s):
	str = ""
	if (number > 19):
		str += ten[number // 10] + one[number % 10]
	else:
		str += one[number]
	if (number):
		str += s
	return str
  
def convertToWords(number):
	out = ""
	out += spell_it(((number // 100) % 10)," hundred ")
	if (number > 100 and number % 100):
		out += "and "
	out += spell_it((number % 100), "")
	return out

number=int(input("enter the number"))
print(convertToWords(number))
```

# EXPLANATION
  *Two functions are defined
  *One for splitting the digits to ones and tens and the other for printing the name
  *Two arrays are defined one with names one to nineteen and the other contains tens place value names
  *The user input is taken from the main function and is passed to the convertowords function
  *An empty string is defined here which is concatinated by the function spell_it
  *If the number is greater than 100 a string hundred and an and are inserted
  *If ithe number is less than 100 we have define all names in one and ten arrays and the name is given according to the index value
