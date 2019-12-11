The vast majority of software comes with a **man page** - a manual to explain
how to run the software.

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

This will automatically open up a help page in the terminal for `pwd`. 
The help page is opening in the **default** program for opening text 
files on this machine, a program called `less` - something we covered in 
tutorial 2. Remember, in order to return to the command prompt just press 
`q` for **q**uit.

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

##### Note:
**Don't worry** about understanding everything in this manual - how many times do 
you read an entire manual?  It's more important to 
work out *how* to read the manual than remember what you're reading.  
The manual is for reference, you can check back whenever you need it - you 
don't need to store the whole thing in your head.  

The manual is for everyone from people just 
starting out through to seasoned professionals so not everything in the 
manual makes sense until you need it and that's ok.  
