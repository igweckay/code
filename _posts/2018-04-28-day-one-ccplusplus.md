---
layout: post
title:  "day one with C/C++"
author: "Kay Igwe"
---

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

<h2>Program Challenge:</h2>
Write a C program that would take in a name from the user and decide whether it was a palindrome.

User Input: halalah<br/>
Output: IS a palindrome

User Input: marquester<br/>
Output: NOT a palindrome

Solution:
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
