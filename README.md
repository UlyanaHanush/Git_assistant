<p align="center">
 <img width="100px" src="https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white" align="center" alt="Learn GIT & Terminal" />
<img width="100px" src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white" align="center" alt="Learn GIT & Terminal" />
 <h2 align="center">Learn GIT & Terminal</h2>
 <p align="center">Beginner's Guide to Version Control & Command Line</p>
<p align="center">
<a href="docs/readme_rus.md">Русский</a>
</p>

<p align="center">Please note that documentation translations may be outdated; try to use English documentation if possible.</p>

# Features <!-- omit in toc -->

- [Installing Git](#installing-git)
    - [Installing Git](#installing-git)
    - [Working with the .gitconfig](#working-with-the-.gitconfig)
    - [List of all config properties](#list-of-all-config-properties)
    - [Case sensitivity](#case-sensitivity)
    - [Creating a local Git-repository](#creating-a-local-git-repository)
    - [Create Add Save](#create-add-save)
    - [Make a commit](#make-a-commit)
- [Recommendations](#recommendations)
- [Generate-SSH key](#generate-ssh-key)
- [Add an SSH key to your GitHub account](#add-an-ssh-key-to-your-github-account)


# Installing Git
git --version  

And if the command is not found, then use this:
xcode-select --install  

# Working with the .gitconfig 
git config --global user.name "Practicum"  
git config --global user.email uluana.hanush@gmail.com  

# List of all config properties
git config --list  

# Case sensitivity
git config --global core.ignorecase false  

# Creating a local Git-repository
Creating folder :  
mkdir  nameFolder  
Moving in folder  
cd nameFolder  
git init  

If you need: delate repository  
rm -rf .git  

# Create Add Save  
touch file.txt   
git add file.txt  

Save all file  
git add --all  
git add  .  

# Make a commit  
git commit -m "Text of changes!"  


> [!WARNING]\
> MUST be on the English layout :q! <!-- git will ask you to enter the name of the commit in the default editor. Sometimes in this case the Vim editor opens. Quit Vim -->

# Recommendations
consider in detail the service information from the .git folder


# Generate SSH-key

Open Terminal and enter the command:  
ssh-keygen -t ed25519 -C "<YOUR EMAIL when registering with GitHub>"  

Next, the command will prompt you to enter the path to the folder where you want to save the key:  
Enter file in which to save the key (/Users/practicum/.ssh/id_ed25519)    
I recommend agreeing with the proposed option - just press Enter.  

Enter a passphrase for the file:  
Enter passphrase (empty for no passphrase)
This password will be needed every time you try to print part of the key.  
The program offers to create a key without a password; to skip a step, press Enter.  
Next, run a command that will add the key to the SSH agent (a program that remembers your private SSH key and automatically substitutes it when you connect to the server via SSH) and saves it in the Keychain:  
ssh-add --apple-use-keychain ~/.ssh/id_ed25519  
Now copy the public key id_ed25519.pub to the clipboard:  
pbcopy < ~/.ssh/id_ed25519.pub  


# Add an SSH key to your GitHub account

*  Go to GitHub and go to Settings.  
*  In the left menu, select SSH and GPG keys.  
*  Click New SSH key or Add SSH key.  
*  In the Title field, enter the name of the key (for example, the name of your computer).   
*  In the Key field, paste the key from the clipboard using the hot keys Cmd + V.  
*  Click Add SSH key.


![Ulyana's GitHub stats](https://github-readme-stats.vercel.app/api?username=ulyanahanush\&show_icons=true\&theme=radical)
