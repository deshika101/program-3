# program-3
There are N frustrated coders standing in a circle with a gun in their hands. Each coder
has a skill value S[ i ] and he can only kill those coders that have strictly less skill than
him. One more thing, all the guns have only 1 bullet. This roulette can take place in
any random order. Fortunately, you have the time stone (haaan wo harre wala) and
you can see all possible outcomes of this scenario. Find the outcome where the total
sum of the remaining coder's skill is minimum. Print this sum.



#include<bits/stdc++.h>

using namespace std;

main()

{

ios_base::sync_with_stdio(false);

cin.tie(NULL);

int n;

cin>>n;

int a[n];

int sum=0;

for(int i=0; i<n; i++)
{
	cin>>a[i];
}
sort(a,a+n);

for(int i=1; i<n; i++)

{
  for(int j=i-1; j>=0; j--)
  
  {
  	if(a[i]>a[j]&&a[j]!=0)
	
	{

		a[j]=0;
		
		break;
}

}

}

sum=0;

for(int i=0; i<n; i++)

{

	sum+=a[i];
	
}

cout<<sum;

}
