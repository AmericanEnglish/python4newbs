Startup
=======

1.  First start Python3 (32bit)

2.  Open Sublime Text 3

3.  Now in the interpreter type these commands

    ``` python
            >>> import robuts
            >>> from robuts import *
            >>> from importlib import reload
            >>> changedir("learn")
       
    ```

4.  Then in Sublime Text 3 start a new file by double clicking the dark space above the typing area

5.  Then save the file in your Document/Code/Learn folder as filename.py

6.  To run a file FOR THE FIRST TIME type

    1.  import filename

    2.  There should be NO .py when importing

7.  If you’ve already imported a file then to reimport it use

    1.  reload(filename)

I’m here to make lists and pet cats, and I’m all out of cats
============================================================

So today we’ll be talking about a very import concept in Python. Lists

``` python
>>> mylist = [1, 2, "string", "four"]
>>> mylist
[1, 2, "string", "four"]
```

Lists, often called “array” in other programming languages, are an integral (important) part of programming. They allow you to basically store several things and access them at your leisure. So if I had a favorite color, of course it’s blue, I would store it like

``` python
>>> mycolor = "blue"
```

Although I know that some *other people* have multiple favorite colors, the **heathens**. So if you had several colors you wanted to store you would have to have a variable for every color

``` python
>>> color1 = "red"
>>> color2 = "blue"
>>> color3 = "green"
```

I mean look at it. Three favorite colors? Terrible. Not nearly as terrible as how much you’ll have to type over and over again. Instead a more sensible approach would be to just type

``` python
>>> mycolors = ["red", "blue", "green"]
```

That’s so much quicker. It’s quick enough that in the time you saved you could buy stocks or motor oil or something . . . I’m not really on the up and up on what you kids are buying these days. I assume it’s like decorative socks or something. Anyways, if one day you were to think “Holy pineapples mermaid man, I also LUV the color orange”, you’d be a monster but you would also need to add orange to your list `mycolors`. So what you would do is something pretty simple

``` python
>>> mycolors
["red", "blue", "green"]
>>> mycolors.append("orange")
>>> mycolors
["red", "blue", "green", "orange"]
```

Notice how orange is at the end of the list. Every time you append something to a list it has to go to the back of the bus. Not like a regular bus, but like a computer bus; it has like 12 wheels or something idk I’m just here for the free food. So at this point what if we didn’t want to add things to the back of the list? Well it’s simple

``` python
>>> mycolors.insert(0, "purple")
>>> mycolors
["purple", "red", "blue", "green", "orange"]
```

By using the `.insert(index, item)` we can insert any item into the list at some index. Although I’m not a fan of the fact that I just purpled up that list.

``` python
>>> mycolors.remove("purple")
>>> mycolors
["red", "blue", "green", "orange"]
```

SHAHBAM AND LIKE THAT I SENT THAT PURPLE TO THE AFTERPURPLELIFE. If I want to access or use an item in the list

``` python
>>> mycolors[0]
"red"
>>> mycolors[3]
"orange"
>>> mycolors[1:3]
["red", "blue"]
>>> mycolors[4] # lists start at 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
>>> mycolors[2:]
["green", "orange"]
>>> mycolors[3:]
["orange"]
```

Using a colon will always give you a list in return. I know what you’re about to ask and it’s ok. I **have** always wanted to buy a ferret and travel the country singing the national anthem and here I am writing handouts. Crushed. Dreams. More importantly think of how a person could look at `mycolors` and be able to use it within the list. Of course they could index it but HOW WOULD THE PROGRAM KNOW? You would have to search for it using the `.index` method.

``` python
>>> mycolors.index("orange")
3
>>> mycolors[mycolors.index("orange")]
"orange"
>>> "orange" in mycolors
True
```

SPPPPOOOooooOOoOoOOOoKY. Fur real though it is a very useful technique for pulling things out of a list.

The big LLL. Loops, Lists, and Latvia
-------------------------------------

Yes, Latvia, the country. What do they have to do with this? To be honest I just needed another L name for that sick alliteration I just did. Marvel at it and all of its serious sounded syllabic splendor.

So as you might remember, maybe you don’t, I’m not keeping track, from the last handout that we used loops to traverse and add up all of our cookies inside that cray cray amounts of bags. So instead we’re going to do math (yaaaaaaay).

Now we’re going to tie some concepts together for a big list extravaganza. So let’s look at a very old tale from some country in Asia. I don’t know where it’s from, that’s the job of a historian.

