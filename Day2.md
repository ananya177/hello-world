# Question Day 2
#Solution Codechef DSA series
#Euron Problem
#Coding C++
#include <iostream>
using namespace std;
#define l1 long long
l1 result=0;
void mergecomb(l1 arr[],l1 s,l1 mid,l1 e)
{
    l1 n1=mid-s+1;
    l1 n2=e-mid;
    l1 left[n1],right[n2];
    
    for(int i=0;i<n1;i++)
        left[i]=arr[s+i];
    for(int i=0;i<n2;i++)
        right[i]=arr[mid+1+i];
    l1 p=0,q=0,r=s;
    while(p<n1&&q<n2)
    {
        if(left[p]<=right[q])
        {
            arr[r++]=left[p];
            p++;
        }
        else
        {
            arr[r++]=right[q];
            result=result+n1-p;
            q++;
            
            
        }
        
    }
    while(p<n1)
    {
        arr[r++]=left[p++];
    }
    while(q<n2)
    {
        arr[r++]=right[q++];
    }
}
void mergesorting(l1 arr[],l1 s,l1 e)
{
    if(s<e)
    {
        l1 mid=(s+e)/2;
        mergesorting(arr,s,mid);
        mergesorting(arr,mid+1,e);
        mergecomb(arr,s,mid,e);
    }
}
int main() {
	// your code goes here
	l1 n;
	cin>>n;
	l1 arr[n];
	for(int i=0;i<n;i++)
	    cin>>arr[i];
	/*int count=0;
	
	for(int i=0;i<n;i++)
	{
	    if(arr[i]<arr[i+1])
	        count++;
	          
	}
	if(count==1)
	    cout<<(sizeof(arr)/sizeof(arr[0])) * 2<<"\n";
	else
	    cout<<count<<"\n";
	return 0;*/
	
	//Doing with the help of merge sorting
	mergesorting(arr,0,n-1);
	cout<<result;
}
#Thank you
