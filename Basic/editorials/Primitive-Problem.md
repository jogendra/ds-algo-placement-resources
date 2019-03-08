## Primitive Problem

### Link
https://www.hackerrank.com/contests/infinitum17/challenges/primitive-problem

### Prerequisite
Euler's totient function 

### Explanation
I hope you have gone through the link for [primitive roots](https://www.hackerrank.com/external_redirect?to=http://math.stackexchange.com/questions/124408/finding-a-primitive-root-of-a-prime-number).
Actually ,Euler's totient function of x tells us about the total number of co-prime numbers of x in the range of [1,x)
For example phi(4) = 2 {as 1,3 are co-prime numbers to 4 in [1,4) }
Thus as for prime all the numbers before it , is co-prime to it thus 
phi(prime) =prime-1
Generally , if any number is factorized as:-
x= {p1^q1 }*{ p2^q2} *{p3…...where p1 ,p2 ...are prime numbers and q1 , q2… are their corrosponding exponents then ,
phi(x)= {(p1-1)*(p1^(q1-1)) } *{(p2-1)*(p2^(q2-1)) } *{(p3-1)*(p3^(q3-1)) }....

For smallest primitive root do as the link says , and second number is phi(n-1).

### Author’s  Code
https://pastebin.com/qLMpMPNW
