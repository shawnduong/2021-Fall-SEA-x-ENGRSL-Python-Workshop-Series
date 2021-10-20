# Workshop 1: Hello Python!

In this workshop, you'll be learning the basics of programming and Python! This document is essentially a reference sheet for you, and will also contain the activities and descriptions.

## Important Topics

- The Big Picture Idea
- Logic
- Conditionals
- Loops
- Functions

## Logic Activity

(There is nothing here because this is done as a class.)

## Conditionals Activity

1. As a group, **think of 3 everyday examples of conditionals and express them in pseudocode.**
   - Example: "If the temperature is greater than 90 degrees, then I'll take my jacket off."
```python
if temperature > 90:
	I'll take my jacket off
```

2. As a group, **write and run your first real Python conditional: let X = 20. If X is an even number, print out, "X is even." Else, print out, "X is odd."**
   - Solve the problem as a group, but try to run it on your own individual devices! That way, everyone in the group will know how to run Python on their personal devices.

## Loops Activity

1. As a group, **think of an everyday example of a while loop, for x in y loop, and for x in range(N) loop, and express them in pseudocode.**
   - Example: "While I am hungry, I will eat. For every item in my shopping list, I will search for that item and then buy it. For every year my friend has been alive, I will give them a birthday punch."
```python
while I am hungry:
	I will eat

for item in shoppingList:
	search for item
	buy item

for year in range(friendAge):
	birthday punch friend
```

2. As a group, **write and run your first real set of Python loops that print out all the even numbers from 0 to 10, but not including 10.** You're basically solving the same problem in 3 different ways.
   - For "for x in y" loops, you may find the following line of code useful: `numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]`
   - Solve the problem as a group, but try to run it on your own individual devices!

## Functions Activity

1. As a group, **create a real Python function that just says "Good morning!" Then, call it.**
   - Solve the problem as a group, but try to run it on your own individual devices!

## Puzzles

1. Let's suppose that you have a list of unsorted numbers: `[1, 8, 2, 6, 3, 9, 0, 1, 4, 2, 8]`. How can you sort these numbers so that we have `[0, 1, 1, ...]`?
   - You don't need to write any code -- just think about the problem and try to use words like **if** and **for.** You can try writing pseudocode.
   - If you do want to write real Python code, feel free!

2. Let's suppose that we have the list of numbers: `[1, 5, 2, 3, 0, 0, 1]`. How can we turn this list into the number `1523001`?
   - You don't need to write any code -- just think about the problem and try to use words like **if** and **for.** You can try writing pseudocode.
   - If you do want to write real Python code, feel free!
   - Hint: multiplying any number by 10 adds a rightmost zero.

## Python Reference Sheet

```python
# Comments look like this. They start with a '#' sign.

# Conditionals look like this.
if condition:
	instructions

# Here are a few examples.

if x < 5:
	print("x is less than 5.")

if x < 5 and x % 2 == 0:
	print("x is less than 5, and x is also an even number.")

if passwordEntered == actualPassword:
	print("You entered the right password!")
	print("Hello user.")

# There are 3 kinds of loops:
# - while loops do something while a condition is true.
# - for x in y loops do something for every item x in a collection of items y.
# - for x in range(N) will do something N many times.

# Here are a few examples.

letter = input("Enter a letter: ")
while letter != 'a':
	print("You didn't enter letter the letter 'a'")
	letter = input("Enter a letter: ")

people = ["John", "Jane", "Jack", "Jill"]
for person in people:
	print("Hello", person)

for i in range(10):
	print("Hi!")

# Functions look like this.
def greet():
	print("Hello!")

# That's just the definition. It doesn't actually run the function. In order to do that, you need to call it.
greet()
```

## Tello Reference Sheet

Remember to install the libraries first before you proceed! In order to install the libraries, run the following commands:

```sh
pip install easytello
pip install opencv-python
```

This reference sheet only contains items relevant to workshop 1. You can check out the full documentation at: https://github.com/Virodroid/easyTello

```python
# Remember to import the libraries that you need.
# We'll talk more about libraries in the future.
import easytello

# This is how you make drone objects.
# We'll talk more about objects in the future.
drone = easytello.tello.Tello()

# This is how you turn the camera on and view the feed.
drone.streamon()

# This is how you turn the camera off and stop viewing the feed.
drone.streamoff()
```

**Important note:** your program will try to finish as fast as possible. This means that it'll turn the camera on, *but then it immediately turns it off.* You might find this code useful:

```python
# Import the time library.
import time

# Sleep for 5 minutes. 5 minutes * 60 seconds/minute = 300 seconds.
time.sleep(300)
```
