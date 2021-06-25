# code

```python
def mergesort(array):
   
    if (len (array) == 1):
        return array
    if len(array) > 1:
        mid = len(array)//2
        array1 = array[:mid]
        array2 = array[mid:]
        mergesort(array1)
        mergesort(array2)
 
        i = j = k = 0
        while i < len(array1) and j < len(array2):
            if array1[i] < array2[j]:
                array[k] = array1[i]
                i = i+1
            else:
                array[k] = array2[j]
                j =j+ 1
            k=k+1
 
        
        while i < len(array1):
            array[k] = array1[i]
            i =i+1
            k =k+1
 
        while j < len(array2):
            array[k] = array2[j]
            j =j+1
            k =k+1
        return array
limit = int(input("Enter the limit of your array:\n"))
array = []
print("Enter the Numbers to be Sorted:\n")
for i in range(limit):
    x = int(input())
    array.append(x)
print ("Array before merge sort:",array)
print("Array after merge sort:",mergesort(array))
```

# Explanation
Here, we input an array named array.This array is divided into two equal halves named array1 and array2.First both these arrays are sorted and then they are combined by comparing elements
in both arrays and they are sorted and finally this array is given as output.
