To understand `cut` - let's go read the man page!

`man cut`{{execute}}

Right, the important sections to read are the **synopsis** which tells
you how to run the command.

```
cut OPTION... [FILE]...
```

As we have discussed before, this means that in order to run the command
you need to specify some options (and you can specify multiple options
hence the "...") and then you specify a path to a file (though this is
optional).  The optional file path indicates that if you want you can
**pipe** `|` an input file directly into the command e.g. by using `cat`.


Now these are the two options that we will look at today:

```
-d, --delimiter=DELIM
            use DELIM instead of TAB for field delimiter

-f, --fields=LIST
            select only these fields;  also print any line that contains
            no delimiter character, unless the -s option is specified
 ```

If you remember before a CSV stands for comma-**separated**-values.  This
means that each value is separated or **delimited** by a comma ','. The
`-f` option shows that you can select particular columns or 'fields'.
Unfortunately the help file isn't very helpful on *how* to specify which
fields you want but this is where this tutorial comes in!
