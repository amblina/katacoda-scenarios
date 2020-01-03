#### What happens if you choose an option that doesn't exist?

Before we finish up let's find out what will happen if you execute a command 
 on the command line with an option that doesn't exist.  Try the following:

`ls -e`{{execute}}

You should get the following error message:

```
ls: invalid option -- 'e'
Try 'ls --help' for more information.
```

Let's try another:

`ls --mystery`{{execute}}

You should get the following error message:

```
ls: unrecognized option '--mystery'
Try 'ls --help' for more information
```

There is a pattern here - try out your own silly parameter!

What this also highlights is another common convention for finding out how a 
program works: the `--help` argument.

**Note:** There is not always a `--help` option but lots of helpful developers 
have added them.

`ls --help`{{execute}}

This should print out:

```
Usage: ls [OPTION]... [FILE]...
List information about the FILEs (the current directory by default).
Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.
...
 -h, --human-readable       with -l, print sizes in human readable format
                               (e.g., 1K 234M 2G)
...
 -l                         use a long listing format
...
```

It is a shorter version of the man page and it just prints it to screen which 
can be very convenient.  Help text can be pretty comprehensive like it is here 
but it can just contain simple usage instructions.

Almost all software installed on your machine will have a `man page`.  However,
if there is no manual for a command line tool, using the `--help` option will
often display some help info.

While we are trying out wacky commands, try running the `man` command for a 
piece of software that doesn't exist:

`man mystery-software`{{execute}}

```
No manual entry for mystery-software
```

That's a pretty straight-forward error message, but note that - like all command line 
instructions - it does **literally** what you ask.  Say you wanted to find out 
about `ls` but you accidentally type `sl` instead you will get a message like 
this:

```
No manual entry for sl
```

But it won't be answering the question you were **actually** asking so always 
check your spelling if you can't find a manual!
