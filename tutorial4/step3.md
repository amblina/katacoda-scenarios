So we've been looking at some useful commands for reading files: `head`, `tail` 
and `cat`.  We've looked up the manpage for each of these commands using the 
`man` command. We have then worked together to find out what each command does 
and how to use it using the manual.  Now let's try out a new command in the 
same way:

Another useful utility is `wc`. Let's take a look at the man page:

``man wc``{{execute}}

This is what you should see:

```
 Name
    wc - print newline, word, and byte counts for each file
Synopsis
    wc [OPTION]... [FILE]...
    wc [OPTION]... --files0-from=F
Description
    Print newline, word, and byte counts for each FILE, and a total line if 
    more than one FILE is specified. With no FILE, or when FILE is -, 
    read standard input.
     -c, --bytes
        print the byte counts
    -m, --chars
        print the character counts
    -l, --lines
        print the newline counts
    --files0-from=F
        read input from the files specified by NUL-terminated names in file F; 
        If F is - then read names from standard input
    -L, --max-line-length
        print the length of the longest line
    -w, --words
        print the word counts
    --help
        display this help and exit
    --version
        output version information and exit
```

Try running this command on ``numbers.txt``. What does the output look like?

Now try reading the man page and trying out the challenges below:


#### Challenges

<ol>
    <li> 
        Run `wc` on `numbers.txt` to identify the number of lines in the file.
        <details>
            <summary>Hint</summary>
                Take a look at the manpage for wc again, look at the `-l` argument
        </details>
        <details>
            <summary>Answer</summary>
                `wc -l numbers.txt`{{execute}}
        </details>
    </li>
    <li>
        2. Run `wc` on `numbers.txt` to identify the length of the longest number.
        <details>
            <summary>Hint</summary>
                Take a look at the manpage for wc again, look at the `-L` argument
        </details>
        <details>
            <summary>Answer</summary>
                `wc -L numbers.txt`{{execute}}
        </details>
    </li>
    <li>
        3. Run `wc` on `numbers.txt` to identify the number of full numbers in the file.
        <details>
            <summary>Hint</summary>
                Take a look at the manpage for wc again, look at the `-w` argument
        </details>
        <details>
            <summary>Answer</summary>
                `wc -w numbers.txt`{{execute}}
        </details>
    </li>
    <li>
        4. Run `wc` on `numbers.txt` to identify the number of characters in the files.
        <details>
            <summary>Hint</summary>
                Take a look at the manpage for wc again, look at the `-m` argument
        </details>
        <details>
            <summary>Answer</summary>
                `wc -m numbers.txt`{{execute}}
        </details>
    </li>
 </ol>