# Exploring Markdown

This is a repo/document for me to keep track of my bash commands and also practice with Markdown.

___

## Common Bash Commands

- `cd` - **command for changing directory**
    > **Example:**
    >
    >    `$ cd ~`
    >
    > This will change to the home directory of the logged user.  
- `~` (tilde) - **refers to the home directory**
- `touch` - **command for creating empty files**
    > **Example 1:**
    >
    > `$ touch index.html`
    >
    > This would add an `index.html` file to whichever directory you're currently in
    >
    > ___
    >
    > **Example 2:**
    >
    > `$ touch resources/style.css`
    >
    > This would add a `style.css` file to the `resources` directory (from whichever directory your currently in)
- `ls` - **command for listing a directory's content**
    - `ls -a` - displays all files in current directory, even hidden ones with a period at the beginning of them  
    - `tree` - displays a graphical representation of a directory and it's nested directories (install it by typing `brew install tree`)

- `pwd` - **command prints the current (working) directory**
- `mkdir` - **command to create directories**
    > **Example:**  
    >
    > `$ mkdir ~/drawers`
    >
    > This will create a `drawers` directory inside of the *__home__* directory  
    >
    > Note: you do not have to specify the *full path* if we are already in the *__home__* directory.
  
- `mv` - move files or directories, as well as rename files or directories

    > **Example 1: Moving files/directories**
    > 
    > `$ mv ~/shorts ~/drawers`
    >
    > Moves the `shorts` directory to the `drawers` directory.
    >
    > ___
    > 
    > **Example 2: Renaming files/directories**
    > 
    > `$ mv ~/drawers/pjs/warm.pjs ~/drawers/pjs/summer.pjs`
    > 
    > This will change the `warm.pjs` file to be named `summer.pjs`.
    >
    > *Note: you can change a file's name and it's location simultaneously.*
    >
    >___
    >
    > **Example 3: Moving multiple files**
    >
    > `$ mv *.socks`
    >
    > This will move all of the `.socks` files out of the `socks` directory and into our *home* folder.

- `rm` - deletes both files and directories

    > **Example:**
    >
    > `$ cd ~/drawers/socks && rm dress.socks`
    >
    > This would remove the `dress.socks` file from the `socks` directory within the `drawers` directory.
    >
    > *Note: using the **wildcard** character (\*), it's possible to delete and move multiple files. For example, typing* `\*.socks` *would match all files with an extension of socks.*

- `rm -r` - deleting directories
    - The `rm` command followed by the `-r` is the combination to use when deleting **directories only**.
    - The `-r` option runs the `rm` command **recursively**, meaning it deletes a directory and all of it's contents

    > **Example:**
    >
    > `$ rm -r ~/drawers/pjs`
    >
    > This will remove the `pjs` directory from the `drawers` directory.

- `cp` - copying files and directories

    > **Example:**
    >
    > `$ cp *.js ~/dest-folder`
    >
    > This copies all `.js` files from the `dest-folder` directory

    - `cp -r` - copies whole directories

        > **Example:**
        >
        > `cp -r ./sample-code ~/dest-folder`
        >
        > This copies the directory `./sample-code` from the `~/dest-folder` directory

- `clear` or `command K` - clears terminal, but does not delete previous commands taken; if you scroll up after running the `clear` command, you'll see previous commands from current session

- `history` - view log of all commands made previously, even before current session
___

## Tactics  

### **Auto-Tab Completion**

+ Let's say you want to access a directory called `drawers` in your *home* directory
+ You go to type it out, but only type the frist letter of the directory you want to access: `cd d`.
+ Here, you can press tab which will auto-complete directory names
+ If you have multiple files in the current directory that start with the same letter (in this case, `d`), the terminal will give you multiple options to choose from
    - Here, you can cycle between matching directory names by continuing to press **tab**
  
### **Using a single command for two commands**

+ Put the two commands on the same line and add two **ampersand** (`&`) symbols between the commands  

    > **Example 1:**  
    >
    > `$ mkdir socks && cd socks`
    >
    > This would create a directory called `socks` and also move us into the directory `socks`.
    >
    > ___
    >
    > **Example 2:**
    >
    > `$ touch resources/style.css && resources/index.html`
    >
    > This would add a `style.css` file as well as an `index.html` file to the `resources` directory.
