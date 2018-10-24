So now you have created some directories!

Let's check where we are and what is in our current directory:

``pwd``{{execute}}

``ls``{{execute}}

Let's look at how to move around the file system, first let's create a
directory..

`mkdir step3`{{execute}}

Now when you `ls`{{execute}} you should be able to see the `step3` directory.

#### 3.1 Changing directory with `cd`

The `cd` command let's you **c**hange **d**irectory. To run this command you
run:

`cd <path/to/where/you/want/to/go>`

Now lets check where we are, then **c**hange **d**irectory into `step3`!

`pwd`{{execute}}

`cd step3`{{execute}}

`pwd`{{execute}}

Now if you run `ls`{{execute}} in this folder you'll see that it's empty -
this is unsurprising - we just created it.

Now let's use *cd* to go back to where we were before:

`cd /home/scrapbook/tutorial`{{execute}}

That's a bit of a mouthful - what if we'd not checked the directory path
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

___
### Task

1) Create a folder in the step3 folder called `test_folder`
    <details>
        <summary>Hint</summary>
            Remember to **m**a**k**e a **dir**ectory use ``mkdir``.
    </details>
    <details>
        <summary>Answer</summary>
            `mkdir step3`{{execute}}
    </details>

2) List the contents of this new `test_folder` folder
    <details>
        <summary>Hint</summary>
            Remember to **l**i**s**t the contents of a directory use ``ls``.
    </details>
    <details>
        <summary>Answer</summary>
            `ls step3`{{execute}}
    </details>

3) Change directory into `/home/scrapbook/tutorial/step3/test` and list the 
contents of the folder above

    <details>
        <summary>Hint</summary>
            Remember to **l**i**s**t the contents of a directory use ``ls``.
    </details>
    <details>
        <summary>Hint</summary>
            Remember that `..` can be used as shorthand for "folder above"
    </details>
    <details>
        <summary>Answer</summary>
            `ls ..`{{execute}}
            `ls /home/scrapbook/tutorial/step3`{{execute}}
    </details>