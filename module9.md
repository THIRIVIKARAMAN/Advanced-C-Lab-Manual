EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

//type your code here
```
#include <stdio.h>
#define SIZE 5

int stack[SIZE];
int top = -1;

void display() {
    if (top == -1) {
        printf("Stack is empty.\n");
        return;
    }
    printf("Stack elements are: ");
    for (int i = top; i >= 0; i--) {
        printf("%d ", stack[i]);
    }
    printf("\n");
}

int main() {
    stack[++top] = 10;
    stack[++top] = 20;
    stack[++top] = 30;
    display();
    return 0;
}
```
Output:

//paste your output here
![image](https://github.com/user-attachments/assets/8136ee92-8edd-487b-9aa2-0d9886e7ad5a)



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

//type your code here
```
#include <stdio.h>
#define SIZE 5

float stack[SIZE];
int top = -1;

void push(float value) {
    if (top == SIZE - 1) {
        printf("Stack Overflow.\n");
    } else {
        stack[++top] = value;
        printf("%.2f pushed into the stack.\n", value);
    }
}

int main() {
    push(1.1);
    push(2.2);
    push(3.3);
    return 0;
}
```

Output:

//paste your output here
![image](https://github.com/user-attachments/assets/b46893e0-9bd6-41fd-80e9-bd03c91051d6)




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

//type your code here
```
#include <stdio.h>
#define SIZE 5

int queue[SIZE];
int front = -1, rear = -1;

void display() {
    if (front == -1 || front > rear) {
        printf("Queue is empty.\n");
        return;
    }
    printf("Queue elements are: ");
    for (int i = front; i <= rear; i++) {
        printf("%d ", queue[i]);
    }
    printf("\n");
}

int main() {
    front = 0;
    rear = 2;
    queue[0] = 11;
    queue[1] = 22;
    queue[2] = 33;
    display();
    return 0;
}
```

Output:

//paste your output here
![image](https://github.com/user-attachments/assets/c017e513-caee-4fe2-a486-c2d25118e0b0)



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

//type your code here
```
#include <stdio.h>
#define SIZE 5

float queue[SIZE];
int front = -1, rear = -1;

void enqueue(float value) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow.\n");
    } else {
        if (front == -1) front = 0;
        queue[++rear] = value;
        printf("%.2f inserted into the queue.\n", value);
    }
}

int main() {
    enqueue(10.5);
    enqueue(20.75);
    enqueue(30.25);
    return 0;
}
```

Output:

//paste your output here
![image](https://github.com/user-attachments/assets/80a39dd6-910a-4ee0-a13f-6029a24cf2ae)


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

//type your code here
```
#include <stdio.h>
#define SIZE 5

int queue[SIZE];
int front = -1, rear = -1;

void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue is empty.\n");
    } else {
        printf("Deleted element: %d\n", queue[front++]);
        if (front > rear) {
            front = rear = -1;
        }
    }
}

int main() {
    front = 0;
    rear = 2;
    queue[0] = 100;
    queue[1] = 200;
    queue[2] = 300;
    
    dequeue();
    dequeue();
    dequeue();
    dequeue();  // Test underflow
    return 0;
}
```

Output:

//paste your output here
![image](https://github.com/user-attachments/assets/ea77624e-4294-40be-af25-bde2f1390b00)


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
