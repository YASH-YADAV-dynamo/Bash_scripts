<h1 align="center">Guide for BASH Scripting</h1>

<p align"center">
  <img src="https://repository-images.githubusercontent.com/560483284/d197fd68-fe5a-44a3-acd4-fdd9a026da2a">
</p>

This repository contains a walk-through guide required for you to start BASH-Scripting

#Prerequisites

To use this repository, you need the have a linux installed on your system.
>For windows users --->Use WSL (windows subsystem for linux).

 ## What is BASH?
   **The main creator of Bash is Brian Fox, who started coding it in 1988 for the GNU Project.**<br>
   To understand it,
   imagine Bash as a translator. Instead of clicking buttons and menus, you tell it what you want to do by typing simple commands. It then translates those commands into actions your computer can understand.

  Think of it like a super cool assistant:

  Need to copy a file? Tell Bash, and it'll do it in a snap.
  Want to open a website? Just ask Bash, and it'll launch your browser.
  Feeling lazy and want to rename all your cat pictures at once? Bash can write a quick script to do it for you!
  
  No fancy mouse clicks: Learning a few commands opens up a whole world of possibilities.
  Like building puzzles? Scripting with Bash is like putting little commands together to make cool things happen.
  Get things done faster: Save time by automating repetitive tasks.
# Basic Commands
pwd: `pwd` command is used to print present working directory, it returns the directory where you are present.
```
pwd
```
cd: `cd` command is used to surf through directories (directories are like folders and files)
```
cd [directory name]
```
this command will direct you into your [directory name]
For example :To move into Desktop
```
cd Desktop
```
ls: `ls` command is used to list all directories or files inside that directory
```
ls [filename]
```
For example,to see all directories in desktop 
```
ls Desktop
```
mkdir: it is used to make new directory
```
mkdir [foldername]
```
For example, you want to make a folder named "frontend.txt"
```
mkdir frontend.txt
```
If you want to create new folder "frontend.txt" and want to be inside this directory also ,then use `&&`
```
mkdir frontend.txt && cd frontend.txt
```
touch: it creates an empty file and it also use to update time-stamps.
```
touch [filename]
```
For example, you want to create a new file named name.txt 
```
touch name.txt
```
To update time-stamps use `touch -t YYYYMMHHmm.ss [filename].txt`
here, 
<br>y-year
<br> M-month
<br> H-hour
<br>m-minutes
<br>s-seconds
<br>
For example, to update time-stamp of name.txt 
```
touch -t 202402011200.00 name.txt
```
cat: to prints the contents inside the directory
```
cat [directory]
```
For example, to view content inside name.txt
```
cat name.txt
```








  
  
    
 
