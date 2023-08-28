### Git Bash:If os is a nut ..............the kernel is the hardware(memory ,cpu,etc) and the shell is the interface that you use to communicate with the kernel.
BASH stands for Bourne Added SHell.
Many types of interfaces:Graphical User Interface,Command line interface
GUI hides a lot of information and is more userfriendly,CLI is faster and has more functionality.
More developers prefer CLI.
~(Tilde) in bash terminal denotes the level at which you are.If it is ~ it means that youre at root level,i.e,This PC folder .
### How to create a see all the files in a folder
Go to the desired folder and type ls
### How to create a secret folder
mkdir .<whatever_name>
### How to navigate between directories
cd <one_level_down_folder>
tab auto fills the name of the folder
if we have documents and downloads and we type cd do and then press tab,then it gives us the names of the files starting with do. 
cd ~ =>takes back to the root
cd Documents/Learn/Languages/ =>goes inside a language folder
cd .. takes us back one level
If we write cd <path> anywhere it goes to that path specified folder.
If you want to move the cursor where you want then hold alt and take the cursor where it needs to be.
To clear a command before running use CTRL+U.
### Creating,Opening and removing files using CLI
mkdir <folder_name>
touch <file_name> to make a file .eg-touch anna.txt
start anna.txt=>opens the file in required application ,here .txt so notepad
To open anna.txt in VS code =>code anna.txt
To delete anna.txt=>rm anna.txt
To know which directory youre in=>pwd
To delete all the files in a folder,make sure that youre in that folder =>rm *
Be careful while removing anythhing
To remove a directory named Ananya=>rm -r Ananya/