The King of PastanoodleEmpire6000 demanded that he have the most beautiful chessboard in the land constructed for himself. So he asked his court to find the best chessboard maker in the land named Teddy Stroodle McGuire otherwise known as Tim. Tim said that he would gladly make the chessboard for his holynoodlesness. When the his holy pasta bowl asked what the carpenter needed for payment he was met with a humble request, “My King. I wish only for a coin the first day. Then five coins the next and then coins equal to two times the day worked plus one more coin for good measure”. The king of course agreed to such meager sums for the high noodleEmpire6000 had been doing good on its taxes that year. Tim figured it could take an upwards of a year to complete but no less than six months if he never slept, ate, and died at completion.

So the first thing we can do is start a new file called timNnoodles.py in Sublime. Then in our file what we’ll do is setup our variables

``` python
money_earned = 0
money_by_day = [] 
days_left = 365
current_day = 1
```

So Tim, being a normal bro with needs, has to eat nothing but fancy eggs costing a total of 12 coins each once a day. Like holy fox Tim that’s not normal that’s some rishfish habits you got fam but we’re not here to judge only to math. The boy also got 45 coins in the bank right now all saved up and biz.

``` python
egg_price = 12
saved_money = 45
```

So first we’ll need to figure out how much money he’ll earn every day and we’ll do it with a loop and a list.

``` python
while days_left >= current_day: # he might work on the last day
    money_by_day.append(2 * current_day + 1) # this is how he much he earns that day
    current_day += 1 # This keeps track of the day of work he's on
print("money_by_day \n>{}".format(money_by_day)) # this will print our list to see it!
```

From here we now know have 365 items inside our list `money_by_day`. So now how much money will he have earned if he works for the year?

``` python
for earning in money_by_day:
    money_earned += earning - egg_price # man's gotta eat amirite?
print("1 Year of work ~~~")
print("Money Earned: {}".format(sum(money_by_day)))
print("Costs of those yummy eggs: {}".format(365*egg_price))
print("Total money earned after egg prices: {}".format(money_earned))
```

What about six months of work?

``` python
current_day = 1
money_earned = 0
while current_day < days_left // 2: # Half a year after all
    money_earned += money_by_day[current_day - 1] # days start at 1 but lists start at 0
    current_day += 1
print("Six months of work ~~~")
print("Money Earned: {}".format(sum(money_by_day)))
print("Costs of those yummy eggs: {}".format(365*egg_price))
print("Total money earned after egg prices: {}".format(money_earned))
```

Goodness tim, maybe you should’ve stretched it out your work a little more because you would’ve made more and not been super ded.

So as you can see we use lists to store data like `money_by_day`. That’s it. Man was this long for something like that.

BONUS ROUND WOOOOMP WOOOOOMPWOMPWOMPWOMP, like an air horn guys....
===================================================================

If statements
-------------

An if statement is something that says IF thing THEN do this ELSE do this. It’s not worth a full handout but I *really* need this out of the way, so please roll with it.

``` python
>>> answer1 = True
>>> answer2 = False
>>> if answer1 == True: # answer1 is true, so this is true
...     print(1)
... 
1
>>> if answer1: # you can just say this instead
...     print(1)
... 
1
>>> if answer2: # answer2 is false
...    print(1)
... elif not answer2: # not false IS true
...    print(2)
2
>>>
```

Basically if statements just let us do things when some things are true. So if you have a number like 5 and want to add 5 if it’s less than 10 you would write

``` python
>>> mynum = 5
>>> if mynum < 10:
...     mynum += 5
... else:
...     mynum -= 5
>>> mynum
10
```

This will come in handy for a future handout. If you get bored feel free to solve the following example

Illihonk loves to pick up cherries from the market, but sometimes forgets that he doesn’t have space at home! Silly Illihonk is always complaining about it... so he needs us to help, like blue clues style. So he currently has 12 cherries at home but only has room for 200 cherries. He eats two cherries a day but buys five cherries everyday. How many days can he keep mindlessly buying these gross cherries (lol) before he is all stocked up? Assuming he stops buying when he’s fully stock how long until he needs to buy them again?

I’ll put some sample code up in here for y’all.

``` python
cherries_a_day = 5
eats_a_day = 2
max_cherries = 200
current_cherries = 12
days = 0
# This loop add cherries until he's stocked up make another one that will subtract  
# cherries till he's ready to buy again.
while True: # now it runs foreveeeeeeeeer or fiveever some would say
    days += 1
    if current_cherries + 5 < max_cherries:
        current_cherries += cherries_a_day
        current_cherries -= eat_a_day
    elif current_cherries + 5 == max_cherries:
        current_cherries += cherries_a_day
        current_cherries -= eat_a_day
        break # this stops the loop
   else:
        break
print("Eating {} cherries a day, and buying {} cherries a day.".format(
    eat_a_day, cherries_a_day))
print("He'll hit his limit of {} cherries in {} days.".format(max_cherries, days))
```
