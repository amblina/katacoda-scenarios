The command line is case sensitive, so always type commands exactly as given. 
For more complex commands spaces are important as well.

A <strong>prompt</strong> will be displayed in the terminal window on 
the right.

Prompts will look slightly different on different systems but for this 
tutorial this will be:

`>` or `$`

To instruct your terminal to do something, you need to enter specific commands 
and press enter.  Let's try running the ``pwd`` command!
 
 ``pwd`` stands for: 
 
 **p**resent **w**orking **d**irectory
 
This will tell you where you are in the filesystem.

`pwd`{{copy}}

You should see this output:

`/home/scrapbook/tutorial`

### Don't panic!

Don't worry about running any commands in this environment - you can't break 
anything here!

Let's try running a command that doesn't exist:

`hello`{{execute}}

You should get the following message telling you what you already know:

`bash: hello: command not found`

This error message is telling you **what** is complaining and **why**.  Error 
messages happen all the time and are not necessarily a bad thing. Some are 
helpful and descriptive and can tell you what you need to do instead.

The error message is telling you that `bash` (the command line interpreter - 
the software that executes your commands) has an issue with the command `hello` 
that you entered and that that issue is that it doesn't know what to do with 
the instruction `hello` as that command doesn't exist.


### Task

1) Find out which directory (folder) you are in currently: 


You should see the following output:
`/home/scrapbook/tutorial`

