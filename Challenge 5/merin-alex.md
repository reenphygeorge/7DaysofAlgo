## Code: Python3

```python3
string=input('enter string to be encrypted: ')
shift=int(input('enter shift: '))
s=''
for i in list(string):
    if i.isupper()==True:
        s+=chr(((ord(i)-65+shift)%26)+65)  
    elif i.islower()==True:
        s+=chr(((ord(i)-97+shift)%26)+97) 
    else:
        s+=i
print(s)
```
## Code Explanation
 * read the string
 * read shift value
 * create an empty string s
 * iterate through each character i in the string
 * do the following:
    * append the new character, so obtained by subtacting (65 if the i is uppercase else 97 if i is in lowercase) and adding the 
  ord (ord fn returns unicode of i) of i with shift
  and then applying modulo on the above result with 26 (since there are 26 alphabets hence ensuring that the result range bw 0 and 25), followed by 
  adding (65 if the i is uppercase else 97 if i is in lowercase), with s.
    * if not an alphabetical character, simply append that character to s.

## Ouptut

| string   |      shift    |   s   |
|----------|:-------------:|------:|
| merin    |       1       | nfsjo |
| ABCD     |       2       |  CDEF |

---
☕️ and </> ❤️
  
  
  
