# code
```python
def mergeSort(list1):
    if len(list1) > 1:
        mid=len(list1) // 2
        left=list1[:mid]
        right=list1[mid:]
        mergeSort(left)
        mergeSort(right)
        i = 0
        j = 0
        k = 0
        while i < len(left) and j < len(right):
            if left[i] <= right[j]:
              list1[k] = left[i]
              i += 1
            else:
                list1[k] = right[j]
                j += 1
            k += 1
        while i < len(left):
            list1[k] = left[i]
            i += 1
            k += 1
        while j < len(right):
            list1[k]=right[j]
            j += 1
            k += 1
print("Enter the Array elements:")
list1=list(map(int,input().strip().split()))
mergeSort(list1)
print(list1)
```
# Explanation
1. Input the array elements into a list(`list1`)
2. Call `mergeSort()` function and pass list1 as parameter
   * Divide the list and pass the resultant list to mergeSort() as recursive function call
   * Using while loops sort and combine the divided list elements
   * After sorting andcombining every sublists, the entire list will get sorted
3. print the sorted list 
