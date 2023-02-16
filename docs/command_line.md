---
layout: default
title: Command Line
date:   2023-01-02
author: Susanna Allés Torrent
nav_order: 4
---

# Practise 1: Bash Command

- Graphical-User Interface (GUI) VS Terminal/Command line/ Bash
- Windows users can follow along by installing popular shells such as Cygwin (<https://www.cygwin.com/>) or Git Bash <https://gitforwindows.org/>.
- Goals:
  * Navigate through your file system: where are you, what's in the folder.
  * Open, create, delete files and folders
  * Perform basic data manipulation tasks such as combining and copying files
  * Reading them and making relatively simple edits
- Open shell:
  * `Applications -> Utilities -> Terminal`
- Change the default visual appearance of the terminal in Preferences (choose your color, a clear readable font).
- Get to know yourself: `whoami`
- Moving around your computer’s file system:
  * `pwd`
  * `ls`
  * `man ls` and leave with `q`
  * `ls *.txt` (* command is a wildcard)
  * `ls -l` more information about items
  * `cd desktop`
  * `cd ..`
  * `cd --` goes back to the home directory
  * `open .` open up your GUI at the current directory
- Interacting with files
  * `pwd`, `ls`, `cd Documents`
  * create a new directory: `mkdir DHPracticum` and `ls`
  * create a new file: `touch`, e.g. `touch new_file.txt`
  * `open new_file.txt`
- Edit your file in you text editor 

# Install Wget
- Check if you have it: `wget -V` see if you have it installed.
- In Mac (nb. sometimes the terminal ask you to write some additional command, read it through, copy and paste):
  * Install Homebrew: `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
  * You might get this error:  
    `Error: The Ruby Homebrew installer is now disabled and has been rewritten in
Bash. Please migrate to the following command:
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
  * If so, write `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
  * Follow the prompts in the terminal (press return, write your password (remember that you don't see it)
  * You might get en error as well like this 
    `xcode-select: error: invalid developer directory '/Library/Developer/CommandLineTools'
     Failed during: /usr/bin/sudo /usr/bin/xcode-select --switch /Library/Developer/CommandLineTools`
  * If so, install XCode: `xcode-select --install`
  * Install Wget: `brew install wget`
- In Windows:
  * Go to `https://eternallybored.org/misc/wget/`
  * Copy the `wget.exe` file into your `C:\Windows\System32` folder.
  * Open the command prompt (`cmd.exe`) and run `wget` to see if it is installed.

# Exercise 1 with -wget and other commands 
  * Write in your terminal this to download this file: `wget http://www.gutenberg.org/files/2600/2600-0.txt`
  * `open 2600-0.txt`(opens the file)
  * `cat 2600-0.txt` (preview the file)
  * `head 2600-0.txt` (preview the begining of the file)
  * `tail 2600-0.txt` (preview the end of the file)
  * `mv 2600-0.txt tolstoy.txt` (change name)
  * `cp 2600-0.txt tolstoy.txt` (make a copy)
  * `cp tolstoy.txt tolstoy2.txt` (copy a file into another)
  * `cat tolstoy.txt tolstoy2.txt` (prints, or displays, the combined files within the shell)
  * `cat tolstoy.txt tolstoy2.txt` > tolstoy-twice.txt (make one single file from two)
  * `cat *.txt > everything-together.txt` (put all txt files together)
  * `rm tolstoy.txt`

# Exercise 2 

1. Try to experiment and understand the code behind an HTML template, such as the [Foundation templates](https://get.foundation/templates.html)
2. Choose a template you like, e.g. <https://get.foundation/templates-previews-sites-f6-xy-grid/portfolio.html>
3. Go to your terminal and place yourself in our folder, e.g. `/Users/yourusername/Documents/DHPracticum`
4. Download a template using wget: `wget https://get.foundation/templates-previews-sites-f6-xy-grid/portfolio.html`
5. Open the file with your web browser and check the URL: what does it mean? where is the file?
6. Right click in the website and choose "View Page source". Identify the HTML structre (the head, the body, etc.), the CSS and the Javascript scripts. 

# Exercise 3

  1. Go to our personal website, ex. <https://susannalles.github.io/>, make right click on the site and choose "View Page Source"
  2. Download the file with wget (in my case) `wget https://susannalles.github.io/test/`
  3. Open the file with your editor of choice, like the Visual Studio Code.
  4. Open the file with your web browser. What do you see? What's the problem?
  5. Fix the Path to the CSS to see the design. 

  
