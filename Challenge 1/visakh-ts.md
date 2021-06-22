# Code
```
 const isPrime = num=>{
    let i;
     for(i=2;i<num;i++){
       if(num%i===0)
            return false
    }
  return true
 }

console.log(isPrime(4))
```

# Explanation

1.Here is a function called isPrime which will accept a natural number as a parameter and check the number is prime or not. 
2.We know a prime number is only divisible by 1 and that number
3.So if there is any number between 1 and that number which can divide the number then we can say the number is not a prime
4.So we need a loop that iterate between 2 and that number ,but actually we need to iterate between 2 and half of that number
because a number greater than half of that number will not produce a reminder 0, so that we can reduce time complexity
5.So we will take modulus of the input with all the numbers between 1 and half of that number
6.When we get 0 as modulus then we can say that the number is divisible by i and the function will return true ,otherwise after 
completing all the iterations the controll will come out side the loop and it will return false.
