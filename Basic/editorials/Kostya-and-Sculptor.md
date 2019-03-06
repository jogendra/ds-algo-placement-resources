## Kostya and Sculptor

### Problem
http://codeforces.com/contest/733/problem/D
### Prerequisite
STL- Map, Iterators
### Explanation
It is clear that radius of sphere with rectangle of sides (a,b,c) will be min(a,b,c)/2 and if two parallelepipeds exist with two same side (a,b) then after glueing these two together , radius  will be min(a,b,c1+c2)/2.
For  every pair (a,b) let us find maximal adjacent sides c1 and c2 ,then we will check for which pair(a,b)  min(a,b,c1+c2)  is maximum.
We can make a map of pair to (vector of pair) . In which for every distinct pair (a,b) we store what is the third side and corresponding index.
Then we iterate through the map and find maximal c1 and c2 for every pair (a,b).
Then we find for which pair min(a,b,c1+c2) is maximum and output the corresponding answer.

**NOTE:** Do not  forget when there is only one maximal side for pair (a,b).
### Code
http://codeforces.com/contest/733/submission/27111913
