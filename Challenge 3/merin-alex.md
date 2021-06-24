# Challenge 3
## Code: Python3

```python
#convert a whole number in either base 2 or base 10 format to base 16 

def to_hex(num):
      return 'hex value is '+hex(num)[2:]
print(to_hex(int(input("Enter a decimal number: "))))
print(to_hex(int(input("Enter a binary number: "),2)))
```
## Code Explantion
* The function `to_hex()` is declared and it accepts a decimal number(base 10) and binary number(base 2) from the user and returns hexadecimal value(base 16) of that number
* The `hex()` function converts the input number(decimal or binary number) to hex value
* A slicing operation `hex(num)[2:]` is performed on `hex()` function to eliminate initial two indexes values '0x' (it is an indication of base and does not contribute to the value)
* Finally hexadecimal value(base 16) is returned to the calling function
## Output

Decimal number | Heaxdecimal number |
---            |                --- | 
123456         | 1e240              |




Binary number | Heaxdecimal number  |
---           |                ---  |  
11111000111   | 7c7                 |


  ------
  Done with ☕️ and code 🙋‍♀️
