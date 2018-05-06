---
layout: post
title:  "day three with python"
author: "kay"
---

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
