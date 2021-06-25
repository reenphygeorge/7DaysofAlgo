# CODE
~~~python
array=[]
def mergeSort(array):
    if len(array) > 1:
        mid = len(array)//2
        left= array[:mid]
        right= array[mid:]
        mergeSort(left)
        mergeSort(right)
        i = j = k = 0
        while i < len(left) and j < len(right):
            if left[i] < right[j]:
                array[k] = left[i]
                i=i+1
            else:
                array[k] = right[j]
                j=j+1
            k=k+1
        while i < len(left):
            array[k] = left[i]
            i=i+1
            k=k+1
        while j < len(right):
            array[k] = right[j]
            j=j+1
            k=k+1
n=int(input("ENTER THE LENGTH OF THE ARRAY TO BE SORTED"))
for i in range(n):
    x=int(input())
    array.append(x)
mergeSort(array)

print("THE SORTED ARRAY IS :")
for i in range(n):
        print(array[i], end=" ")
print()
~~~

# EXPLANATION
  *In the main function the user inputs the length of the array and the elements of the array
  *The array elements are passed to the function mergeSort
  *In the mergeSort function the array is divided into two sub arrays left and rigth
  *This process is repeated until sub arrays become a length of 1
  *All the sub arrays are compared and sorted and merged together to form the new array
  *The new array formed is passed to the main function to print the result
