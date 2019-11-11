Let's try learning more about a command we have been using a lot: `ls`.

First we learned that `ls` can be used 
to check out what is in your current directory.  Next we learned we could `ls` 
other directories by specifying an absolute or relative filepath to that 
directory.

Now we are going to learn something new about `ls`. Like many commands `ls` can 
be customised with arguments.  You've already used an argument with `ls` - the 
filepath!

`ls /home/scrapbook/tutorial`{{execute}}

You can also run `ls` like this:

`ls -l /home/scrapbook/tutorial`{{execute}}

This also gives you a list of items in `/home/scrapbook/tutorial` but in a 
different **l**onger format. This format tells you what permissions are on the 
files (the drwxr-xr-x part), ownership of the file, the size of the files, 
when it was created and lastly the filename.  

```
$ ls -l
total 20
-rw-r--r-- 1 root root      4913 Sep 28 13:44 ada_lovelace_bio.txt
drwxr-xr-x 2 root scrapbook 4096 Sep  3 21:03 docker
-rw-r--r-- 1 root root       681 Sep 28 13:44 sample.fastq
-rw-r--r-- 1 root root        57 Sep 28 13:44 small_file.txt
```

The `-` is a common convention with command line 
programs for specifying an option.  Another option you can run is `-h` which 
stands for **h**uman readable.  This can be run like in addition of `-l`:


`ls -l -h`{{execute}}

As you can see the output has changed again, this time converting the filesize 
which was previously in bytes into "human-readable" units:

```
$ ls -l -h
total 20K
-rw-r--r-- 1 root root      4.8K Sep 28 13:44 ada_lovelace_bio.txt
drwxr-xr-x 2 root scrapbook 4.0K Sep  3 21:03 docker
-rw-r--r-- 1 root root       681 Sep 28 13:44 sample.fastq
-rw-r--r-- 1 root root        57 Sep 28 13:44 small_file.txt
```

Extra options, that are structured like `-l` (or any other 
hyphen-letter combo) that turn something on/off e.g. a change in format, are 
known as **flags**.  This isn't that important now, but it's a good thing to 
know.
