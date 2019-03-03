## How to move from C to C++
*   Header Files
    *   In C,  you generally use the header files 
        *   stdio.h
        *   string.h
        *   math.h
    *   In C++, you generally use the header files
        *   iostream
        *   cmath
        *   cstring
        *   Other STL libraries
    *   In C++, unlike C, you don't need to include a bunch of header files. Instead you can include only one header file which will include most of the required header files
        *   bits/stdc++.h

        **Caution**: Using bits/stdc++.h may slow down compilation.

*   Input Output functions
    *   In C, the basic input output functions are scanf, printf, gets, puts.
    *   In C++, you use cin, cout.
    *   For a new line, in C we use '\n' in printf statement while we can use **endl **in cout statement in c++. **Caution**: endl slows down output, so better use '\n'.
    *   To input a line i.e. to input a string with spaces we use gets in c while getline in C++.
    *   All the functions like cin, cout etc. are defined in a standard namespace. So, instead of directly using it we usually add a namespace to avoid writing std everytime. You do not need to understand much about namespace. Just remember to add a statement
        *    **`using namespace std;`** At the top in all C++ codes.


See the table for better understanding.
     


<table>
  <tr>
   <td>
C
   </td>
   <td>Cpp
   </td>
   <td>Explanation
   </td>
  </tr>
  <tr>
   <td>#include<stdio.h>,
<p>
#include<math.h>....
   </td>
   <td>#include
<p>
<bits/stdc++.h>
   </td>
   <td>You need to include only one header file
   </td>
  </tr>
  <tr>
   <td>No namespace statement
   </td>
   <td>using namespace std;
   </td>
   <td>Namespace std is used in cpp
   </td>
  </tr>
  <tr>
   <td>int a;
<p>
scanf("%d",&a);
<p>
printf("%d,a);
   </td>
   <td>int a;
<p>
cin>>a;
<p>
cout<<a;
   </td>
   <td>Use of cin, cout in place of scanf and printf
   </td>
  </tr>
  <tr>
   <td>int a;float b;char c;
<p>
scanf("%d%f%c",
<p>
&a,&b,&c);
<p>
printf("%d%f%c",
<p>
a,b,c);
   </td>
   <td>int a;float b;char c;
<p>
cin>>a>>b>>c;
<p>
cout<<a<<b<<c;
   </td>
   <td>Multiple input output at the same time
   </td>
  </tr>
  <tr>
   <td>printf("%d\n",a);
   </td>
   <td>cout<<a<<endl;
   </td>
   <td>To print some variable a followed by a newline character
   </td>
  </tr>
  <tr>
   <td>char a[100];
<p>
scanf("%s",a);
   </td>
   <td>char a[100];
<p>
cin>>a;
   </td>
   <td>To input a string
   </td>
  </tr>
  <tr>
   <td>char a[100];
<p>
gets(a);
   </td>
   <td>stri ng a;
<p>
getline(cin,a);
   </td>
   <td>To input a line 
<p>
Note - If you make a character array, you will have to use gets in cpp as well.
   </td>
  </tr>
</table>


See the codes for better understanding.



![comparing the codes](https://user-images.githubusercontent.com/20956124/53696666-7de2bb80-3def-11e9-865c-64df901b719b.png)


Do note the use of two gets in cpp code (line 11) and '\n' in scanf statement in C code (line 10). This is because when use press enter after taking a, b, c as input '\n' gets stored in d. So, we need to input d again. In C code, we already take \n as input in scanf statement. So we don't need to use gets. If we do not use \n in scanf, then we will have to use two gets. This might be a little bit confusing but you shall understand it as you practice.

Another very important thing that need to be mentioned is the fact that cin cout are very slow as compared to scanf printf. Therefore, you should never synchronize C++ streams to standard C streams. 

**ios_base::sync_with_stdio(false);**

**cin.tie(0);**

**cout.tie(0);**

This makes cin, cout work comparatively faster. It is advised to add this statement at the top of your main function in all your codes. Although this is still slower as compared to scanf, printf. Therefore, some times you will be forced to use scanf, printf in place of cin, cout when input or output is quite large. Infact, at some occasions even scanf won't help. So you will have to use fast I/O. You can read about them [here](https://www.geeksforgeeks.org/fast-io-for-competitive-programming/). Although in most problems unsynchronized cin cout will work fine.
