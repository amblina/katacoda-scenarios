In the previous step we create directories inside the directory we were in.

We were doing this by specifying a name for that new directory.  This name acts
as a relative path to the new directory.  You can create a directory inside a 
directory using this method too.

First, let's see where we are, and what is in the directory:

``pwd``{{execute}}

``ls``{{execute}}

Now we can create a directory _inside_ ``test_folder``.  We can do this by 
moving into the folder and creating a new directory OR we can create the folder 
from where we are now by specifying a path to the new directory!

so this:

``cd test_folder``

``mkdir new_folder``

will do the same as this:

`mkdir test_folder/new_folder`{{execute}}

Now if you `ls` the `test_folder` you will find `new_folder`.

#### Relative vs absolute paths

So now you know that when you create a new folder with `mkdir` you are not only 
saying "create a new folder with this name" - you are specifying *WHERE* that 
folder should be i.e. "Create a new folder with this name in this location".

This is a good time to introduce the idea of **relative** and **absolute** 
paths.

When you called `mkdir` you were specifying the **relative** path.  This means 
you were specifying the new folder name *relative* to the folder you were in 
i.e. `/home/scrapbook/tutorial`.

So instead of having to type the **abosolute** (full) filepath:

`mkdir /home/scrapbook/tutorial/test_folder/new_folder`

You can just type:

`mkdir test_folder/new_folder`

The command `mkdir` by **default** assumes that you want to create a directory
relative to where you are now i.e your **working directory** (`pwd`).

You also learned in the previous section about the shortcut `..` which means 
"directory above".  This is another way of specifying a relative path.

If you want to create your directory in a very specific place in your 
filesystem, such that it will create it there no matter where you are currently 
in the filesystem, you can specify the *absolute* path.

`mkdir /home/scrapbook/tutorial/test_folder/new_folder`{{execute}}

If you `cd` into any directory and try and run this command you will only 
be trying to create the same folder in the same location as before.  You will 
be able to tell this because you will see this error message no matter where
you try and run the command:

`mkdir: cannot create directory '/home/scrapbook/tutorial/test_folder/new_folder': File exists`



