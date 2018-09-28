In the previous tutorial we covered `less` how to scroll up and down a file 
openned in `less`.  One thing we talked about was that help is packaged up with
almost all commands - you just need to find out where and how to read it.  This 
is what this tutorial will be covering.

This tutorial will be covering what to do when you're faced with unfamiliar 
commands.  First though, let's review what we've learned from the commands 
we've already tried.  Like before, anywhere I write `<something>` what I'm 
saying is that part of the command depends on what you want to achieve e.g. 
which directory you wish to move to (`cd`) or what you want to name your 
directory (`mkdir`).

|Command|What it does|
|-----|------|
|`pwd`| prints working directory|
|`ls`| lists what is saved in your working directory (files and directories)|
|`ls <path> `| lists what is saved in "path" (files and directories)|
|`ls -l <path>`| lists (in detail) what is saved in "path" (files and directories)|
|`ls -l -h <path>`| lists (in detail) what is saved in "path" (files and directories) with human-readable units|
|`mkdir <path>` | makes a directory at "path"|
|`cd <path> `| changes your working directory to "path"|
|`less <path>` | opens the file "path" for reading|

What you might have noticed is that these follow a similar structure:

```
<command>
```
or
```
<command> <arguments / options>
```

Some commands have arguments and some don't.  Arguments and options can be 
anything you can type - numbers, letters, paths etc and customise the command 
you are running.  There are multiple ways of specifying arguments and some need 
to be entered with a specific structure but how do you work out what options 
are available for what program? How do you know what types of argument are 
allowed? What defaults does the software use?

Read the **man**ual A.K.A the 
[man page](https://en.wikipedia.org/wiki/Man_page)!

