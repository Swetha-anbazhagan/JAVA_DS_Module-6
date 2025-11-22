# EX 1  
# **You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.**

## **DATE:**  

## **AIM:**  
To write a JAVA program to determine the minimum value (e.g., lowest heartbeat) using a recursive method.

---

## **Algorithm**

1. Start the program.  
2. Initialize an array containing sensor readings.  
3. Define a recursive function `findMin(arr, index)` to find the minimum value.  
4. Compare current element with the result of the recursive call.  
5. Print the minimum value.  
6. End the program.

---

## **Program**
```
import java.util.*;

public class MinValueRecursive {

    public static int findMin(int[] arr, int index) {
        if (index == arr.length - 1) {
            return arr[index];
        }
        int minOfRest = findMin(arr, index + 1);
        return Math.min(arr[index], minOfRest);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of sensor readings: ");
        int n = sc.nextInt();

        int[] readings = new int[n];
        System.out.println("Enter the sensor readings:");
        for (int i = 0; i < n; i++) {
            readings[i] = sc.nextInt();
        }

        int minValue = findMin(readings, 0);
        System.out.println("Minimum sensor value (Lowest heartbeat): " + minValue);
    }
}
```
## Output:


## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
