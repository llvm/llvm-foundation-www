---
title: Infrastructure Working Group
bookToc: true
---
# Infrastructure Working Group (in the course of formation)

The infrastructure working group (IWG) understands the needs and pains of the
community and shapes the project infrastructure to meet these needs.

*Note:* This page is an initial proposal. We will improve our setup and work
mode as we go along and gain experience.

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

Working group members should have the opportunity to dedicate 4-8 hours per
week on a regular basis in the initial phase, as we expect to have a significant
pile of decisions to take. It should be less than 4 hours once the roadmap has
become more stable.

We would like to have broad and diverse community representation within the
working group as we are convinced such groups deliver the best results. Please
contact us if you want to participate.

Useful skill to bring to the committee or acquire while working there:

* Managing or hosting software development infrastructure
* Designing software development workflows and infrastructure
* Understanding needs of contributors and downstream users
* IT security and privacy
* Coordinating work in Open Source Projects
* Tools and technologies currently used in the Infrastructure
  (e.g. Mailman, AWS, GCP, Sphinx, GitHub, WWW development, buildbots,
  Phabricator, ...)

Members (in alphabetical order):

* Anton Korobeynikov
* Christian Kühnel
* Wei Wu
* ... we're recruiting please contact us at [iwg@llvm.org](mailto:iwg@llvm.org)!

## Proposal for getting started

Until we have found a permanent place for our work backlog, Christian
created a temporary [kanban board](https://github.com/ChristianKuehnel/iwg-workspace/projects/1)
so we can track the work.

## Proposal for day-to-day work mode

This section describes a proposal for the flow for the day to day work of the
working group. Note that only the good case is described here. A proposal can be
cancelled in any of these steps. There might also be some iterations as some
parts of a statement of work (SOW) are not clear or feasible.

1. Anyone in the LLVM community (including contractors) can propose a change by
   creating an issue on the issue tracker.
1. The working group will create a statement of work (SOW) based on the  
   proposals they want to move forward on. The SOW will consist of a problem
   description and (functional and non-functional) requirements for a solution
   of the problem. The SOW shall be made public and discussed with the
   community.
1. Once the SOW and it’s costs are clear enough, the working group will decide
   if and how it shall be implemented (community contribution, paid community
   bounty, contractor)
    1. If it requires spending money, the working group will propose the change
       to the board and go through a Request for Proposal process (RFP). The
       details of that RFP process need to be worked out.
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
Service Level Agreements (availability, response times, recovery time,
handling GDPR requests, ...).

For *implementing individual changes* there are a few options:

* Community volunteers: There is someone from the community willing to
  implement the change.
* Community bounty: We're offering a bounty for a community member to implement
  the change. This is a chance to give back something to community members
  who are not paid for their contributions by some company or organisation.
* Contractor: In case something is very large or we can't find anyone to do it
  the work can be handed off to a contractor.

## Ideas for initial work items

Until we have a permanent solution for our backlog, Christian started to collect
ideas for work items in a
[list](https://github.com/ChristianKuehnel/iwg-workspace/blob/main/collection_of_work_items.md).

## Links

* [GitHub project](https://github.com/llvm/llvm-iwg)
* [Discourse category](https://llvm.discourse.group/c/infrastructure/iwg/42)
* [Discord channel](https://discord.com/channels/636084430946959380/802119671780081674)
* Email address: [iwg@llvm.org](mailto:iwg@llvm.org)
* Original proposal: ([Google Doc](https://docs.google.com/document/d/1T7dJ9DgrgaJHN1RZ5vhJJ2D9CBwMQl6lOdN41QPsnAg/),
  [PDF Export](/static/documents/iwg/Proposal_Infrastructure_Working_Group_2020-01-11.pdf))
