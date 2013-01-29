Python notes
============

## Simple HTTP server

    cd <folder>
    python -m SimpleHTTPServer [port]


## Virtualenvwrapper

    workon envname


## Swapping Variables

    x = 6
    y = 5
     
    x, y = y, x
     
    print x
    >>> 5
    print y
    >>> 6


## Inline if Statement

    print "Hello" if True else "World"
    >>> Hello

## Concatenations

    nfc = ["Packers", "49ers"]
    afc = ["Ravens", "Patriots"]
    print nfc + afc
    >>> ['Packers', '49ers', 'Ravens', 'Patriots']
     
    print str(1) + " world"
    >>> 1 world
     
    print `1` + " world"
    >>> 1 world
     
    print 1, "world"
    >>> 1 world
    print nfc, 1
    >>> ['Packers', '49ers'] 1

## Numbers

### Floor Division (rounds down)
    print 5.0//2
    >>> 2
     
### Powers

    print 2**5
    >> 32

### Floating point warning

    print .3/.1
    >>> 2.9999999999999996
     
    print .3//.1
    >>> 2.0

### Comparison

    x = 2
     
    if 3 > x > 1:
        print x
    >>> 2
     
    if 1 < x > 0:
        print x
    >>> 2


## Dictionary Comprehension

    teams = ["Packers", "49ers", "Ravens", "Patriots"]
    print {key: value for value, key in enumerate(teams)}
    >>> {'49ers': 1, 'Ravens': 2, 'Patriots': 3, 'Packers': 0}

### Get item with default value

 > Instead of

    data = {'user': 1, 'name': 'Max'}
    try:
        is_admin = data['admin']
    except KeyError:
        is_admin = False

 > Do this

    data = {'user': 1, 'name': 'Max'}
    is_admin = data.get('admin', False)


## Lists

### Iterate Through Two Lists at the Same Time

    nfc = ["Packers", "49ers"]
    afc = ["Ravens", "Patriots"]
     
    for teama, teamb in zip(nfc, afc):
        print teama + " vs. " + teamb
     
    >>> Packers vs. Ravens
    >>> 49ers vs. Patriots

### Iterate Through List With an Index

    teams = ["Packers", "49ers", "Ravens", "Patriots"]
    for index, team in enumerate(teams):
        print index, team
     
    >>> 0 Packers
    >>> 1 49ers
    >>> 2 Ravens
    >>> 3 Patriots

### List Comprehension

 > Turn this:

    numbers = [1,2,3,4,5,6]
    even = []
    for number in numbers:
        if number%2 == 0:
            even.append(number)

> Into this:

    numbers = [1,2,3,4,5,6]
    even = [number for number in numbers if number%2 == 0]
    Pretty sweet huh?

### Initialize List Values

    items = [0]*3
    print items
    >>> [0,0,0]

### Converting a List to a String

    teams = ["Packers", "49ers", "Ravens", "Patriots"]
    print ", ".join(teams)
    >>> 'Packers, 49ers, Ravens, Patriots'

### Subsets

    x = [1,2,3,4,5,6]
     
    #First 3 
    print x[:3]
    >>> [1,2,3]
     
    #Middle 4
    print x[1:5]
    >>> [2,3,4,5]
     
    #Last 3
    print x[3:]
    >>> [4,5,6]
     
    #Odd numbers
    print x[::2]
    >>> [1,3,5]
     
    #Even numbers
    print x[1::2]
    >>> [2,4,6]


## FizzBuzz in 60 Characters

    for x in range(101):print"fizz"[x%3*4::]+"buzz"[x%5*4::]or x


## [Collections](http://docs.python.org/2/library/collections.html)

### Counter

    In addition to python's built in datatypes they also include a few extra for special use cases in the collections module. I find the Counter to be quite useful on occasion. Some of you may even find it useful if you're participating in this year's Facebook HackerCup.

    from collections import Counter
     
    print Counter("hello")
    >>> Counter({'l': 2, 'h': 1, 'e': 1, 'o': 1})
    Itertools


## [Itertools](http://docs.python.org/2/library/itertools.html)

### Combinations

    from itertools import combinations
     
    teams = ["Packers", "49ers", "Ravens", "Patriots"]
    for game in combinations(teams, 2):
        print game
     
    >>> ('Packers', '49ers')
    >>> ('Packers', 'Ravens')
    >>> ('Packers', 'Patriots')
    >>> ('49ers', 'Ravens')
    >>> ('49ers', 'Patriots')
    >>> ('Ravens', 'Patriots')

## Sources

[Max Burstein](http://maxburstein.com/blog/python-shortcuts-for-the-python-beginner/)

## To-Do

  * sets
  * yield
  * decorators
  * functools
