# Multidimensional Array 

In Java, a multidimensional array is an array of arrays, where each element of the outer array is an array itself. The number of dimensions in a multidimensional array is called its rank. A two-dimensional array, for example, has a rank of 2 and is essentially a matrix with rows and columns.

Here's an example of how to create and use a two-dimensional array in Java:

```
int[][] matrix = new int[3][3];

matrix[0][0] = 1;
matrix[0][1] = 2;
matrix[0][2] = 3;

matrix[1][0] = 4;
matrix[1][1] = 5;
matrix[1][2] = 6;

matrix[2][0] = 7;
matrix[2][1] = 8;
matrix[2][2] = 9;

for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        System.out.print(matrix[i][j] + " ");
    }
    System.out.println();
}
```

In this example, we create a 3x3 two-dimensional array called matrix and initialize its values. We then use nested for loops to iterate over each element of the array and print its value to the console.

The output of this program is:

```
1 2 3
4 5 6
7 8 9
```

In Java, you can create multidimensional arrays of any rank (i.e., any number of dimensions) and any size. To access elements of a multidimensional array, you use multiple index values, one for each dimension. For example, matrix[1][2] would access the element in the second row and third column of the matrix.