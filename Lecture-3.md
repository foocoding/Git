# Lecture 3
Section three of FooCoding Git. This focuses on these parts:
1. GitHub
2. Forking workflow
3. Pull requests
4. Issues in GitHub

In the end you can find **exercises/katas**.

# 1. GitHub

## 1.1 What is GitHub
GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

### Registering/Creating the account on GitHub
You need
- A valid Email address
- An SSH key-pair

## 1.2 Generating the ssh keypair

In the terminal, use:
```
ssh-keygen -t rsa -C "username@email.com"
```

Supply your Github email address instead of this fake one.

Accept the default location storage (default file) for the keys. When prompted for a passphrase, you can choose to make one up or just press enter to skip having a passphrase. If you make one up, don't forget it!

You will have `id_rsa` and `id_rsa.pub` files in the directory at the path `~/.ssh/`

**The `id_rsa` file is your private key, do not share it with anyone.**

You want to copy the contents of the id\_rsa.pub.
```
cat ~/.ssh/id_rsa.pub
```
After you copy the contents of the id\_rsa.pub file, Go to the GitHub account, go to the settings find SSH and GPG keys option and add New SSH key.

## 1.3 Creating a repository

Using your GitHub account, create a repository to which you can add files. Name the repository as `MyFirst`. Create a public repository and check the box to create a README file. After you create the repository, the URL of your web page would be something like https://github.com/kvarak/MyFirst. Replace kvarak with your username.

# 2 Forking workflow

In the Forking workflow, a developer pushes a completed feature to their own public repository instad of a shared one. After that, they create a pull request to let the project maintainer know that it's ready for review.

Since each developer has their own public repository, the pull request's source repository will differ from its destination repository.
The source repository is the developer's public repository and the source branch is the one that contains the proposed changes.
If the developer is trying to merge the feature into the main codebase, then the destination repository is the official project and
the destination branch is "master".

Steps in Forking Workflow:
* You fork a public repository
* You clone the repository (so that you have a working copy on your machine)
* You create a (feature) branch and make some commits
* You push the branch in your repository
* You create a pull request by navigating to your forked repository

[Here](https://www.youtube.com/watch?v=-o0yomUVVpU&index=2&list=PLVYDhqbgYpYUGxRdtQdYVE5Q8h3bt6SIA) you can also find a tutorial made by Daan explaining the same concepts of how we would like you to hand in your homework from now on.



# 3. Pull requests
Pull requests make it easier for developers to collaborate. They provide a user-friendly (web) interface for discussing
proposed changes before integrating them into the official project.
In the simplest form, pull requests are means for a developer to notify a team member that they have completed a feature. But the pull-request is more than just a notification. It's a dedicated forum where teammates can post feedback, push follow-up commits.

## What does a pull request contain:
When you create a pull request, you want another developer to pull a branch from your repository into their repository. This means that you need to
provide 4 pieces of information to create a pull request:
* the source repository
* the source branch
* the destination repository
* the destination branch

Pull requests can be used in conjunction with various workflows:
* Feature-branch workflow
* Gitflow workflow
* Forking workflow

# 4. Issues in GitHub

### 4.1 Connect your change with an issue

- Create issues in GitHub
  - `https://github.com/<yourusername>/<yourrepo>/issues`
- Add the issues to a card in Trello
  - Power-ups: GitHub
- Mention commits in an issue
  - `git commit -m”#X the message text”`
- Make commits that “fixes” the issue
  - `git commit -m”fix #X another message”`


# Katas
A Kata is like an exercise, but it's structured in such a way that you should repeat it often, and the goal is to master it. To master it you need to do the Katas every week, until you find them easy, then do them more and more seldom.

Before doing the Katas, git clone the git-katas repository somewhere on your computer. When you want to do an Kata, change directory (`cd`) to the actual Kata folder. Follow the instructions on the instructions page (`README.md`) carefully.
```
git clone https://github.com/praqma-training/gitkatas.git
```

[Kata 12: Git Reset](https://github.com/praqma-training/git-katas/blob/master/reset) - Reset is a powerful and slightly dangerous command if you do not know what you are doing. Go trough the three modes of resetting here.

[Kata 13: Basic Stashing](https://github.com/praqma-training/git-katas/blob/master/basic-stashing) - The first stride into stashing.

[Kata 14: Squashing](https://github.com/praqma-training/git-katas/blob/master/squashing) - A lot of small commits is good when you are working locally, but for sharing your code, it might be more beneficial to deliver your code changes in large sets. Go here to experiment with that.



[Exercise: Connect a commit with a GitHub Issue (TBD)]()

