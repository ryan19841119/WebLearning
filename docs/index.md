# Git Configuration

1. Open your terminal application.
2. Type `git --version` to ensure Git is installed. Version 1.9.5 or upper is better. Check git-scm to download the latest version.
3. Type `git config --global user.name "USER NAME"`, replacing `USERNAME` with your first and last name.
4. Type `git config --global user.email "EMAIL"`, replacing `EMAIL` with the email account associated with your GitHub account.
5. Set the `core.autocrlf`.  Mac & Linux users: Type `git config --global core.autocrlf input`
6. Type `git config --list` to see your current configurations.

```bash
~ git --version
git version 2.8.1
~ git config --global user.name "Briana Swift"
~ git config --global user.email "sereces@github.com"
~ git config --global core.autocrlf input
~ git config --list
```
# Create the Remoto Repositoy on GitHub
1. On GitHub.com, [create a new repository](https://github.com/new).
2. Name your repository. The name of your repository will be part of the link to your website.
3. Enter a description for your repository. 
4. We recommend you create a public repository. Public repositories are free. Even if you select a private repository, your published website will be public. 
5. Check the box to initialize the repository with a README. 
6. Click **Create repository**.

# Choose a Github Pages Theme
1. With your repository created, click the **Settings** tab. 
2. On the Options sections (default information displayed), scroll down to the **GitHub Pages** section. 
3. Click **Choose a theme**.
4. Decide which theme you would like to use, and click **Select theme**.
5. Accept the filler text by scrolling to the bottom of the page and click on **Commit Changes**.
6. Your site is published at: `USERNAME.github.io/REPONAME`.

# Clone the Repository Using the Command Line
1. Navigate to the Code tab of the repository on GitHub.com. 
2. Click **Clone or download**.
3. Copy the **Clone URL** provided.
4. Open your command line/terminal application and `cd` into the directory where you would like to copy the repository. This can be anywhere in your local file system. 
5. Type `git clone URL`. Be sure to replace `URL` with the Clone URL you copied in the previous step. The repository will be cloned into a new directory in this location. 
6. Type `cd REPOSITORY-NAME` to move into the directory of the repository you just created. 
7. Type `git status`.

# Create Local Branches With Git
1. Create a new branch with a descriptive name:`git branch BRANCH-NAME`.
2. Type `git status` to see that although you created a new branch, you are still checked out to **master** (as indicated by the in-line response from Git). 
3. Check out to your new branch: `git checkout BRANCH-NAME`. 
4. Type `git status` to verify you are now checked out to your new branch.

# Make Local Changes With Git
1. Make sure you are checked out to the new branch you just creaed. You change branches by clickig the **Current Branch** button at the top of the application, then selecting a branch. 
2. Open your preferred text editor. 

# Add Local Commits With Git
1. Type `git status`. Remember that `git status` allows us to see the status of the files on our branch at any given time. Your file is listed under the heading *Untracked files*. 
2. Type `git add FILE-NAME`. This adds the file to the staging area and prepares it to become part of the next commit. 
3. Type `git status` again to see what has changed. Your file is now listed under the heading *Changes to be committed*. This tells us that the file is in the staging area. It also indicates this is a new file. 
4. Type `git commit`. This tells git to collect all of the files in the staging area and commit them to version control as a single unit of work. Git will open your default text editor where you can enter the commit message. 
5. Type the commit message, save and quit your editor. 
	* The default text editor associated with git is `vi` in most cases, which requires that you press the `Esc` key then type `:wq` to save and quit after entering your commit message. 
	* Alternatively, you can bypass `vi` altogether and enter your commit message inline with `git commit -m "your message"`
6. To see the history of commits, type `git log`. 

# Open a Pull Request on Github

1. Type `git push -u origin BRANCH-NAME` to push your commits to the remote, and set tracking branch. 
2. Enter your GitHub username and password, if prompted to do so. 
3. Crete a Pull Request on GitHub
4. Fill out the body of the Pull Request with information about the changes you're introducing. 

# Most important
1. `git clone URL`
2. `git branch BRANCH-NAME`
3. `git add FILE`
4. `git commit -m "MESSAGE"`
5. `git push -u origin "BRANCH-NAME"`
6. `git status`
7. `git log`

