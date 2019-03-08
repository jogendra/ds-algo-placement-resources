## Shaas and lights

### Problem
http://codeforces.com/problemset/problem/294/C
### Prerequisite
Combinatorics and Number theory
### Explanation
 Lets try to solve the third sample to get a better idea of problem
                         1 2 3 4 5 6 789 10 11
Third sample is ***#***#*** here ‘*’ implies light is off and ‘#’ implies light is on . Now let’s denote contiguous interval of off lights as A,B,C here A denotes light from 1 to 3, B denotes light from 5 to 7 ,C denotes lights from 9 to 11. As it can easily observed that there are 9!/(3!3!3!)=1680 permutations of String AAABBBCCC ,it gives us idea about how to combine steps of different types .Turning on of light is done uniquely for types 1 and 3 ,since it is a condition of problem that one could on switch if and only if one of its neighbour is switched on.But for type 2 each time we have two possible options until we are left with one off light. So number of ways for type 2 is 2^(3-1).So total number ways is 1680*1*(2^(3-1))*1=6720

In general we have to get all contiguous segments of off lights then divide them into group then calculate total permutation after which we calculate number of ways for all segments individually which would be 2^(k-1) if k is number of elements in segment.

Implementation needs some standard Combinatorial computation which can be seen just by going through my code :)
### Code
http://codeforces.com/contest/294/submission/27271076 
