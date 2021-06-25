# Code
```python
def mergeSort(array):
    if len(array) > 1:
        mid = len(array)//2
        left_array = array[:mid]
        right_array = array[mid:]
        mergeSort(left_array)
        mergeSort(right_array)
        i = j = k = 0
        while i < len(left_array) and j < len(right_array):
            if left_array[i] < right_array[j]:
                array[k] = left_array[i]
                i += 1
            else:
                array[k] = right_array[j]
                j += 1
            k += 1
        while i < len(left_array):
            array[k] = left_array[i]
            i += 1
            k += 1
        while j < len(right_array):
            array[k] = right_array[j]
            j += 1
            k += 1
def printArray(array):
    for i in range(len(array)):
        print(array[i], end=" ")
    print()
num = int(input("Enter how many number of elements you want: "))
array = list(map(int,input("Enter the numbers in single line with space : ").strip().split()))[:num]
print("Unsorted array is:",array)
mergeSort(array)
print("Sorted array is: ",end="")
printArray(array)
```
# Explanation
* In this program,I have taken two function mergeSort,used to sort and printArray,used to print the sorted array.
* In mergeSort function,
    1.  first split the Unsorted array.
    2.  compare each of the elements and group.
    3.  repeat step2 until whole list is merged and sorted.  
* In printArray function,the sorted array gets displayed.
