## DATE: 28-03-2026

## AIM:
To write a C program that demonstrates the use of `typedef` to create a new alias name for a data type.

## Algorithm
1. **Start** the program.
2. **Use** the `typedef` keyword to define an alias for an existing data type (e.g., `typedef unsigned int unit;`).
3. **Declare** variables using the new alias name instead of the original data type.
4. **Assign** values to these variables.
5. **Print** the values to verify that the alias works identically to the original type.
6. **Stop** the program.

## Program:
```c
#include <stdio.h>

typedef unsigned int unit;
typedef float decimal;

int main() {
    unit quantity = 50;
    decimal price = 125.50;
    printf("Quantity: %u\n", quantity);
    printf("Price: %.2f\n", price);
    return 0;
}
```

## Output:
```text
Quantity: 50
Price: 125.50
```

## Result:
Thus the program was executed and the output was verified successfully.

---
Would you like me to show you how `typedef` is commonly used with **structures** to simplify variable declarations?
