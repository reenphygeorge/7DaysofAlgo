# Code
```c
#include <stdio.h>

int isPrime (int num){
  if(num==1){
    return 0;
  }
  
  for(int i=2;i<num;i++){
      if(num%i==0){
          return 0;
      }
  }
  return 1; 
}

int main() {
	isPrime(7);
return 0;
}
```

# Explanation

* The user defined function isPrime() is of data type int.
* At first in this function it checks whether the number is one and stops the execution of function if it is 1.
* The for loop in the function runs from 2 to the the highest number less than the entered number.
  * In each iteration it is checked if the number is perfectly divisible by iterator.
    * If number is perfectly divisible the function will return 0 indicating it is not a prime number and stops the itteration and saves time
  * If the iteration completes that means the number is not perfectly divisible by any number other than one and that number itself so it is prime.
    * So it returns 1 indicating it is prime number. 
   
