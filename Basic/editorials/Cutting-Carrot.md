## Cutting Carrot

### Link
http://codeforces.com/problemset/problem/794/B

### Prerequisite
Basic properties of triangle

### Explanation
The total area of triangle is ½*(base*hight)=h/2.
So after deviding it in n parts of equal area ,area of each part=h/(2*n)

Now let the first cut be at height x from apex thus by using similiarity of triangle the base of small triangle(b) will be
		`x/b=h/1`  {since base of bigger triangle is 1}
	So,       `b=x/h`
	Thus ,  `area =h/(2*n)`
		,  `½*(x/h)(x) =h/(2*n)`
	`=>       x=h*sqrt(1/n)`
Generally,
For k’th  cut , we can say that area of triangle from apex to that cut will be equal to sum of k pieces which is equal to k times of individual area,

 So,
    `½*(x/h)(x) =k*h/(2*n)`
 	  `=>    x=h*sqrt(k/n)`

### Author’s Code
http://codeforces.com/contest/794/submission/27111751
