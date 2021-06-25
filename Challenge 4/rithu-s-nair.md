# Code

```python
array=[]
def mergeSort(array):
    if len(array) > 1:
        mid = len(array)//2
        left_list = array[:mid]
        right_list= array[mid:]

        mergeSort(left_list)
        mergeSort(right_list)

        i = j = k = 0
        while i < len(left_list) and j < len(right_list):
            if left_list[i] < right_list[j]:
                array[k] = left_list[i]
                i=i+1
            else:
                array[k] = right_list[j]
                j=j+1
            k=k+1

        while i < len(left_list):
            array[k] = left_list[i]
            i=i+1
            k=k+1

        while j < len(right_list):
            array[k] = right_list[j]
            j=j+1
            k=k+1
    
n=int(input("enter the length of array"))
for i in range(n):
    x=int(input())
    array.append(x)
mergeSort(array)

for i in range(n):
        print(array[i], end=" ")
print()


```
# Explanation

1.firstly user has to enter the unsorted array
2.function mergeSort() is called,array is passed as the parameter 
3.array should be divided so that,take the middle element by dividing(//) length of the array by 2.
4.After splitting,we will get two subarrays,here it is left_list and right_list
5.mergeSort() function is recursively called because we have to repeat splitting until length of array becomes 1.
6.Next we have to merge the subarrays.for that we are checking each element in the left_list with that of the right_list.
7.if the element in the left_list is lesser than the right_list,then enter the left_list element into the array,else enter the right_list element into the array.
8.Then we are using two while loops for adding the element left in the left_list or right_list into the array.
9.Finally,the sorted array is printed
