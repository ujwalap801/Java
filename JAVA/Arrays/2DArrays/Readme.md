# 2D Arrays in Java

A 2D array (Two-Dimensional array) is a data structure in Java that stores data in a table-like format with rows and columns. It's essentially an array of arrays, where each inner array represents a row in the table.

## Example

```java
int[][] my2DArray = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

System.out.println(my2DArray[0][1]); // Output: 2


# Key Points about 2D Arrays in Java

- **Declaration**: `type[][] arrayName = new type[rowCount][columnCount];`
- **Initialization**: `type[][] arrayName = {{row1}, {row2}, ...};`
- **Accessing elements**: `arrayName[rowIndex][columnIndex]`
- **Length**: `arrayName.length` (number of rows), `arrayName[0].length` (number of columns)

2D arrays in Java are useful for representing matrices, tables, game boards, and other structured data where information is organized in rows and columns.
