# 19CS301 Module-9
### EX: 9.1 MATRIX OPERATIONS

### Aim:

To Write a Python Program to subtract two matrices by reading the matrix from the user.

### Algorithm:

1. Start the program.
2. Define a function `create_matrix(n, m)` to create an n x m matrix by:
   a. Taking integer input for each element using nested list comprehension.
3. Read two integers `r` and `c` (number of rows and columns) from the user.
4. Call `create_matrix(r, c)` twice to create matrices A and B.
5. Subtract matrix B from matrix A element-wise using nested list comprehension:
   - For each element C[i][j], compute A[i][j] - B[i][j].
6. Print matrices A, B, and the result matrix C.
7. End the program.

### Program:
```python

# Name: Nidhish B
# Reg no: 212223050032

def create_matrix(n, m):
    return [[int(input()) for _ in range(m)] for _ in range(n)]

r, c = map(int, input().split())
A = create_matrix(r, c)
B = create_matrix(r, c)

C = [[A[i][j] - B[i][j] for j in range(c)] for i in range(r)]

print(A)
print(B)
print(C)
```
### Output:

![image](https://github.com/user-attachments/assets/580f0ff1-317a-4e46-af17-80416f82ddc3)

### Result:

Thus,the given program is implemented and executed successfully.

### EX: 9.2 LIST COMPREHENSION

### Aim:

To Write a Python program to generate an Arithmetic Progression using list Comprehension with first number, difference and last number as input.

### Algorithm:

1. Start the program.
2. Read the first term of the AP and store it in the variable `first`.
3. Read the common difference of the AP and store it in the variable `diff`.
4. Read the last term of the AP and store it in the variable `last`.
5. Use a list comprehension to generate the AP:
   - For each `i` from 0 to (last - first) // diff,
   - Compute each term using the formula: first + i * diff.
6. Store the generated list in the variable `ap`.
7. Print the first term, common difference, last term, and the AP list.
8. End the program.

### Program:
```python

# Name: Nidhish B
# Reg no: 212223050032

first = int(input())
diff = int(input())
last = int(input())

ap = [first + i * diff for i in range((last - first) // diff + 1)]

print("First Number", first)
print("Difference", diff)
print("Last Number", last)
print(ap)
```
### Output:

![image](https://github.com/user-attachments/assets/3c843a0b-a28e-4bd3-aae6-3ad9dad1eb0a)

### Result:

Thus, the given program is implemented and executed successfully .

### EX: 9.3 ADVANCED LIST PROCESSING

### Aim:
To Write a Python program to add two matrices using list Comprehension

### Algorithm:

1. Start the program.
2. Read the number of rows and columns and store them in `rows` and `cols`.
3. Create the first matrix `m1` using nested list comprehension:
   - Loop through each row and column,
   - Read input for each element.
4. Similarly, create the second matrix `m2` with the same dimensions.
5. Initialize an empty result matrix `summatrix`.
6. For each element position (i, j):
   - Add m1[i][j] and m2[i][j],
   - Store the result in the corresponding position of `summatrix`.
7. Print the original matrices `m1`, `m2`, and the result matrix `summatrix`.
8. End the program.


### Program:
```python

# Name: Nidhish B
# Reg no: 212223050032

rows,cols=map(int,input().split())

m1=[[int(input()) for _ in range(cols)]for _ in range(rows)]
m2=[[int(input()) for _ in range(cols)] for _ in range(rows)]

summatrix=[[m1[i][j] + m2[i][j] for j in range(cols)]for i in range(rows)]

print(m1)
print(m2)
print(summatrix)

```
### Output:

![image](https://github.com/user-attachments/assets/dd5a571e-bc60-4884-9143-bc0b75764028)

### Result:

Thus,the given program is implemented and executed successfully.
 


### EX: 9.4 TOEPLITZ MATRIX

### Aim: 

To Write a Python Program to check whether the given matrix is Toeplitz Matrix.

### Algorithm:

1. Start the program.
2. Create a matrix using nested loops with user input.
3. Define a function to check if all diagonal elements are equal (Toeplitz condition).
4. Read number of rows and columns.
5. Create the matrix.
6. Check if the matrix is Toeplitz.
7. Print the result and matrix.
8. End.

### Program:

```python
# Name: Nidhish B
# Reg no: 212223050032

def create_matrix(n,m):
    M=[]
    for i in range(n):
        row=[]
        for j in range(m):
            x=int(input())
            row.append(x)
        M.append(row)
    return M 
def print_matrix(M):
    for i in range(len(M)):
        for j in range(len(M[0])):
            print(M[i][j], end=' ')
        print()
def isThoeplitz(M):
    for i in range(len(M)):
        for j in range(len(M[0])):
            if i>0 and j>0 and M[i][j]!=M[i-1][j-1]:
                return False
    return True
r,c=input().split()
A=create_matrix(int(r),int(c))
print('A=',A)
if isThoeplitz(A):
    print(A,'is a Toeplitz Matrix')
else:
    print(A,'is not a Toeplitz Matrix')
print_matrix(A)

```
### Output:

![image](https://github.com/user-attachments/assets/46558fc8-4f94-4311-bfdf-6906b39787b6)


### Result: Thus, the given program is implemented and executed successfully.
 

