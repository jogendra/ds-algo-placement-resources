## Thor

- ### Problem
	http://codeforces.com/problemset/problem/704/A
- ### Prerequisite
	STL- Map,Queue
- ### Explanation
	Consider a queue e for every application and also a queue Q for the notification bar. When an event of the first type happens, increase the number of unread notifications by 1 and push pair (i, x) to Q where i is the index of this event among events of the first type, and also push number i to queue e[x].
When a second type event happens, mark all numbers in queue e[x] as visited,clear this queue and decrease the number of unread notifications by the number of elements in this queue before clearing.
When a third type query happens, do the following-
  ```
  while Q is not empty and Q.front().first<=t:
	i = Q.front().first
	x= Q.front().second
	Q.pop()
         if mark[i] is false:
		Mark[i] = true	
	e[v].pop()
	ans = ans - 1
  ```
- ### Code
  http://codeforces.com/contest/704/submission/27111975
