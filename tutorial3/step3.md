OK, let's read about a command we have experience with: `ls`.

`man ls`{{execute}}

Remember the man page can be navigated using your directional keys - 
try pressing the down arrow ⇩.

First there is the `NAME` section which says what we already know:

```
NAME
    ls - list directory contents
```

Next we will take a look at `SYNOPSIS` which will say how to run `ls`:

```
SYNOPSIS
    ls [OPTION]... [FILE]...
```

This is saying that `ls` takes optional arguments (`OPTIONS`) and a filepath 
(`FILE`). 

The square brackets mean that both `OPTION` and `FILE` are both 
optional - don't need to be specified - for the command to run. We already know 
this as we have used `ls` on its own before.  

The `...` refers to the fact that you can specify 
multiple `OPTION` arguments and `FILE` arguments (as long as they are in that 
order).  We already know this too - remember when we ran `ls -l -h`?

Let's try this multiple argument thing out on command line - let's quit the 
man page:

`q`{{execute}}

Now we are on the command line again let's test what we have learnt:

We already know that we can run `ls` on its own (without options or paths) and 
that we can run it with options and a path.  These combinations are shown below.
Try running these commands and predicting what will be produced by each command.

|COMMAND|Number of OPTION(s)| Number of FILE(s)|
|-------|-------------------|------------------|
|`ls`{{execute}}|0|0|
|`ls -l`{{execute}}|1|0|
|`ls -l -h`{{execute}}|2|0|
|`ls /home/scrapbook/tutorial`{{execute}}|0|1|
|`ls -l /home/scrapbook/tutorial`{{execute}}|1|1|
|`ls -l -h /home/scrapbook/tutorial`{{execute}}|2|1|
|`ls /home/scrapbook/tutorial /home/scrapbook/`{{execute}}|0|2|
|`ls -l /home/scrapbook/tutorial /home/scrapbook/`{{execute}}|1|2|
|`ls -l -h /home/scrapbook/tutorial /home/scrapbook/`{{execute}}|2|2|