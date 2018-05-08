---
layout: post
title: "day four"
author: "kay"
permalink: /python/
---

## Programming Challenge

Programming Hangman.

This will be a continuation of the challenge from day three. Now that you have been able to randomly choose a word from the document vocab_words.txt and parse through the word, you will now start asking for user input. Ask the user for a letter and if it matches one of the letters in the word, print out the letter at its position, if not, print out that they have guessed wrongly, and show them how many guesses they have remaining.

Example run ...
{% highlight %}
Let's Play Hangman! It is a 3 letter word
_ _ _  
What is your first guess:  a
That is incorrect, you now have 5 more chances. What is your next guess: h
There is 1 'h'
_ h _
Next guess: e
Correct.
_ h e
There is one 'e'. Next guess: g
Incorrect, you now have 4 guesses remaining. Next guess: t
Hooray! You won! You have correctly spelled out the word 'the'.
t h e

{% endhighlight %}

Hangman Rules: <br/>
1. The guesser has 11 chances. A chance is deducted everytime they guess wrongly.
<br/> 2. If the user guesses correctly, no deductions should occur.
Below is a picture of a sample run.
<center> <img src="../assets/hangman.png">
</center>
<i>Photo curtesy of printactivities.com [Link](http://www.printactivities.com/Paper-Games/Rules-For-Hangman.shtml)</i>

<b>[BONUS]: </b> Print out each part of the hangman upon each guess, only adding to it if the user guesses wrong.




----------------------------------------------

<h1>day three</h1>

Today starts an Android app development series, where over the next week, we will program the steps of a game and build it into an app. Then you can add it to the app store if you would like.

Today we are going to code the first part of a game called Hangman. We will be learning the following ...
1. reading input from a text file
2. output from a file
3. various functions in the math library

First, go to the following link and download the text file called 'phobias.txt'. [Link](https://github.com/igweckay/code/tree/gh-pages/python_files)

Place the file in the same directory as your script. First we are going to load the file and then print out the contents of the file to the screen.

{% highlight python %}
filename = 'phobias.txt'
fopen = open(filename, 'r')
{% endhighlight %}

The 'r', means that we are opening the file as a read only. There are several different modes we can choose. The list is below.

1. r : open a file for reading
2. r+ : open for reading a writing, starting at the beginning of the file
3. w : open file for writing and add to the beginning of the file
4. a : open file for writing and append to the end of the file
5. a+ : open for reading and writing. If the file does not exist, it is created. content is appended to the end of the file

Now that the file is open, let's print the contents of the file using the following lines.

{% highlight python %}
  data = fopen.read()
  print(data)
{% endhighlight %}

In order to isolate one line from the file, we can use the following lines of code.

{% highlight python %}
  data = fopen.readline()
  print(data)
{% endhighlight %}

To save all of the content into a list of lines, we use the following ...


{% highlight python %}
  data = fopen.readlines()
{% endhighlight %}
We just add an 's' to the end of readline.
When you are done using the file, you have to close the file. Not closing the file could lead to problems such as memory leaks.

{% highlight python %}
  fopen.close()
{% endhighlight %}

To avoid having to use fclose, we can open the file using a 'with' statement. You can think of it as a while loop. It stays open and excutes everything in the with loop until it reaches an end of file. At this point, it exits the 'with' loop and close the file.
Next we are going to output the contents of the file line by line using a 'with' statement.

{% highlight python linenos%}
  #!/usr/bin/python
  # -*- coding: latin-1 -*-
  with open('phobias.txt', 'r') as file:
      for line in file:
          print(line)
{% endhighlight %}

If you are using Atom as your text editor, you may have to add lines 1 and 2 to your code. Those are the encoding declarations. For other editors, such as sublime, or if using Anaconda, adding those 2 lines may not be necessary.

## Programming challenge

Your challenge is to randomly choose a word from the list and spell it out onto the screen. A sample output is below. If the word chosen is 'arachnoid':

The file you will be reading files in from is named vocab_words.txt, and can be downloaded from the following [link](https://github.com/igweckay/code/tree/gh-pages/python_files).

<i><b>(bonus)</b> Have the program randomly choose a word from the list to be spelled. Have the program keep choosing words until you enter an exit key.</i>

{% highlight python linenos %}
  a
  r
  a
  c
  h
  n
  o
  i
  d
{% endhighlight %}

have fun!

----------------------------------------

<h1>day two</h1>

Today's challenge will be to code the first 3 challenges in Project Euler.
These programs are a great way to exercise some of your new skills. Slack me if you have any questions.

Link to [Project Euler](https://projecteuler.net/archives)

## Solutions

Problem 1:
{% highlight python %}

  ##########################################################################
  # multiples of 3 and 5
  # If we list all the natural numbers below 10 that are multiples of 3 or 5,
  # we get 3, 5, 6, and 9. The sum of these multiples is 23. Find the sum of
  # all the multiples of 3 or 5 below 1000.
  ##########################################################################
  i = 0; sum =0;
  while (i<1000):
  	if (i%3==0):
  		sum = sum + i;
  	elif (i % 5 == 0):
  		sum = sum + i;
  	i+=1;
  print(sum);

{% endhighlight %}

 answer:
 {% highlight python %}
 233168
 {% endhighlight %}

 Problem 2:

Best Solution, Chip's solution. My solution follows...
{% highlight python %}
  sum = 0
  f1, f2 = 0, 1
  while f2 < 4000000:
     if f2 % 2 == 0:
         sum += f2
     f1, f2 = f2, f1 + f2
  print(sum)
{% endhighlight %}

  answer:
  {% highlight python %}
  4613732
  {% endhighlight %}
 {% highlight python %}

   ##########################################################################################
   # Even Fibonacci numbers
   #
   # Each new term in the Fibonacci sequence is generated by adding the previous two terms.
   # By starting with 1 and 2, the first 10 terms will be:
   # 				1,2,3,5,8,13,21,34,55,89, ...
   # By considering the terms in the Fibonacci sequence whose values do not exceed four million,
   # find the sum of the even-valued terms.
   ##########################################################################################
  fib = [0,1,1]; i = 2; sum = 1
  while(fib[i]<4000000):
     fib.append(fib[i]+fib[i-1])
     if (fib[i]%2):
         sum = sum + fib[i]
     i += 1

  print(sum)

 {% endhighlight %}

  answer:
  {% highlight python %}
  4613732
  {% endhighlight %}


 Problem 3:


 {% highlight python %}

   num = 600851475143
   i = 2
   while i * i < num:
        while num % i == 0:
            num = num / i
        i = i + 1
   print(num)

 {% endhighlight %}

 answer:
 {% highlight python %}
   6857
 {% endhighlight %}
 <i>[reference for 3](https://www.w3resource.com/euler-project/euler-problem3.php)</i>

----------------------------------------------------

<h1>day one</h1>

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

---------------------------------------------

<h1>day zero</h1>

## Environment Setup

Make sure you have Python installed. We will be using Python3 throughout this 100 days. If you have a mac or a linux machine, you can check by opening up a terminal and typing the following commands.

{% highlight markdown %}
  python --version
{% endhighlight %}

Opening terminal,

Mac: To find terminal, go to your Launchpad, and click the "Other" app. You will see Terminal inside. Click on it.

Windows: Click on the start menu, and type in 'cmd'. Then press enter.

If you have a mac, it probably comes with Python 2.7.10 preinstalled.<br/>
Output:
{% highlight markdown %}
  Python 2.7.10
{% endhighlight %}

If you have a Windows machine, you can use the command as above to check your python version. If you do not know how to do this, it is ok, we will all be installing Anaconda, which will download all packages necessary for you to use Python. There is a video, by
Corey Schafer from youtube, at the bottom of this post that can guide you through the installation of Anaconda installation on both Mac and Windows.

## Downloading Anaconda
Go to the following link and click on download in the upper left hand corner. <br/>
[Anaconda Link](https://www.anaconda.com/what-is-anaconda/)

<center> <img src="../assets/anaconda_0.png">
</center>

Next click on your OS, Mac, Wndows, or Linux, which is circled in the blue in the image below. Once you have done that, click the download button in the Python 3.6 version box.

<center> <img src="../assets/anaconda_1.png">
</center>

Next, follow the installation steps given by the prompt.
<br/>Once you have installed anaconda, open up a terminal, for mac users, and cmd, for Windows users.

Mac: To find terminal, go to your Launchpad, and click the "Other" app. You will see Terminal inside. Click on it.

Windows: Click on the start menu, and type in 'cmd'. Then press enter.

Once you have terminal and cmd open, type the following...

{% highlight markdown %}
  jupyter notebook
{% endhighlight %}

Your jupyter notebook should start. This means you are ready to get started!! Stay tuned for day one, when we write our first program.

## VIDEO Tutorial:
You only need to pay attention to the first 3:11 minutes of the video.
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/YJC6ldI3hWk?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></center>
<br/><br/><br/>

--------------------------------------------------------------------
<h1>Introduction to 100 days of Code with Python</h1>
Welcome to the first day of 100 days of code. It is going to be a fun and exciting journey through programming with Python. Each day you will be given a tutorial and a program to code. You must complete coding the program and post it in the slack channel. Solutions will be posted both in the slack channel and on this blog the day after it is assigned.

Feel free to ask any question you would like. You can ping me on Slack and I can answer you there or we can do a Hangout or Slack meeting. Also feel free to post questions in the 'general' channel if you would like to ask questions to the group. That way any one could answer your questions as well.

## Outline
- Sign up with Slack
- Sign up for a Github Account
- Receiving Daily Projects
- Useful Videos
- Where to ask questions

## SLACK
Sign Up for a slack account via the following link: [100daysCodePython](https://100dayscodepython.slack.com/messages/CAETU36H2/) 👍🏼

I will be placing the projects in the ‘projects’ channel daily.

## BLOG
I will also be posting the projects, daily, on this blog.

## Github
Github is a great online repository to save all of your work. Create an account via this link: [Join Github](https://github.com/join?source=header-home)
If you have a github account, great! You are almost ready to begin! Follow this link on how to commit your first document to your repo.

## Receiving Daily projects
As written before, all projects will be posted on both the blog and on Slack.

## Useful Videos
thenewboston on youtube has a bunch of great programming video tutorials. Here is one of them. I will be pointing to these videos as time goes on. Here is their first video about installing Python. For this 100 days of Code, we will be working with Python 3.*

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/HBxCHonP6Ro?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></center>

## Where to ask question
You can ask all of your questions in the Slack channel.
