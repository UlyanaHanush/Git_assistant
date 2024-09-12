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

[![Ulyana's GitHub stats](https://github-readme-stats.vercel.app/api?username=ulyanahanush)](https://github.com/ulyanahanush/github-readme-stats)

![Ulyana's GitHub stats](https://github-readme-stats.vercel.app/api?username=ulyanahanush\&show_icons=true\&theme=radical)
