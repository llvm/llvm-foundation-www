---
title: Branch Renaming
bookToc: true
---

# Renaming Default Branch to 'Main'

Many tech communities, including GitHub and Git, have moved away from the term
“master branch” and replaced it with “main branch” in an effort to remove
unnecessary references to slavery and use more inclusive terms.  This was also
discussed on the LLVM-dev mailing list and there was strong consensus from LLVM
Developers’ that the LLVM Project should also rename our master branch as well.
Now that an industry standard name has been selected by GitHub, the LLVM
Project can begin the renaming process of the default branch to “main”.

This change will occur at **06:00GMT on Monday, December 7, 2020**
(time is **GMT**, please adjust for your local timezone).

To make this as easy as possible we plan to do the following prior to
November 20, 2020:

* Create a new branch named 'test-main' on the llvm-project repository
  * This branch will be read-only except for the LLVMBOT account
  * Set up a GitHub action to mirror commits from 'master' to ‘test-main'
    automatically
  * Allow the configuration to soak for a few days to ensure everything works
* Create a new branch named “main” on the llvm-project repository
  * This branch will be readonly initially
  * Reuse the previous Github Action to mirror master to main
  * This configuration will stay in place until cut over takes place on Dec. 7

On December 7, 2020:

* We will lock the master branch and change it to be readonly (except the
  llvmbot account)
* Switch the GitHub action to mirror commits from the new main branch back to
  the old master branch
* Make a few test commits to ensure the GitHub action is functioning as expected
* Open the main branch to commits from community members
* In parallel, we will begin to work through the rest of the llvm organization
  repositories to update branch names as well
* We will update the developer policy to reflect the change in workflow

On January 28th, 2021:

* We will remove the ‘master’ branch from all repositories in the llvm
  organization

As we work towards December 7, 2020 we are going to set up a test of this system
on a fork of the llvm-project in order to simulate the cut over. If we
encounter any issues we will update the community on llvm-dev. We expect the
llvm-project repository to be unavailable to developers for approximately 1 hour
while the switch is made. Lockout will occur promptly at 06:00GMT on the 7th.
Certainly if we finish sooner, we will update llvm-dev to let everyone know the
repository is available for use once again.

## Instructions

It was noted on the mailing list it might be helpful to include some basic
instructions for folks requiring assistance with migrating to the new 'main'
branch.  Here are two examples of steps one might take to accomplish this task:

In my local llvm-project directory:

    git fetch origin
    git checkout origin/main -b main

When you are ready to remove your local 'master' branch run:

    git branch -d master

Here is an alternative approach provided by Mehdi Amini

    # if not already on the master branch
    git checkout master

    # Rename the branch locally
    git branch -m main

    # Update the tracking so that `git pull`/`git push` lookup the remote main
    git branch -u origin/main

## Status

Project status updates and news will be kept up to date and shared on this
webpage. Please refer to this page to find the most up to date information.

### As of 2020.11.12

* Following discussion on llvm-dev, we have reached a decision to rename the
  default branch for llvm-project
to 'main'
  * [Thread](https://lists.llvm.org/pipermail/llvm-dev/2020-June/142445.html)
* Tom Stellard is working through testing the GitHub actions used to keep
  branches in sync
* We anticipate having the new 'main' branch created and syncing with 'master'
  by November 20th

### As of 2020.12.02

* We have completed testing of the use of the llvmbot account to keep test-main
  branch in sync with the master branch
* We have dropped the test-main branch and have created the permanent main
  branch
* LLVMBOT is now keeping main in sync with master
* Unless any major issues are encountered in the next few days, we are on track
  to swap the default branch to main on December 7 as expected

### As of 2020.12.07

* We have updated the llvm-project repository to use the 'main' branch by
  default
* We have corrected issues with the commit mail-list integration
* The 'master' branch is now in "read-only" mode and will remain so until
  January 28th, 2021
* We are beginning to work through documentation and other projects in the llvm
  org to get them updated as well

### As of 2021.01.11

* We are working through the remaining repositories in the LLVM GitHub
  organization
* llvm-lnt & llvm-testsuite were updated to use main today
* We have sent emails out to other repository owners to enlist their assistance
  with renaming
* We still look good to have this effort wrapped up by the 28th of this month
