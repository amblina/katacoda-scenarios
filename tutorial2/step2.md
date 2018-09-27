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
`:q` and it would have the same effect.  This way of writing alternatives is 
continued down the page.

The two main sections we are going to look at are the first two sections: 
`MOVING` and `SEARCHING` in this tutorial.  

#### MOVING in less

Let's check out the first two commands given in the 
`MOVING SECTION`.  

```
e ^e j ^N CR    *   Forward one line (or N lines).
y ^y k ^K ^P    *   Backward one line (or N lines) 
```

Let's interpret these together and try them out on the ada lovelace file.  
Click `q` to **q**uit the help so we can try these commands out.

Now what do these commands do?  These commands allow you to move one line 
forward (down) or backward (up) in a file. Let's try that out:

`e`{{execute}}
`y`{{execute}}

You should see the file move forward then backward by one line.  The other 
alternatives should also work.  

How do you type `^e`?  A common convention is that 
the caret symbol or `^` signifies the `ctrl` key on your keyboard.  So `^e` 
means that you need to hold the `ctrl` button at the same time as `e` - give 
this a go.

Both commands have also been marked with `*` this is not an alternative key 
for moving forward and backward in the file. What it signifies according to 
the help file's first sentence is that the default behaviour (moving one line) 
can be altered by supplying a number before the command.


`5e`{{execute}}
`5y`{{execute}}

You should notice the file moving by 5 lines.

Using this knowledge try and look back at the help file:

`h`{{execute}}

and try out other `MOVEMENT` commands.