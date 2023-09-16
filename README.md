# Matrix Multiplication with OpenMP

## Code Explanation

This program performs the following steps:

1. **Command-Line Arguments**: It accepts two command-line arguments - `matrix_size` and `num_threads`. These arguments determine the size of the matrices and the number of threads to use for parallel execution.

2. **Memory Allocation**: Dynamic memory allocation is used to create three matrices `A`, `B`, and `C`. These matrices will hold the input matrices and the result of matrix multiplication.

3. **Initialization**: Matrices `A` and `B` are initialized with the value 2, while matrix `C` is initialized with zeros.

4. **Parallel Matrix Multiplication**: The core matrix multiplication operation is parallelized using OpenMP. The `#pragma omp parallel for` directive splits the work among multiple threads. Each thread calculates a portion of the result matrix `C`.

5. **Timing**: The program measures the elapsed time for the matrix multiplication using the `gettimeofday` function. This provides a measure of the program's performance.

6. **Memory Deallocation**: After the matrix multiplication is complete, memory is deallocated to prevent memory leaks.

## How to Compile and Run

To compile the program, open a terminal and navigate to the directory containing the code. Use the following command:

```bash
gcc -o matrix_multiplication matrix_multiplication.c -fopenmp
```

This command compiles the code with OpenMP support and generates an executable named matrix_multiplication.

To run the program, use the following command:
```bash
./matrix_multiplication <matrix_size> <num_threads>
```

For finding nth power of the matrix:
```bash
./matrix_multiplication <matrix_size> <exponent> <num_threads>
```

Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2
```

For nth power:
Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2 4
```

This will perform matrix multiplication with matrices of size 1000x1000 using 4 threads.

## Output

The program will display the size of the matrices, the number of threads used, and the elapsed time for matrix multiplication.

Graph for the same are as below:

1. **OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/849810a8-2563-400b-8429-ba44da03a6d9)

     ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/9af1046d-1c50-4596-b64f-62bf3d5b641f)

     ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/4024d1c8-33b6-472e-846b-a78b2c6c1c8f)



   
2. **Nth Power of Matrix with OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/00715e16-320a-45cf-9d98-86f9478c85d4)

     ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/1961d922-76cc-45a9-bd1d-bdb8360f4456)

     ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/32fb37f0-cafb-4c4a-b369-cb9cf9fda942)
   

## Conclusion

This C program demonstrates how to use OpenMP to parallelize matrix multiplication, improving the performance of the computation. You can adjust the matrix size and the number of threads to observe the impact on execution time.




# Block Matrix Multiplication

```markdown
# Block Matrix Multiplication

Compile the program using a C compiler. For example:

gcc -o block_matrix_mult block_matrix_mult.c -fopenmp
```

Here, block_matrix_mult is the name of the executable.

To run the program, use the following command-line format:
```bash
./block_matrix_mult <matrix_size> <num_threads> <block_size>
```

For nth power of a matrix using BMM:
```bash
./block_matrix_mult <matrix_size> <exponent> <num_threads> <block_size>
```

<matrix_size>: The size of the square matrices (e.g., 100 for a 100x100 matrix).
<block_size>: The size of the square blocks (e.g., 10 for a 10x10 block).
For example, to multiply two 100x100 matrices using 10x10 blocks:

```bash
./block_matrix_mult 1024 6 4
```

For nth power:
```bash
./block_matrix_mult 1024 2 6 4
```

## Output
The program will display the size of the matrices, the block size, and the result of the multiplication.

1. **BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/fa9d97e7-1a4b-4fc1-b951-aee78d1c9f42)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/32cd9ae0-cb93-4534-b22d-8a9d4eb9d8a1)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/13efd22e-f7f8-48c6-99ef-c2b98fa728d0)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/d72284cf-fc77-4f5b-a30c-595c1812ef24)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/08f59f7c-6fc1-4fe5-93ab-1c3c72bf2cb2)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/ef993aa3-340f-440e-9b9d-b9f3fb34dae6)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/86c7d394-e144-4c7d-8c3f-de727cb690f9)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/8f30055c-f9dc-4b32-8e1a-757f14dd33d8)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/bad4e8ca-d363-4905-9f48-376fba22704b)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/64005011-d04f-4165-8319-91cf1d66f3b9)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/0dde34b3-ec13-4e2b-9269-fa65f005160e)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/d39c0483-5764-4dea-969a-6d596d28e5ae)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/cd67a740-fb3d-49e7-9001-050569986a69)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/98ddcaf1-c381-4a03-a67e-b9f19141cadb)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/34dfaa23-6cd4-4322-a168-2690fc74468c)
   
3. **Nth Power of Matrix with BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/4c067ed1-f485-4c5b-aea5-44c60c960e50)

   ![image](https://github.com/Bhavyareddysadula/hpc_readme/assets/126856102/09d91bf5-cd2e-4a7d-98b1-e2e729f938ba)


## Memory Management
The program dynamically allocates memory for matrices A, B, and C, as well as for the block buffers. It frees the allocated memory after the multiplication is complete to prevent memory leaks.
