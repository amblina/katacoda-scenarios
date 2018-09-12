OK, so now you feel alright using `cat`, `head`, `tail` and `wc`.  
The commands read a various parts of a file and print the result to your screen.

But how do you save the output of a command to a new file? This is useful if 
you want to run multiple commands e.g. if you want to run `wc -l` on the first 
500 lines of `numbers.txt`.

You can **redirect** the output of a command to a file using the `>` operator.
Think of it like an arrow pointing where your output will be going.  Let's run 
a command we are comfortable with:

`head numbers.txt`{{execute}}

Now let's try running this so the output goes into a new file called 
`first_lines.txt`.

`head numbers.txt > first_lines.txt`{{execute}}

Now let's list the contents of the directory we are in (remember `ls`)?  You 
should see a new file called `first_lines.txt`. Now you can run `wc` on this 
file to check the number of lines!

`wc first_lines.txt`{{execute}}

Now if we run the command again, do you think the file will be replaced or do 
you think that the command will **append** the output to the file?

`head -n 20 numbers.txt > first_lines.txt`{{execute}}

`wc first_lines.txt`{{execute}}

The file should have 20 lines - so the file has been replaced. This is 
something to bear in mind when you're redirecting files!

But what about if we want to **append** I hear you ask! Luckily shell has an 
operator for that too: `>>`.

Let's repeat what we did before:

```
head numbers.txt > first_lines.txt
head -n 20 numbers.txt >> first_lines.txt
wc first_lines.txt
```

#### Challenges

1. Create a file that contains the first 2 lines of `numbers.txt`.

2. Create a file that contains the first 10 lines of `numbers.txt` 5 times.

3. Create a file that contains teh first 10 lines and last 10 lines 
of `numbers.txt`