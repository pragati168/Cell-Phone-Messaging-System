#include<stdio.h>
#include<stdlib.h>
struct node
{
	char data[100];
	struct node *left , *right;
	struct node *temp;
};
struct node *first=NULL;
void insert()
{
	struct node *temp , *p;
	temp=(struct node*)malloc(sizeof(struct node));
	printf("Enter a Message\n");
	getchar();
	gets(temp->data);
	temp->left=NULL;
	temp->right=NULL;
	if(first==NULL)
{
	first=temp;
}
	else
	{
		p=first;
		while(p->right!=NULL)
			p=p->right;
		temp->left=p;
		p->right=temp;
	}
}
int length()
{
	int count=0;
	struct node *temp;
	temp=first;
	while(temp!=NULL)
	{
		count++;
		temp=temp->right;
	}
	return count;
}
void deleteatposition()
{
	struct node *p,*temp,*q;
	int pos,loc,i=1,len;
	len=length();
	printf("Enter the location");
	scanf("%d",&pos);
	if(pos>len)
		printf("Invalid position");
	else
		if(pos==1)
		{
			if(first->right!=NULL)
			{
				temp=first;
				first=temp->right;
				temp->right=NULL;
				first->left=NULL;
				free(temp);
			}
			else
			{
				free(first);
				first=NULL;
			}			
		}
		else if(pos==len)
		{
			p=first;
			temp=first->right;
			while(temp->right!=NULL)
			{
				p=temp;				
				temp=temp->right;
			}
			p->right=NULL;
			temp->left=NULL;
			free(temp);
		}
		else
		{
			q=p=first;
			i=1;
			while(i<(pos-1))
			{
				q=q->right;
			}
			p=q->right;
			temp=p;
			temp=temp->right;
			temp->left=q;
			q->right=temp;
			p->right=NULL;
			q->left=NULL;
			free(p);
		}
}

void display()
{
	struct node *temp;
	if(first==NULL)
		printf("List is Empty\n");
	else
{
		temp=first;
		while(temp!=NULL){
			printf("%s\n",temp->data);
		temp=temp->right;}
	}
	printf("\n");
}
void main()
{
	for(;;)
{
		int choice;
		printf("1.Insert\n2.Delete At Position\n3.Display\n4.Exit\n");
		printf("Enter your choice\n");
		scanf("%d",&choice);
		switch(choice)
		{
			case 1:insert();
				break;		
			case 2:deleteatposition();
				break;
			case 3:display();
				break;
			case 4:exit(0);	
}
}
}
