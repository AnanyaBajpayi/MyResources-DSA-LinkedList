
### Git Bash:If os is a nut ..............the kernel is the hardware(memory ,cpu,etc) and the shell is the interface that you use to communicate with the kernel.
```c
1. BASH stands for Bourne Added SHell.
2. Many types of interfaces:Graphical User Interface,Command line interface
3. GUI hides a lot of information and is more userfriendly,CLI is faster and has more functionality.
4. More developers prefer CLI.
5. ~(Tilde) in bash terminal denotes the level at which you are.If it is ~ it means that youre at root level,i.e,This PC folder .
 ```

### How to create a see all the files in a folder
```c
Go to the desired folder and type ls
```

### How to create a secret folder
```c
mkdir .<whatever_name>
```
### How to navigate between directories
```c
1. cd <one_level_down_folder>
2. tab auto fills the name of the folder
3. if we have documents and downloads and we type cd do and then press tab,then it gives us the names of the files starting with do. 
4. cd ~ =>takes back to the root
5. cd Documents/Learn/Languages/ =>goes inside a language folder
6. cd .. takes us back one level
7. If we write cd <path> anywhere it goes to that path specified folder.
8. If you want to move the cursor where you want then hold alt and take the cursor where it needs to be.
9. To clear a command before running use CTRL+U.
```
### Creating,Opening and removing files using CLI
```c
1. mkdir <folder_name>
2. touch <file_name> to make a file .eg-touch anna.txt
3. start anna.txt=>opens the file in required application ,here .txt so notepad
4. To open anna.txt in VS code =>code anna.txt
5. To delete anna.txt=>rm anna.txt
6. To know which directory youre in=>pwd
7. To delete all the files in a folder,make sure that youre in that folder =>rm *
8. Be careful while removing anythhing
9. To remove a directory named Ananya=>rm -r Ananya/
```
