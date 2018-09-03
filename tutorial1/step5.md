###THIS WILL BE ADDED TO DIFFERENT TUTORIAL

Finally let's take a deeper look at the commands we have been running.  We have
been using `ls` a lot in this tutorial.  First we learned that `ls` can be used 
to check out what is in your current directory.  Next we learned we could `ls` 
other directories by specifying an absolute or relative filepath.

Now we are going to learn something new about `ls`. Like many commands `ls` can 
be customised with arguments.  You've already used an argument with `ls` - the 
filepath!

`ls my_data`{{execute}}

The structure of the command is:

`<program> <arguments>`

Note the plural - *arguments* - what other arguments can you use with `ls`? 
There is a program for that! The **man**ual which you can query using `man`.

First let's try running `man` with no arguments:

`man`{{execute}}

You will see this returned:

`What manual page do you want?`

This is a sensible question - when you run `man` you should add the program 
you want to read about as an **argument**.

`man ls`{{execute}}

This will automatically open up a help page in the terminal - don't 
panic! In order to return to the command prompt just press `q` for **q**uit.  
The help page is opening in the **default** program for opening text files on 
this machine - a program called `less` - don't worry about this for now - 
we'll cover this in further tutorials.

Now check out the [man page](https://en.wikipedia.org/wiki/Man_page) for `ls`.
You will first see sections called `NAME`, `SYNOPSIS`, `DESCRIPTION`.  Most 
programs will have these sections filled out describing what the program is and 
how to use the software.

The man page can be navigated using your directional keys - try pressing the 
down arrow ⇩.  There are a LOT of options here - don't feel overwhelmed if you 
don't understand what all these options do by their descriptions alone and you 
certainly don't need to remember them - that's what the man page 
(and the internet!) is for.

What I want you to see is the `DESCRIPTION` section which says what we already 
know: 

`List information about FILEs (the current directory by default)`

Next we will take a look at `SYNOPSIS` which will say how to run `ls`:

`ls [OPTION]... [FILE]...`

This is saying that `ls` takes optional arguments (`OPTIONS`) and a filepath 
(`FILE`).  It is saying that any `OPTION` needs to be specified before the 
filepath.  The square brackets mean that both `OPTION` and `FILE` are both 
optional (don't need to be specified).  We already know this as we have used 
`ls` on it's own before.  The `...` refers to the fact that you can specify 
multiple `OPTION` arguments and `FILE` arguments (as long as they are in that 
option)

OK, we are going to try running `ls` again but with the optional argument `-l` 
from the man page:

`-l      use a long listing format`

Let's exit the man page:

`q`{execute}

Now we're back on the command line:

`ls -l`{execute}

This should return your results in a different format.  Now try running it 
with a filepath - remember filepath MUST go after OPTIONS.

`ls -l /home/scrapbook/tutorial`{execute}

If you remember from the man page we should be able to add multiple paths to 
this.

`ls -l /home/scrapbook/tutorial /home/scrapbook/`{execute}

What happens if we give the same path argument twice?

`ls -l /home/scrapbook /home/scrapbook`{execute}


