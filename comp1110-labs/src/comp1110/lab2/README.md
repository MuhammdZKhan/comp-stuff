# COMP1110 Lab 2

## Purpose

In this lab you will write, test, and debug some small Java programs.   All of the exercises are done inside your IntelliJ environment, in your labs repo.   You may work on your own computer, but you will need to share your work with your tutor and discuss it with them in your lab.

**It is essential that you complete this lab and have a tutor mark it off**.

## Tasks

1. **Countries**

    Inside the package `comp1110.lab2` make a new class `Countries`. Inside your new class create an array of `String`s that has the names of the following countries: Germany, Argentina, Netherlands, Brazil. Print out the elements of the array on separate lines (you do not need to use a loop for this, just use fixed indices into the array).

2. **Reverse**

    Make a new class `Reverse` within the `comp1110.lab2` package and using a `while` loop, write a program that prints (on separate lines) the numbers between and including 10 and 30 in reverse order. i.e. the program should print on separate lines: 30 29 28 ... 10.

3. **Triangle**

    Create a class `Triangle` within the `comp1110.lab2` package, that draws simple triangles using ASCII characters and prints to standard output. The program should read in from the console an integer which represents the height (in characters) of the triangle. Use the `*` character to draw the resulting triangle. The first line should have one`*`, the second will have a `*` followed by one space, followed by a `*`, the third will have three spaces, the fourth will have five, etc. The last line will have (height x 2) - 1 `*`'s. For example, for an input of 5, the output might look like this (here a '_' is drawn to represent a space character):
```
____*
___*_*
__*___*
_*_____*
*********
```
Test your program using the `TriangleTest` class.

4. **Commit and push your work**

    Commit your changes locally (navigate through `VCS` and select `Commit changes...` (*or* press `Ctrl + K`). Write a commit message that says: `Done with Lab 2!`. Leave everything else to its defaults.

    Push your changes, which will allow your tutor to see them (`VCS` -> `Git` -> `Push` (*or* `Crl + Shift + K`).

5. **Prepare for the lab test**

    If you finish early, use any spare time you have to do further preparation for lab test 1. You are encouraged to ask your tutor for help in understanding how to complete any of those questions.
