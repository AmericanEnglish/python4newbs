Startup
=======

1.  First start Python3 (32bit)

2.  Open Sublime Text 3

3.  Now in the interpreter type these commands

    ``` python
            import robuts
            from robuts import *
            from importlib import reload
            changedir("learn")
       
    ```

4.  Then in Sublime Text 3 start a new file by double clicking the dark space above the typing area

5.  Then save the file in your Document/Code/Learn folder as filename.py

6.  To run a file FOR THE FIRST TIME type

    1.  import filename

    2.  There should be NO .py when importing

7.  If you’ve already imported a file then to reimport it use

    1.  reload(filename)

THE STRIIINGS! THE STRRRIIIIIINNNNGGGSSSS!
==========================================

First start by creating a new file called ex3.py

For this handout we’ll be using string “methods” and other things to solve problems. What is a method? A method, in python, is something that’s accessed with a . operator. Like

``` python
something.methodname()
"This is a string".StringMethod()
```

So what kind of things can we do with strings? Well we can do the following:

1.  We can slice them

    ``` python
    >>> "LoveBuns"[0:3]
    "Lov"
    >>> "LoveBuns"[3:]
    "eBuns"
    >>> "LoveBuns"[2:3]
    "v"
    ```

2.  We can use their methods to do stuff as well

    ``` python
    >>> "Honk honk".title() # Make it movie cased
    "Honk Honk"
    >>> "Honkhonk".lower() # lower cases all letters
    "honkhonk"
    >>> "Honkhonk".upper() # upper cases all letters
    "HONKHONK"
    ```

3.  Then finally, we can, compare them!

    ``` python
    >>> "A" == "a"
    False
    >>> "B" == "a"
    False
    >>> "Honkhonk" == "Honkhonk"
    True
    >>> "Meep" == "meep".title()
    True
    >>> "meep".upper() == "MEEP"
    True
    ```

Applications
============

Palindromes
-----------

So in your ex3.py let’s store some things in variables:

``` python
quizzacious = "quizzacious"
aibohphobia = "aibohphobia"
supremum = "SUPREMUM"
```

So to this we need to know what is a Palindrome:

-   Palindrome - A word that is spelled the same forward and backwards. For example, racecar and “look kool”.

Of those three which words are Palindromes? Well first let’s check and see what the words are backwards

``` python
>>> "quizzacious"[::-1] # This reverses the string
'suoicazziuq'
>>> "quizzacious" == "quizzacious"[::-1] # This compares the normal and reversed
False
```

So let’s check if the words are Palindromes and store the True/False value in a variable. In your file put

``` python
# This will either be true or false
quiz_palindrome = (quizzacious == quizzacious[::-1])
aibh_palindrome = (aibohphobia == aibohphobia[::-1])
supr_palindrome = (supremum == supremum[::-1])
```

Then we can just print those values!

``` python
print("Quizzacious is a Palindrome? {}".format(quiz_palindrome))
print("Aibohphobia is a Palindrome? {}".format(aibh_palindrome))
print("Supremum is a  Palindrome? {}".format(supr_palindrome))
```

Now go ahead and import the file. Or reload the file if you’ve already import it once.

Methods
-------

Now open another file called ex4.py. What we’ll do now is test out some of the string methods that we talked about earlier. Let’s start by putting defining some variables

``` python
myname = "Thomas Jenkins"
sentence = "The quick brown fox jumps over the lazy dog"
another = "I can tell you pie is 3.1415926 that's for sure!"
OtherWords = ["cat", "dog", "bat"]
finally = "I can finally own a {}"
```

So the fourth variable is called a “list” which is just a collection of stuff. In this case our list is a collection of strings. So what we’ll do with is is just:

``` python
>>> [10, 20, 30][0]
10
>>> [10, 20, 30][1]
20
>>> [10, 20, 30][2]
30
```

You don’t have to worry too much about what’s going on with it just know we’ll be using it So now we can start to do some more fun stuff. What if they came out with a movie called “The Quick Brown Fox Jumps Over The Lazy Dog”? I’d have to change my sentence variable to be in the Title Case. So I’ll put this in the file

``` python
print(sentence.title())
```

Now the sentence will print in a title casing. Now my complaint falls upon the variable called another. I’m VERY excited about pi. Why should that sentence now be FULLY capital?? I WANT IT TO BE SHOUTING BAOUT PI. Let’s make it happen:

``` python
print(another.upper())
```

My final complain is that I also like to rebel a little bit in my spare time. So I’m going to decapitalize Thomas’ name. Help my fight the powa with this in your file

``` python
print(myname.lower())
```

Nice! We’ve used these string methods to do . . . a random collection of things I guess. Although, do you, remember that third variable and fourth variable? We can use to express out love for one of those three animals! I’ll put my personal favorite up in here but you feel free to chose either the first, second, or zeroth option. Yes. Zeroth. Strings and Lists start by counting at zero. So in my file I’ll have

``` python
print(finally.format(OtherWords[0]))
```

Now look at that line because it is VERY special.

``` python
finally.format(OtherWords[0])
 finally
#~~~~~~~        
#Variable name 
        .format()
#        ~~~~~~~
#       The method name
               OtherWords
#               ~~~~~~~~~~
#               The list's variable name
                         [0]
#                        ~~~
#                        The index/item number in the list to use!
```

All these combine into something that will let us stop having to type out long print statements. In the future we’ll just be able to use variables and stuff to make it automated! That’s all for now!
