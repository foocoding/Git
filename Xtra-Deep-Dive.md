# Lecture 5 - under the hood
This section is a deep dive for the students that want to learn more. This section is not required to learn.
1. Advanced commands


# 1. Advanced commands

## 1.1 Searching the history
- Searching for the abstract
- When was this **bug** introduced?
- When was this **feature** removed?
- When did our logo become **orange**?

Find the last commit that added or removed a reference to a specific function:
```
git log -S function_name
```
## 1.2 Searching the history - Bisect
Test if state is good or bad…
```
git bisect bad
git bisect good
```
When you are done...
```
git bisect reset
```
Automating bisect
```
git bisect start HEAD v1.0
git bisect run test-error.sh
```

## 1.3 Ordinals

      HEAD@{0}            (current value of HEAD)
      HEAD@{3}         	  (third prior value of HEAD)
      master@{0}  	      (current value of master)
      master@{yesterday}  (yesterday's value of master)
      master@{1.week.ago} (last week's value of master)

## 1.4 Git show
Explore git show.
What useful information can you find?
Write a cool alias that uses git show.
```
git show [options] <object>..
git show HEAD@{5}
git show master@{yesterday}
```

## 1.5 Reflog
Where has your HEAD been?
```
git reflog
git reflog --relative-date
git reflog HEAD
```

## 1.6 Dangling commits
It's still there, desperately clinging on

## 1.7 Pick and choose
We could have a really crappy branch, with one glorious commit.
Let's just pick that one and delete the branch.
```
git checkout master
git cherry-pick ed84249
git branch -d crappy
```
Git protects unintegrated branches
```
git branch -D monster
```

## 1.8 Rewriting history
Git is a very powerful tool.
It can even rewrite history.
But with great power comes great responsibility...
**Don't rewrite public history!**

Brute-forcing history. When all else fails and you are in PANIC.
```
git checkout master
git reset --hard HEAD~
git push -f origin master
```
This is **NOT** the correct way of undoing your last commit.

## 1.9 Amending mistakes
Let's commit foo!
```
git add foo.txt
git commit
```
Crud, we forgot bar!
```
git add bar.txt
git commit --amend
```
Now call git log, what happened?

## 1.10 Interactive rebase
Perfect for cleaning up before the push
```
git rebase -i [commit]
```
Hopefully, your local history is now nice and messy.
Time to perform an interactive rebase.
Clean up your history so it only contains nice, clean, commits.
One commit = one logical feature/addition

# Katas
A Kata is like an exercise, but it's structured in such a way that you should repeat it often, and the goal is to master it. To master it you need to do the Katas every week, until you find them easy, then do them more and more seldom.

Before doing the Katas, git clone the git-katas repository somewhere on your computer. When you want to do an Kata, change directory (`cd`) to the actual Kata folder. Follow the instructions on the instructions page (`README.md`) carefully.
```
git clone https://github.com/praqma-training/gitkatas.git
```

The below katas can be very hard, proceed with caution ;-)

[Kata 16: Bad Commit](https://github.com/praqma-training/git-katas/blob/master/bad-commit) - Cleaning up a bit.

[Kata 17: Reorder the History](https://github.com/praqma-training/git-katas/blob/master/reorder-the-history) - We might have created our commits in a suboptimal order, practice to fix that scenario here.

[Kata 18: Save my Commit](https://github.com/praqma-training/git-katas/blob/master/save-my-commit) - Should you accidentally or on purpose delete a commit, go here to try and save it.

[Kata 19: Reverted Merge](https://github.com/praqma-training/git-katas/blob/master/reverted-merge) - A merge has to be reverted, but this causes problems.

[Kata 20: Pre Push Hooks](https://github.com/praqma-training/git-katas/blob/master/pre-push) - A quick exercise in using Git hooks.

[Kata 21: Submodules](https://github.com/praqma-training/git-katas/blob/master/submodules) - Submodules are loathed by many. Run through this exercise to see what the ruckus is all about.

[Kata 22: Investigation](https://github.com/praqma-training/git-katas/blob/master/investigation) - Discover what is going on in a Git repo, figure out what it looks like under the hood.

[Kata 23: Objects](https://github.com/praqma-training/git-katas/blob/master/objects) - A small exercise into Git internals.
