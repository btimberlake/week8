# The Command Line

One trait that is very common among professional software developers is that they are also power-users of the computer. Since I can't have you doing things like a total noob out there, here is a quick cheat sheet to help you use your computer like a boss.

### What is this mythical "command-line" you speak of?

A computer's command-line interface (CLI) is a way for you to tell your computer to do things by inputting commands, instead of using the mouse. It's old-school. But it's also a way to do things much, much faster than clicking around all the time, so it's the preferred way for many professional developers to manage files and run software.

### How to access the command-line

On Mac, you use the "Terminal" application, which lives at Applications -> Utilities -> Terminal.

On Windows, it's called "Command Prompt". The fastest way to get there is from the Start Menu, and type `cmd` from the search bar. The blazing fast way is `Windows-R` and `cmd`.

### What can I do with it?

Almost anything you'd normally do with the mouse and keyboard. In this cheat sheet, we'll focus on something simple – how to traverse and browse the directory structure on your computer. We're going to learn how to use the command-line to do the things you'd ordinarily use Finder (Mac) or Explorer (Windows) to do.

### Knowing about and changing the current working directory

On Windows, the prompt itself will tell you what directory you're currently in, otherwise known as the "working directory".

On Mac, it may not. The easiest way to figure it out is by issuing the command:

```
pwd  
```

This stands for "print working directory". More likely than not, when you first open the command-line interface, your working directory will be your "home" or "user" directory (e.g. `/Users/jeff` on Mac or `c:\Users\jeff` on Windows). We want to head over to our code directory to do some stuff, so we're going to change our working directory by issuing the command:

`cd \code` (Windows)

`cd ~/code` (Mac)

Of course, this won't work if you were a rebel and didn't name your code folder like this, so modify this appropriately to match the name of your actual code folder.

### Listing files

Now that the command-line's working directory is set to our code folder, we can list the files inside. To list the files in the current working directory, we use the command:

`dir` (windows)

-OR-

`ls` (Mac)

### Combine the two and move around

This is roughly equivalent to what we're doing when we use Finder or Explorer to browse file using the mouse. Instead of double-clicking on a folder and seeing the files inside, we use a combination of cd and ls/dir to do the same thing. For example:

```
cd code  
ls  
cd hello-javascript  
ls  
cd ..  
ls  
```
That last one is a doozy. The `..` is shorthand for "up one directory". So we're using this command to change into the parent directory of the current working directory.

You can, of course, also `cd` directly to a folder, if you know its exact location:

`cd \code\hello-javascript` (Windows)

`cd code/hello-javascript` (Mac)

### Ok, what now?

Most commands you issue at the command-line (like `ls` or `dir`) will operate on the files in the current working directory.

Try viewing a file in the current working directory:

`type index.html` (Windows)

`cat index.html` (Mac)

We can also copy it:

`copy index.html index2.html` (Windows)

`cp index.html index2.html` (Mac)

Or move (rename) it:

`move index.html index2.html` (Windows)

`mv index.html index2.html` (Mac)

Or delete it (watch out! There's no undo):

`del index2.html` (Windows)

`rm index2.html` (Mac)

This only scratches the surface of what can be done via the command-line, and as with any new skill, can only be improved upon with practice!
