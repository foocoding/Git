# Lecture 1
Section one of FooCoding Git. This focuses on these parts:
1. Version Control
2. Terminal Time
3. Singleplayer Git

In the end you can find **exercises/katas**.

# 1. Version Control

## 1.1 What is Git, Etymology and a short history.
- [ ] How was SW managed before version control was used
- [ ] Why do we need a version control software (VCS)?
- [ ] Version Control (aka Revision control, source control)
- [ ] Git remote model; distributed version control system
- [ ] Why do we choose Git?

# 2. Terminal Time

## 2.1 Why are we using the terminal?
- [ ] Educational - *no magic buttons*
- [ ] Usability - *most complete interface*
- [ ] Customizable - *aliases, shortcuts and hooks*

## 2.2 Installing Git
 For Windows,
 install Git Bash:
 https://git-scm.com/downloads *(Note, when you install it, use all defaults, but if you don't have any personal preference, then selecting **`Nano`** as your editor is recommended.)*

 For Linux, open gnome-terminal for GNome desktops  or Konsole for KDE desktops and type the command to install git based on your Linux distribution.

 For a RedHat based Linux (Like CEntOS)
```
 sudo yum install git
```

 For Fedora
```
 sudo yum install git-core
```

 For a Debian based Linux (like Ubuntu)
```
 sudo apt-get install git
```

 For Arch Linux
```
 sudo paceman -Sy git
```

 For Gentoo Linux
```
 sudo emerge ask —verbose dev-util/git
```

 For a MAC, open Terminal and execute following command
```
 brew install git
```

## 2.3 Bash commands

### 2.3.1 Navigating
- Where am I?
```
pwd
```
- Create folder
```
mkdir theplace
```
### 2.3.2 Manipulating
- Put this in a file (replacing content)
```
echo "Hello world!" > file.txt
```
- Append this to the file
```
echo "Another line" >> file.txt
```
- What’s in that file?
```
cat file.txt
```
### 2.3.3 Finding
- What’s in here?
```
ls
```
- Go there!
```
cd theplace
```
### 2.3.4 Pointers to places
- This directory
```
cd .
```
- Parent directory
```
cd ..
```
- Root directory
```
cd /
```
- Home directory
```
cd ~
```

# 3. Singleplayer Git
## 3.1 Basic git commands
- Cloning a repository
  - `git clone`
- Exploring the repository
  - `git status`
  - `git log`
- Letting Git know you
  - `git config`

## 3.2 Letting Git know you
```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor nano
```

## 3.3 Creating a repository
Create a new directory in your home directory or any other suitable location using
```
mkdir hello-world
# Enter it
cd hello-world
# and create a new git repository using
git init
```
You can clone a repository with `git clone <URL>` command. This copies the repository from a remote machine and initializes it on your machine. You can try to clone some public repositories on github.com. For instance the gitkatas repository that will be used later on. `git clone` will create a local folder with the same name as the repository.
```
git clone https://github.com/praqma-training/gitkatas.git
```

## 3.4 A first commit
- Staging files
```
git add myScript.bat
```
- See it staged
```
git status
```
- Get an overview of file changes
```
git diff
```
- Commit your change
```
git commit -m "My first commit!"
```

# Fun snack: Time to customize!
Aliases are a great way to speed up your command line experience.

**Simple commit alias**
```
git config --global alias.co "commit"
```
**Pretty log alias**
```
git config --global alias.sl "log --graph --oneline --pretty"
```
**Log alias to show the last 20 commits in a pretty format**
```
git config --global alias.l20 "log -n 20 --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --all"
```


# Katas
A Kata is like an exercise, but it's structured in such a way that you should repeat it often, and the goal is to master it. To master it you need to do the Katas every week, until you find them easy, then do them more and more seldom.

Before doing the Katas, git clone the git-katas repository somewhere on your computer. When you want to do an Kata, change directory (`cd`) to the actual Kata folder. Follow the instructions on the instructions page (`README.md`) carefully.
```
git clone https://github.com/praqma-training/gitkatas.git
```

[Configure Git](https://github.com/praqma-training/git-katas/tree/master/configure-git)

[Kata 1: Basic Commits](https://github.com/praqma-training/git-katas/tree/master/basic-commits) - Very basic creation of commits.

[Kata 2: Basic Staging](https://github.com/praqma-training/git-katas/blob/master/basic-staging) - interacting with the stage (index).

[Kata 3: Basic Branching](https://github.com/praqma-training/git-katas/blob/master/basic-branching) - The first stride into branching.

[Kata 4: Basic Cleaning](https://github.com/praqma-training/git-katas/blob/master/basic-cleaning) - Cleaning the workspace.

[Kata 5: The Ignore-file](https://github.com/praqma-training/git-katas/blob/master/ignore) - The basics of using the `.gitignore` file.

