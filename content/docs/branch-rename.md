---
title: Branch Renaming
bookToc: true
---
# Renaming Default Branch to 'Main'

In response to community request and in order to facilitate more inclusive language used throughout
the LLVM project space we will be renaming the default branch of llvm-project to 'main'. This change
will occur at **06:00GMT on Monday December 7, 2020** (time is **GMT**, please adjust for your local timezone).

To make this as easy as possible we plan to do the following prior to November 20, 2020:
* Create a new branch named 'test-main' on the llvm-project repository
    * This branch will be readonly except for the llvmbot account
    * Setup a GitHub action to mirror commits from 'master' to 'test-main' automatically
    * Allow the configuration to soak for a few days to ensure everything works
* Create a new branch named 'main' on the llvm-project repository
    * This branch will be readonly initially
    * Reuse the previous Github Action to mirror master to main
    * This configuration will stay in place until cutover takes place on the Dec. 7 


On December 7, 2020:
* We will lock the master branch and change it to be readonly (with the exception of llvmbot)
* Switch the GitHub action to mirror commits from the new main branch back to the old master branch
* Make a few test commits to ensure the GitHub action is functioning as expected
* Open the main branch to commits from community members
    * At this time all users will be required to now make commits to the main branch
* We will also update the developer policy to reflect the new workflow


As we work towards December 7, 2020 we are going to setup a test of this system on a fork of the llvm-project
in order to simulate the cutover. If we encounter any issues we will update the community on llvm-dev.
We expect the llvm-project repository to be unavailable to developers for approximately 1 hour while the
switch is made. Lockout will occur promptly at 06:00GMT on the 7th. Certainly if we finish sooner, we will
update llvm-dev to let everyone know the repository is available for use once again.


## Status

Project status updates and news will be kept up to date and shared on this webpage. Please refer to this page 
to find the most up to date information.

#### As of 2020.11.12
* Following discussion on llvm-dev, we have reached a decision to rename the default branch for llvm-project
to 'main'
    * https://lists.llvm.org/pipermail/llvm-dev/2020-June/142445.html
* Tom Stellard is working through testing the GitHub actions used to keep branches in sync
* We anticipate having the new 'main' branch created and syncing with 'master' by November 20th
