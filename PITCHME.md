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
  * Easier to accept one feature, and not bundled changes
  *
* When creating a new feature branch, make sure it's created from the latests changes in NeTEx CEN master repository
* Keep this branch updated
* Clear and descriptive commit messages makes it easier to understand why something was changed
* Validate all pull requests (already available in the CEN repo)

----

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
https://github.com/NeTEx-CEN/NeTEx.git
```

---

## Checkout a feature branch

Remember: always pull from master before creating a new branch
```
git pull
```

Example creating a branch from the master branch
```
git checkout master -b journey_frequency_group_id_constraint_check
```

----

## Push that feature branch up remotely

```
git push --set-upstream origin journey_frequency_group_id_constraint_check
```
----

## What remotes do I have?
Side note: You can see what remotes you have by issuing the command:
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

For me, *origin* is the Entur fork. I like to name remotes after where they are located on github.

##