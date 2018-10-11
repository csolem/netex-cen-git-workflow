## NeTEx GIT workflow?

---

## Example workflow

Example workflows for forked repositories

![workflow](images/workflow.png)

---

## Example workflow when you own the repository

![workflow](images/workflow_2.png)

Still possible to use a private fork if desirable

---

## Guidelines

* Keep feature branches small and manageable
* Easier to review
* Easier to see the difference with `git diff`
* Easier to revert (if required)
* It is easier to accept one feature without lots of other stuff

---

## Guidelines #2
* When creating a new feature branch, make sure it's created from the latests changes in NeTEx CEN master repository
* Keep the feature branch updated when working on it to detect and handle conflicts at an early stage
* Clear and descriptive commit messages makes it easier to understand why something was changed
* Validate all pull requests (already available in the CEN repo)

---

## Set up private key
It may not be necesarry but helps a lot when working with git, as you do not have to authenticate for every commit. This guide explains the process for mac/windows/linux:

https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/#platform-windows

---

## Use the command line for git

There are many tools for git. But most examples and guides on the internet are using command line.

Download git:
https://git-scm.com/downloads

---

## Git clone

Clone the repository

```
git clone https://github.com/NeTEx-CEN/NeTEx.git
```
```
cd NeTEx
```

---

## Checkout a feature branch

Remember: always pull from master before creating a new branch.
This ensures that changes are made on recent changes, and avoids merging issues later.
```
git pull
```

Example creating a branch from the master branch. Example branch name: *journey_frequency_group_id_constraint_check*
```
git checkout master -b journey_frequency_group_id_constraint_check
```

----

## Push that feature branch up remotely

```
git push --set-upstream origin journey_frequency_group_id_constraint_check
```
This allows other to follow your work.
If the laptop is run over by a car, the work will not be lost if changes were commited and pushed.


----

## What remotes do I have?
*Side note:* You can see what remotes you have by issuing the command:
```
git remote -vv
```

I have multiple remotes, the following is the output for NeTEx-CEN:
```
NeTEx-CEN	https://github.com/NeTEx-CEN/NeTEx.git (fetch)
NeTEx-CEN	https://github.com/NeTEx-CEN/NeTEx.git (push)
nick-knowles	https://github.com/nick-knowles/NeTEx.git (fetch)
nick-knowles	https://github.com/nick-knowles/NeTEx.git (push)
origin	git@github.com:entur/NeTEx.git (fetch)
origin	git@github.com:entur/NeTEx.git (push)
```

For me, *origin* is the Entur fork. Name remotes after where they are located on github.

---

## Prepare to do some changes
* First, make sure that you do not have uncommited changes before changing anything:
```
git status
```
* Then make sure your feature branch is up to sync with the master branch
```
git fetch
git merge master
```

---

## Do some changes in the feature branch
* Change files relevant to the feature branch
* To see what changes that have been done, execute `git diff`
* Àdd the file or files you want to commit:
```
git add examples/functions/calendar/NeTEx_Calendar_se_PA1.xml
```
* Commit with a descriptive message:
```
git commit -m "Fix NeTEx calendar example so that it validates."
```
* Push the changes remotely
```
git push
```

---

##



