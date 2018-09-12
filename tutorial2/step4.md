OK, so now you feel alright using `cat`, `head` and `tail`.  The commands read 
a various parts of a file and print it to your screen.  What if you wanted to 
save that output?  What if you had a burning need to save the first 10 lines of 
`numbers.txt` in order to do something useful with it?  This is what this step 
will be covering.


####STDOUT
In the documentation for all three 
commands, the structure of the command was:

`<command> [options] [files]`

We learnt in the previous scenario that `[]` indicates that an argument is 
optional.  But if we run `head` on it's own with no parameters what happens?