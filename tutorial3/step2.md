In the previous tutorial we covered `less` how to scroll up and down a file 
openned in `less`.  One thing we talked about was that help is packaged up with
almost all commands - you just need to find out where and how to read it.  This 
is what this tutorial will be covering.

The vast majority of software packaged with unix and unix-like operating 
systems come with a **man page** - a manual to explain how to run the software.

This manual can be accessed by running `man`.

First let's try running `man` with no arguments:

`man`{{execute}}

You will see this returned:

`What manual page do you want?`

This is a sensible question - when you run `man` you should add the program 
you want to read about as an **argument**.

Let's try and find out about the first command that we ran: `pwd` which we 
know that when run, **p**rints the **w**orking **d**irectory - a.k.a prints to 
the screen where we currently are in the filesystem.

`man pwd`{{execute}}

This opens the manual page for `pwd` using `less` - the default program for 
reading files on this system.

The manual page is broken up into sections - these sections are:


|Section| What it tells you|
|--------------|------------------|
|NAME|What the software is called and briefly what it does|
|SYNOPSIS|How, in general, to run the software|
|DESCRIPTION|More detail, tell you what options you can run and what they do.|
|AUTHOR|Who wrote the software|
|REPORTING BUGS| Ways of reporting bugs|
|COPYRIGHT| Who owns the software / license info|
|SEE ALSO| Related software you may want to investigate|


The sections we'll be concentrating on are the first three in this tutorial.