---
title: Infrastructure Working Group
bookToc: true
---
# Infrastructure Working Group
The infrastructure working group (IWG) understands the needs and pains of the 
community and shapes the project infrastructure to meet these needs. 

The focus of the IWG will be on identifying, designing and agreeing on 
infrastructure improvements. The implementation of the changes and the 
operations of our infrastructure can be offloaded to community members or 
contractors. This way we keep the workload for the working group low.

## Scope

The working group will work on the LLVM project infrastructure including:

* source code repository
* bug tracker
* build servers/machines
* web sites
* build system/scripts
* code review tool
* mailing lists
* internet forum
* chat
* Documentation of the tools and their work flows.


## Working group members

We would like to have broad and diverse community representation within the 
working group as we are convinced such groups deliver the best results. Please
contact us if you want to participate.

Initial members:

* Christian Kühnel
* ... we're recruting plese contact us at TODO!

## Proposal for getting started

Proposal for steps to get the working group started.

1. Advertise for the IWG and recruit initial group of >5 members by the end of 
   2020.
1. Agree on how we want to work and review/update this page end January 2021.
1. Agree on infrastructure for the working group itself and set it up
   (issue tracker, mailing list, document storage, ...) end January 2021.
1. Agree on intial set of the most pressing issues we want to work end of 
   February 2021.

## Proposal for day-to-day work mode

This section describes a proposal for the flow for the day to day work of the 
working group. Note that only the good case is described here. A proposal can be
cancelled in any of these steps. There might also be some iterations as some 
parts of the SOW are not clear or feasible.

1. Anyone in the LLVM community (including contractors) can propose a change by 
   creating an issue on the issue tracker. 
1. The working group will create an statement of work (SOW) based on the  
   proposals they want to move forward onit. The SOW will consist of a problem 
   description and (functional and non-functional) requirements for a solution 
   of the problem. The SOW shall be made public and discusses with the 
   community.
1. Once the SOW and it’s costs are clear enough, the working group will decide 
   if and how it shall be implemented (community contribution, paid community 
   bounty, contractor)
    1. If it requires spending money, the working group will propose the change 
       to the board.
    1. The board will then review and approve the expenditure.
    1. The Foundation will set up the contract and manage the payments.
1. The working group will work with the contractor/community on a day-to-day 
   basis to get the work done.
1. The working group will approve the work and authorize payments with the 
   treasurer (if needed).

All of this shall be open and transparent for the community. Feedback from the
community is appreciated in all of these steps. In parallel to this, community 
members are welcome to take over certain SOWs and will get help from the 
respective contractor if needed. If that work touches shared infrastructure or 
impacts the future maintenance, the solution needs to be agreed with the 
working group and the contractor.


## Ideas for initial work items

This is an unsorted list of ideas the working group could look into: 

* Run a survey in the community to understand the largest pain points and 
  prioritze potential improvements.
* Create and maintain a public documentation of the existing infrastructure and 
  the supported workflows (what, why, who), including down-stream usages of 
  LLVM.
* Define and agree a vision for LLVM infrastructure and for the design 
  principles thereof: What should the development workflow and the 
  infrastructure look like?
* Identify the need for addons for Github the community is missing right now 
  (e.g. subscribing to labels on Github Issues).
* Come to a decision on using Phabricator vs. GitHub Pull Requests for code
  reviews, then implement the change.
* Create a roadmap for the handover of the existing infrastructure to a 
  contractor. Components ready for immediate takeover:
  * Phabricator (in case we stay with it)
  * Pre-merge testing
  * Buildbot workers
  * ...
* Create new design and structure for the LLVM website, migrate the existing 
  content there.
* Create a test strategy for the LLVM project and refactor the existing build 
  infrastructure to meet the new test strategy. Some ideas:
  * Multi-stage CI: run “cheap” builds first, run “expensive” builds only on
    commits where the cheap builds have passed.
  * Set up a collector dashboard showing build results for all CI systems per 
    commit, e.g. Treeherder or something GitHub based.
  * Investigate if we can get a good deal from GitHub Actions with sponsored 
    hardware.
* Gather user feedback on the existing infrastructure: Where are the pain 
  points? What would our community like to see improved?
* Migration of all python scripts and tools to Python 3 as Python 2 is 
  deprecated.
* Reach out to downstream infrastructure teams (e.g. Rust, Tensorflow) and 
  understand if we have infrastructure topics we want to cooperate on.
* Define Service Level Objectives (SLO) for our infrastructure and monitor 
  them. Set up monitoring and altering for our infrastructure.  Derive measure
  where we do not meet our SLOs.
* Migrate Windows setup instructions off GnuWin32 as it’s deprecated and add
  installation instructions users can copy-and-paste into their shell.
* Investigate the Rust project infrastructure and see what would be helpful to 
  LLVM. Some examples:
  * Create a benchmark tool to compare the performance of the compiler and the
    compiled code across versions, there is also a project for that.
  * Set up some central source of truth for managing user accounts, group
    membership and user/group permissions. Then configure all tools 
    accordingly.

## Links
* issue tracker and Kanban board (to be created)
* Discourse channel (to be created)
* Mailing list (to be created)