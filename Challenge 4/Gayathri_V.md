# Code
```

/*

Author     : Gayathri V
Challenge 4: Sort Me

*/


import java.util.Scanner;
public class MergeSort {

        public static void merge(int[] leftArr, int[] rightArr, int[] arr, int left, int right) {

            int i = 0, l = 0, r = 0;
            while (l < left && r < right) {

                if (leftArr[l] < rightArr[r]) {
                    arr[i++] = leftArr[l++];
                } else {
                    arr[i++] = rightArr[r++];
                }
            }
            while (l < left) {
                arr[i++] = leftArr[l++];
            }
            while (r < right) {
                arr[i++] = rightArr[r++];
            }
        }

        public static void mergeSort(int[] arr, int len) {
            if (len < 2) {
                return;
            }

            int mid = len / 2;
            int[] leftArr = new int[mid];
            int[] rightArr = new int[len - mid];

            //Dividing array into two and copying into two separate arrays
            int k = 0;
            for (int i = 0; i < len; ++i) {
                if (i < mid) {
                    leftArr[i] = arr[i];
                } else {
                    rightArr[k] = arr[i];
                    k = k + 1;
                }
            }
            mergeSort(leftArr, mid);
            mergeSort(rightArr, len - mid);
            merge(leftArr, rightArr, arr, mid, len - mid);
        }

        public static void main(String args[]) {

            Scanner scanner = new Scanner (System.in);

            int[] array= new int[40];

            for (int i = 0; i < array.length; ++i) {
                array[i] = scanner.nextInt();
            }

            mergeSort(array, array.length);
            for (int i = 0; i < array.length; ++i) {
                System.out.print(array[i] + " ");
            }
        }
    }

```

# Explanation
User able set of numbers into a array.
There is a function to perform divide the array into two equal parts and recalling the function to divide the obtained array again.
The array is divided with the formula last index plus first index and all divided by 2.
Finally the mergeSort with left and right array is called and separate function to merge is called.
Merge is done by checking the passed left and right index value and middle value , then comparing the elements with respect to the size of value.
The above process continued till the left value is less than right value.
Returning the sorted array and array is printed in main method.
Program terminates.
