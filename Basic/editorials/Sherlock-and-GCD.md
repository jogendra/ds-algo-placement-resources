## Sherlock and GCD

### Problem
https://www.hackerrank.com/challenges/sherlock-and-gcd
### Prerequisite
Greatest common divisor
### Explanation
This question can be reduced to a simpler one: Check if there is a non-empty subset such that the Greatest Common Divisor (GCD) of the whole subset is 1. 
Note that if you have a and b such that GCD(a,b) is 1, then GCD(a,b,x,y,z,...)  will always be 1. 
Based on the above approach, it's always better to include more and more numbers since it will always reduce or keep the GCD the same. So, if the whole array has GCD 1, then print YES, else print NO.
### Code
```
#include <bits/stdc++.h>

using namespace std;

int hcf(int n1, int n2)
{
    if (n2 != 0)
       return hcf(n2, n1%n2);
    else 
       return n1;
}

int main()
{
    int t,n,x;
    cin >> t;
    while ( t-- ) {
        cin >> n;
        int val;
        for ( int i = 0; i < n; i++ ) {
            cin >> x;
            if ( i == 0 ) val = x;
            else val = hcf(val,x);
        }
        if ( val == 1 ) cout << "YES" << endl;
        else cout << "NO" << endl;
    }
    return 0;
}
```
