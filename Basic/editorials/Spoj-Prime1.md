## Spoj-Prime1

### Link
http://www.spoj.com/problems/PRIME1/

### Prerequisite
knowledge of prime numbers 

### Explanation
As n and m are quite large thus we can’t check each and every value to be prime or not ,so we need something fast.
<br>
**Sieve of eratosthenes** -  consider you start to find all the prime numbers from 2 thus as you get 2  to you can say {4,6,8,10…} can’t be prime because they all are multiple of two so we cut them and then we go to the next uncut element and cut all of it’s multiple and so on ,at last all the uncut numbers are prime.
<br>
**Time complexity** - as upper loop that you will run to iterate all over 
range to get primes will be of n and to cut multiples of a prime let say k u have to run a loop of n/k. Thus total iterations will be 1 for non prime and n/k for prime k.
	So 
  ```
  time complexity = O( n/2 + n/3 + 1 + n/5 + 1 + n/7 + 1 + 1 + 1 + n/11…….)
			         ~ O( n*(½ + ⅓ + ⅕…….)
			         = O(n(log(logn)))
  ```
**Segmented sieve** - we can apply sieve in any segment of n to m if we have all the prime numbers upto sqrt(m) .as we can cut all the numbers from n to m by primes from 2 to sqrt(m) ans if any of the no have no factor up to it’s square root i.e it is uncut ,means it is prime.

So, first store all the prime from 2 to 100000 and then apply segmented sieve from n to m and print all the primes from n to m

### Author’s  Code
https://ideone.com/Ytz875

