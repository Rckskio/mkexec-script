# Bash Script MKEXEC
## Description
**Mkexec** is a bash script to help place your own scripts or binary files to **/home/user/.local/bin**. The PATH to place the file can be edited to your own preference. It's possible to use this script to place itself to the path **/home/user/.local/bin** or other specified path using **-p** flag. The main goal is to make it easier to run user scripts or programs, by placing it on a directory that is usually already on user $PATH. Type **echo $PATH** on terminal to see all the directories already on it.

## How to Install
To install or better saying copy this script to $HOME/.local/bin and allow it to execute, extract the downloaded files and change directory ( **cd** ), to the same directory mkexec is, then type **bash mkexec -i**, or to see some information of what is being done type **bash mkexec -iv**

## Steps of this scrip
### Using one time only with bash mkexec filename 
By default, this script will first allow your script or binary file to be executable and then place it inside /home/user/.local/bin.
The commands it runs are:
**chmod +x** $NAME
**cp** $NAME $DEFAULT_PATH
Take note that $NAME is the name of your script or binary file, and $DEFAULT_PATH is by default /home/user/.local/bin, you can change to another directory using the flag **-p** and typing the path you prefer.

### -i flag
Using **bash mkexec mkexec** for the first time after downloading it, it will do the same as it would do to any other script, allow to execute and copy to /home/user/.local/bin.
But it also tries to place a manual page to /usr/share/man/man8, so any time you need to check the options or information about it just type **man mkexec**, or **mkexec -h**
To place the manual page it will need privilege access to be able to copy the manual to /urs/share/man/man8 and zip it with gzip.
The commands it runs are:
**chmod +x** $0
**cp** $0 $C_PATH
**sudo** **cp** man/mkexec.8 /usr/share/man/man8/mkexec.8
**sudo** **gzip** /usr/share/man/man8/mkexec.8

# Remove
To remove just enter **mkexec -u**, it will remove the files from the directories described before. But be aware, it only remove the mkexec itself, not the scripts or binary you created before using mkexec. 
To make sure it is deleted you can check on each directory described here manually or type **whereis mkexec**, it will display where on your system the files are.



# Notice
This script was made only for study purposes, also to make it easy to try my own bash scripts or binary files that I create.
