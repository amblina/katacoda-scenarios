#### Side story

So, in step 1 we tried running `cat` with no file as an argument and it just 
sat there doing nothing.  The same thing would happen if you ran `tail` and 
`head`.  What are they doing?  They're waiting for something to read! 
But from where?

Remember when we read the docs for `head` the command SYNOPSIS said that you 
run the command like this:

`head [OPTION]... [FILE]...`

Remember we discussed that `[]` means that those parts of the command are 
optional - i.e. the command won't complain if you don't have them. If we read 
the DESCRIPTION we find out why:

```
Print the first 10 lines of each FILE to standard output. 
With more than one FILE, precede each with a header giving 
the file name. With no FILE, or when FILE is -, 
read standard input.
```

So when we don't give `head` a file, it reads from standard input - how do we 
do that?

#### Pipe dreams

In the previous step we discussed two useful operators, `>` and `>>`, which can 
be used to create new files from the output of commands.  We discussed how you 
might want to do this to save the output and run new commands on the output.  

However, creating a new file every time you want to check the output of a 
command is a faff - particularly if you're not interested in saving the 
contents of a command for other purposes.

Introducing the pipe operator `|`.  Use of this operator is the bread and 
butter of bioinformatics (outside of format conversion obviously).  You can use 
the `|` operator in similar situations as the `>` operator.

Using the example we had before - checking that you have `head` 10 lines by 
using `wc -l` on your output.

Original: 
```
head numbers.txt > first_lines.txt
wc -l first_lines.txt
```

New and improved with pipe:

`head numbers.txt | wc -l`{{execute}}

These commands should get you the same answer.

#### Challenges
Try finding a one-line answer to these questions with `|`. If you 
are struggling, try and work out the individual commands you'd like to run and then 
try and convert these to only one line.

1. Find out how many characters are in the first 2 lines of `numbers.txt`
<details>
    <summary>Hint</summary>
        If you need to, check the man pages for `head` and `wc`.
</details>
<details>
    <summary>Answer</summary>
        `head -n 2 numbers.txt | wc -m`{{execute}}
</details>

2. Print the **second** 5 lines of `numbers.txt`
<details>
    <summary>Hint 1</summary>
        Can you get the first 10 lines? What if you then take the last 5 lines of that?
</details>
<details>
    <summary>Hint 2</summary>
        Check the man pages for `head` and `tail`.
</details>
<details>
    <summary>Answer</summary>
        `head -n 10 numbers.txt | tail -n 5`{{execute}}
</details>

3. Count the characters in the the second 5 lines of `numbers.txt`
<details>
    <summary>Hint</summary>
        Try combining your answers to the previous two challenges.
</details>
<details>
    <summary>Answer</summary>
        `head -n 10 numbers.txt | tail -n 5 | wc -m`{{execute}}
</details>
