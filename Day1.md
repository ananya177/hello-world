# Question Day 1
#Coding in C++
#problem from COdechef
#Stack
#Solution
#include <iostream>
using namespace std;
#include<vector>

int main() {

	
	int t;
	cin>>t;
	while(t--)
	{
	    int n;
	    cin>>n;
	    vector<int> A;
	    for(int i=0;i<n;i++)
	    {
	        int tp;
	        cin>>tp;
	        auto itr=lower_bound(A.begin(),A.end(),tp+1);
	        if(itr==A.end())
	            A.push_back(tp);
	        else
	           *itr=tp;
	       
	        
	    }
	    cout<<A.size()<<" ";
	    for(auto i:A)
	        cout<<i<<" ";
        cout<<"\n";
	        
	}
	
	return 0;
}
