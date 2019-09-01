# Lecture 4
Section four of FooCoding Git. This focuses on these parts:
1. Multiplayer Git

# 1. Multiplayer Git

## 1.1 Remotes
- `git remote -v`
- `git remote add <name> <url>`
- `git remote rm <name>`
- Remote tracking branches

**Fetch**
- `git fetch`
- `git fetch <remote>`
- `git fetch <remote> <branch>`

**Pull**
- `git pull <remote>`
- `git pull --rebase`


# Katas
A Kata is like an exercise, but it's structured in such a way that you should repeat it often, and the goal is to master it. To master it you need to do the Katas every week, until you find them easy, then do them more and more seldom.

Before doing the Katas, git clone the git-katas repository somewhere on your computer. When you want to do an Kata, change directory (`cd`) to the actual Kata folder. Follow the instructions on the instructions page (`README.md`) carefully.
```
git clone https://github.com/praqma-training/gitkatas.git
```

[Kata 15: Rebase Branch](https://github.com/praqma-training/git-katas/blob/master/rebase-branch) - Using rebase as an alternative to merging.


# Group exercises

## Multiplayer Git 1
- Split up in groups of ~3
- Come up with a witty team name
- Create and clone a shared repository on GitHub
```
git clone ssh://<remote url>/<witty team name>.git
```
- Add a file `<your name>.txt` on the `master` branch. In the file:
- Write a fun title
- Draw a small ASCII art drawing to show off your skills
- Every useful change should be separate commit. Share often.
- Use `git push` and `git pull`.

## Multiplayer Git 2

- Split up in groups of ~3
- Come up with a witty team name
- Create and clone a shared repository on GitHub
```
git clone ssh://<remote url>/<witty team name>.git
```
- Build a fully functional ASCII art house together
- Deliver to house.txt on the master branch:
  - A door
  - A roof
  - A garden
- Cooperate and keep adding things to show off your ASCII art skills
- Use `git push` and `git pull --rebase`.


