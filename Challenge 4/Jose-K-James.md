# Code
```
def mergeSort(sortList):
    if len(sortList) > 1:
        mid = len(sortList)//2
        left = sortList[:mid]
        right = sortList[mid:]

        mergeSort(left)
        mergeSort(right)
        i = j = k = 0
        while i < len(left) and j < len(right):
            if left[i] < right[j]:
                sortList[k] = left[i]
                i = i+1
            else:
                sortList[k] = right[j]
                j = j+1
            k = k+1

        while i < len(left):
            sortList[k] = left[i]
            i = i+1
            k = k+1

        while j < len(right):
            sortList[k] = right[j]
            j = j+1
            k = k+1


sortList = [28, 5, 99, 124, 13, 12, 55, 11]
mergeSort(sortList)
print(sortList)
```

# Explanation
The program takes an array of numbers as an argument and return the sorted array using merge sort algorithm.  
- Here merge sort works as dividing the unsorted list into equal halves
- Repeatedly merge sublists to produce new sorted sublists until there is only 1 sublist remaining.
- This will be the sorted list.


Implemented a **Pure Function** that takes an array of numbers as an argument and return
> the **array sorted**  
> Using **merge sort** algorithm

******************************
Language used: Python3  
