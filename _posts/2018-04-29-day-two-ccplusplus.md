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

Solutions to the Quadratic equation are given by:

$$x = \frac{\displaystyle\ -b \pm sqrt({b^2 - 4ac})}{2a}$$

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

## Programming Challenge:

Your challenge is to rewrite this program in a way that is more robust and efficient, and is able to take in any value for a, b, and c. The values for a, b, and c, need to be supplied by the user. The goal is to try to break the code written above in as many ways as possible, and then rewrite it in a way where you account for those bugs. Enjoy!


## Solution:
{% highlight markdown %}
  #include <iostream>
  #include <cmath>
  #include <cctype>
  #include <string>
  using namespace std;

  int main() {
  	double root1, root, root2; string a, b, c; double x; int flag = 1;

  	while (flag > 0) {
  		flag = 0;
  		cout << "Enter numeric value for a: "; cin >> a;
  		try {
  			x = std::stod(a);
  		}
  		catch (std::exception& ia) {
  			flag ++;
  		}

  		cout << "Enter numeric value for b: "; cin >> b;
  		try {
  			x = std::stod(b);
  		}
  		catch (std::exception& ia) {
  			flag ++;
  		}
  		cout << "Enter a numeric value for c: "; cin >> c;
  		try {
  			x = std::stod(a);
  		}
  		catch (std::exception& ia) {
  			flag ++;
  		}
  		if (flag > 0) {
  			cout << "One or more numbers entered are not numerics, please reenter values\n\n";
  		}
  	}

  	if (stod(a)==0) {
  		cout << "Anything divided by zero is INFINITY.";
  	}
  	else {
  		root = atof(b.c_str())*atof(b.c_str()) - 4.0 * atof(a.c_str()) * atof(c.c_str());
  		if (root < 0) {
  			cout << "Values result in negative root, so coefficients are INVALID";
  		}
  		else {
  			root = sqrt(root);
  			root1 = 0.5 * (root - atof(b.c_str()) / atof(a.c_str()));
  			root2 = -0.5 * (root + atof(b.c_str())) / atof(a.c_str());
  			cout << "The solutions are " << root1 << " and " << root2 << "\n";
  		}		
  	}

  	system("pause");

  	return(0);
  }
{% endhighlight %}
<br/><br/><br/><br/>
<i>Reference: Book: C++ for Scientists, Engineers and Mathematicians 2nd Edition</i>
