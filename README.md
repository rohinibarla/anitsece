### Programming concepts to crack interviews

#### Pre-workshop 

Read fundamentals of computing (computer, assembler, compiler) [here](https://github.com/rohinibarla/anitsece/raw/master/ref/FOC_cac.pdf).  

Click on examples to check the visualization of the code.

[Simple swap example](http://www.pythontutor.com/c.html#code=%23include%20%3Cstdio.h%3E%0A%0Avoid%20swap%28int%20a,%20int%20b%29%20%7B%0A%20%20%20%20int%20temp%3B%0A%20%20%20%20temp%20%3D%20a%3B%0A%20%20%20%20a%20%3D%20b%3B%0A%20%20%20%20b%20%3D%20temp%3B%0A%7D%0A%0Aint%20main%28%29%20%7B%0A%0A%20%20%20%20int%20a%20%3D%205,%20b%20%3D%2010%3B%0A%20%20%20%20printf%28%22a%20%3D%20%25d,%20b%20%3D%20%25d%5Cn%22,%20a,%20b%29%3B%0A%0A%20%20%20%20swap%28a,%20b%29%3B%0A%20%20%20%20printf%28%22a%20%3D%20%25d,%20b%20%3D%20%25d%5Cn%22,%20a,%20b%29%3B%0A%0A%20%20%20%20swap%28a%2B2,%20b%2B5%29%3B%0A%0A%20%20%20%20return%200%3B%0A%7D&curInstr=17&mode=display&origin=opt-frontend.js&py=c&rawInputLstJSON=%5B%5D)

```c
#include <stdio.h>

void swap(int a, int b) {
	int temp;
	temp = a;
	a = b;
	b = temp;
}

int main() {

	int a = 5, b = 10;
	printf("a = %d, b = %d\n", a, b);

	swap(a, b);
	printf("a = %d, b = %d\n", a, b);

	swap(a+2, b+5);

	return 0;
}
```

[Linked List example](http://www.pythontutor.com/c.html#code=%23include%20%3Cstdio.h%3E%0A%23include%20%3Cstdlib.h%3E%0A%0Atypedef%20struct%20node%20%7B%0A%20%20%20%20int%20value%3B%0A%20%20%20%20struct%20node%20*next%3B%0A%7D%20LinkedListNode%3B%0A%0A%0ALinkedListNode%20*createLinkedListNode%28int%20data%29%20%7B%0A%20%20%20%20LinkedListNode%20*node%20%3D%20%28LinkedListNode%20*%29malloc%28sizeof%28LinkedListNode%29%29%3B%0A%20%20%20%20node-%3Enext%20%3D%20NULL%3B%0A%20%20%20%20node-%3Evalue%20%3D%20data%3B%0A%20%20%20%20return%20node%3B%0A%7D%0A%0A%0ALinkedListNode%20*createLL%28%29%20%7B%0A%20%20%20%20LinkedListNode%20*a%20%3D%20createLinkedListNode%285%29%3B%0A%20%20%20%20LinkedListNode%20*b%20%3D%20createLinkedListNode%281%29%3B%0A%20%20%20%20LinkedListNode%20*c%20%3D%20createLinkedListNode%289%29%3B%0A%0A%20%20%20%20a-%3Enext%20%3D%20b%3B%0A%20%20%20%20b-%3Enext%20%3D%20c%3B%0A%0A%20%20%20%20return%20a%3B%0A%7D%0A%0Aint%20main%28%29%20%7B%0A%20%20%20%20LinkedListNode%20*head%3B%0A%20%20%20%20head%20%3D%20createLL%28%29%3B%0A%20%20%20%20return%200%3B%0A%7D&curInstr=0&mode=display&origin=opt-frontend.js&py=c&rawInputLstJSON=%5B%5D)

Read about [Linked List DS](https://github.com/rohinibarla/anitsece/blob/master/ref/LLDS.pdf)

```c
#include <stdio.h>
#include <stdlib.h>

typedef struct node {
  int value;
  struct node *next;
} LinkedListNode;


LinkedListNode *createLinkedListNode(int data) {
  LinkedListNode *node = (LinkedListNode *)malloc(sizeof(LinkedListNode));
  node->next = NULL;
  node->value = data;
  return node;
}


LinkedListNode *createLL() {
  LinkedListNode *a = createLinkedListNode(5);
  LinkedListNode *b = createLinkedListNode(1);
  LinkedListNode *c = createLinkedListNode(9);

  a->next = b;
  b->next = c;

  return a;
}

int main() {
  LinkedListNode *head;
  head = createLL();
  return 0;
}
```


#### Workshop

Pointers, Recursive functions, Memory, LL Data Structure.

C program execution model  

Functions
+ Abstraction
+ Implementation
+ Execution


activities
+ function declarations
+ function executions
+ linked list creation
+ swap
+ array updates


#### Post-workshop
