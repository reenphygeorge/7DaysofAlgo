##### Challenge 4: Sort Me.
##### Problem Statement: Implement a pure function that takes an array of numbers as an argument and return the array sorted. The sorting must be done through the merge sort algorithm
##### Author: Dona Maria Sunny (S6, CSE)
##### Language used: Python 3
# Code
```python
def mergeSort(numberArray):
    length=len(numberArray)
    if(length>1):
        i=0
        j=0
        k=0
        middle=length//2
        leftArray=numberArray[:middle]
        rightArray=numberArray[middle:]
        mergeSort(leftArray)
        mergeSort(rightArray)

        while( i<len(leftArray) and j<len(rightArray) ):
            if(leftArray[i]<rightArray[j]):
                numberArray[k]=leftArray[i]
                i=i+1
            else:
                numberArray[k]=rightArray[j]
                j=j+1
            k=k+1

        while(i<len(leftArray)):
            numberArray[k]=leftArray[i]
            i=i+1
            k=k+1
        while(j<len(rightArray)):
            numberArray[k]=rightArray[j]
            j=j+1
            k=k+1
        return(numberArray)



length=int(input("Enter length of your array:"))
numberArray=[]

for x in range(0,length):
    element=int(input("Enter element:"))
    numberArray.append(element)

sortedArray=mergeSort(numberArray)

print("\nSorted array is:")
for x in range(0,length):
    print(sortedArray[x], end=" ")
    



```
# Explanation
1. User enters the ```length``` and ```elements``` of array. Elements are stored in ```numberArray```
2. Now the function **mergeSort()** is called. ```numberArray``` is passed to it.
3. Inside the function the following happens:
   * Middle of the array is found. Using that the ```numberArray``` is divided into two sub arrays.  
   * **mergeSort()** is called again, for the left array and also for the right array.
   * Merging of sub arrays done after the two sub arrays are sorted.
   * Process continued till all ```elements``` are sorted.
   * Sorted array is returned and is printed as output.     
             
   
