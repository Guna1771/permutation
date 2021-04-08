# permutation
Finding all possible permutations in which 'n' people can occupy 'r' seats

#include<stdio.h>

int main()
{
	long int n,r,p,temp;
	long int num=1,x=1;
	// Enter the number of seats
	printf(“Enter the number of seats available : “);
	scanf(“%ld”,&r);
	// Enter the number of people
	printf(“nEnter the number of persons : “);
	scanf(“%ld”,&n);

	if(n < r)
	{
		temp=n;
		n=r;
		r=temp;
	}
	long int i;
	for(i=1;i<=num;i++)
		{
			num=num*i;
		}
   
	for(i=1;i<=n-r;i++)
		{
			x=x*i;
		}


	
	p=num/x;
	printf(“nNumber of ways people can be seated : “);
	printf(“%ld”,p);
}

