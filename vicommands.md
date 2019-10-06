# Getting friendly with Filesystems and Vi Commands



## What is a Filesystem?

* A file system stores and organizes data and can be thought of as a type of index for all the data contained in a storage device.
* Without a file system, stored information wouldn't be isolated into individual files and difficult to identify.
* As data capacities increase, the organization and accessibility of individual files are becoming even more important in storage.

## What is vi?
* The vi editor (short for visual editor) is a screen editor which is available on almost all Unix systems. Once you have learned vi, you will find that it is a fast and powerful editor. vi has no menus but instead uses combinations of keystrokes in order to accomplish commands. 
* vi (pronounced "vee-eye") is short for "vi"sual editor. It displays a window into the file being edited that shows 24 lines of text.
* vi lets you add, change, and delete text, but does not provide such formatting capabilities as centering lines or indenting paragraphs.



1. cd

* It stands for change directory. 
* It is used to change directories and go to other directories.
* We use the command cd followed by the file name we want to go.

To go to a particular directory
```
cd <directoryname>
```
To go a directory back or up
```  
cd ..
```
To go multiple directory up or back
```
cd ../..
```

2. mkdir

* It stands for make directory.
* It is used to create a folder to store files and information. 
* We use the command mkdir followed by file name.

To make a directory we use
```
mkdir <directoryname>
```

3. cp 
* It stands for make directory
* It is used to create a folder to store files and information 
* We use the command mkdir followed by file name. 

To copy files 
```
cp frida.txt linoln.txt
```
If we want to copy a file to a directory we use cp with the source file as the first argument and the destination directory as the second argument.
```
cp biopic/ cleopatra.txt historical/
```
If we want to copy multiple files into a directory we use cp with a list of source files as the first arguments and the destination directory as the last argument.
```
cp biopic/ray.txt  biopic/notorious.txt  historical/
```

4. pwd 
* It provides the current working directory. 
* Used to check where are we working in the file system. 
* The command is pwd.

To print current working directory simple write 
```
pwd
```
5. mv  

* It is used to move files from one directory to another within the filesystem. 
* Instead of copy pasting manually we can move any file with a simple command in the terminal. 
* The Syntax is mv <filename> <dir>.

To move a file simply write source file as first argument and the destination directory as the second argument
```
mv superman.txt superhero/
``` 
To move multiple files use mv with a list of source files as the first argument and the destination directory as last argument
```
mv wonderwoman.txt batman.txt superhero/
```
6. rm   

* rm stands for remove. 
* It is used to delete files or directories. 
* The command is used by typing rm followed by the file or directory we want to delete.

To remove a file use rm followed by file name
```
rm waterboy.txt
``` 
7. history 

* It provides the history of the commands in the terminal. 
* It is used to look throught the commands that you have entered. 
* The syntax is history

8. Home directory and ~
* It shows and directs to the users **home directory** in the filesystem, simply enter the following.

9. Filepath in Linux
* A path is a unique location to a file or a folder in a file system. It is a combination of ( / ) and alpha-numeric characters.
* An absolute path is defined as the specifying the location of a file or directory from the root directory( / ).
* Start at the root directory ( / ) and work down.

10. Using tab key to complete file paths
* The tab key is used to complete to filenames or git commands.
* Instead of typing the complete filename or command, just enter 2-3 inital characters
 
and press tab key.

11. Using up and down arrow key for history
* Up and Down arrow keys can be used to toggle through the previous commands that were entered.
