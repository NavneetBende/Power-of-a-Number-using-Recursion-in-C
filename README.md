# Power-of-a-Number-using-Recursion-in-C

Power of Number using Recursion in C
Given two integer numbers the objective of the program is to write a code to find the Power of Number using Recursion in C Language.

For instance,

Input : a = 2 , b = 3
Output : 2^3 or 8
Power of Number using Recursion in C
 

The objective of the Code is to Recursively multiply the Number a with itself until the Power variable b is exhausted. We set the base case which checks whether the Power is exhausted or not as b==0, if true return 1. The Recursive step call with keep decrementing the power variable i.e b with each recursive call. That whole recursion will return the number multiplied to itself for Power times.

Let’s try and understand it better using the working of the recursion with an example. Let the Number a be 2 and the Power b be 3. The objective is to perform 2*2*2 recursively. In order to do so we’ll return 2*powRec(Number,Power-1). The Last iteration depicted in the Adjacent image, has b==0. Therefore it’ll return 1. Then 1*2 is returned by second recursive call. 2*2 is returned by first recursive call and finally 2*2*2 is returned as the output.

Power of a Number Using Recursion in C
While loop in C
C Code
Run

#include <stdio.h>
#include <math.h>

int powRec(int a,int b)
{
  if(b==0)
    return 1;
  return a*powRec(a,b-1);
}
int main()
{
  int a = 2,b=3;
  printf("The number %d to the power %d is %d",a,b,powRec(a,b));
}
Output
The number 2 to the power 3 is 8
Explanation 

The objective of the above code is to Recursively call the function and with each recursion multiply the number with itself until the power variable is 0. We set a base case as when the power variable it 0, we terminate the recursion and return 1. With every recursive step call we decrement power variable. The final value is 

The algorithm for the above code is as follows,

Include all the required libraries using include keyword.
define a function powRec() which accepts two integers a and  and returns the value of a raised to the power b.
Set base case as b==0, if true return 1 ending the termination and decrement b with every recursive call in recursive step call.
return the value of a*powRec(a,b-1).
In the int main() function initialize all the required variables and call the powRec() function.
Print the returned value using printf() function.
The output for the above code is The number 2 raised to the power 3 is 8.

