# Text Editor

It won't matter which text editor you use, though some of them have options the others don't, but it's all about the one you can comfortablly use. 

### What is a text editor?

A text editor is a piece of software that you download and install on your computer, or you access online through your web browser, that allows you to write and manage text, especially the text that you write
to build a web site. The text editor has to be one of the most important tools you can use as an aspiring web developer.

### Important Features to look up un Text Editor:

1. code completion.
It could give you suggestions based on what you originally
typed.

2. syntax highlighting.
Syntax highlighting is a feature that takes the text you
type, and makes it more noticeable by colorizing the text. Attributes are a different color than elements. And elements are a different color than copy. This makes it so much easier when you’re looking for an error and you can’t find it. As well as making your text easier to read.

3. a nice variety of themes (to reduce eye strain and
fatigue).
These themes will allow you to change the color of
the background of your text editor, the series of colors in your text, and sometimes themes will affect other aspects of your text editing software as well. Usually, web developers use a dark background and brightly colored text. This combination seems to be easier on the eyes —but there are other themes to choose from as well. Since you’ll be
using your text editor most of the time, it’s good to find a theme that might reduce eye strain and fatigue.

4. the ability to choose from a healthy selection of
extensions available when you need them. You might find some other features that are must-have’s, but I think these features are a good start. 
(You want a text editor that can grow with you as your
needs grow. This comes in the form of extensions. Extensions are like plugins for your text editor, that allow you to have superpowers that you wouldn’t have otherwise. A text editor that has a great selection of extension will ensure that you have the ability to add functionality
as you need it.)

Text Editor that **already exsists** on the computer, but they don’t have many features to speak of. They’re the barest bare bones text editors you’ll encounter.

These are few things you should give your **attention** to: 

1. Make sure that you are using the plain text while you are coding on you text editor.
2. It would be better to save the entire website in one folder in a remarkable place for you.
3. Pay attention to the extensions of the created files (.html, .css, .js)

### Third-Party Options 

Notepad++, Text Wrangler, BB Edit, Visual Studio Code, Atom, Brackets, and Sublime Text. These text editors can all be downloaded and installed to your computer from their respective websites. Each of these titles do have some if not all of the features that was mentioned about earlier, and most of this software is absolutely free! They are widely used in web development today.

### The Difference Between Text Editors and IDEs

A text editor kind of gives away what it does in the title—it edits text. It also manages text, and manages files. I love that name “textwrangler” because in a way that’s what really a text editor does. It wrangles your text together into something meaningful.

An IDE (Integrated Development Environment) is really a suite of different software all coming together. An IDE is a text editor, a file manager, a compiler, and a debugger all in one software package.

# The Line Command 
A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands. Here is an example:

> 1. user@bash: ls -l /home/ryan
2. total 3
3. drwxr-xr-x  2 ryan users 4096 Mar 23 13:34 bin
4. drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
5. drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html
6. user@bash: 

Let's break it down:

Line 1 presents us with a prompt ( user@bash ). After that we entered a command ( ls ). Typically a command is always the first thing you type. After that we have what are referred to as command line arguments ( -l /home/ryan ). Important to note, these are separated by spaces (there must be a space between the command and the first command line argument also). The first command line argument ( -l ) is also referred to as an option. Options are typically used to modify the behaviour of the command. Options are usually listed before other arguments and typically start with a dash ( - ).

Lines 2 - 5 are output from running the command. Most commands produce output and it will be listed straight under the issuing of the command. Other commands just perform their task and don't display any information unless there was an error.

Line 6 presents us with a prompt again. After the command has run and the terminal is ready for you to enter another command the prompt will be displayed. If no prompt is displayed then the command may still be running (you will learn later how to deal with this).
Your terminal probably won't have line numbers on it. I have just included them here to make it easier to refer to different parts of the material.

### The Shell, Bash

Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called bash which stands for Bourne again shell. This tutorial will assume you are using bash as your shell.

If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. echo is a command which is used to display messages.



## Linux
Though I'm currently using Windows 10 instead of Linux, we have bellow some notes (VImp) you have to make sure you got them well. 

1. Linux is extensionless system: 
It does not matter wether you add an extension to the file or not, or even if you add a wrong extension in Linux. So, in order to know the type of the file (extension), we have the command 
file [path]

2. Linux is Case Sensitive
It matters if use an uppercase or lowercase, for example: 
(file1.txt) is not as smiliar as (file1.TXT)

3. Spaces are not valid ll the time! 

Spaces in file and directory names are perfectly valid but we need to be a little careful with them. As you would remember, a space on the command line is how we seperate items. They are how we know what is the program name and can identify each command line argument. If we wanted to move into a directory called Holiday Photos for example the following would not work.

> user@bash: ls Documents

> FILE1.txt File1.txt file1.TXT Holiday Photos

>...

> user@bash: cd Holiday Photos

>bash: cd: Holiday: No such file or directory


What happens is that Holiday Photos is seen as two command line arguments. cd moves into whichever directory is specified by the first command line argument only. To get around this we need to identify to the terminal that we wish Holiday Photos to be seen as a single command line argument. There are two ways to go about this, either way is just as valid.

