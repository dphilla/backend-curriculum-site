---
title: Primer on .each
length: 60
tags: enumerable, ruby, collections, arrays, each, debugger, pry
---

# Intro to .each

### Goals

* Understand how to use single-line and multi-line each
* Learn how to use a debugger to pause and interact with running code


#### Debuggers

As programmers we often make assumptions about what our code is doing. We are often wrong. One of the most important and effective debugging techniques is to validate your assumptions.

Have you ever found yourself working on a programming problem and as you attempt to solve it, you are forced to run the entire file over and over again until you get the correct result? Wouldn't it be awesome if you could pause your code at a specific line and interact with it? Enter debuggers.

Debuggers are great to see what your code is actually doing. The most common debuggers in ruby are `byebug` and `pry`. You can pick whichever you prefer. For this exercise we will use `pry`.

### Using `pry`

* Make sure it is installed globally (we will do in class in a moment)

`gem install pry`

You need to require it at the top of your Ruby file.

```
require "pry"
```

Now you can use it like this...

```
favorite_celebs = ["Kim", "Kourtney", "Khloe"]
binding.pry
```

We're going to use your debugger to explore `.each` and on the challenges below.

Let's use [this gist](https://gist.github.com/ameseee/d060d7ed237d02ead7c1c6837817107b) as a guide.

#### Setup

In your terminal:
  * Install pry `gem install pry`
  * Make a new directory & cd into it (probably inside of your Mod1 directory)"" `mkdir intro_to_each && cd intro_to_each`
  * Create a file for practice: `touch each_practice.rb`
  * Open the file in atom: `atom .`
  * Copy and paste the contents of the Gist above into your file (`cmd + a` will highlight all, `cmd + c` will copy, and `cmd + v` will paste!)


#### What are enumerable methods?

* methods that can be used on arrays and hashes to go through each element or
search for elements or  an element (today we focus on what iterating over _arrays_ only!)


#### What is .each?

* .each is the base for enumerable methods.
* it allows you to iterate over a collection
* it **returns** the original collection


#### What is the syntax for writing enumerable methods?
Multi-Line
```ruby
array_of_items.each do |item|
  item.do_something
end
```
Single-Line
```ruby
array_of_items.each { |item| item.do_something }
```

**Discuss:** What are some of the key differences between the two ways to write an each method? Do you prefer one over the other? Why?


#### Basic use of .each

Let's say we have an array of words, and we want to print out to the screen
each word in the array, but in all capitalized letters.

```ruby
celeb_kids = ["Reign", "Penelope", "Mason"]

celeb_kids.each do |kid|
  puts kid.upcase
end
```
This can also be written:
```ruby
celeb_kids = ["Reign", "Penelope", "Mason"]

celeb_kids.each { |kid| puts kid.upcase }
```

What do you think each of these **returns**?

Remember that there is a difference between what gets output to a screen
vs what a bit of code returns.


#### Exercises

Use your debugger to work through the following...

* If you had an array of numbers, e.g. [1,2,3,4], how do you print out the
doubles of each number? Triples?
* If you had the same array, how would you only print out the even numbers?
What about the odd numbers?
* How could you create a new array which contains each number multiplied by 2?

* Given an array of first and last names, e.g. ["Kris Kardashian", "Rob Kardashian", "Kaitlyn Jenner"], how would you print out the full names line by line?
* How would you print out only the first name?
* How would you print out only the last name?
* How could you print out only the initials?
* How can you print out the last name and how many characters are in it?
* How can you create an integer which represents the total number of characters in all the names?
