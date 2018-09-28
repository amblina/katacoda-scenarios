Like in tutorial 1, let's check where we are and what is in our directory;

`pwd`{{execute}}

`ls`{{execute}}

These commands should show that we are in:

`/home/scrapbook/tutorial`

And in this folder we have two files: `sample.fastq` and `small_file.txt`

These are files that we will be playing with during this 
tutorial.  The fastq file is copied from the fastq example 
[on wikipedia](https://en.wikipedia.org/wiki/FASTQ_format).

Let's read these files!  We will be using a program called `cat`. This program
con**cat**enates files and prints them onto your screen. Let's give it a go:

`cat sample.fastq`{{execute}}

You will see that the file contains 5 reads which are suspiciously similar to 
one another (with the exception of the ID line).

Now let's check out `small_file.txt`

`cat small_file.txt`{{execute}}

Let's open the man page for `cat` 
(remember you can leave the man page by typing `q`):

`man cat`{{execute}}

````
NAME         
       cat - concatenate files and print on the standard output
SYNOPSIS
       cat [OPTION]... [FILE]...
````

`q`{{execute}}

OK, so this is telling us that you can run `cat` with any number of optional 
arguments followed by any number of filepaths.  It also means you can run `cat` 
with no arguments at all!

Let's give multiple files a go - what do you think will happen?

`cat small_file.txt small_file.txt`{{execute}}

```
first line
second line
third line
fourth line
fifth line
first line
second line
third line
fourth line
fifth line
```
It just prints (or **cats**) the contents of the two files one after the other.

Now how about running cat on it's own?

`cat`{{execute}}

Hmm, nothing is going? The command isn't ending? How do we stop it?

`ctrl + c`

This will interrupt this command - what was happening? It was waiting for some 
input to cat to screen.  We will talk about this later in this tutorial so keep 
this question in your mind!

### Questions

1. Print to screen `sample.fastq` twice in one command.
<details>
    <summary>Answer</summary>
    `cat sample.fastq sample.fastq`{{execute}}
</details>








