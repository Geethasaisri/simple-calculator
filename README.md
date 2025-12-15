# simple-calculator
#simple calculator performs basic arithmetic (add, subtract, multiply, divide) on two numbers, featuring a numerical keypad, operator buttons (+, -, *, /), an equals (=) button, and a display screen to show inputs and results, designed for everyday tasks like budgeting or quick math without complex functions
// C Program to make a Simple Calculator using 
// switch-case statements
#include <stdio.h>
#include <float.h>

int main() {
    char op;
    double a, b, res;

    // Read the operator
    printf("Enter an operator (+, -, *, /): ");
    scanf("%c", &op);

    // Read the two numbers
    printf("Enter two operands: ");
    scanf("%lf %lf", &a, &b);
    
    // Define all four operations in the corresponding
    // switch-case
    switch (op) {
    case '+':
        res = a + b;
        break;
    case '-':
        res = a - b;
        break;
    case '*':
         res = a * b;
        break;
    case '/':
        res = a / b;
        break;
    default:
        printf("Error! Incorrect Operator Value\n");
        res = -DBL_MAX;
    }
    if(res!=-DBL_MAX)
      printf("%.2lf", res);
    
    return 0;
}
