---
layout: post
title: "day one"
author: "kay"
permalink: /ccplusplus/
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

<h2>Programming Challenge:</h2>
Write a C program that would take in a name from the user and decide whether it was a palindrome.

User Input: halalah<br/>
Output: IS a palindrome

User Input: marquester<br/>
Output: NOT a palindrome


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
