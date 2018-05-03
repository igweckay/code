---
layout: post
title:  "day one with python"
author: "kay"
---

Today we will learn about variable assignment, user input, and printing to the console.

There are many data types in python. Some of the datatypes include...
1. int (signed integer type)
2. strings (string type)
3. boolean (True/ False)
4. float (floating point type)
5. time (date/ time type)
6. enum (enumerated type)

We will focus on the first 2 types today. A string is a sequence of characters, which can include numbers, letters, or characters, such as '. and ,'. Below the name 'Sonia' is being assigned to the variable x.

{% highlight python %}

  x = "Sonia"
  x = 'Sonia'

{% endhighlight %}

Both print out the same results. For string assignment, you can use either type of quotations; the single quotes, or the double quotes. The The one time you may decide to use one over the other is if you actually want to print out the quotes as in the example below.

{% highlight python linenos %}
  print("'Sonia'")
{% endhighlight %}
<b>output:</b>
{% highlight python linenos %}
  'Sonia'
{% endhighlight %}

An integer is a Real number, a non-decimal number. For example, -3, 5, and 1432 are all integers. When you do integer division, numbers are automatically floored. This means that the decimal part of the number becomes "irrelevant" and is taken out of the equation. An example follows...

{% highlight python linenos %}
  int(x = 7); int(y=3)
  x/y = 2
  y/x = 0
{% endhighlight %}

The only way to access the remainder of these numbers is to use the '%' operator.

{% highlight python linenos %}
  x%y = 1
  y%x = 7
{% endhighlight %}

A boolean is a data type that returns true or false, 1 or 0 respectively, depending on the statement that is even. For example

{% highlight python linenos %}
   x = 10 # assigning integer value 10 to x, does not produce output
   y = 5 # assigning integer value 5 to y, does not produce output
   x == y
   x != y
   x > y
   x < y
{% endhighlight %}

The above code returns the following...

{% highlight python linenos %}
   False
   True
   True
   False
{% endhighlight %}

We will create a simple game called, "Guess that number", that takes in a integer value from the user and lets them know if they guessed the number correctly.

First, I will show you how to capture user input. In python 3, you can use the command 'input', and assign the user's response to a variable as shown below...

{% highlight python linenos %}
  response = input('Guess a number between 1 and 10: ')
{% endhighlight %}

The following will be outputted to the console...
{% highlight python linenos %}
  Guess a number between 1 and 10:
{% endhighlight %}

Let's open a jupyter notebook.
The video below walks you through opening the notebook and

<iframe width="560" height="315" src="https://www.youtube.com/embed/M1KPSJ3WWog?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

{% highlight python linenos %}
  guess = int(7)
  response = int(input('Guess a number: '))
  if (response == guess):
      print("Great guess! The number was 7")
  else:
      print("Wrong guess, the number was 7")
{% endhighlight %}

## Programming Challenge

Ask the user for their name, store it in a variable and print out...
Hello [the user's name]
Then, ask them for their age, and favorite color, and display the answers to the screen.
</br>

Hello, [insert name]! Nice to meet you. Your age is [age], and your favorite color is [insert color].
Is this information correct?

{extra} If the information is correct, tell the user 'Bye', otherwise, ask for the user's information again.
