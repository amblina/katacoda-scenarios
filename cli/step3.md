So now you have created some directories!

Let's check where we are and what is in our current directory:

``pwd``{{execute}}
``ls``{{execute}}

Let's look at how to move around the file system, first let's create a
directory..

`mkdir step3`{{execute}}

Now when you `ls`{{execute}} you should be able to see the `step3` directory.

#### 3.1 Chanding directory with `cd`

The `cd` command let's you **c**ange **d**irectory. To run this command you
run:

`cd <path/to/where/you/want/to/go>`

Now lets check where we are, then **c**ange **d**irectory into `step3`!

`pwd`{{execute}}
`cd step3`{{execute}}
`pwd`{{execute}}

Now if you run `ls`{{execute}} in this folder you'll see that it's empty -
this is unsurprising - we just created it.

Now let's use *cd* to go back to where we were before:

`cd /home/scrapbook/tutorial`{{execute}}

That's a bit of a mouthfull - what if we'd not checked the directory path
before  we moved into the subdirectory?

You can use the shorthand `..` which means "the directory above"

`pwd`{{execute}}
`cd step3`{{execute}}
`pwd`{{execute}}
`cd ..`{{execute}}
`pwd`{{execute}}

What about if you wanted to move two folders above? You can use `../../`!

Let's try this:

`cd /home/scrapbook/tutorial`{{execute}}
`pwd`{{execute}}
`mkdir step3/my_folder`{{execute}}
`cd step3/my_folder`{{execute}}
`pwd`{{execute}}
`cd ../../`{{execute}}
`pwd`{{execute}}

### Task

1) Create a folder in the step3 folder called `test`
2) List the contents of this new `test` folder
3) Change directory into `/home/scrapbook/tutorial/step3/test` and list the contents of the folder above