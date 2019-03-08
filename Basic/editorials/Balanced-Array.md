## Balanced Array

### Problem
https://www.codechef.com/problems/COOK82B
### Prerequisite
Sieve of eratosthenes, Modular exponentiation
### Explanation
Observation 1-Since we divide a number by some positive integer k and then multiply a different number by k, then we see that the sum powers of k in all the numbers must remain same.
For example in sample test case 25,15,5,27- sum of frequency of 5 is 2(25=5*5)+1(15=3*5)+1(5)+0(27=3*3*3)=2+1+1+0=4
Similarly for 3 we have 0+1+0+3=4.
When we perform some operation, then we see that this sum for 3 and 5 remains constant.
Observation 2- To make all the numbers equal we must divide the frequency of all k’s equally.
For example in sample test case 25,15,5,27, we finally get 15,15,15,15 . We see that frequency of 3 and 5 are equally distributed finally.
So first we analyze the condition where we don’t need to add another number. In this case the sum of powers of each prime factor should be divisible by N so that we can divide the powers equally.
What is the minimum number to be added to the array?
Again we need to divide sum of powers of all prime factors equally among all numbers. But in this case the number of elements are N+1. So if the sum of powers of a prime factor is s, then the required no of powers is (N+1)-(s%(N+1)) i.e.( the multiple of (N+1) greater than or equal to N+1 ) - s. 
For implementation details, see the code.

### Code
https://www.codechef.com/viewsolution/13766135 
