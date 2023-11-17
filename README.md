# Prime_between.c

#include<stdio.h>

int isprime(int n)
{
if(n<=1)
return 0;

for(int i=2;i*i<=n;i++)
{
if(n%i==0)
{
return 0;
}
}
return  1;
}

void main()
{
int n;
printf("Enter a number : ");
scanf("%d",&n);

int c=0;
for(int i=1;i<=n;i++)
{
if(n%i==0)
{
c++;
}
}
if(c==2)
{
printf("Number is prime\n ");
}
else
{
printf("Number is not Prime\n");
}

int start;
printf("Enter first number : ");
scanf("%d",&start);

int end;
printf("Enter second number : ");
scanf("%d",&end);

for(int i=start;i<=end;i++)
{
if(isprime(i))
printf("%d , ",i);

}

}
