EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```c
#include <stdio.h>
#include <stdlib.h>
struct node{int data;struct node*next;};int main(){int n,x,key,i;struct node*h=0,*t=0,*p;scanf("%d",&n);for(i=0;i<n;i++){scanf("%d",&x);p=malloc(sizeof(*p));p->data=x;p->next=0;if(!h)h=p;else t->next=p;t=p;}scanf("%d",&key);for(p=h;p;p=p->next)if(p->data==key){printf("Element found");return 0;}printf("Element not found");return 0;}
```

Output:

![Experiment 16 output](outputs/exp16.svg)



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

```c
#include <stdio.h>
#include <stdlib.h>
struct node{int data;struct node*next;};int main(){int n,x,i;struct node*h=0,*t=0,*p;scanf("%d",&n);for(i=0;i<n;i++){scanf("%d",&x);p=malloc(sizeof(*p));p->data=x;p->next=0;if(!h)h=p;else t->next=p;t=p;}scanf("%d",&x);p=malloc(sizeof(*p));p->data=x;p->next=0;if(!h)h=p;else t->next=p;printf("List: ");for(p=h;p;p=p->next)printf("%d ",p->data);return 0;}
```

Output:

![Experiment 17 output](outputs/exp17.svg)

 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```c
#include <stdio.h>
struct node{int data;struct node*prev,*next;};int main(){struct node a={10,0,0},b={20,&a,0},c={30,&b,0};a.next=&b;b.next=&c;struct node*p=&a;printf("Doubly Linked List: ");while(p){printf("%d ",p->data);p=p->next;}return 0;}
```

Output:

![Experiment 18 output](outputs/exp18.svg)


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

```c
#include <stdio.h>
#include <stdlib.h>
struct node{int data;struct node*prev,*next;};int main(){int n,x,i;struct node*h=0,*t=0,*p;scanf("%d",&n);for(i=0;i<n;i++){scanf("%d",&x);p=malloc(sizeof(*p));p->data=x;p->prev=t;p->next=0;if(t)t->next=p;else h=p;t=p;}scanf("%d",&x);p=malloc(sizeof(*p));p->data=x;p->prev=t;p->next=0;if(t)t->next=p;else h=p;printf("List: ");for(p=h;p;p=p->next)printf("%d ",p->data);return 0;}
```

Output:

![Experiment 19 output](outputs/exp19.svg)


Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

```c
#include <stdio.h>
#include <stdlib.h>
struct node{int data;struct node*next;};int main(){int n,x,key,i;struct node*h=0,*t=0,*p,*q;scanf("%d",&n);for(i=0;i<n;i++){scanf("%d",&x);p=malloc(sizeof(*p));p->data=x;p->next=0;if(!h)h=p;else t->next=p;t=p;}scanf("%d",&key);p=h;q=0;while(p&&p->data!=key){q=p;p=p->next;}if(p){if(q)q->next=p->next;else h=p->next;free(p);}printf("List: ");for(p=h;p;p=p->next)printf("%d ",p->data);return 0;}
```

Output:

![Experiment 20 output](outputs/exp20.svg)





Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





