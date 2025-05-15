# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
#include <stdio.h>

int main() {
    int M, N;
    
    printf("Enter the value of M: ");
    scanf("%d", &M);
    printf("Enter the value of N: ");
    scanf("%d", &N);
    
    for (int i = M; i <= N; i++) {
        if (i % 2 == 0) {
            printf("%d\n", i);
        }
    }
    
    return 0;
}
## OUTPUT:

![{728BBD43-3CFF-49F4-9CB6-ECD2B710091C}](https://github.com/user-attachments/assets/d5268362-c05d-402a-b33c-d59e86091a76)









## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
#include <stdio.h>

int main() {
    int rows;
    
    printf("Enter the number of rows: ");
    scanf("%d", &rows);
    
    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }
    
    return 0;
}


## OUTPUT:


![{787FF8E8-E92C-4C2F-87DB-82279C30B5F2}](https://github.com/user-attachments/assets/02c5d61c-ff62-4630-8eb7-caf6cece7b07)



## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
#include <stdio.h>

void add(int a, int b) {
    int sum = a + b;
    printf("Sum: %d\n", sum);
}

void subtract(int a, int b) {
    int difference = a - b;
    printf("Difference: %d\n", difference);
}

int main() {
    int num1, num2;
    
    printf("Enter first number: ");
    scanf("%d", &num1);
    printf("Enter second number: ");
    scanf("%d", &num2);
    
    add(num1, num2);
    subtract(num1, num2);
    
    return 0;
}

## OUTPUT:

![{3104F84E-DDF0-4481-9D27-107ABBA4828C}](https://github.com/user-attachments/assets/601dd1f0-74ca-4a1c-b6ad-a8a834c9f32a)





## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
#include <stdio.h>

int main() {
    int number, sum_odd = 0;
    
    printf("Enter a number: ");
    scanf("%d", &number);
    
    // Handle negative numbers by converting to positive
    if (number < 0) {
        number = -number;
    }
    
    for (; number > 0; number /= 10) {
        int digit = number % 10;
        if (digit % 2 != 0) {
            sum_odd += digit;
        }
    }
    
    printf("Sum of odd digits: %d\n", sum_odd);
    
    return 0;
}

## OUTPUT:

![{6C1DAD57-9642-44BF-AF4D-E02BCC1CB5E1}](https://github.com/user-attachments/assets/3ec8651c-2b32-45e5-b943-435975c0bc28)



## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
#include <stdio.h>

void fact() {
    int i, N;
    long long fact = 1; // Using long long to handle larger factorials
    
    printf("Enter a number: ");
    scanf("%d", &N);
    
    // Handle negative input
    if (N < 0) {
        printf("Factorial is not defined for negative numbers.\n");
        return;
    }
    
    for (i = 1; i <= N; i++) {
        fact *= i;
    }
    
    printf("Factorial of %d is: %lld\n", N, fact);
}

int main() {
    fact();
    return 0;
}

## OUTPUT:
![{4F91AC24-54B3-46A0-B8A2-35D9CF70F7AF}](https://github.com/user-attachments/assets/5a507c04-0f79-4007-baad-2d13f9bee18e)

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
