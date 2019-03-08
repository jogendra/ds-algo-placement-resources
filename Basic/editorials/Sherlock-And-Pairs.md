## Sherlock And Pairs

### Link
https://www.hackerrank.com/challenges/sherlock-and-pairs

### Prerequisite
Basics of Combinatorics

### Explanation
We have to count pairs (i,j) such that A[i]=A[j]. Suppose a number x, appears k times in the whole array say, at index p1,p2,...pk. Then we can pick any two indexes pi and pj which will be counted as 1 pair. Similarily, pj and pi can also be pair. So, choose(k,2)*2 is the number of pairs such that A[i]=A[j]=x.
We keep a hash of the values of A[i] (since all values are less than 10^6), and for each x=0 to 10^6, we add to answer the required value.

### Author’s  Code
```
#include<bits/stdc++.h>
using namespace std;
long long arr[1000009]={};
int main()
{
    int t;
    cin>>t;
    while(t--)
    {
        memset(arr,0,sizeof(arr));
        long long n,i,j,ans=0,x;
        cin>>n;
        for(i=0; i<n; i++)
        {
            cin>>x;
            arr[x]++;
        }
        for(i=1; i<=1000000; i++)
            ans+=(arr[i]*(arr[i]-1));
        cout << ans << endl;
    }
    return 0;
}
```
