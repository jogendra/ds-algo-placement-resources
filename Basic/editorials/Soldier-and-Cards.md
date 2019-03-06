## Soldier and Cards
Codeforces - 546C

### Problem
http://codeforces.com/problemset/problem/546/C

### Prerequisite - Vector, Map

### Explanation
Firstly let's count a number of different states that we can have in the game. Cards can be arranged in any one of n! ways. In every of this combination, we must separate first soldier's cards from the second one's. We can separate it in n + 1 places .
So war has (n + 1)! states. If we'd do (n + 1)! "fights" and we have not finished the game yes, then we'll be sure that there is a state, that we passed at least twice. That means that we have a cycle, and game won't end. Otherwise , the game would end simply with one soldier having empty set.
Since , n is very small one can use the above brute force method , so the time complexity will be O(n*(n+1)!). The other n is used by map to check the repetition of the states. 
One can use vectors to represent states of the soldiers. In every fight do as said in the problem and store the states . Also keep the count of no. of fights. If any of the state gets repeated , then the game would end in an infinite loop, hence print -1 and end the game. If at any instant either of the vectors is empty , the other soldier wins .
To keep count of the states, one can use stl::map of a pair of vectors , where the first vector would represent the set of cards of soldier 1 and the second vector for soldier 2. One can map the pair of vector with bool values which represent whether that state is already visited or not.

### Source Code
http://codeforces.com/contest/546/submission/27116094
