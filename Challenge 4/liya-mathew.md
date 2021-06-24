# Code
```code:python3
def mergesort(arr):
    if (len(arr) > 1):
        middle_index = len(arr) // 2
        left_array = mergesort(arr[:middle_index])
        right_array = mergesort(arr[middle_index:])
        return merge(left_array, right_array)
    else:
        return arr

def merge(left_array, right_array):
    output_array = []
    i, j = 0, 0
    while i < len(left_array) and j < len(right_array):
        if left_array[i] <= right_array[j]:
            output_array.append(left_array[i])
            i += 1
        else:
            output_array.append(right_array[j])
            j += 1

    output_array += left_array[i:]
    output_array += right_array[j:]
    return output_array



print("Enter array to be sorted seperated by space:")
arr = list(map(int, input().split()))
print(mergesort(arr))

```

# Explanation
We need to implement a function accepting an array as its argument and sort it using merge sort.
* First we accept an array from the user seperated by space and call a function mergesort passing that array as its argument
* Inside the mergesort() function , we are dividing the intial unsorted array into two subarrays which are further being divided into sub arrays until each sub array has only one element.
*  * For this ,In all cases where the length of array is greater than one i.e, the array has more than one element ,we calculate the middle index and recursively call the mergesort() function passing the new sub arrays as its parameters.The two subarrays(leftarray and rightarray) are created by slicing the array based on middle index.Inorder to merge the new sub arrays after recursion we use another function called merge()
*   * In short we are performing for all recursion,
*   * * mergesort(leftarray)
*  * * mergesort(rightarray)
*   * * merge(leftarray,rightarray)
*   * In the merge() function,our primary objective is to merge the sub arrays in the same order in which it was divided. Let 'i' represent the index of leftarray and 'j' represent index of right array.We are checking whether each  index is less than the length of the correspoding arrays.if so,we check whether the value corresponding to the index in leftarray or rightarray is minimum,if it is minimum in the left array,we append the element in the leftararay to the outputarray and increment value of x. outputarray is an array(list) representing result of merging operation.If the minimum value lies in the rightarray,then we append the element from right array to output array and increment value of j.This process continues until any one index is more than its length. After this,we concatinate the remaining elements in the left array and right array(if it exists) into the output array and the outputarray is returned.
# OUTPUT

Enter array to be sorted seperated by space:
78 67 89  90 56 78 56 35
[35, 56, 56, 67, 78, 78, 89, 90]


