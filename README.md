###What is it about?
This is a simple introduction to the basic usage of gnuplot command line tool.
Exemples and scripts templates can be downloaded.

###Is Gnuplot what you are searching for?
Gnuplot is a simple-to-use command-line driven graphing utility.


----------------------------------

﻿﻿﻿This is an introduction to the basic usage of thle graphics command line tool Gnuplot, in a unix-like environement (linux, mac).

We generate the graphs by the following command (arguments are facultatif):

gnuplot scriptfile [arguments]

Lines that that start with a **#** are comments.

1. Simple graph :
For a basic ploting, you need a file with the dots coordinates (x,y).
The **x** and **y** axis are represented in a file by two lines separated (by default) by a space (other separator may be defined) 
The following example shows the variation in temperature during the first week of July 2014:
[Data1]:(clicable, to download the data1 file)
1 29
2 31
3 30
4 28
5 32
6 34
7 35

Let's write a script that draws a graph for this data:
First we define ...

[Script1]:

The result will be as follows:
[Graph1]

2. Multiple graphs
Lets take the same example. But this time, we are also measuring the "humidité" level.
So our file would look like this:
[Data2]:
1 29 64
2 31 62
3 30 69
4 28 67
5 32 74
6 34 78
7 35 82

Only one line is going to be modified in our script file:
[Script2]:

The result will be as follows:
[Graph2]

3. Tips and trics:

- Rotate data in axis for lisibility:
Lets take the example of a population growth (million person) during the years. Data is as follows:
[Data3]:
1990 40
1991 41
1992 41
1993 42 
1994 42
1995 42
1996 41
1997 40
1998 41
1999 42
2000 43
2001 44
2002 45
2003 47
2004 49
2005 50
2006 52
2007 52
2008 54

We can see in the figure bellow that there is a lisibility problem, which we are going to solve by rotating the display of the years in the following script:
[Script3]:

The result will be as follows:
[Graph3]

- Using variables:
We can generalise a script to use it with different data files, by the use of variables.
Lets use the following data files [Data1] and [Data3].
The script will look like this:
[Script4]

The graph will then be generated with the following command:

gnuplot scriptfile title=blahnlah xtitle=.... ytitlee=....

The result will be as follows:
[Graph4]


- Using the *for* loop:
When we have a repeated task to do, wecan use a loop to helps us.
For example, we want to draw a graph representing the time taken by 6 different algorithms to check whether a number is prime or not.
Data are represented in the file [Data5].
The script will be:
[Script5]


The result will be as follows:
[Graph5]















