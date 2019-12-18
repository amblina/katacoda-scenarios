So in the previous step we discussed that `cut` could be used to display
only certain columns of a CSV.

Original field names:

|Park Code|Park Name|State|Acres|Latitude|Longitude|
|---------|---------|-----|-----|--------|---------|

We will start by only displaying the first column:

`cut -d ',' -f 1 parks.csv`{{execute}}

This command is saying you will be using `cut` to split up each line in
the file by ',' and then only showing the first field.

How do you think you would display the second column?

<details>
    <summary>Answer</summary>
        `cut -d ',' -f 2 parks.csv`{{execute}}
</details>

This is because `-f` can be used to specify the column number you wish
to view!

What do you think will happen if you run the following?


1. `cut -f ',' -f 3 parks.csv`{{execute}}
2. `cut -f ',' -f 1-3 parks.csv`{{execute}}
3. `cut -f ',' -f 1,3 parks.csv`{{execute}}

The `-f` argument takes the field number (1 for the first field,
2 for the second etc.) and displays that field.  You can select a range
e.g. `1-4` will print out the 1,2,3 and 4 field. (Park Code to Acres).
You can also give a list of columns e.g. 1,3 will display the first and
third column (Park Code and State).

Here are some challenges to test your knowledge!

Challenges
==========
1. How would you display only the third column?
<details>
    <summary>Hint</summary>
        Take a look at the examples above!
</details>
<details>
    <summary>Answer</summary>
        `cut -d ',' -f 3 parks.csv`{{execute}}
</details>
2. How would you display the second and fourth columns?
<details>
    <summary>Hint</summary>
        Take a look at the examples above!
</details>
<details>
    <summary>Answer</summary>
        `cut -d ',' -f 2,4 parks.csv`{{execute}}
</details>
3. How would you display the Park Name and Acres of the first three
    records in the table in one command?
<details>
    <summary>Hint (what is a record)</summary>
        A record is a row in the table that contains data
        (not the field names)
</details>
<details>
    <summary>Hint (how do I get the first X records of a table?)</summary>
        Remember `head` can be used to give you the first few
        lines of a file
</details>
<details>
    <summary>Hint</summary>
        Remember `|` can be used to **pipe** the results of one
        command into another.
</details>
<details>
    <summary>Answer</summary>
        `cut -d ',' -f 2,4 parks.csv | head -n 4`{{execute}}
        `head -n 4 parks.csv | cut -d ',' -f 2,4`{{execute}}
</details>