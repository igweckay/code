---
layout: post
title: "day five"
author: "kay"
permalink: /ccplusplus/
---

<!---Latex Equations  http://latex.codecogs.com/eqneditor/editor.php --->

Today will be a continuation of day four with Pointers.

## Programming Challenge

Use nested, comma-seprated lists to initialize the array, a[2][3][4], so that ot corresponds to:

![first matrix](http://latex.codecogs.com/gif.latex?%5CLARGE%20%7B%5Ccolor%7BBlue%7D%20a_0ij%20%3D%20%5Cleft%20%28%20%5Cbegin%7Bmatrix%7D%201%20%26%202%20%26%203%20%26%204%5C%5C%205%20%26%206%20%26%207%20%26%208%5C%5C%209%20%26%2010%20%26%2011%20%26%2012%20%5Cend%7Bmatrix%7D%20%5Cright%20%29%7D)

![second matrix](http://latex.codecogs.com/gif.latex?%5CLARGE%20%7B%5Ccolor%7BBlue%7D%20a_1ij%20%3D%20%5Cleft%20%28%20%5Cbegin%7Bmatrix%7D%2013%20%26%2014%20%26%2015%20%26%2016%5C%5C%2017%20%26%2018%20%26%2019%20%26%2020%5C%5C%2021%20%26%2022%20%26%2023%20%26%2024%20%5Cend%7Bmatrix%7D%20%5Cright%20%29%7D)

Using only pointer arithmetic and the array name (that is a, but not a[0][0][0] or a[i][j][k]), list the array elements and hence verify your method of access.
<br/><br/>
Link to book pages: [Section 6.5.1](https://github.com/igweckay/code/blob/gh-pages/ccplusplus_files/pointers-arrays.pdf)
<br/><br/>
<i>Problem from C++ for Scientists, Engineers, and Mathematicians</i>

-------------------------------------------

<h1>day four</h1>

## Pointers

Here are four videos from mycodeschool on Youtube that eloquently describe how to use pointers and why they are important. They also give a great tutorial on working with pointers. All videos are below ...

## Video Series
[Pointers Video Series](https://www.youtube.com/watch?v=h-HBipu_1P0&list=PL2_aWCzGMAwLZp6LMUKI3cc7pgGsasm2_)<br/><br/>
I think the first 4 videos are really good, but feel free to go through as many of them as you would like.


## Programming Challenge

The results of an experiment are stored in a five-dimensional array:

{% highlight markdown %}
    float data[SIZE_1][SIZE_2][SIZE_3][SIZE_4][SIZE_5];
{% endhighlight %}

One requirement is to find the average of all elements. Write two programs to calculate this average; one version should use the standard array notation, whereas the other should use a pointer. Compare the times taken by the two programs for various values of SIZE_1, ..., SIZE_5. Can you make the pointer version any faster?

------------------------------------------------

<h1>day three</h1>

More C++

In C++ there are several ways to display text to a screen. One of them, we have used before, the 'cout' command. The one we will use today is the 'printf' command. Both printf and cout can preform the same function, one may just require less typing depending on the task. For example
---output formatting---
{% highlight markdown %}
  1. cout << hello     world 18!;
  2. cout << hello\tworld 18!;
{% endhighlight %}

prints output

{% highlight markdown %}
  1. hello     world 18!
  2. hello     world 18!
{% endhighlight %}

All of the spaces are not ignored. However, if we use the printf command and use the '\t', we get the same results as above.

{% highlight markdown %}
  printf("hello \t world 18!")
{% endhighlight %}

Below is a full program example.

{% highlight markdown %}
  # include <iostream>
  using namespace std;

  int main(){
    char name[] = "Maria";
    printf("\nhello\t %s, how are you?\n", name);
    cout<<"\nhello\t<< name<< ", how are you?";
  return(0);
  }
{% endhighlight %}

{% highlight markdown %}
  hello     Maria, how are you?
  hello     Maria, how are you?
{% endhighlight %}

## Programming Challenge:

Conversion of a Fahrenheit Temperature to Celsius<br/>
When dealing with temperatures, one common problem is the conversion of a temperature in Fahrenheit degrees into Celsius degrees. The formula is

$$x = \frac{\displaystyle\ 5( F - 32 )}{9}$$

Write a program that converts a constant Fahrenheit temperature into the correspondingCelsius temperature. Prompt the user to enter a Fahrenheit temperature. Then, calculate the Celsius equivalent and display the results using the format shown below. You should produce precisely these results; observe the formatting. Make three test runs of the program entering the indicated Fahrenheit temperatures.
{% highlight markdown %}
  100.0 F =  37.8 C
  32.0 F =    0.0 C
  212.0 F = 100.0 C
{% endhighlight %}

Make sure the formatting is the same as the one above. You can use either 'cout' or 'printf' for this exercise.
It should not look like the one below, (which is unformatted)...
{% highlight markdown %}
  100.0F = 37.8 C
  32.0F = 0.0C
  212.0 F = 100.0 C
{% endhighlight %}

<br/><br/><br/><br/>
<i>Reference: C++ for Computer Scientists and Engineers</i>

---------------------------------------------
<h1> day two </h1>
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

--------------------------------------------------------------
<h1>day one</h1>

Let's Start with C.

Every C program usually begins with the following programming block.

{% highlight markdown %}
#include <stdio.h>

int main()
{
  printf("\nHello World!")
  return 0;
}
{% endhighlight %}


Libraries enable you to be able to use certain functions that are provided by the program. The stdio.h library allows the use of input and output functions. Whenever you se a library, the '#include ' line has to be included, and the library name itself should be wrapped in < >, as seen above. All the code is wrapped in a main function, with a return of '0', that executes when the program is compiled.

printf, allows you to print something, or display something to the screen upon execution. Anything wrapped in quotation marks is considered a string except for formatting expressions as seen below. The '/n' expression means to add a new line before the string is displayed.  

{% highlight markdown %}
  printf("\nHello World!")
{% endhighlight %}

The output of these lines of code is as follows...

{% highlight markdown %}
  1.
  2. Hello World!
{% endhighlight %}

The numbers just symbolize the blank spaces.

Variables are very useful and are used to store information. Whenever you use a variable, you must initialize the variable by giving it a datatype. You can also initialize the variable by giving it a value, but this is not necessary.
{% highlight markdown %}
#include <stdio.h>

int main()
{
  string expression;
  expression = "Hello World!";

  return 0;
}
{% endhighlight %}
In the code snippet above, we initialize the variable 'expression' as a string, and then assign the string "Hello World", to it. This means that upon execution, nothing will show up on the screen, but the Hello World string, will still be assigned to expression. In order to have this show up on the screen, you would have to add the following piece of code to the program.
{% highlight markdown %}
  printf(expression)
{% endhighlight %}

To capture user input into a variable we use the function scanf as seen below.
{% highlight markdown %}
#include <stdio.h>

int main()
{
  string expression="Nothing Entered";
  printf("/nPlease write an expression: /t");
  scanf("%s", &expression);
  print("%s", expression)

  return 0;
}
{% endhighlight %}

The variable expression is initialized as a string and with the string "Nothing Entered", although, if nothing is entered by the user, the nothing will be printed. The ampersand, "&" allows the user's inputs to be saved into "expression". Try it out for yourself...

Here is a good video from iTzAdam5X on youtube that further explains how to accept user input.

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/z8evnLrYm9I?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></center>

<h2>Programming Challenge:</h2>
Write a C program that would take in a name from the user and decide whether it was a palindrome.

User Input: halalah<br/>
Output: IS a palindrome

User Input: marquester<br/>
Output: NOT a palindrome

## Solution:
{% highlight markdown %}
#include<stdio.h>
int main ()
{
  char name[]; int length, check, size = len(name), i =0, flag=0;

  printf("Please enter your name\n"); scanf("%s",&name);

  while (flag == 0 || (i>int(size/2)){
    if(name[i] != name[size-1]){
      flag++;
      printf("%s is not a Palindrome", name)
    }
    i++; size--;
  }
  if flag == 0{
    printf("%s is a Palindrome", name);
  }
return 0;
}
{% endhighlight %}


------------------------------------------------------------

<h1>100 Days of Code with C/C++</h1>

Welcome to the first day of 100 days of code. It is going to be a fun and exciting journey through programming with C and C++. Each day you will be given a tutorial and a program to code. You must complete coding the program and post it in the slack channel. Solutions will be posted both in the slack channel and on this blog the day after it is assigned.

Feel free to ask any question you would like. You can ping me on Slack and I can answer you there or we can do a Hangout or Slack meeting. Also feel free to post questions in the 'general' channel if you would like to ask questions to the group. That way any one could answer your questions as well.

The Book [C++ for Computer Science and Engineering](https://7chan.org/pr/src/TheBook.pdf)

## <u>Outline</u>
- Sign up with Slack
- The Blog
- Sign up for a Github Account
- Receiving Daily Projects
- Useful Videos
- Where to ask questions

## Slack
Sign Up for a slack account via the following link: [100daysofCodetk](https://100daysofcodetk.slack.com/messages/C9YT8D34N/) 👍🏼

I will be placing the projects in the ‘projects’ channel daily.

## Blog
I will also be posting the projects, daily, on this blog.

## Github
Github is a great online repository to save all of your work. Create an account via this link: [Join Github](https://github.com/join?source=header-home)
If you have a github account, great! You are almost ready to begin! Follow this link on how to commit your first document to your repo.

## Receiving Daily projects
As written before, all projects will be posted on both the blog and on Slack.

## Useful Videos
Here is a nice introduction into C programming from Geeky Shares, on youtube.
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/ot9LoXNSqLU?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></center>
<br/><br/>
Here is a nice introduction into C++ programming from Buckys C++ Programming Tutorials on youtube.
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/tvC1WCdV1XU?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></center>

## Where to ask question
You can ask all of your questions in the Slack channel.
