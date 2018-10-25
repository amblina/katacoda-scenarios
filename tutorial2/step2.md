Let's do something more interesting with less!  You already know how to open, 
close and scroll through a file. Let's check out what else we can do with less.

First, let's open the same file again:

`less ada_lovelace_bio.txt`{{execute}}

Remember you can **q**uit this file anytime using `q`{{execute}}

Ok, now you're in the file type:

``h``{{execute}}

Like almost everything in unix, this software comes with help - you just need 
to know how to access it and work out how to interpret it - this is something 
you will gain a feel for over time.

The first thing the help file explains is how to read the help - we'll touch on 
that in a minute.  

First, note that it says that `h` brings up the help message 
and `q` causes `less` to exit.  Along with `q` and `h` are a bunch of other 
symbols. These are just alternatives.  So instead of using `q` you can type 
`:q` (typing `:` then `q`) and it would have the same effect.  
This way of writing alternatives is continued down the page.

The two main sections we are going to look at are the first two sections: 
`MOVING` and `SEARCHING` in this tutorial.  

#### MOVING in less

Let's check out the first two commands given in the 
`MOVING SECTION` along with the help intro.  

```
            SUMMARY OF LESS COMMANDS
            
Commands marked with * may be preceded by a number, N.
Notes in parentheses indicate the behaviour if N is given.
A key preceded by a caret indicates the Ctrl key; thus ^K is ctrl-K.

--------

                    MOVING

e ^E j ^N CR    *   Forward one line (or N lines).
y ^Y k ^K ^P    *   Backward one line (or N lines)
f ^F ^V SPACE   *   Forward one window (or N lines)
b ^B ESC-V      *   Backward on window (or N lines)
```

Let's interpret these together and try them out on the ada lovelace file.  
Click `q` to **q**uit the help so we can try these commands out.

Now what do these commands do?  These commands allow you to move one line 
forward (down) or backward (up) in a file. Let's try that out:

`e`{{execute}}
`y`{{execute}}

You should see the file move forward then backward by one line.  The other 
alternatives should also work for example '^E'.  

**Remember** according to the 
beginning of the help file '^' stands for the `ctrl` key. So to move forward 
one line you would need press `ctrl` and the `E` key on your keyboard at the 
same time.  This can also be written as: `ctrl+e`, `ctrl+E`, 
`ctrl-e` or `ctrl-E`.

Both commands have also been marked with `*`, this is not an alternative key 
for moving forward and backward in the file. This was described in the 
first part of the help:

```
            SUMMARY OF LESS COMMANDS
            
Commands marked with * may be preceded by a number, N.
```
Commands marked with the star can be changed from their default behaviour by 
typing a number (N) before typing the command e.g. typing `5` THEN `e`.  The 
 default behaviour of `e` is to move forward one line - adding a number just 
 increases how many lines you're moving forward in the file:
 
```
e ^E j ^N CR    *   Forward one line (or N lines).
```

`5e`{{execute}}
`5y`{{execute}}

You should notice the file moving by 5 lines each time rather than 1.

Using this knowledge try and look back at the help file:

`h`{{execute}}

and try out other `MOVEMENT` commands.

________
**Tasks**

Try out the following commands:

```
f ^F ^V SPACE   *   Forward one window (or N lines)
b ^B ESC-V      *   Backward on window (or N lines)
```

so:

`f`{{execute}} to move forward one screen (or page)
`b`{{execute}} to move backwards one screen (or page)

