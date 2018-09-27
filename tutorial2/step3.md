Ok, so we have a rough grasp on `MOVING` through the file, let's try 
`SEARCHING`.

We are only going to cover basic searching right now i.e. how to use something 
similar to "Find in page" on your web browser (`CMD + f` or `ctrl + f`).

Re-open ada-lovelace file:

``less ada_lovelace_bio.txt``{{execute}}`

Let's open the help page again:

`h`{{execute}}

Let's scroll to the `SEARCHING` section and pick out a couple of commands and 
learn their usage together.

```
/pattern          *  Search forward for (N-th) matching line.
ESC-u                Undo (toggle) search highlighting.
```

Quit the help page so that you're looking at the Ada Lovelace biography file 
again.

The first command says that it'll look at all future lines in the file for a 
particular pattern - this pattern can be a word:

`/Ada`{{execute}}

You should see all mentions of "Ada" are now highlighted in the file and you 
can page through the file as normal.  If you wish to search for something else 
you can just type `/` followed by your search term:

`/Legacy`{{execute}}

This should take you to the bottom of the file.  Now let's search for "born":

`/born`{{execute}}

You will get an error message:

`Pattern not found (press RETURN)`

If you now scroll upwards to the top of the page you will see that 'born' has 
been highlighted at the top of the document - you got the error message 
because there were no mentions of "born" after the point in the file you were.  
As the description says - you are searching forward for a matching line.

Now, if we search for "Ada" again and fill the terminal up with highlights:

`/Ada`{{execute}}

these can be removed by using `ESC-u` - pressing the `ESC` key on your keyboard 
and `u` key at the same time.