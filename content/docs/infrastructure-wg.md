---
title: Infrastructure Working Group
bookToc: true
---
# Infrastructure Working Group (in the course of formation)
The infrastructure working group (IWG) understands the needs and pains of the 
community and shapes the project infrastructure to meet these needs. 

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

The focus of IWG members will be on identifying, designing and agreeing on 
infrastructure improvements. The implementation of the changes and the 
operations of our infrastructure can be offloaded to community members or 
contractors. This way we keep the workload for the working group low.

Working group members should have the oppurtunity to dedicate 4-8 hours per 
week on a regular basis in the initial phase, as we expect to have a significant 
pile of decisions to take. It should be less than 4 hours once the roadmap has 
become more stable.

We would like to have broad and diverse community representation within the 
working group as we are convinced such groups deliver the best results. Please
contact us if you want to participate.

Useful skill to bring to the committee or aquire while working there:
* Managing or hosting software development infrastructure
* Designing software development workflows and infrastructure
* Understanding needs of contributors and downstream users
* IT security and privacy
* Coordinating work in Open Source Projects
* Tools and technologies technologies currently used in the Infrastracture 
  (e.g. Mailman, AWS, GCP, Sphinx, GitHub, WWW development, buildbots, 
  Phabricator, ...)

Initial members:

* Christian Kühnel
* ... we're recruting plese contact us at TODO!

## Proposal for getting started

Proposal for steps to get the working group started.

1. Create email account for working group.
1. Advertise for the IWG and recruit initial group of >5 members (end of 
   January 2021).
1. Hold an initial meeting of the working group (in February 2021).
1. Agree on how we want to work and review/update this page (end of February 
   2021.)
1. Agree on infrastructure for the working group itself and set it up
   (issue tracker, mailing list, document storage, ...) (end February 2021).
1. Agree on intial set of the most pressing issues we want to work (end of 
   March 2021).
1. Prepare quick reports for the board meetings.
1. Give overview on current situation and roadmap during virtual EuroLLVM 
   dev meeting (in April 2021).

## Proposal for day-to-day work mode

This section describes a proposal for the flow for the day to day work of the 
working group. Note that only the good case is described here. A proposal can be
cancelled in any of these steps. There might also be some iterations as some 
parts of a statement of work (SOW) are not clear or feasible.

1. Anyone in the LLVM community (including contractors) can propose a change by 
   creating an issue on the issue tracker. 
1. The working group will create an statement of work (SOW) based on the  
   proposals they want to move forward on. The SOW will consist of a problem 
   description and (functional and non-functional) requirements for a solution 
   of the problem. The SOW shall be made public and discussed with the 
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

## Proposal for implementation and operations

To keep the workload for the IWG low and scale up the work, the implementation
of changes shall be mostly done by a 3rd party. 

*Operations of services* shall be done by contractors with whom we can have
Service Level Agreements (availibility, response times, recovery time, 
handling GDPR requests, ...).

For *implementing individual changes* there are a few options:
* Community volunteers: There is someone from the community willing to 
  implement the change.
* Community bounty: We're offering a bounty for a community member to implement
  the change. This is a chance to give back something to community members
  who are not paid for their contirbutions by some company or organisation.
* Contractor: In case something is very large or we can't find anyone to do it
  the work can be handed off to a contractor.


## Ideas for initial work items

This is an unsorted, unprioritized list of ideas the working group could look
into: 

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
  * clangd remote index for LLVM
  * [LNT service](http://lnt.llvm.org/)
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
  * Create a plan of the "important" buildbot configuration we need in order to 
    detect the bugs with large impact (contributors and downstream). Then have
    one central team/contractor operate these to ensure consistency and quality.
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
* Investigate if/where we need to have Terms of Service and Pricacy Agreements.
* Figure out where we need to be able to handle GDPR-related requests and
  how that could be done.
* Decide what to do with the mailing lists and GDPR deletion requests.
* Decide if we want to have mandatory pre-merge testing and what it should 
  look like.

## Links
* issue tracker and Kanban board (to be created)
* Discourse channel (to be created)
* Email account (to be created)
* Original proposal ([Google Doc](https://docs.google.com/document/d/1T7dJ9DgrgaJHN1RZ5vhJJ2D9CBwMQl6lOdN41QPsnAg/), 
  [PDF Export](/static/documents/infra-wg/Proposal_Infrastructure_Working_Group_2020-01-11.pdf))