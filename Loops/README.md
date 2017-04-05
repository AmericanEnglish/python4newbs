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

No Shoes, Just Loops.
=====================

What and Why do we do the loop da loop?
---------------------------------------

So this handout is probably going to be much harder than the previous handouts. You’re going to be handling what are called “loops” you may call them: “loops”, “circles with no edges”, or even “Johanna the Fallen Soldier of the Nexas”. Whichever you prefer.

Basically imagine that you have add a WHOLE TON OF STUFF I MEAN LIKE 12 WHOLE THINGS. So in the interpreter I have:

``` python
>>> mystuff = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
```

If I wanted to add all of those up, like omg Tina, I couldn’t do it easily. This is how you add them by hand:

``` python
>>> mystuff[0] + mystuff[1] + mystuff[2] + mystuff[3] +  mystuff[4] +  mystuff[5] +  mystuff[6] +  mystuff[7] +  mystuff[8] +  mystuff[9] +  mystuff[10] +  mystuff[11] 
78
>>> # lists start counting at 0 remember?
>>> 1+2+3+4+5+6+7+8+9+10+11+12
78
```

Just typing that out for this handout hurts my feelings and my wrists. More importantly this is a lot of typing and every time I add another item to “mystuff” I have to type EVEN MOAR! In programming this is regarded to as crazy people stuff and instead we just loops.

FOR THE KING
------------

So there are actually two types of loops in MOST programming languages. The first one is a FOR loop. We use a for loop when we “know” how many things we have to work with. If you know that you have 12 bags of cookies and need to count the cookies that’s a for loop! If you have a ton of numbers in your stuff and need to sum them then that’s a for loop!

``` python
>>> x = 0
>>> for item in mystuff: # click enter and the dots will appear
...     x = x + item  # click enter twice to end the ``...''
... 
>>> x
78
```

That was WAAAAAAAAAYYYYYY QUICKER.

WHILE IN ROME FAM FAM
---------------------

The other type of loop is called a “while” loop. The purpose of a while loop is to run and stop when “something special happens”. If you think that sounds vague you should ask me about how building a website is. Imagine you run a bakery, yes I know my baking examples are on fleek, and you get a call that says “Hey there Momo of Harrington I’m going to send you cookies to count until like 5pm aight?” You know when you’re going to stop counting: 5pm. Do you have any idea how many cookies you’ll be counting? No. So assume we get a bag of cookies every hour from noon till 5pm.

``` python
>>> bag0 = [1, 1, 1, 1]
>>> bag1 = [1, 1, 1, 1, 1, 1, 1]
>>> bag2 = [1, 1, 1, 1, 1]
>>> bag3 = [1, 1, 1, 1, 1, 1, 1, 1]
>>> bag4 = [1, 1, 1, 1, 1, 1, 1, 1]
>>> bag5 = [1]
>>> all_bags = [bag0, bag1, bag2, bag3, bag4, bag5]
```

Now to use the loop you’ll need to know one other Python thing. Python will tell you the length of things using `len`.

``` python
>>> len("string")
6
>>> len([1, 2, 3])
3
>>> len("123")
3
```

So to do the while loop you would write it like

``` python
>>> i = 0 # this helps the loop stop
>>> total = 0
>>> while i < len(bag0):
...     total += bag[i]
...     i = i + 1
...
>>> total
4
```

We managed to sum all of the item in the first bag with a while loop!

Two loops for the price of two!
-------------------------------

Now to tie these loops together in one example what... what if ... No we can’t. BUT WAIT WE CAN. WE CAN SUM ALL THE BAGZ. ALL UR BAGZ R BELONGS TO LOOPZ. So what we’ll do is use a while loop to go through `all_bags` and use a for loop to go through each bag individually.

``` python
>>> i = 0
>>> total = 0
>>> while i < len(all_bags):
...     for item in all_bags[i]:
...          total += item
...     i += 1
...
>>> total
33 # probably. I'm not actually testing these.
```

