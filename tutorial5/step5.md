Understanding how to filter which columns we see or how many rows is very useful.  
However, what is often even more useful is the ability to only pull out lines from a
 table that contain a certain value.
 
In this tutorial we will be learning how to use **`grep`**. This stands for "Global 
Regular Expression and Print". You will literally never need to know that it stands for 
that - I looked it up to double check!  The important this to understand is that the 
`grep` tool will print out any line in a file that contains a particular pattern of characters 
just like using `Ctrl+F` or `Cmd+F`!

Usage:

`grep <search term> <file path>`

Now let's do a similar search on our table `parks.csv`.  Let's take a look at all 
the records that have "Canyon" in their name:

`grep 'Canyon' parks.csv`{{execute}}

You should see 5 records now!

What happens when you change "Canyon" to "canyon"?

`grep "canyon" parks.csv`{{execute}}

You won't see any lines printed. This is because "canyon" does not appear in the file where as
"Canyon" does.  `grep` is very particular about looking for *exactly* what you ask for! We call 
this kind of tool *case-sensitive* which means that the capitalisation matters to the program.

`grep` is an extremely powerful with lots of different options but for now let's concentrate on using 
it to search for simple words in the table!

###Challenges

1. Find all the national parks in Utah, USA from the `parks.csv` table
<details>
    <summary>Hint</summary>
        Utah's code in the table is "UT"
</details>
<details>
    <summary>Answer</summary>
        `grep 'UT' parks.csv`{{execute}}
</details>

2. Find the number of records in the national parks table in Utah (in one command!)
<details>
    <summary>How do you count how many lines there are?</summary>
        `wc -l` will count how many lines there are.
</details>
<details>
    <summary>How do you *pipe* the output of one command into the next command?</summary>
        You use pipe i.e. the `|` symbol e.g. `head parks.csv | wc -l` will run the 
        `wc` command on the output of the `head` command.
</details>
<details>
    <summary>Answer</summary>
        `grep 'UT' parks.csv | wc -l`{{execute}}
</details>
