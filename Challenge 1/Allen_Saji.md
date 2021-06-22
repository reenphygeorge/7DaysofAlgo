# Code
```cpp
#include<iostream>
#include<math.h>
using namespace std;

bool isPrime(int num){
for(int i=2;i<=sqrt(num);i++){
    if(num%i==0){
        return  false;
    }
}
return true;
}

int main(){
    int n;
    cout<<"Enter a natural number: ";
    cin>>n;

if(isPrime(n)){
    cout<<"True"<<endl;
} else{
    cout<<"False"<<endl;
}

return 0;
}
```


# Explanation
1.A number is said to be prime if it has only two factors,i.e, one and the number itself.
2.A function named isPrime() is defined:
 It contains a loop which checks if the inputted  natural natural is a prime number or not.
3. The loops checks the divisiblity of the inputted natural number ranging from 2 to square root of the inputted number.
  (square root of the number because even if  there is a factor that is greater than square root of n , the factor will still be the multiple of a number smaller than square root of the inputted number which has already been checked.)
4. So if the inputted number is divisible by any of the numbers in the above mentioned loop's range, then a false value is returned , otherwise True.
5. Then this function is called in the int main() function and if isPrime() is true ,then true is printed, else false is printed.

