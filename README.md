# permutation
Finding all possible permutations in which 'n' people can occupy 'r' seats
#include<stdio.h>
int fact(long int x)
{
	long int f=1,i;
	for(i=1;i<=x;i++)
		{
			f=f*i;
		}
	return f;
}

int main()
{
	long int n,r,p,temp;
	long int num,x;
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
	num=fact(n);
	x=fact(n-r);
	p=num/x;
	printf(“nNumber of ways people can be seated : “);
	printf(“%ld”,p);
}

