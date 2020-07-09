# Solution 
#Bear and house queries
#coding in c++
#include <bits/stdc++.h>
using namespace std;

int main() {
	// your code goes here
	int x,y,s;
	int l,r;
	l=0;
	r=1000;
	string response;
	int mid;
	while(l<r)
	{
	    
	     mid=ceil((l+r)/2.0);
	    cout<<"?"<<" "<<mid<<" "<<0<<"\n"<<flush;
	    //fflush(stdout);
	    cin>>response;
	    if(response=="YES")
	    {
	        
	        l=mid;
	    }
	    if(response=="NO")
	        r=mid-1;
	}
	x=2*l;
	l=x;
	r=1000;
	while(l<r)
	{
	    
	     mid=ceil((l+r)/2.0);
	    cout<<"? 0"<<" "<<mid<<"\n"<<flush;
	 //   fflush(stdout);
	    cin>>response;
	    if(response=="YES")
	    {
	        
	        l=mid;
	    }
	    if(response=="NO")
	        r=mid-1;
	        
	}
	y=l;
	l=0;
	r=1000;
	while(l<r)
	{
	    
	    mid=ceil((l+r)/2.0);
	    cout<<"? "<<mid<<" "<<x<<"\n"<<flush;
	    
	    cin>>response;
	    if(response=="YES")
	    {
	        
	        l=mid;
	        
	        
	    }
	    if(response=="NO")
	        r=mid-1;
	        
	}
	s=2*l;
	int totalarea=(s*(y-x))/2 + x*x;
	cout<<"!"<<" "<<totalarea<<"\n";
	return 0;
}
