# Code
```python
'''
Documentation
Program to sort an arry using merge sort

Name   : Thushar Thomas
Branch : AI & DS
'''
def Merge_Sort(arr):    # Function to sort an array 
    if len(arr) > 1:    # Checking whether the array has more than 1 element
        i=0
        j=0 
        k=0
        mid=int(len(arr)/2)    
        arr1=arr[:mid]    # First half of the original array
        arr2=arr[mid:]    # Second half of the original array
        Merge_Sort(arr1)  # Dividing the array further
        Merge_Sort(arr2)

        while i<len(arr1) and j<len(arr2):    # Sorting the array 
            if arr1[i]<arr2[j]:
                arr[k]=arr1[i]
                i+=1
            else:
                arr[k]=arr2[j]
                j+=1
            k+=1
        
        while i < len(arr1):    # Inserting already sorted array
            arr[k] = arr1[i]
            i+=1
            k+=1
        while j < len(arr2):
            arr[k] = arr2[j]
            j+=1
            k+=1

Arr = []
n = int(input("Enter number of elements : "))
if n>20:
    print("\n Array with more than 20 elements is forbidden in this program.\n Please try again.")
else:
    for i in range(0, n):
        print("Enter the element",i+1,":",end=" ")
        e = int(input())
        Arr.append(e)
    print("\nArray before sorting: ",Arr)
    Merge_Sort(Arr)
    print("\nArray after sorting: ",Arr)
```

# Explanation
In this program, user can enter an array with elements upto 20 elements.
<p> <br/>Then the array is sorted using Merge sort method.
         Merge sort uses divide and conquer method. The array is divided into half again and the half is again halved, till it form an array with 1 element.
   <br/>* The last array is compared with it's other half and both the arrays are stored and then merged.
   
<br/>Thank you
