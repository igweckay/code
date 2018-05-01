---
layout: post
title: "day three with C/C++"
author: "kay"
---

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
