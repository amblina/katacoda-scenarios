In the previous step we learned about ``pwd`` which tells us
which folder we are currently in. Let's continuing exploring.

#### 2.1 Listing contents of directories
Next we will look at listing contents of directories.

This is done with a command `ls` which lists the contents of a directory.

``ls``{{execute}}

Q: You will see nothing returned - why?

A: This folder is empty!

#### 2.2 Creating directories
Let's create some directories:

``mkdir my_data``{{execute}}

Now let's check the contents of ``pwd``

``ls``{{execute}}

Now you should see the folder ``my_data`` in your directory.

You can create a directory with any name you want by writing the following:

``mkdir <name_of_your_directory>``

Note: don't create directory names containing spaces!

Now let's try creating the same directory twice - what happens?

`mkdir my_data`{{execute}}

You will see a sensible message telling you why this isn't possible:

`mkdir: cannot create directory 'my_data': File exists`

This error message says that the program `mkdir` is unable to create this 
directory and tells you why: the file (folder) already exists!

## Task:

1 Create a directory called `refs`