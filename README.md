# PFI Github Introduction
This is a repo to demonstrate how to set up github with Eclipse and IntelliJ for MED2 Programming For Interaction (Programmering af Interaktive Systemer)

## Git Client
I recommend both having a command-line and GUI interface for working with Git.
* Git can be downloaded from https://git-scm.com/. This gives you a basic GUI client and a Git Bash, a powerful Command line tool for git.
    * I recommend **NOT** using vim, but chosing a different text editor. Personally I would recommend [Notepad++](https://notepad-plus-plus.org/) or [VS Code](https://code.visualstudio.com/) though any fast plain text editor is good
* In adition to Git, you will want a git client. 
    * [Github Desktop](https://desktop.github.com/) is a simple solution, but again I would recommend against it, as it is lacking in features. 
    * [SourceTree](https://www.sourcetreeapp.com/) is better, but needs to be set up initially with BitBucket and an Attlassian account, and then integrated.
    * [GitKracken](https://www.gitkraken.com/) is a good client, but many of its better features require a paid account.
    * [**Fork**](https://git-fork.com/) is a feature rich client with a simple interface. This gets my recommendation, and all examples will be using this client.
    
## Setting up a Repository
You can create repositories through your command line, your Git Client, or on Github. For simplicity sake, I recommend creating the repository on Github first.

### Via Github
1. Create a new repository, and give it a short but descriptive name.
    * I like to have a `README.md` file for documentation, though it is not necessary.
    * You can find a premade Java gitignore, but this doesn't have everything that you want.
2. Clone Your project from Github to your computer.
    * Click "Clone or Download" on your repository's home page, and copy the link (e.g. `https://github.com/EoinRaff/PFS_Github_Introduction.git`)
3. Use either your command line or client to clone the repository.

#### Via Command Line
1. Open your command line and navigate to the directory where you want to store your projects
    * If using git bash, you can (in windows, at least) navigate to this folder in the explorer, right-click and select "Git Bash here"
2. Use the `git clone` command followed by the address of you git repo to clone it (e.g. `$ git clone https://github.com/EoinRaff/PFS_Github_Introduction.git`)
    * Sometimes an error can occur here when pasting the address, so try typing it by hand
3. This will create a folder for your repository.

#### Via Fork

## .gitignore
Either add the `.gitignore` file from this repo, or edit your `.gitignore` to include the following lines:
```
# Eclipse
.classpath
.project
.settings/

# Intellij
.idea/
*.iml
*.iws

# Mac
.DS_Store

# Maven
log/
target/
```

As the name suggests, this file tells git what files to ignore.
Many files will be generated by your IDE (i.e. Eclipse or IntelliJ) or by Java when comiling and running your projects. 
These files do not need to be tracked by Git, as they will be automatically generated if they cannot be found.
As such, in order to keep your repository small and tidy, we ignore these files.
Likewise you may want to add files such as .png, .mp4 etc. if you have large texture or audio files, as they may be too large to upload to Github. 
* Git LFS exists for handling Large Files, though this has a tight storage limit on the free plan, and is somewhat complicated to manage. I will not go into it here, but it is worth knowing that it exists if you need it.
