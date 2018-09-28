Let's go back to the man page for `ls`:

`man ls`{{execute}}

Let's continue reading the other sections:

What I want you to see is the `DESCRIPTION` section which says what we already 
know: 

```
DESCRIPTION
    List information about FILEs (the current directory by default)
```

There are a LOT of options here - don't feel overwhelmed if you 
don't understand what all these options do by their descriptions alone and you 
certainly don't need to remember them - that's what the man page 
(and the internet!) is for.

Let's check the description of options we have tried before: `-l` and `-h`:

```
-l      use a long listing format
```

Nothing particularly revelatory here, let's look at `-h`:

```
-h, --human-readable    with -l, print sizes in human readable format (e.g., 1K 234M 2G)
```
OK, so the description matches what we know, that file sizes are printed in 
a human readable format but it has two other interesting things:

1) This option only works when you use `-l`
2) There is an alternative way of calling this functionality: `--human-readable`

Let's test this out - let's exit the man page:

`q`{{execute}}

Now we're back on the command line:

`ls -l /home/scrapbook/tutorial`{{execute}}

Let's try running this with `-h` like we have before:

`ls -l -h /home/scrapbook/tutorial`{{execute}}

Now let's try running `-h` on it's own (without `-l`):

`ls -h /home/scrapbook/tutorial`{{execute}}

Nothing interesting happens which makes sense - there are no sizes to convert 
in this format.

Next, let's try using the more explicit way of calling `-h`

`ls -l --human-readable /home/scrapbook/tutorial`{{execute}}

It should do the same as calling `-l` and `-h`.

Something to note is the longer (more explicit) version of the argument has 
two hyphens i.e. `--human-readable` vs `-h` this is a common convention.  The 
longer versions are easier to remember but the shorter ones are quicker to 
type (and easier not to typo!) so more people use them on a day-to-day basis.  
they do the exact same thing so you should use what you are more comfortable 
with.