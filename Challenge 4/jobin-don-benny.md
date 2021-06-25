CODE:
```java

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        System.out.println("Enter the size of the Array");
        Scanner scanner = new Scanner(System.in);
        int size= scanner.nextInt();
        int[] array = new int[size];
        System.out.println("Enter the Numbers to be Sorted");
        for (int i=0; i<size; i++){
            array[i] = scanner.nextInt();
        }
        sortArray(array,size);
        printArray(array);

    }
    static void sortArray(int[] array,int length){

        if(length<=1)
            return;
        int mid=length/2;
        int[] left =new int[mid];
        int[] right =new int[length-mid];
        System.arraycopy(array, 0, left, 0, mid);
        if (length - mid >= 0) System.arraycopy(array, mid, right, 0, length - mid);
        sortArray(left,mid);
        sortArray(right,length-mid);
        merge(left,right,array);


    }
    static void merge(int[] left,int[] right,int[] array){
        int numberL=left.length;
        int numberR=right.length;
        int i,j,k;
        i=j=k=0;
        while(i<numberL&&j<numberR)
        {
            if(left[i]<=right[j])
            {
                array[k]=left[i];
                i++;
            }
            else
            {
                array[k]=right[j];
                j++;
            }
            k++;
        }
        while(i<numberL)
        {
            array[k]=left[i];
            i++;
            k++;
        }
        while(j<numberR)
        {
            array[k]=right[j];
            j++;
            k++;
        }

    }
    static void printArray(int[] arr)
    {
        System.out.println("Sorted Array is:");
        for (int j : arr) System.out.print(j + " ");
    }


}

```
Explanation:
```java
- This code is the implementation of a Merge Sort.
- In the Main() method we obtain the size of the array to be created and the elements of the array.
- The sortArray() method divides the input array into two halves, calls itself for the two halves until each sub array has only one element.
- The merge() function is used for merging the smaller arrays into new array in sorted order.

