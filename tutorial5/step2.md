In previous tutorials we have covered the following commands:

* `cat` : print a whole file
* `head`: only print the first 10 (or custom) number of lines
* `tail`: only print the last 10 (or custom) number of lines
* `wc`: print word count / line counts to the screen

We have also covered file redirection

* `>` to redirect the result of a command to a new file
* `>>` to append the result of a command to a file
* `|` to *pipe* the result of a command to a new command

If you are unsure on these commands, please revisit tutorial 4 or check out their **man** pages!

Let's take a look at `parks.csv`

First let's see what is in our **working directory**:

`ls`{{execute}}

Next, let's take a look at `parks.csv` by printing it to the
screen using `cat`:

`cat parks.csv`{{execute}}

As we can see the first line tells us what is in each column.

```
Park Code,Park Name,State,Acres,Latitude,Longitude
```

Another name for "column" is **field**.  This row of column names (or labels)
are known as **field names**.

Challenges
==========

1. Print to screen the whole of `parks.csv`
<details>
    <summary>Answer</summary>
    `cat parks.csv`{{execute}}
</details>

2. Print to screen only the **field names** of `parks.csv`

<details>
    <summary>Hint</summary>
        Remember that the **field names** are found in the
        first line so you only want to print the first line.
</details>
<details>
    <summary>Hint 2</summary>
        Remember you can print the first X number of lines of a file
        using the `head` command.
</details>
<details>
    <summary>Hint 3</summary>
        Remember you can specify the how many lines to print
        with `head` by running it with the parameter `-n`
</details>
<details>
    <summary>Answer</summary>
        `head -n 1 parks.csv`{{execute}}
</details>

<!--
3. Print how many words there are in *fields names* of `parks.csv` -
    **Bonus** try and do it in one command!

<details>
    <summary>Hint (how to count!)</summary>
        Remember that you can find word counts using "wc"
</details>
<details>
    <summary>Hint (one command)</summary>
        Remember that you can pipe the results of one command
        into another using `|`
</details>
<details>
    <summary>Hint (how to find out how to count words)</summary>
        You can read the **man page** for `wc` by running:
        `man wc`{{execute}}
</details>
<details>
    <summary>Hint (what to use to count words)</summary>
        You can specify that you want wc to return character
        count with `-c`, lines with `-l` and words with `-w`
</details>
<details>
    <summary>Answer</summary>
        `head -n 1 parks.csv | wc -w`{{execute}}
</details>
-->


