## Sherlock and his girlfriend

### Problem
http://codeforces.com/contest/776/problem/B

### Prerequisite
Prime numbers (Sieve of Eratosthenes) 
### Explanation
We are required to color the jewelry pieces such that for every jewelry piece i having a price i + 1, all the pieces whose prices are prime divisors of i + 1 should have colors different from that of the ith piece. This can be achieved by simply coloring all the pieces with their prices as primes in one color, and all the other pieces in a second color. We calculate the Sieve of Eratosthenes upto the range of n( ≤ 10^5) and thus, obtain the list of primes as well as non-primes.
### Code
http://codeforces.com/contest/776/submission/24934550
