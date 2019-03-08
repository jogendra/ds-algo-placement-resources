## Ceil and Flowers

### Problem
http://codeforces.com/contest/322/problem/B
### Prerequisite
Basic programming
### Explanation
If we don’t take mixed bouquet then our answer is r/3+g/3+b/3.
It is easy to notice that if we take 3 mixed bouquet then  we can change it to (1 red bouquet + 1 green bouquet + 1 blue bouquet) .So we have to check only cases of 0,1,2 mixed bouquets.
So answer is `max( r/3+g/3+b/3 ,1+(r-1)/3+(g-1)/3+(b-1)/3 , 2+(r-2)/3+(g-2)/3+(b-2)/3 )`.
### Code
http://codeforces.com/contest/322/submission/27268441
