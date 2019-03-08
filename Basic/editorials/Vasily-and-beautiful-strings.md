## Vasily and beautiful strings

### Problem
http://codeforces.com/problemset/problem/336/D 
### Prerequisite
Combinatorics and Number theory
### Explanation

Let’s define  ‘Xstring’ as — random binary string,
 s + g  is defined as— concatenation of strings, MOD = 1000000007.
String 1 + Xstring always transforms into 0 since modification of string is defined as operation :we replace last two characters with exactly one character.This character equals one if it replaces two zeroes otherwise it equals zero because string 1 transforms into 1. String 01 + Xstring always transforms into 1, because string 01 transforms into 0. String 001 + Xstring transforms into 0 because string 001 transforms into 1, and so on. Using these facts let's consider following solution.
Cases like strings without ones or zeroes are easy. For every i (in zero-based numbering) let's assume that it is position of the first occurrence of 1 in our string. Using already known facts we can understand what is the final result of transformations for such string. If the result equals to g, we add C(cnt[0] + cnt[1] - i - 1, cnt[1] - 1) to the answer. Calculation of binomial coefficients is following:    fact[i] = i!%MOD, , C(n, k) = fact[n]inv(fact[n - i]fact[i]), where inv(a) — inverse element modulo MOD. inv(a) = aMOD - 2, because *MOD* is prime number.

### Code
http://codeforces.com/contest/336/submission/27348657
