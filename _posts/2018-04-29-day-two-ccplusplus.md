---
layout: post
title:  "day two with C/C++"
author: "Kay Igwe"
---

Now for C++

Every C program usually begins with the following programming block.

{% highlight markdown %}
#include <iostream>
using namespace std;

int main()
{
  cout << "Hello World!\n";
  return(0);
}
{% endhighlight %}

The header file <iostream> enables the use of functions such as cout and cin. cout allows us to output content onton the console, while cin allows us to take in user input. The results of the above program is as follows...

{% highlight markdown %}
 Hello World!

{% endhighlight %}

where the '\n' character means to go to a new line, as it does in C.
THe following program computes the quadratic function, where, a, b, and, c are values taken from the user.

{% highlight markdown %}
// Solve the quadratic equation:
// a*x^2 + b*x + c = 0

#include <iostream>
#include <cmath>  //for the sqrt() function
using namespace std;

int main(){

  double root1, root2, a, b, c, root;

  cout << "Enter the coefficients, a, b, c";
  cin >> a >> b >> c;
  root = sqrt(B*B - 4.0 * a * C);
  root1 = 0.5 * (root - b) / a;
  root2 = - 0.5 * (root + b) / a;
  cout << "The solutions are " << root1 << " and " << root2 << "/n";

return(0);
}

{% endhighlight %}

The above program will run, however it is not robust and can crash if given an inappropriate value such as a letter, or a space. Also, the program is not written to handle division by zero.

Programming Challenge:

Your challenge is to rewrite this program in a way that is more robust and efficient, and is able to take in any value for a, b, and c. The values for a, b, and c, need to be supplied by the user. The goal is to try to break the code written above in as many ways as possible, and then rewrite it in a way where you account for those bugs. Enjoy!
