# Array2D

This project involves creating a class `Array2DTest` that demonstrates the use of a two-dimensional array in Java. The program fills the array with random integers, replaces all occurrences of the number `2` with `-1`, and prints the array before and after the modification.

## Objective

Create a Java program that:

- Initializes a 5x5 two-dimensional array of integers.
- Fills the array with random numbers.
- Replaces all occurrences of the number `2` with `-1`.
- Prints the array before and after the replacement.

### Example Implementation

#### Array2DTest.java

```java
import java.util.Random;

public class Array2DTest {
    public static void main(String[] args) {
        int rows = 5;
        int cols = 5;
        int[][] array = new int[rows][cols];
        Random random = new Random();

        // Fill the array with random numbers between 1 and 10
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                array[i][j] = random.nextInt(10) + 1; // Random number between 1 and 10
            }
        }

        // Print the original array
        System.out.println("Original Array:");
        printArray(array);

        // Replace all occurrences of 2 with -1
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (array[i][j] == 2) {
                    array[i][j] = -1;
                }
            }
        }

        // Print the modified array
        System.out.println("-------------------------");
        System.out.println("Modified Array:");
        printArray(array);
    }

    // Helper method to print the 2D array
    private static void printArray(int[][] array) {
        for (int[] row : array) {
            for (int value : row) {
                System.out.print(value + " ");
            }
            System.out.println();
        }
    }
}
```

### Example Output

When you run the `Array2DTest` class, you might get an output similar to this:

```
Original Array:
3 8 6 7 10 
3 3 8 9 5 
1 6 2 2 10 
7 10 2 2 7 
9 1 10 9 2 
-------------------------
Modified Array:
3 8 6 7 10 
3 3 8 9 5 
1 6 -1 -1 10 
7 10 -1 -1 7 
9 1 10 9 -1 
```

### Notes

- Ensure that you have the necessary Java environment set up to compile and run the program.
- You can modify the size of the array or the range of random numbers as needed.

Happy coding! 🎉