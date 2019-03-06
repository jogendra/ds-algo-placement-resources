## T-shirt Buying

### Link
http://codeforces.com/problemset/problem/799/B

### Prerequisite
Set / Priority_queue

### Explanation
let the colour of T-shirt  which buyer wants be x. So our task is                     to find the T-shirt having that colour on any of back or front side and remove it from our available collection of T-shirts.

Here as our collection of data from which we want to select minimum is dynammic(i.e it is updating after removing each T-shirt) ,so we will use priority_queue that have both update and query(for minimum) in O(log(n)) time complexity;

We can use priority_queue of pair<prize_of_t-shirt , index_of_T-shirt> , as by default the ordering is on the basis of first element and we can use index of T-shirt to remove it from collection.

### Author’sCode
http://codeforces.com/contest/799/submission/27110773
