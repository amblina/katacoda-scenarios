Next, let's consider how to filter the csv by field (or column).
The csv has the following **field names**:

|Park Code|Park Name|State|Acres|Latitude|Longitude|
|---------|---------|-----|-----|--------|---------|

This csv hasn't got a huge number of columns but imagine if you
only want to know the park name and the state the park was in:

|Park Name|State|
|---------|-----|

This is where the `cut` comes in! The `cut` command allows you
to split each line in a file by a particular character creating columns
and then letting you select which columns you wish to show.

This is how to use the `cut` command:

`cut --d <delimiter> -f <column number(s)> <path>`

A **delimiter** is another word for **separator**. As we have discussed
before, CSV stands for **c**omma-**s**eparated-**v**alues.  So the
delimter in a CSV is a comma!  The `-f` allows you to specify the column
number e.g `-f 1` will give you the first column and `-f 2` will give you
the second!

What do you think this command will produce?

`cut -d ',' -f 1 parks.csv`{{execute}}

<details>
    <summary>Answer</summary>
        The first column
</details>

What about this command?

`cut -d ',' -f 2 parks.csv`{{execute}}

<details>
    <summary>Answer</summary>
        The second column
</details>

You can also specify a range of columns!

`cut -d ',' -f 1-3 parks.csv`{{execute}}

<details>
    <summary>Answer</summary>
        The first to third column e.g. 1,2,3
</details>

Or a list of columns!

`cut -d ',' -f 1,3 parks.csv`{{execute}}

<details>
    <summary>Answer</summary>
        The first and third column e.g. 1 and 3
</details>




