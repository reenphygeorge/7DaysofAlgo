# Code
```
def mergeSort(n):
    if len(n) > 1:
        mid = len(n) // 2
        l = n[:mid]
        r = n[mid:]

        mergeSort(l)
        mergeSort(r)
        i = j = k = 0
        while i < len(l) and j < len(r):
            if l[i] < r[j]:
                n[k] = l[i]
                i = i + 1
            else:
                n[k] = r[j]
                j = j + 1
            k = k + 1

        while i < len(l):
            n[k] = l[i]
            i = i + 1
            k = k + 1

        while j < len(r):
            n[k] = r[j]
            j = j + 1
            k = k + 1
list = int(input("no.of values : "))
n = [(input("Enter values:")) for i in range(list)]
mergeSort(n)
print("sorted list : " + str(n))
```

# Explanation
Enter the number of elements
enter the values
in function mergeSort     if len(n) > 1:
        mid = len(n) // 2
        l = n[:mid]
        r = n[mid:]
       mergesort l,r
   if l[i] < r[j]:
                n[k] = l[i]
                i = i + 1
            else:
                n[k] = r[j]
                j = j + 1
            k = k + 1

        while i < len(l):
            n[k] = l[i]
            i = i + 1
            k = k + 1

        while j < len(r):
            n[k] = r[j]
            j = j + 1
            k = k + 1
 print the sorted list
