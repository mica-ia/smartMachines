# Smart Machines Crash Course
So it's worth noting now, this stuff is complicated. _Really_ complicated. If you feel hopelessly lost, guess what? You're not alone! We struggled through learning how this stuff works too, and hopefully you can learn from our experience.

## Course Contents
* [Vocab List](#vocab-list)
* [Setting up your workspace](#setting-up-your-workspace)
* [Terminal, command line, interpreters, oh my!](#what-is-the-terminal)
* [Python](#python)

## Vocab List
<details>
  <summary>Click to expand!</summary>

  Here are some words we'll be using throughout this document. We'll elaborate further down below, but here's a few to start:
  ### Terminal:
  The difference between a terminal, shell, and console is...fuzzy. Nerds could quibble all day about the exact definition of each, but for our purposes, a terminal is a special app used to write and send commands to our computer. If you've seen Tron, or any cheesy 90's hacker movies, you'll have seen something like this:
  ```
  $ whoami
  flynn
  ```
  This is a terminal. It uses a command-line style (basically, just text) interface that we can send commands to.

  ### Interpreter:
  In our case, Python.
  ### Filepath:
  The "path" through the folders/directories to reach a particular location. For example, "/Users/deckardkane/Documents".
  ### Directory:
  A folder, more or less.

</details>

## Setting up your workspace
Creating a workspace that suits your preferences is important, and we'll give some recommendations, but instructions will vary depending on your operating system.

You'll need a terminal, a code editor, and Python 3. If you've got that, carry on! If you're not sure, check out the instructions for your operating system by clicking below.

<details>
  <summary>Setup for macOS</summary>

  1. Install [Python 3](https://www.python.org/downloads/release/python-373/). Follow the link to the Python downloads page, select the macOS 64-bit/32-bit installer, and install it like you would any other program.
  2. Install a code/text editor of your choice. We recommend [Atom](https://atom.io/), but there are many other options, including [Sublime Text](https://www.sublimetext.com/3) and [Visual Studio Code](https://code.visualstudio.com/download).
  3. Make sure your code editor is easily accessible by putting it in your dock.
  4. Mac users already have a terminal app, appropriately titled "Terminal". Use the Spotlight tool to search for it, and add it to your dock as well. This will be how you run the code you write!


</details>

<details>
  <summary>Setup for Windows</summary>

  1. Install [Python 3](https://www.python.org/downloads/release/python-373/). Follow the link to the Python downloads page, select the Windows x86/64-bit installer, and install it like you would any other program.
    * TAKE NOTE: Windows users may have some choices to make about whether or not to add Python 3 to the system path. For now, check the box in the Python installer that adds it to the system path. It'll allow you to run the `python` command in your terminal without issue.
  2. Install a code/text editor of your choice. We recommend [Atom](https://atom.io/), but there are many other options, including [Sublime Text](https://www.sublimetext.com/3), [Visual Studio Code](https://code.visualstudio.com/download), and [Notepad++](https://notepad-plus-plus.org/download/v7.6.6.html).
  3. Make sure your code editor is easily accessible in your taskbar/Start Menu/whatever.
  4. Windows users have several options for terminal apps. The one that comes preinstalled is called PowerShell. Does it work? ...mostly. It can come with some weird quirks and errors. They're in no way impossible to solve, but if that intimidates you, it's worth checking out alternative terminal apps. We recommend [cmder](https://cmder.net/). It's highly customizable (and free!), and you can plug something like [git bash](https://git-scm.com/downloads) into it if you so desire.

</details>

<details>
  <summary>Setup for Linux</summary>
  1. Install [Python 3](https://www.python.org/downloads/release/python-373/). Follow the link to the Python downloads page, select the , and install it like you would any other program.
  2. Install a code/text editor of your choice. We recommend [Atom](https://atom.io/), but there are many other options, including [Sublime Text](https://www.sublimetext.com/3) and [Visual Studio Code](https://code.visualstudio.com/download).
  3. Make sure your code editor is easily accessible in your taskbar/dock.
  4. Linux

</details>

## What is the terminal?
Well, good question. When you start up your terminal app, you'll see something like this:
```
deckardkane@RIPLEY ~/Documents/GitHub/smartMachines
$
```
This is your command line. You can type into it! The text above the $ (or next to it) will vary, depending on your username, the name of the device you're using, and your current filepath. The $ (or similar, it's dependent on what terminal app you're using) is just a character that prompts you for input. Of course, it'll only respond to specific words and phrases. For instance, you can type (and hit enter afterwards!):
```
$ pwd
```
And you should see something like this:
```
/Users/deckardkane/Documents/GitHub/smartMachines
```
This is your current filepath. `pwd` stands for "Print Work Directory", and it does exactly that: it tells you which directory you are currently working in.

So now we know _where_ we are, but what's in the directory we're currently at? To find out, type:
```
$ ls
```
You'll get a list of files and/or directories. Depending on your terminal app, regular files may appear in white, directories in blue, and "executable" files (files that you can run) in green.
```
crashCourse.md README.md thisIsATest.md data
```
The `ls` command lists files in the directory you're currently in. So you won't necessarily have the same files or folders as the output above.

Okay, now we know where we are, and what's in that directory, but now we want to go somewhere else. Type:
```
$ cd ..
```
...and it may look like nothing has happened, but notice that the reported filepath has changed:
```
deckardkane@RIPLEY ~/Documents/GitHub
$
```
You can also confirm this with `pwd`, and get:
```
/Users/deckardkane/Documents/GitHub
```
It's worth noting that the ~ (this symbol is called a tilde) is an abbreviation for a "home" directory, in this case, `/Users/deckardkane`.

We are now no longer in the `smartMachines` directory. We are now one folder above it. `cd ..` is just shorthand for "back out of this folder, go to the one above it". Now, let's go somewhere else. Run `ls` to see what's what in our new directory.
```
smartMachines mySecretProject
```
Oooh, interesting. Let's check out that other directory.
```
$ cd mySecretProject
```
And now we have:
```
deckardkane@RIPLEY ~/Documents/GitHub/mySecretProject
$
```
Run `ls` again, and...
```
planForWorldDomination.py step1.py step2.py step3.py
```
These are Python code files! Interesting.

Those are the very basics of using terminal commands. For more on these, put "terminal commands" or "shell commands" into a search engine of your choice.

## Python
If you want to become more comfortable with Python, and are looking for a good resource, we highly recommend _Learn Python the Hard Way_, by Zed Shaw. It's what we used for the class, and it reiterates many of the concepts listed above, and has a set of exercises for you to practice with.
