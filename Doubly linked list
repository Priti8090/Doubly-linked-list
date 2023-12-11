#include <stdio.h>
#include<stdlib.h>
struct node{
    int data;
    struct node *next;
    struct node *prev;
};
struct node *first=0,*last=0,*newnode=0;
void creat(struct node *p)
{
    if(first==0)
    first=last=p;
    else
    {
        last->next=p;
        p->prev=last;
        last=p;
    }

}
void delet_at_first()
{
	  struct node *p;
    p=first;
      if(first==0)
    printf("no element exist for deletion !!");
    else if(first==last)
     {
    	last=first=0;
    	free(p);
	}
    else
    {
    p=p->next;
    free(first);
    p->prev=0;
    first=p;
    }
}
void delet_at_last()
{
	 struct node *p;
    p=last;
    if(first==0)
    printf("no element exist for deletion !!");
    else if(first==last)
    {
    	last=first=0;
    	free(p);
	}
	else
	{
    p=p->prev;
    free(last);
    p->next=0;
    last=p;
    
   }
}
void delet_at_info()
{
	 struct node *p;
    p=first;
    int m;
    printf("Enter data which is to be deleted : ");
    scanf("%d",&m);
     if(first==0)
    printf("no element exist for deletion !!");
    else if(first==last)
    {
        first=last=0;
        free(p);
        return 0;
    }
    else if(first->data==m)
      delet_at_first();
      else if(last->data==m)
      delet_at_last();
	else
	{
	while(p!=0 && p->data!=m)
	p=p->next;
	if(p==0)
	printf("data is not found in the list !!");
	else
	{
		p->prev->next=p->next;
		p->next->prev=p->prev;
		free(p);
	}
  }
}
void travers_forword()
{
    struct node *p;
    p=first;
    while(p!=0)
    {
        printf(" %d->",p->data);
        p=p->next;
    }
}
void travers_backword()
{
    struct node *p;
    p=last;
    while(p!=0)
    {
        printf(" %d->",p->data);
        p=p->prev;
    }
}
void insert_at_first()
{
    struct node *p,*t;
    p=(struct node *)malloc(sizeof(struct node));
    printf("Enter data for insert:");
    scanf("%d",&p->data);
    p->prev=0;
    if(first==0)
    {
    first=last=p;
    p->next=0;
    }
    else
    {
    p->next=first;
    first->prev=p;
    first=p;
    }
}
void insert_at_last()
{
    struct node *p;
      p=(struct node *)malloc(sizeof(struct node));
    printf("Enter data for insert:");
    scanf("%d",&p->data);
    p->next=0;
     if(first==0)
    {
    first=last=p;
    p->prev=0;
    }
    else
    {
        last->next=p;
        p->prev=last;
        last=p;
    }
}
void insert_at_info()
{
    struct node *p,*t;
    t=first;
    int m;
    printf("Enter data after which data to be insert:");
    scanf("%d",&m);
   
    while(t!=0 && t->data!=m)
    {
        t=t->next;
    }
   if(t==0)
    printf("Data after which data to be insert is not found in the list !!");
    else
    {
        printf("Enter data to insert:-");
         p=(struct node *)malloc(sizeof(struct node));
          scanf("%d",&p->data);
          p->next= t->next;
          p->prev=t;
          t->next=p;
          if(p->next!=0)
          p->next->prev=p;
          else
          last=p;
    }
}
void max()
{
	struct node *t;
	t=first;
	int p;
	p=first->data;
     while(t!=0)
     {
     	if(p<t->data)
     	p=t->data;
     	t=t->next;
	 }
	 printf("Max data = %d",p);
}
void search()
{
 	struct node *t;
	t=first;
	int p,k=1;
	printf("Enter data to be seach :");
	scanf("%d",&p);
	if(first==0)
	printf("There are no any list to search !!");
	else
	{
		while(t!=0 && t->data!=p)
		{    k++;
			t=t->next;
		}
		printf("Searching is successfully done .\n\n");
		if(t==0)
		printf("Data is not found in the list !!");
		else
		printf("Data is found at _%d th_position.",k);
		  }  	
}
void min()
{
		struct node *t;
	t=first;
	int p;
	p=first->data;
     while(t!=0)
     {
     	if(p>t->data)
     	p=t->data;
     	t=t->next;
	 }
	 printf("Min data = %d",p);
}
void manu()
{
    
    printf("\n\n   ***************************************************************************\n");
    printf("   *****************WELCOME TO DOUBLY LINKED LIST WORLD **********************\n");
    printf("   ***************************************************************************\n\n");
    printf("    Enter 1 for creat a node:\n");
    printf("    Enter 2 for traverse forword:\n");
    printf("    Enter 3 for traverse backword:\n");
    printf("    Enter 4 for delete at first:\n");
    printf("    Enter 5 for delete at last:\n");
    printf("    Enter 6 for delete at given info:\n");
    printf("    Enter 7 for insert at last:\n ");
    printf("   Enter 8 for insert at first:\n");
    printf("    Enter 9 for insert data at between:\n");
    printf("    Enter 10 for find max term:\n");
    printf("    Enter 11 for find min term:\n");
    printf("    Enter 12 for search any data:\n");
    printf("    Enter 13 for Exit:\n");
    printf("                                                     **** MADE BY PRITI ****\n");
    
}
int main()
{ 
  int a;
  while(1)
  { 
  manu();
  scanf("%d",&a);
  switch(a)
  {
  case 1:{
  	 printf("Enter data in the list:");
    while(1)
    {
    newnode=(struct node*)malloc(sizeof(struct node));
    scanf("%d",&newnode->data);
    newnode->next=0;
    newnode->prev=0;
      if(newnode->data==0)
    break;
    creat(newnode);
  
    }
  }
	break;
	case 2: travers_forword();
		break;
  case 3:travers_backword();
  	break;
   case 4:delet_at_first();
   break;
   case 5:delet_at_last();
   break;
   case 6:delet_at_info();
   break;
   case 7:insert_at_last();
   break;
    case 8:insert_at_first();
   break;
   case 9:insert_at_info();
   break;
   case 10:max();
   break;
    case 11:min();
   break;
   case 12:search();
   break;
   case 13: return 0;
   
   }
 }
}
