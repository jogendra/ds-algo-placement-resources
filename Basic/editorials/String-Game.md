## String Game

### Link
http://codeforces.com/contest/779/problem/D

### Prerequisite
binary search  

### Explanation
For the problem at hand, let us define a boolean  function
check(x) which returns  true  if it is possible to remove at least x character from the string  otherwise it returns false

Now it is easy to see that if check(x) = false , check (y)=false  for all y>x. Thus, the problem satisfies the monotonicity condition necessary for binary search. 
Our  maximal possible answer is size of string t  (when string p is empty ,we can remove all letters of  t)  and  Our minimal possible answer is zero( when string p==string t and we can’t remove any element)
  
 So we will check at mid of our maximum and minimum values and if it comes true then reduce our search space to the upper half else to the lower half.

Now, how do we define check (x) for a general value of x? We can do this with following step:-
   - Make a copy of t (so that original string remains intact for further operation)
   - Remove x element (i.e make them 0 or * or # etc.)
   - Now check if we can get string p from string t or not ,  if yes return true otherwise return false 
		
### Author’s  Code
https://ideone.com/t9sH0g
