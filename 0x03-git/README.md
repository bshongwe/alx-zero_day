# 0x03. Git

## General
    What is source code management
    What is Git
    What is GitHub
    What is the difference between Git and GitHub
    How to create a repository
    What is a README
    How to write good READMEs
    How to commit
    How to write helpful commit messages
    How to push code
    How to pull updates
    How to create a branch
    How to merge branches
    How to work as collaborators on a project
    Which files should and which files should not appear in your repo

## Requirements
### General
    A README.md file at the root of the alx-zero_day repo, containing a description of the repository
    A README.md file, at the root of the folder of this project (i.e. 0x03-git), describing what this project is about
    Do not use GitHub’s web UI, but the command line to perform the exercise (except for operations that can not possibly be done any other way than through the web UI). You won’t be able to perform many of the task requirements on the web UI, and you should start getting used to the command line for simple tasks because many complex tasks can only be done via the command line.
    Your answer files should only contain the command, and nothing else

# Tasks
## Task 0. Create and setup your Git and GitHub account
#mandatory

Step 0 - Create an account on GitHub [if you do not have one already]
You will need a GitHub account for all your projects at ALX. If you do not already have a github.com account, you can create an account for free here

Step 1 - Create a Personal Access Token on Github
To have access to your repositories and authenticate yourself, you need to create a Personal Access Token on Github.
You can follow this tutorial (https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) to create a token.
Once it’s created, you should have a token that looks like this: <img src="https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2022/2/a449483cd76a72cef1b42df831e686c64faa1cf6.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230808%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230808T035210Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=d03ad6934ada27aeb2a864835bd5e9e74538ce11dde4750d70f7894e8d5c0743" />

Step 2 - Update your profile on the Intranet
Update your Intranet profile by adding your Github username
If it’s not done the Checker won’t be able to correct your work

Step 3 - Create your first repository
Using the graphic interface on the github website, create your first repository.

    Name: alx-zero_day
    Description: I'm now a ALX Student, this is my first repository as a full-stack engineer
    Public repo
    No README, .gitignore, or license

Step 4 - Open the sandbox
On the intranet, just under the task, click on the button  and run to start the machine.
Once the container is started, click on  to open a shell where you can start work from.

Step 5 - Clone your repository
On the webterm of the sandbox, do the following:

Clone your repository
<code>git clone https://{YOUR_PERSONAL_TOKEN}@github.com/{YOUR_USERNAME}/alx-zero_day.git</code>

    Cloning into 'alx-zero_day'...
    warning: You appear to have cloned an empty repository.       
Replace {YOUR_PERSONAL_TOKEN} with your token from step 1
Replace {YOUR_USERNAME} with your username from step 0 and 1
Pro-Tip: On windows, use CTRL + A + V to paste in the web terminal

Step 6 - Create the README.md and push the modifications
Navigate to this new directory
Create the file README.md with the content My first readme
Update your git identity:

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"
Add this new file to git, commit the change with this message “My first commit” and push to the remote server / origin

Repo:

    GitHub repository: alx-zero_day
    File: README.md
    

## Task 1
#mandatory

Create a new directory called 0x03-git in your alx-zero_day repo.
Make sure you include a not empty README.md in your directory:

at the root of your repository alx-zero_day
AND in the directory 0x03-git
And important part: Make sure your commit and push your code to Github - otherwise the Checker will always fail.

Repo:

    GitHub repository: alx-zero_day
    

## Task 2
#mandatory

For the moment we have an empty project directory containing only a README.md. It’s time to code!
Create these directories at the root of your project: bash, c, js
Create these empty files:
<code>c/c_is_fun.c</code>
<code>js/main.js</code>
<code>js/index.js</code>

Create a file bash/alx with these two lines inside: <code>#!/bin/bash and echo "ALX"</code>
Create a file bash/school with these two lines inside: <code>#!/bin/bash and echo "School"</code>

Add all these new files to git
Commit your changes (message: “Starting to code today, so cool”) and push to the remote server

Repo:

    GitHub repository: alx-zero_day
    Directory: 0x03-git
    File: bash/alx, bash/school, c/c_is_fun.c, js/main.js, js/index.js
    

## Task 3
#mandatory

A branch is like a copy of your project. It’s used mainly for:
- adding a feature in development
- collaborating on the same project with other developers
- not breaking your entire repository
- not upsetting your co-workers

The purpose of a branch is to isolate your work from the main code base of your project and/or from your co-workers’ work.

For this project, create a branch update_script and in this branch:
- Create an empty file named bash/98
- Update bash/alx by replacing echo "ALX" with echo "ALX School"
- Update bash/school by replacing echo "School" with echo "The school is open!"
- Add and commit these changes (message: “My personal work”)

Ho wait, your manager needs a quick fix in your project and it needs to be deployed now:
- Change branch to main
- Update the file bash/alx by replacing echo "ALX" with echo "ALX School is so cool!"
- Delete the directory js
- Commit your changes (message: “Hot fix”) and push to the origin


Repo:

    GitHub repository: alx-zero_day
    Directory: 0x03-git
    File: bash/alx, bash/school, bash/98
    

## Task 4
#mandatory

For this task – and only for this task – please update your file README.md in the main branch from GitHub.com. It’s the only time you are allowed to update and commit from GitHub interface.

After you have done that, in your terminal:
- Get all changes of the main branch locally (i.e. your README.md file will be updated)
- Create a new file up_to_date at the root of your directory and in it, write the git command line used
- Add up_to_date to git, commit (message: “How to be up to date in git”), and push to the origin

Repo:

    GitHub repository: alx-zero_day
    Directory: 0x03-git
    File: README.md, up_to_date
    

## Task 5
#advanced

Merge the branch update_script to main: “Cool, all my changes will be now part of the main branch, ready to be deployed!”

CONFLICT (content): Merge conflict in bash/alx
As you can see, you have conflicts between two branches on the same file.

Your goal now is to resolve conflicts by using the version of the branch update_script, and push the result to the origin.
At the end, you should have all your work from the branch update_script (new file and two updated files) and all latest main commits (new files, delete folder, etc.), without conflicts.

Repo:

    GitHub repository: alx-zero_day
    Directory: 0x03-git
    

## Task 6
#advanced

Create a .gitignore file and define a rule to never push ~ files (generated by Emacs). Tips

Repo:

    GitHub repository: alx-zero_day
    Directory: 0x03-git
    File: .gitignore
    

