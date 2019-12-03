In the previous tutorial we covered how to open a file in `less` along with 
how to move through the file and search for particular words.  We were able to
find out how to use `less` by using the help that was packaged with the software.

Help is packaged up with almost all commands - you just need to 
find out where and how to read it.  This is what this tutorial will be covering.

This tutorial will be covering what to do when you're faced with unfamiliar 
commands.  First though, let's review what we've learned from the commands 
we've already tried.  

**Note:**
> Anywhere I write  something in angle brackets (`< >`) e.g. 
 `<something>` is a placeholder for something the user would add themselves e.g.
 if I were telling you how to run `mkdir` I might write:
>   
>   
> ```mkdir <path>```  
>
>   
> to indicate that you need to add a filepath after the `mkdir` command.  
What you put instead of the angle brackets depends on 
what you want to achieve e.g. what you want to name your directory (`mkdir`) or
which directory you wish to move to with `cd`.

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
anything you can type - numbers, letters, paths, etc - and customise the command 
you are running.  There are multiple ways of specifying arguments and some need 
to be entered with a specific structure but how do you work out what options 
are available for what program? How do you know what types of argument are 
allowed? What defaults does the software use?

Read the **man**ual A.K.A the 
[man page](https://en.wikipedia.org/wiki/Man_page)!

