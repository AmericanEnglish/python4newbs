Startup
=======

1.  First start Python3 (32bit)

2.  Open Sublime Text 3

3.  Now in the interpreter type these commands

    1.  import robuts

    2.  from robuts import \*

    3.  from importlib import reload

    4.  changedir(“learn”)

4.  Then in Sublime Text 3 start a new file by double clicking the dark space above the typing area

5.  Then save the file in your Document/Code/Learn folder as filename.py

6.  To run a file FOR THE FIRST TIME type

    1.  import filename

    2.  There should be NO .py when importing

7.  If you’ve already imported a file then to reimport it use

    1.  reload(filename)

Printing, Variables, and Mathematics OH MY!
===========================================

Mathematics & Printing
----------------------

### Basics

First start by creating a newfile called ex1.py Then to Solve the Otter problem we’ll be using the remainder function %. For example:

``` python
n % m
```

This says give me the remainder of `n//m`. So:

``` python
>>> 12 // 2
6
>>> 12 % 2
0
>>> 17 // 2
6
>>> 17 % 2
1
```

If you were to put `n//m` you would see like above. If were to import or reload NOTHING would appear in the interpreter. Why? This is because you did TELL python to put TELL the user something has happened. The only way python can tell the user what’s happening is with the `print` function. So if you have:

``` python
print("Here is some data fam")
print("17 % 2 = {}".format(17 % 2))
```

In the case above the `.format(thing)` says "Please replace the {} in ’17 % 2 = {}’ with the math answer to `17 % 2`.

So when you import a file containing the code above this will happen:

``` python
>>> import ex1
Here is some data fam
17 % 2 = 1
>>>
```

Try it! Otherwise let’s move onto some actual math problems

### Application

So now we’ve moved onto actually using this information for good, possibly evil, purposes? That seems just . . . dandy? Fine? Meow? Anyways I’ll present a story problem for you:

Once upon a time there was a baker named Geo and had two parties who requested slabs o’ sweets otherwise known as SLOS. He knew that he only had 157 SLOS available and knew that the Ruby Roses demanded two SLOS for every member (a total of 27). The Sad Sapphire want to divide the remaining sweets evenly among themselves with no leftovers (there are 11 of them). All leftovers are kept by the baker. How many total go to each party?

First we want to start off by making another file called prob1.py Start off by storing ALL of the needed numbers into variables like so

``` python
total_sweets = 157
rubies = 27
sweets_per_member = 2
```

Then the next step is for us to do some math AND STORE IT AS A VARIABLE

``` python
rubies_total = rubies * sweets_per_member
saph_total = (total_sweets - rubies_total) // 11
leftovers = (total_sweets - rubies_total) % 11
```

Remember that the % lets of return the remainder and the `//` lets us divide and round down so we won’t have a decimal. Now all we have to do is PRINT the answer like so

``` python
print("The Rubies get {} SLOS".format(rubies_total))
print("The Sapphires get {} SLOS".format(saph_total))
print("The baker keeps {} SLOS for himself".format(leftovers))
```

Now import this file and you should see that all the print statements work and display the information in an IMPORTANT and MEANINGFUL MANNER I recommend that you change around the numbers and also change the variables names. Maybe try changing the print statements and see what happens.
