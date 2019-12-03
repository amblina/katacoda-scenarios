First we will be running this command to create a long and boring file:

`seq 0 1000000 > /home/scrapbook/tutorial/numbers.txt`{{execute}}

Don't worry about this command for now - we'll come back to it later. 
Suffice to say that a file is created called `numbers.txt` which contains 
the numbers 0 to 1000000, one number per line.

Let's read this file!

`cat numbers.txt`{{execute}}

OK, that took a little while to print the whole file to screen.

**Question:** What if we wanted to stop it running half way through?

<details>
    <summary>Answer</summary>
        Use `ctrl + c`.
</details>


Try that out so that you know you can do it. Don't panic if it doesn't stop 
right away - it's just finishing up catting the of the part the file it was on 
before it was interrupted.

OK, so you have a large file - what if you were only interested in the first few 
lines?  This is particularly useful in bioinformatics if you want to only want 
to analyse the first 100 reads or if you want to check the format of the file 
before you do something with it.


### The `head` command

We can check the top of the file using `head` another inbuilt command that lets 
you cat a certain number of lines from a file.  Like before, let's check the 
**man page** (remember you can exit the man page by typing q).

`man head`{{execute}}

```shell
Name
    head - output the first part of files
Synopsis
    head [OPTION]... [FILE]...
Description
    Print the first 10 lines of each FILE to standard output.
    ...
    -n, --lines=[-]K
        print the first K lines instead of the first 10; with the leading '-', 
        print all but the last K lines of each file
    ...
```

OK, so what this man page is telling us is that we can use the command by 
writing the command name `head` followed by options and then filename(s). By 
default the number of lines that are printed to the screen is 10.  This can be 
changed using the `-n` command.  Let's give it a go! Have a think before 
running the command - what do you think should happen?

`head numbers.txt`{{execute}}

Brill, so what we see is the first 10 lines (0-9) of the file being printed.  

Let's try using that `-n` option.  If you want to a reminder from the man page, 
just call up the documentation again with the `man` command.
 
`head -n 5 numbers.txt`{{execute}}

So this will print the first 5 lines because the `-n` parameter **overrides** 
the default number of lines to print, 10.

### The `tail` command

OK, so now you're happy with reading the top `n` lines of a file - how do you 
read the last `n` lines of a file? What's the opposite of `head`? `tail`!

Just like with `head` let's check out the **man**page for `tail`.  What we see 
is similar to `head`.

```shell
Name
    tail - output the last part of files
Synopsis
    tail [OPTION]... [FILE]...
Description
    Print the last 10 lines of each FILE to standard output.
    ...
    -n, --lines=K
        output the last K lines, instead of the last 10; or use -n +K to output 
        lines starting with the Kth
    ...
```
Just like `head` the default number of lines output by `tail` is 10.  Let's 
give that a go:

`tail numbers.txt`{{execute}}

What about finding the last 5 lines?

`tail -n 5 numbers.txt`{{execute}}

Excellent!

#### Questions
1. How do you print the first line of the `numbers.txt` file?
<details>
    <summary>Answer</summary>
        `head -n 1 numbers.txt`{{execute}}
</details>

2. How do you print the last line of the `numbers.txt` file?
<details>
    <summary>Answer</summary>
        `tail -n 1 numbers.txt`{{execute}}
</details>

3. If you wanted to print out the first record in `sample.fastq` how would you 
do that?
<details>
    <summary>Hint</summary>
        Remember that fastq have 4 lines per record, so you'll need to 
        grab the first 4 lines using `head`.
</details>
<details>
    <summary>Answer</summary>
        `head -n 4 sample.fastq`{{execute}}
</details>