Quotes
The first approach involves using quotes around the entire item. You may use either single or double quotes (later on we will see that there is a subtle difference between the two but for now that difference is not a problem). Anything inside quotes is considered a single item.

`user@bash: cd 'Holiday Photos'`

`user@bash: pwd`

`/home/ryan/Documents/Holiday Photos`


Escape Characters
Another method is to use what is called an escape character, which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.

`user@bash: cd Holiday\ Photos`

`user@bash: pwd`

`/home/ryan/Documents/Holiday Photos`

In the above example the space between Holiday and Photos would normally have a special meaning which is to separate them as distinct command line arguments. Because we placed a backslash in front of it, that special meaning was removed.

4. Hidden Files and Directories


Linux actually has a very simple and elegant mechanism for specifying that a file or directory is hidden. If the file or directory's name begins with a . (full stop) then it is considered to be hidden. You don't even need a special command or action to make a file hidden. Files and directories may be hidden for a variety of reasons. Configuration files for a particular user (which are normally stored in their home directory) are hidden for instance so that they don't get in the way of the user doing their everyday tasks.

To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be as such. Likewise you may rename a hidden file to remove the . and it will become unhidden. The command ls which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option -a so that it does show hidden files and directories.

## **Let's dig deep in more commands!**

### pwd
Print Working Directory - ie. Where are we currently.
A lot of commands on the terminal will rely on you being in the right location. As you're moving around, it can be easy to lose track of where you are at. Make use of this command often so as to remind yourself where you presently are.

### ls
List the contents of a directory.
Whereas pwd is just run by itself with no arguments, ls is a little more powerful. We have run it here with no arguments in which case it will just do a plain listing of our current location. We can do more with ls however. Below is an outline of its usage:

ls [options] [location]

In the above example, the square brackets ( [ ] ) mean that those items are optional, we may run the command with or without them. In the terminal below I have run ls in a few different ways to demonstrate.

`1. user@bash: ls`

`2. bin Documents public_html`

`3. user@bash: ls -l`

`4. total 3`

`5. drwxr-xr-x  2 ryan users 4096 Mar 23 13:34 bin`

`6. drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents`

`7. drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html`

`8. user@bash: ls /etc`

`9. a2ps.cfg aliases alsa.d cups fonts my.conf systemd`

`10. ...`

`11. user@bash: ls -l /etc`

`12. total 3`

`13. -rwxr-xr-x  2 root root 123 Mar 23 13:34 a2ps.cfg`

`14. -rwxr-xr-x 18 root root 78 Feb 17 09:12 aliases`

`15. drwxr-xr-x  2 ryan users 4096 May 05 17:25 alsa.d`

`16. ...`

Let's break it down:

**Line 1** - We ran ls in it's most basic form. It listed the contents of our current directory.

**Line 4** - We ran ls with a single command line option ( -l ) which indicates we are going to do a long listing. A long listing has the following:
First character indicates whether it is a normal file ( - ) or directory ( d )
Next 9 characters are permissions for the file or directory (we'll learn more about them in section 6).
The next field is the number of blocks (don't worry too much about this).
The next field is the owner of the file or directory (ryan in this case).
The next field is the group the file or directory belongs to (users in this case).
Following this is the file size.
Next up is the file modification time.
Finally we have the actual name of the file or directory.

**Line 8** - We ran ls with a command line argument ( /etc ). When we do this it tells ls not to list our current directory but instead to list that directories 
contents.

**Line 11** - We ran ls with both a command line option and argument. As such it did a long listing of the directory /etc.
Lines 12 and 18 just indicate that I have cut out some of the commands normal output for brevities sake. When you run the commands you will see a longer listing of files and directories.

### Absolute and Relative Paths
There are 2 types of paths we can use, **absolute** and **relative**. Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).

To begin with, we have to understand that the file system under linux is a hierarchical structure. At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.

Absolute and Relative Paths
There are 2 types of paths we can use, absolute and relative. Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).

To begin with, we have to understand that the file system under linux is a hierarchical structure. At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.

### cd
Change Directories - ie. move to another directory.
The command cd may be run without a location as we saw in the shortcut above but usually will be run with a single command line argument which is the location we would like to change into. The location is specified as a path and as such may be specified as either an absolute or relative path and using any of the path building blocks mentioned above. Here are some examples.

`1. user@bash: pwd`

`2. /home/ryan`

`3. user@bash: cd Documents`

`4. user@bash: ls`

`5. file1.txt file2.txt file3.txt`

`6. ...`

`7. user@bash: cd /`

`8. user@bash: pwd`

`9. /`


`10. user@bash: ls`

`11. bin boot dev etc home lib var`

`12. ...`

`13. user@bash: cd ~/Documents`

`14. user@bash: pwd`

`15. /home/ryan/Documents`

`16. user@bash: cd ../../`

`17. user@bash: pwd`

`18. /home`

`19. user@bash: cd`

`20. user@bash: pwd`

`21. /home/ryan`

