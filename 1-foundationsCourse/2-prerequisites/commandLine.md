#Command Line
[cheatsheet](https://files.fosswire.com/2007/08/fwunixref.pdf)
[material](https://swcarpentry.github.io/shell-novice/03-create.html) **

1. open the terminal by pressing `CTRL + ALT + T`on your keyboard
graphical user interface (GUI)
2. The Unix shell is both a command-line interface (CLI) and a scripting language
3. The shell is a program where users can type commands.
4. Bash is the default shell on most modern implementations of Unix and in most packages that provide Unix-like tools for Windows.
5. ‘Git Bash’ is a piece of software that enables Windows users to use a Bash like interface when interacting with Git.


prompt `$`
text cursor
- Programs can be run in Bash by entering commands at the command-line prompt.
- The shell’s main advantages are its high action-to-keystroke ratio, its support for automating repetitive tasks, and its capacity to access networked machines.
- The shell’s main disadvantages are its primarily textual nature and how cryptic its commands and operation can be.

`cd .`
`cd ..`
`cd -`
`cd ~`
`cd`
`cd /`


- `pwd` prints the user’s current working directory.
- `ls [path]` prints a listing of a specific file or directory; ls on its own lists the current working directory.
- `cd [path]` changes the current working directory.
- Most commands take options that begin with a single `-`.
- Directory names in a path are separated with `/ `on Unix, but `\ `on Windows.
- `/ `on its own is the root directory of the whole file system.
- An absolute path specifies a location from the root of the file system.
- A relative path specifies a location starting from the current location.
- `.` on its own means ‘the current directory’; `..` means ‘the directory above the current one’.

`cp`
