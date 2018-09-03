Finally let's take a deeper look at the commands we have been running.  We have
been using `ls` a lot in this tutorial.  First we learned that `ls` can be used 
to check out what is in your current directory.  Next we learned we could `ls` 
other directories by specifying an absolute or relative filepath.

Now we are going to learn something new about `ls`. Like many commands `ls` can 
be customised with arguments.  You've already used an argument with `ls` - the 
filepath!

`ls my_data`

The structure of the command is:

`<program> <arguments>`

Note the plural!  What other arguments can you use with `ls`? There is a 
program for that! The **man**ual which you can query using `man`.

First let's try running `man` with no arguments:

`man`{{execute}}

You will see this returned:

`What manual page do you want?`

This is a sensible question - when you run `man` you should add the program 
you want to read about as an **argument**.

`man ls`{{execute}}

This will bring up a help page in front of the terminal - don't panic! In order 
to return to the command line just press `q` for **q**uit.

`q`{{execute}}