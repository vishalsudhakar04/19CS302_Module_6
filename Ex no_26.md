## DATE: 28-03-2026

## AIM:
To write a C program to demonstrate a self-referential structure where an employee has a pointer to their manager (another structure of the same type).

## Algorithm
1. **Start** the program.
2. **Define** a self-referential structure `Employee` containing:
    * `name` (string)
    * `id` (int)
    * `struct Employee *manager` (a pointer to the same structure type).
3. **Declare** two structure variables, e.g., `emp1` (Employee) and `mngr1` (Manager).
4. **Input** details for both the manager and the employee.
5. **Link** the employee to the manager by assigning the address of the manager to the employee's pointer member (`emp1.manager = &mngr1`).
6. **Display** the employee's details along with their manager's name by accessing it through the pointer.
7. **Stop** the program.

## Program:
```c
#include <stdio.h>

struct Employee {
    char name[30];
    int id;
    struct Employee *manager;
};

int main() {
    struct Employee mngr1, emp1;
    printf("Enter Manager Name and ID: ");
    scanf("%s %d", mngr1.name, &mngr1.id);
    mngr1.manager = NULL;
    printf("Enter Employee Name and ID: ");
    scanf("%s %d", emp1.name, &emp1.id);
    emp1.manager = &mngr1;
    printf("\nEmployee Details:\n");
    printf("Name: %s, ID: %d\n", emp1.name, emp1.id);
    if (emp1.manager != NULL) {
        printf("Reports to Manager: %s (ID: %d)\n", emp1.manager->name, emp1.manager->id);
    }
    return 0;
}
```

## Output:
```text
Enter Manager Name and ID: Sarah 501
Enter Employee Name and ID: James 1001

Employee Details:
Name: James, ID: 1001
Reports to Manager: Sarah (ID: 501)
```

## Result:
Thus the program was executed and the output was verified successfully.

---
Would you like me to show you how to use this self-referential concept to create a **Linked List** of employees?
