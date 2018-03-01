# Week 8

The theme for this week is:

> Databases

We will also get our first look at the _command line_ approach of
using your computer.

* Notes on our in-class [Command Line Tutorial](cmdline.md) are already provided.
* You can use the [Quick Reference Card for SQL](SQL.md) during the [in-class challenges](CHALLENGES.md).


### Getting Started

1. Download this repository into a folder named `~/code/week10` (Mac)
   or `C:\code\week10` (Windows)

2. Open your command prompt: `cmd` on Windows, or the Terminal app on Mac


### Command-Line Tutorial

See the [notes](cmdline.md) as a reference for what we will cover in class.

### SQL Quick Start


 1. Navigate to your week10 folder:

    `cd \code\week10` (Windows)

    `cd ~/code/week10` (Mac)


2. Start the SQLite3 program like this:

   `sqlite3`

   You should see something like this:

   ```
   SQLite version 3.19.3 2017-06-27 16:48:08
   Enter ".help" for usage hints.
   sqlite> _
   ```

3. At any time, `.exit` or `.quit` will get you back to the command line.

---


Let's create a _table_, which is defined as a series of columns, like a spreadsheet.
Pay attention to the semicolon at the end of the line!

```
sqlite> create table friends(id integer primary key, name text, hometown text);
```

You should now be at the `sqlite>` prompt again.


> NOTE: If you now see something like
   ```
      ...>
   ```
   then you forgot the semicolon!  Just type it now and press `Enter`:
   ```
      ...> ;
   ```

We now have an empty table:

```
sqlite> select name, hometown from friends;
```

Let's add a couple of rows:

```
sqlite> insert into friends (name, hometown) VALUES ("Alice", "Chicago"), ("Bob", "New York");
```

Let's view the table again:

```
sqlite> select name, hometown from friends;
```
```
Alice|Chicago
Bob|New York
```

We can also tweak the table display.  For example:

```
sqlite> .mode column
sqlite> .headers on
sqlite> .width 20 20 20 20
```

And now:

```
sqlite> select name, hometown from friends;
```


---

### SQLite Commands

Do NOT use a semicolon after these commands:

* `.open [filename]` will open the database with the given _filename_
* `.tables` will show you a list of all of the tables
* `.schema [tablenam]` will show you the structure of a given table
* `.help` will show you all possible commands



### More Online Resources

1. The official documentation: https://sqlite.org/cli.html

2. This might sound funny, but W3Schools has a decent reference guide
for all things SQL, including a live query composer that you can try
from within your browser.

    https://www.w3schools.com/sql/default.asp

3. Another decent option is the SQL section of GeeksForGeeks:

    http://www.geeksforgeeks.org/sql-tutorial/
