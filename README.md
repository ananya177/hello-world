# solution DSA series Codechef
#Lowest Sum
#coding in c++
#include<bits/stdc++.h>
using namespace std;
#define l1  long long 

int main() {
	// your code goes here
	int t;
	cin>>t;
	while(t--)
	{
	   int n,k;
	   cin>>n>>k;
	   l1 A[n];
	   l1 B[n];
	   for(int i=0;i<n;i++)
	        cin>>A[i];
	   for(int i=0;i<n;i++)
	        cin>>B[i];
	   
	  sort(A,A+n);
	  sort(B,B+n);
	  vector<l1> sum;
	  for(int i=0;i<n && i<500;i++)
	  {
	       for(int j=0;j<n && j<500;j++)
	       {
	            sum.push_back(A[i]+B[j]);
	       }
	  }
	  
	  sort(sum.begin(),sum.end());
	  while(k--)
	  {
	        int q;
	        cin>>q;
	        cout<<sum[q-1]<<"\n";
	  }
	   
	    
	}
	return 0;
}