So let’s break down that mess more:

``` python
while i < len(all_bags)
```

This line says that as long as our index, or position in `all_bags`, is less than the length keep going. If you try to access magical nonexistent things outside of the list Python gets upsets and prints mean things that we can’t read. The `len(all_bags)` is just a way to use the length of of that list (which is 6). Using len means that we could add more items to `all_bags` and not have to change any of the code.

``` python
for item in all_bags[i]:
    total += item
```

This says that we need to access the i**<sup>*t**h*</sup> item of `all_bags`. Then we add each item to the total.

``` python
i += 1
```

This helps progress the loop. After all if `i < len(all_bags)` ISN’T true the loop will stop. So we add 1 to i so that the loop will EVENTUALLY STOP. If you don’t put this in the loop will run forever. I’m serious though don’t mess around you could crash Python or the computer could lock up. Don’t mess with loops because loops will mess with you.

APPLICATION WITH A VACATION
---------------------------

So let’s start making a file that uses loops! First we’re going to need to put some stuff in our new file looplover12.py

Poor Izzyboo. He wants to go on vacation but doesn’t know if he can afford it! What he’ll do is he’ll start saving money! First day he puts in a dollar and then everyday after that he’ll save DOUBLE that. So the second day he saves TWO WHOLE DOLLARS. Then the third day FOUR WHOLE DOLLARS. If he goes on vacation in three weeks then will he have enough to pay for it? The vacation is like 12,000 dollars or something.

To help lil’ IzzIzz what we’ll do it use loops, variables, and . . . I think that’s it. First setup some variables in your file:

``` python
saved_today = 1
money_saved = 0
days_left = 21
```

So the amount of days he has left is 21. Since we haven’t start a loop we’ll make the money he’s saving on day 1 a dollar and the money save will be 0 because we haven’t looped yet. Now onto the loop.

``` python
while days_left > 0:
    money_saved += saved_today # this stores his money from today
    saved_today 8*= 2 # this doubles the money he'll save tomorrow
    days_left -= 1 # this says that he has one less day to save
```

Now we’re using the while loop to keep doing math until he has zero days left till vacation. He BETTER have saved enough by then or else he’ll be living dat scrub life instead of lounging in Panama.

From this point the loop will work maths out his money. Now we have to print how much money he has saved and if he has enough to go.

``` python
print("Izzy has saved {} dollars".format(money_saved))
print("It is {} that he can go...".format(money_save > 12000))
```

Now import the file and watch the magic. You might also note that this file is very short even though it does a lot. That’s the power of programming kids and Schadler.

Now, clearly he didn’t have to save the entire three weeks. We can use loops to improve the life of the Izzykin. Let’s find out how many days he HAD to save. Start a new file called poorizzy.py Since we DON’T KNOW how many days he’ll have to save we will use a while loop.

``` python
saved_today = 1
money_saved = 0
days_left = 21
```

Then our loop. Pay attention to how it’s different!

``` python
while (money_saved < 12000 and days_left > 0):
    money_saved += saved_today
    saved_today *= 2
    days_left -= 1
```

The two parts to the loop are `money_save < 12000` and `days_left > 0`. Basically if Izzy saved less than 12 grand the loop keeps going BUT it only keeps going if he days left to save. Now let’s print how much he saved and what day he stopped saving!

``` python
print("Izzy saved {} dollars".format(money_saved))
print("Izzy had {} days left to relax".format(days_left))
```

You’ll see he still had a few days to relax before vacation. Though he ended up saving quite a bit more but that’s Izzy’s problem man not ours. Unless we’re going to go with him then it is our anti-problem, whatever they call those.

I recommend that you changed the `saved_today *= 2` to `saved_today += 199` or some other number or change how many `days_lefts` left he starts with. Instead of 21 make it 30, or 12. Test out how the loop works when you do this.
