# nested-structure
#include <stdio.h>

struct department {
    int dept_id;
    char dept_name[50];
};

struct company {
    int emp_id;
    char emp_name[50];
    struct department d;   // nested structure
};

int main() {
    struct company c;

    printf("25331A05E8\n");

    printf("Enter Employee ID: ");
    scanf("%d", &c.emp_id);

    printf("Enter Employee Name: ");
    scanf("%s", c.emp_name);

    printf("Enter Department ID: ");
    scanf("%d", &c.d.dept_id);

    printf("Enter Department Name: ");
    scanf("%s", c.d.dept_name);

    printf("\n--- Company Details ---\n");
    printf("Employee ID: %d\n", c.emp_id);
    printf("Employee Name: %s\n", c.emp_name);
    printf("Department ID: %d\n", c.d.dept_id);
    printf("Department Name: %s\n", c.d.dept_name);

    return 0;
}
