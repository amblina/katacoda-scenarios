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

```bash
Print the first 10 lines of each FILE to standard output. 
With more than one FILE, precede each with a header giving 
the file name. With no FILE, or when FILE is -, 
read standard input.
```

So when we don't give `head` a file, it reads from standard input - how do we 
do that?

#### Pipe dreams

In the previous step we discussed two useful operators: `>` and `>>` which can 
be used to create new files from the output of commands.  We discussed how you 
might want to do this to save the output and run new commands on the output.  

However, creating a new file everytime you want to check the output of a 
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
Try finding the answers to these questions with one command with `|`. If you 
are struggling try and work out individual commands you'd like to run and then 
try and convert these to only one line.

1. Find out how many characters are in the first 2 lines of `numbers.txt`
<details>
    <summary>Hint</summary>
        If you need to check the manpage for `head` and `wc`.
</details>
<details>
    <summary>Answer</summary>
        `wc -l numbers.txt`{{execute}}
</details>
