# Welcome to CMPT 221L: Software Development 2!

In this repository, you will find all of your labs for the semester. We will be leveraging Github to submit and review assignments. This will help us stay organized and expose you to some real-life best practices.

In this README, I've provided everything you need to get yourself set up for the semester, along with some helpful reminders.

# Getting Started
### Step 1: Download VSCode

First things first, you need a code editor to actually complete these labs. If you already have VSCode or another editor of your choosing, you can skip this step.

I strongly recommend using VSCode, as that's what I'll be using for demonstrations throughout the semester, but you can use whatever best suits you.

I like VSCode because it has a bunch of helpful features and (optional) plugins which will make navigating this course a breeze. You can download VSCode here: https://code.visualstudio.com/download

The first feature I recommend enabling is the `code .` feature. This will enable you to open VSCode from the command line by adding VSCode to your PATH (your PATH is an environment variable that tells your computer where things are installed!).
1. Open VSCode
2. Click `View` ❯ `Command Palette`
3. Type `shell command` into the command palette to find `Shell Command: Install 'code' command in PATH` and click on it to install it.

### Step 2: Create a GitHub Account
If you already have an account, you can skip this step. If you're new to Github, follow the instructions at https://github.com/signup.


### Step 3: Import the `cmpt221` Repository
We're importing instead of forking because you cannot control the visibility (i.e. public/private) of a forked repository. I want you all to have the option to choose your privacy.

1. Go to https://github.com/profphip/cmpt221-tmp
2. Click the `<code>` button and copy the [HTTPS URL](https://github.com/profphip/cmpt221-tmp.git) provided in the drop down box
3. Click on your profile picture in the top right corner ❯ `Your repositories`
4. Click `New` in the top right corner
5. Click the `Import a repository` hyperlink (https://github.com/new/import)
6. Paste the [HTTPS URL](https://github.com/profphip/cmpt221-tmp.git) in the source repository URL field and name the repository `cmpt221` (or whatever you'd like, but my instructions will reference `cmpt221`). Verify your credentials are correct, set your visibility, and click `Begin import`. The import will take a couple of minutes.

### Step 4: Add `profphip` as a Collaborator
This allows me to see the activity going on in your repository, create issues, review PRs, etc even if your repository is private.
1. Navigate to your `cmpt221` repository
2. Click `settings` in the top menu bar
3. In the top of the left sidebar, click `Collaborators`.
4. Click `Add People` and type `profphip` into the text box. Click `Add profphip to this repository`

### Step 5: Clone your repository
You've created your repository, but you don't have the code locally on your computer yet. Clone your repo by clicking the `<code>` button, and copying the HTTPS URL provided in the drop down box. Then, open your terminal, use the `cd /path/to/directory` command to go to the directory of your choosing on your computer (I created a `Github` folder), and issue the `git clone` command to clone your repository to your computer.
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
2. Work on your lab in the newly created branch. When you're ready to commit and push your changes, write up a somewhat detailed and/or entertaining commit message explaining what you're committing. Please don't push your changes at once, rather, complete a section of the lab, then push those changes. You should have multiple commits for each lab.
    ```bash
    git add . 
    git commit -m "your message here"
    git push
    ```
    **NOTE**: The first time you push, you might have to authenticate by signing into Github. You will also need to run the following commands to push your new local branch to your remote repository. You'll have to run these every time you make a new branch.
    ```bash
    git push --set-upstream origin <branch name>
    git push -u origin <branch name>
    ```
3. Once your assignment is complete and you're ready to submit it, push your code. Then, go to your `cmpt221` repository and click `Pull requests` in the top menu bar. Click `New pull request`. Keep the `base:main`, and select the branch you'd like to compare: `compare:<branch name>`. Then click `Create pull request`. Add a title and a description, and click `Create pull request`. Once the pull request is created, add `profphip` as a reviewer, copy the link to your pull request, and submit it under the corresponding lab in Brightspace. 