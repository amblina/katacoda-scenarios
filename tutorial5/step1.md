First of all let's talk about what we mean by A CSV. CSV files (or
'comma-separated-value' files) are a **file format** that can be
used to store a table.

A **file format** is a way of describing the way that a file is
structured.  The format of a file is often (but not always!)
indicated by a **file extension** e.g. for an MS Word Document the file name ends with
`.docx` e.g. `my_story.docx`

It's useful to know the format of a file because then you'll
have an idea of what you can do with it, how to open and view
its contents or how to edit the file.

A **CSV** is often stored in a file with the file extension
`.csv`. They are used to store the tables, each column in the
table is separated by a comma.  The first line often has
the labels for each of the columns.

Example table:

|Name|Age|
|:----|---:|
|Jenny|12|
|Tom|12|
|Jason|13|

Example table as a csv:

```
Name,Age
Jenny,12
Tom,12
Jason,13
```

In this tutorial we are going to look at how to:
* read a csv
* subset a csv (only look at the first X lines)
* filter a csv by only showing particular columns
* filter a csv for a particular value
