# Welcome to CMPT 221L: Software Development 2!

In this repository, you will find all of your labs for the semester. We will be leveraging Github to submit and review assignments. This will help us stay organized and expose you to some real-life best practices.

In this README, I've provided everything you need to get yourself set up for the semester, along with some helpful reminders.

# Getting Started
### Step 1: Download VSCode

First things first, you need a code editor to actually complete these labs. If you already have VSCode or another editor of your choosing, you can skip this step.

I strongly recommend using VSCode, as that's what I'll be using for demonstrations throughout the semester, but you can use whatever best suits you.

I like VSCode because it has a bunch of helpful features and (optional) plugins which will make navigating this course a breeze. You can download VSCode here: https://code.visualstudio.com/download

The first feature I recommend enabling is the `code .` feature. This will enable you to open VSCode from the command line by adding VSCode to your PATH (your PATH is an environmental variable that tells your computer where things are installed!).
1. Open VSCode
2. Click `View` ❯ `Command Palette`
3. Type `shell command` into the command palette to find `Shell Command: Install 'code' command in PATH` and click on it to install it.

### Step 2: Create a GitHub Account
If you already have an account, you can skip this step. If you're new to git, follow the instructions at https://github.com/signup.

### Step 3: Create a Personal Access Token
Git made things a little more complicated with 2FA. We are going to create a Personal Access Token to try and avoid some permission/authentication errors. If you already have a Personal Access Token, you can skip this step.
1. Log in to Github
2. Click on your profile picture in the top right corner ❯ `Settings`
3. Click on `Developer Settings` located at the bottom of the menu on the left.
4. Select `Personal Access Tokens` ❯ `Tokens (classic)`
5. Click `Generate new token` ❯ `Generate new token (classic)`
6. Name the token, pick an expiration, select all scopes, and click `Generate token`. 
7. Copy this token and keep it somewhere safe! If you're a MAC user, then your token should get saved to your keychain. If you're a Windows/Linux user, then it should get added to whatever the Windows/Linux equivalent is.

If Personal Access Tokens aren't working for you, or you want something more secure, create an SSH key for authentication using the instructions in the `Add an SSH Key to Github` section here: https://www.geeksforgeeks.org/how-to-authenticate-git-push-with-github-using-a-token/. This link also provides more infomation on creating and configuring tokens.  
  
**NOTE**: If you created an SSH key instead of a Personal Access Token, you'll want to use the `SSH URL` instead of the `HTTPS URL` moving forward.
 

### Step 4: Import the `cmpt221` Repository
We're importing instead of forking because you cannot control the visibility (i.e. public/private) of a fork. I want you all to have the option to choose your privacy.

1. Go to https://github.com/profphip/cmpt221-tmp
2. Click the `<code>` button and copy the [HTTPS URL](https://github.com/profphip/cmpt221-tmp.git) provided in the drop down box
3. Click on your profile picture in the top right corner ❯ `Your repositories`
4. Click `New` in the top right corner
5. Click the `Import a repository` hyperlink (https://github.com/new/import)
6. Paste the [HTTPS URL](https://github.com/profphip/cmpt221-tmp.git) in the source repository URL field and name the repository `cmpt221` (or whatever you'd like, but my instructions will reference `cmpt221`). Verify your credentials are correct, set your visibility, and click `Begin import`. The import will take a couple of minutes.

### Step 5: Add `profphip` as a Collaborator
This allows me to see the activity going on in your repository, create issues, review PRs, etc even if your repository is private.
1. Navigate to your forked  `cmpt221` repository
2. Click `settings` in the top menu bar
3. In the top of the left sidebar, click `Collaborators`.
4. Click `Add People` and type `profphip` into the text box. Click `Add profphip to this repository`

### Step 6: Clone your repository
You've created your repository, but you don't have the code locally on your computer yet. Clone your repo by clicking the `<code>` button, and copying the HTTPS URL provided in the drop down box. Then, open your terminal, use the `cd /path/to/directory` command to go to the directory of your choosing on your computer (I created a `git` folder), and issue the `git clone` command to clone your repository to your computer.
```bash
# this can be wherever you want!
cd /path/to/directory
git clone <HTTPS URL>
```
Once your repository is cloned and I'm added as a collaborator, you're all set!

# Working on & Submitting an Assignment
Submitting an assignment in this class might be different than how you submit an assignment in your other classes, but it simulates how your work will be reviewed in the real world. 
1. Whenever you want to work on a lab, create a new branch and give that branch the same name as the lab
    ```bash
    # create a new branch and switch to it
    git checkout -b "<lab name>"
    ```
2. Work on your lab in the branch. I recommend making multiple commits, and not one big one, but I'll leave the decision up to you. Just make sure you write up a somewhat detailed and/or entertaining commit message explaining what you're committing.
    ```bash
    git add . 
    git commit -m "your message here"
    git push
    ```
    **NOTE**: The first time you push, you might have to authenticate. You will also need to run the following commands to push your new local branch to your remote repository. You'll have to run these every time you make a new branch.
    ```bash
    git push --set-upstream origin <branch name>
    git push -u origin <branch name>
    ```
3. Once your assignment is complete and you're ready to submit it, push your code. Then, go to your `cmpt221` repository and click `Pull requests` in the top menu bar. Click `New pull request`. Keep the `base:main`, and select the branch you'd like to compare: `compare:<branch name>`. Then click `Create pull request`. Add a title and a description, and click `Create pull request`. Once the pull request is created, add `profphip` as a reviewer, copy the link to your pull request, and submit it under the corresponding lab in Brightspace. 