An important aspect of finding and reading help files on command line are 
conventions. These can be contradictary and sometimes unintuitive when you first
start out. However, with time they'll become second nature.

At the start of this tutorial I described the convention I was going to use: 
angle brackets (`<` and `>`).  
When I first started learning programming and command line I 
was totally foxed by this exact convention! In fact - I added the 
angle brackets when trying out a new command e.g.

The instructions I was following said:

`ls <path>`

and I wrote:

`ls <my_folder>`{{execute}}

and got this super helpful error message I didn't know what to do with:

``bash: syntax error near unexpected token `newline` ``

But now that I know what they mean by it - the convention is something I don't 
think about any longer and is very helpful when talking about new commands!

This particular error message is something you'll hit often - this error 
message translated into human is:

The command line interpreter, `bash`, didn't know what to do with this command 
 as it found a weird character or a character in a weird place.  In this example, 
 it was because I used a `>` at the end of the command and `>` has a special 
 function which we'll be covering in the next tutorial.
 
 Examples of conventions we came across in this tutorial include:
 
 CONVENTION | MEANING | EXAMPLE
 -----------|---------|---------
 Square brackets `[]`| Optional: An argument can be used or left out| `ls [PATH]`
 Elipsis ...`|One of more arguments can be added| `mkdir PATH...`
 All caps| Using capital letters to indicate placeholders | `mkdir PATH`
 angle brackets `<>`| Indicate placeholders | `mkdir <PATH>`
 
 These are just some examples - as you can see from the table, these 
 conventions can be combined or contradict each other but with experience
 (and in context) you will work these out without an issue.
 
 ______
 
 ### Tasks
 
 What can you tell me about this totally made up command given this help info?
 
 
```
NAME
    greeting - greet the user

SYNOPSIS
    greeting [OPTION] [NAME]...
    
DESCRIPTION
    Print to screen a friendly message saying hello or goodbye to NAME(s) 
    (--hello by default).
    
    -h --hello     print welcome message (cannot be used with -g)
    -g --goodbye   print goodbye message (cannot be used with -h)
    
AUTHOR
    Somebody 
```
1) Do you think this command will let you greet multiple names?
    <details>
        <summary>Hint</summary>
            Have a think about the meaning of `[NAME]...`
    </details>
    <details>
        <summary>Answer</summary>
            Yes - the elipsis after NAME suggests you can.
    </details>
2) Do you think this command will work given no name?
    <details>
        <summary>Hint</summary>
            Have a think about the meaning of `[NAME]...`
    </details>
    <details>
        <summary>Answer</summary>
            Yes, because NAME is given in square brackets.
    </details>
2) What do you think would happen if you ran `greeting -g -h Tom`
    <details>
        <summary>Hint</summary>
            Have a look at the descriptions of `-h` and `-g`
    </details>
    <details>
        <summary>Answer</summary>
            The program will likely display an error instead of greeting anyone.
    </details>

 
