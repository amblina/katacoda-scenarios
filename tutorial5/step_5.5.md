Some cool parameters that can be useful when using `cut` or `grep`.  These are just
an extension on the previous exercises in case you want to go a little further.  

###`cut` extensions
When you run cut you can get cut to print out your new table with a different 
 delimiter  e.g. if you want to see the first two columns of `parks.csv` but separated with a ;
you can do that easily with this tool by using the `--output-delimiter` paramter:

* Output your new table with a different delimiter:
    * `cut -d ',' -f 1-3 --output-delimiter ';'`{{execute}}
    * `cut -d ',' -f 1-3 --output-delimiter ' HELLO!!!! '`{{execute}}

### Some `grep` extensions:
The `grep` tool can take as a search term a word (like we have used in the tutorial) 
or simply any pattern e.g. "National Park" or just "Nat".  This search term is called 
a "pattern".  

#####Regular expressions

**Regular expressions** are a specific way of writing out search patterns. 
You don't need to understand regular expressions right now but some of the conventions 
are very useful!

* Search only the beginning of a line with `^` symbol:
    * To find every line that contains a capital B: `grep 'B' parks.csv`{{execute}}
    * To find every line that *starts* with a capital B: `grep '^B' parks.csv`{{execute}}

* Search only at the end of a line with the `$` symbol:
    * To find every line that contains '93': `grep '93' parks.csv`{{execute}}
    * To find every line that *ends* with '93': `grep '93$' parks.csv`{{execute}}

#####Other grep parameters

* Reverse searching with `-v`:
    * Find every line that contains a capital B: `grep 'B' parks.csv`{{execute}}
    * Find every line that *doesn't* contain a capital B: `grep -v 'B' parks.csv`{{execute}}
    * Find every lines that *doesn't* start with a capital B: `grep -v '^B' parks.csv`{{execute}}.
    
* Only return lines that contain a whole word that you've searched:
    * Find all instances of the word "Canyon": `grep "Canyon" parks.csv`{{execute}}
        * This will return 5 results - 4 Canyons and one Canyonlands
    * Find all instances of the whole word "Canyon": `grep -w "Canyon" parks.csv`{{execute}}
        * This will return 4 results - no more Canyonlands, only Canyon.