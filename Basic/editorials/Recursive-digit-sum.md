## Recursive Digit Sum
### Problem
https://www.hackerrank.com/challenges/recursive-digit-sum
### Prerequisite
Basics of Recursion
### Explanation
This problem basically consists a number n repeated k times. SInce, n is very large, we initially store it as a string. The key to solving this problem involves two functions :
 Computing the sum of digits of n : Since, the number is stored as a string, we can easily access individual digits and add them together. Pretty basic function
The recursive function : This function finds the sum of digits of the number passed and recursively calls itself over the calculated sum. The end case as required by the question occurs when the number becomes less than 10. 
One may note here that the sum of digits of n calculated by the first function is first multiplied by k as that’s what is required to fed in the recursive function. 
### Code
```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int super_digit( long long k ) {
    if ( k < 10 ) {
        return k;
    }
    
    long long sum = 0;
    while( k > 0 ) {
        sum += k % 10;
        k = k / 10;
    }
    return super_digit( sum );
}


long long sum_initial( string number ){
    long long sum = 0;
    
    for( int i = 0; i < number.size(); i++ ) {
        sum += number[i] - '0';
    }
    
    return sum;
}


int main() {
    string  n;
    int k;
    cin >> n >> k;
    long long repeated = sum_initial(n) * k;
    
    long long result = super_digit(repeated);
    
    cout << result << "\n";
    
    return 0;
}
```
