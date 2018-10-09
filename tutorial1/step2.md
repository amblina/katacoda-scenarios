In the previous step we learned about ``pwd`` which tells us
which folder we are currently in (our **working directory**). 
Let's continue exploring.

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

As good practice, don't include spaces in your directory name - we'll cover 
this later.

##### 2.2.1 Trying to create a directory that already exists

Let's try creating the same directory twice - what happens?

`mkdir my_data`{{execute}}

You will see a sensible message telling you why this isn't possible:

`mkdir: cannot create directory 'my_data': File exists`

This error message says that the program `mkdir` is unable to create this 
directory and tells you why: the file (folder) already exists!

##### 2.2.2 Creating multiple directories

You can also create multiple directories with one command:

``mkdir step_1 step2``{{execute}}

This will create two directories, one called "step_1" and one called "step_2".

**What happens if you create a folder containing spaces?**
What happens when you try and create a folder called "My Documents" like this?

`mkdir My Documents`

<details>
    <summary>Answer</summary>
       It creates two folders called "Documents" and "My". If you wanted to create 
       a folder called "My Documents" you would have to write a command that 
       `mkdir` would not interpret as two separate folders:
       
``mkdir "My Documents"``
   
   We do this with quotation marks.
</details>


## Task:

<ol>
    <li> 
        Create a directory called `test`
        <details>
            <summary>Hint</summary>
                Remember that `mkdir` can be run with:
                ``mkdir <name_of_your_directory>``
        </details>
        <details>
            <summary>Answer</summary>
                `mkdir test`{{execute}}
        </details>
    </li>