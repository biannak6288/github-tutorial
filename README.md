# GitHub Tutorial

_**by Bianna Orielle Krubitski**_

---
## Git vs. GitHub
**Git**: a platform that keeps snapshots of your code (version control)  
* Runs in the Command line 
* not open to viewers besides yourself
* One can create a directory; initalizing git allows the directory to become a repository -->   
later allowing you to:
    * edit files
    * add files
    * commit files

**Github**: stores your code in the cloud platform (a website; for example: Github.com)
* easy way to collaborate on projects when working with a partner
* It is an opensource (everyone with access to github can view your work)
* simple way to track changes made on the project with just a few commands
* MOST IMPORTANTLY: One cannot use Github without Git, however, Git does not need to contain Github to be activated 

---
## Initial Setup
_**How to set up your account with Github...**_

1. Go to github.com and press the button that says "sign up"
    * use an email and password (for HSTAT students, sign up using your school email and password)
    * once you're done signing up, check your email and verify with github  

2. Go to c9.io
    * creat an account(first/last name, email, password, etc.)
    * once set up, press on the gear in the top right corner
    * go to connected services
    * connect your github with cloud9 by clicking on the connect button  

3. In the future you will sign into cloud9 using your github account. This is how you do it...  

![ Alt if you want to sign-in to github using c9, this is where you go...](https://raw.githubusercontent.com/OperationSpark/using-c9/master/img/c9-signin-github.png)    
4. Creating an SSH key(between Github & cloud9)  
* Github  
        * Being signed in at Github.com, go to your profile icon in the top right and press settings  
        * go to the left sidebar and then into SSH and GPG keys  
        * press New SSH and give it a title of your choice (unless a teacher instructs otherwise)    
* Cloud9  
        * go to the gear icon in the top right corner  
        * navigate to the SSH keys tab  
        * copy/paste your SSH key (begins with ssh-rsa) into Github  
        * Add SSH key

---
## Repository Setup
_**To create your 1st repository...**_  
1. go to Github.com and click on the **(+)**, then click **New Repository**
    ![below is the snapshot attached](https://github-images.s3.amazonaws.com/enterprise/11.10.340/user/assets/images/help/repository/repo-create.png)    
2. Create a short and sweet name for your repository (for example: first-repo)  
3. Keep it **Public**, so people can check out your work, fork it, clone it, and add their own changes with your permission)  
4. Finally, click **Create Repository** (this will be your remote repository)  
5. After that, this screen will show up  
![screen of SSH](https://d186loudes4jlv.cloudfront.net/git/images/github_new_repo3.png)  
6. Copy/paste the two links under the section titled "or push an existing repository from the commnad line, one at a time"  
* After creating the repository on cloud9, follow the steps below and then continue with these two links spoken of above

_YAY for you! You successfully created your first repository and initialized a README.md file inside of it_

_**Add, Commit, and Push your First Changes...**_    
_Make your first repository on cloud9:_  
1. Go to c9.io and open your workspace      
2. (Begin typing in the command line) To make sure you're inside your workspace, type:
    ```
    cd ~/workspace
    ```   
3. Next, type:  
    ```
    mkdir and (the name you gave your first repository on github when making it)
    ```
    ```
    for example: mkdir first-repo
    ```   
4. Go inside of your repository by typing:
    ```
    cd (name of your repository) 
    ```    
5. Then, type:
    ```
    git init
    ```    

_Add a README.md file:_  
1. Since the remote repository was already created on github, in your command line on cloud9 after all the code you just typed, continue typing:
    ```
    touch README.md
    ```  
2. Then, as soon as you press enter after making it, you can either press on the file in the sidebar under the name of your repository or you can type:
    ```
    c9 README.md
    ```  
3. In the README.md file, type in a message that will show up in github (for example: This is my first repo )  
4. Press the keyboard keys "command" & "s" to save your work in the file  
5. In the command line, type:
    ```
    git add .
    ```  
6. Next, think of a good commit message that would be in the present tense, once again short, to the point, and about the change you just executed; type:
    ```
    git commit -m "the message you think would be right"
    ```
    ```
    for example: git commit -m "create readme.md"
    ```  
7. Copy/paste the links one at a time, like stated above, in the command line after following the directions(steps) listed before this one:
    ```
    git remote add origin git@github.com:biannak6288/3rd-repo.git
    ```
    ```
    git push -u origin master
    ```
---
## Workflow & Commands
Command        | Definition/Use
---------------| -------------
```git init```|Initializes git in the directory (repository); only done once when the folder is just created. If git is initialized in the wrong directory, then you technically would be working on your project in the wrong place and not the folder originally thought of therefore, you ```cd``` into the directory of your choice and then initialize git.
```git add .```|Adds the current/entire directory: all files that have changes to the cloud
``` git commit -m "message"```|Takes a snapshot of the files on the stage. The message should be present-tense and describe what was modified in the snapshot (short and specific)
``` rm -rf .git```|Uninitializes git in the working directory  (to completely remove your local repository, you type "rm -rf and your repo name"
```git push -u origin master```|Pushes committed changes into the repository
```git log```|This shows the previous commands in detail. It can show the date and message of when you committed the changev
```git diff ```|This checks the files differences between the current and previous commit
```q```|Quits the git diff mode
```git status```|Optional command that lets you see files that have been edited since the last commit (usually red or green)
```git add --all```|Includes all changes; including deleted files
```git remote -v```|See which remote repos are attached to your local repo
```git pull```|replays the changes in the remote until a new change is diverged into the new commit

**Cloning:** making a copy from your remote repository(lives in the cloud) to your local repository
* cloning your remote to rename it after deleting your local repository is done like this:
![snapshot is included](https://files.readme.io/YzvRCcWSxCKV70afj0Ux_GitHub%20-%20SSH%20-%202.png)
* In the command line of your new local repository after being cloned from its parent, type ``` git clone``` in the workspace and the link you copied
* after cloned, ```cd``` into that directory

**Forking:**Producing a personal copy of someone else’s project. This is how to fork a repository on Github:    
![forking snapshot](http://i.imgur.com/7wapvt2.png)

**Pull requests:** help make other people’s projects better by offering your changes to them about the original project  
Step 1:
![first step](http://i.imgur.com/CXlT0f4.png)   
Step 2: Add a description of what you want to change in the repository and submit your pull request
![step2](http://i.imgur.com/8l2heSy.png)






