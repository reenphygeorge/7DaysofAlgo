## Code: Python3
```python3
def hcf_lcm(a,b):
    large=1
    minm=a if a<b else b
    larger=a if a>b else b
    
    for i in range(1,minm+1):   
        if a%i==0 and b%i==0:
            large=i
            
    while(True):
        if a==0 or b==0:
            small=0
            break
        
        elif larger % a == 0 and larger % b == 0:
            small = larger
            break
        larger += 1
    return large,small

    

a,b=map(int,input('enter 2 numbers space seperated ').split())
print('largest number that completely divides both numbers is: ',hcf_lcm(a,b)[0],', the smallest number that is the product of both numbers is:',hcf_lcm(a,b)[1])
```
## Explanation
* largest number that completely divides both numbers is the hcf 
* the smallest number that is the product of both numbers is lcm
* defined a function  hcf_lcm which takes two arguments a and b (integers)
* minm stores smallest of a and b and larger stores largest amongst the two
* To compute hcf, iterate i over range 1 and minm+1(to include value of minm), and find that largest value of i during iteration which
completely divides a and b, and hence the hcf.(note hcf of two factors can never be zero and hance large initialized to 1)
* To compute lcm, note:(lcm will be 0 when either of the 2 numbers is 0, then break and return 0 for lcm), else if larger(largest of and b) on division by a 
as well as b gives a remainder 0, assign lcm as larger and break(since it would be the least value) and if it doesnot return a remainder 0, keep
incrementing larger value by 1
* return values of hcf i.e large and lcm i.e small

---
☕️ and </> ❤️


