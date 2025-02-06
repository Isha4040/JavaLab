public class Main {
    public static void main(String[] args) {
        // 1. Count Array Elements
        int[] arr = {1, 2, 3, 4, 5};
        int count = arr.length;
        System.out.println("Count of elements: " + count);
 
        // 2. Sum of Array Elements
        int sum = 0;
        for (int num : arr) {
            sum += num;
        }
        System.out.println("Sum of elements: " + sum);
 
        // 3. Search for an Element in the Array
        int searchElement = 3;
        boolean found = false;
        for (int num : arr) {
            if (num == searchElement) {
                found = true;
                break;
            }
        }
        System.out.println("Element " + searchElement + (found ? " found." : " not found."));
 
        // 4. Calculate the Average of Array Elements
        double avg = (double) sum / count;
        System.out.println("Average of elements: " + avg);
 
        // 5. 2D Array Operations
        int[][] matrix1 = {{1, 2}, {3, 4}};
        int[][] matrix2 = {{5, 6}, {7, 8}};
 
        // 5.1 Matrix Addition
        int[][] resultAddition = new int[2][2];
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                resultAddition[i][j] = matrix1[i][j] + matrix2[i][j];
            }
        }
        System.out.println("Matrix Addition:");
        printMatrix(resultAddition);
 
        // 5.2 Matrix Subtraction
        int[][] resultSubtraction = new int[2][2];
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                resultSubtraction[i][j] = matrix1[i][j] - matrix2[i][j];
            }
        }
        System.out.println("Matrix Subtraction:");
        printMatrix(resultSubtraction);
 
        // 5.3 Searching for an Element in a 2D Array
        int searchElement2D = 6;
        boolean found2D = false;
        for (int i = 0; i < matrix1.length; i++) {
            for (int j = 0; j < matrix1[i].length; j++) {
                if (matrix1[i][j] == searchElement2D) {
                    found2D = true;
                    break;
                }
            }
        }
        System.out.println("Element " + searchElement2D + (found2D ? " found in the 2D array." : " not found in the 2D array."));
    }
 
    // Helper function to print matrix
    public static void printMatrix(int[][] matrix) {
        for (int[] row : matrix) {
            for (int element : row) {
                System.out.print(element + " ");
            }
            System.out.println();
        }
    }
}
