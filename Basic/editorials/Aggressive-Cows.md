## Aggressive Cows

### Link
http://www.spoj.com/problems/AGGRCOW/

### Prerequisite
binary search  

### Explanation
For the problem at hand, let us define a boolean function check(x) which returns  true  if it is possible to arrange the cows in stalls such that the distance between any two cows is at least x otherwise it returns false

Now it is easy to see that if check(x) = false , check (y)=false  for all y>x. Thus, the problem satisfies the monotonicity condition necessary for binary search. 

If we sort all the positions then, Our  maximal possible answer is last position-first position (when there are only two cows)  and  Our minimal possible answer is zero when we have to put more than two cows at one  stall.
So we will check at mid of our maximum and minimum values and if it comes true then reduce our search space to the upper half else to the lower half.

Now, how do we define check (x) for a general value of x? We can do this with a greedy algorithm: Keep placing cows at the leftmost possible stalls such that they are at least x , if we  able to place all the cows then return true else return false.

### Author’s  Code
https://ideone.com/kncccB
