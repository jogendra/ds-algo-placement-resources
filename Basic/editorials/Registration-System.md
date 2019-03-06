## Registration System

- ### Problem
	http://codeforces.com/problemset/problem/4/C
- ### Prerequisite
	STL- Map
- ### Explanation
	We can clearly see than n ≤ 10^5, that is a naive approach of O(n^2) will not pass. We need a better solution. 
  Here using STL map will make our task easy.
  We can make a map of string and int where string will contain the name of person while int will contain the count. 
  We know that by default map are initialized with zero.
  So if the count of a string is zero print OK and increase its counter by 1 else print the string and the count of string and increase its counter by 1.
- ### Code
  http://codeforces.com/contest/4/submission/27110469
