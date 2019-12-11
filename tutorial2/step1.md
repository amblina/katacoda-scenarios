We are going to learn how to open and read the contents of files.  
We will be doing that in this tutorial using `less`, a **terminal pager 
program**.  It is used primarily to read the contents of a file one screen 
(or page) at a time.  `less` is installed on most computers, so is almost
always available to use.

Just like before, let's try and run `less` on it's own:

`less`{{execute}}

You should see the following error message:

`Missing filename ("less --help" for help)`

We could find out how to run less by running it with `--help` but let's just 
try following the suggestion of adding a filename.

**Hint:** If you don't want to type out a filepath, you can tap tab to 
complete the command. Just type `less ada_l` and then click tab (Tab ↹) this 
should auto-complete the filename.  We will touch on this in more detail 
another time.

`less ada_lovelace_bio.txt`{{execute}}

This will do something different to the terminal than you've experienced 
before. You can use the directional arrow on your keyboard ⇩ to scroll 
downwards through the file. Tap the ⇩ arrow until you reach the end of the 
file.  You will be able to see you've reached the end when you see at the 
bottom of the screen:
 
 `(END)`
 
You can also use the ⇧ to scroll up through the file.

When you feel comfortable scrolling up and down use 


`q`{{execute}}

to **q**uit the program - you will see that you are back on the command line 
again.
