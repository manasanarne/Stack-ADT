# Stack-ADT
#include<stdio.h>
#include<stdlib.h>
#define MAX 50
int a[MAX],top=-1;
void push(int x)
{
    if(top==MAX-1)
    {
        printf("Stack overflown");
    }
    else
    {
        a[++top]=x;
    }
}
int pop()
{
    if(top==-1)
    return -1;
    else
    {
        int x;
        x=a[top];
        top--;
        return x;
    }
}
int peek()
{
    return a[top];
}
int display()
{
    int i;
    if(top==-1)
    {
        printf("No element is found");
    }
    else
    {
        for(i=top;i>=0;i--)
        {
            printf("\n%d",a[i]);
        }
    }
}
void main()
{
    int x,ch;
    while(1)
    {
        printf("\n1.push\n2.pop\n3.peek\n4.display\n");
        printf("Enter your choice");
        scanf("%d",&ch);
        switch(ch)
        {
            case 1:printf("Enter element to insert");
                scanf("%d",&x);
                push(x);
                break;
            case 2:x=pop();
                   if(x==-1)
                   {
                       printf("Stack underflow");
                   }
                   else
                   {
                       printf("Element deleted=%d",x);
                   }
                   break;
            case 3:x=peek();
                   printf("The element on top of stack=%d",x);
                   break;
            case 4:printf("The elements in stack are:");
                   display();
                   break;
            case 5:exit(0);
        }
    }
}

OUTPUT:-
1.push
2.pop
3.peek
4.display
5.exit
Enter choice:1
Enter an element to insert:3
1.push
2.pop
3.peek
4.display
5.exit 
Enter choice:1
Enter an element to insert:6
1.push
2.pop
3.peek
4.display
5.exit
Enter choice:1
Enter an element to insert:5
1.push
2.pop
3.peek
4.display
5.exit
Enter choice:4
5
6
3
3
1.push
2.pop
3.peek
4.display
5.exit
Enter choice:2
Element deleted=5
1.push
2.pop
3.peek
4.display
5.exit
Enter choice:4
6
3
3
1.push
2.pop
3.peek
4.display
5.exit
Enter choice:3
The element on the top of the stack is 6
1.push
2.pop
3.peek
4.display
5.exit
Enter choice:5

