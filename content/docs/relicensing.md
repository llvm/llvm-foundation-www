---
title: Relicensing
bookToc: true
---

# LLVM Relicensing Effort

The LLVM relicensing effort aims to modernize the LLVM Licensing structure and
developer policy. The high level goals of the relicensing effort are to:

* Encourage ongoing contributions to LLVM by preserving a low barrier to entry
  for contributors
* Protect users of LLVM code by providing explicit patent protection in the
  license
* Protect contributors to the LLVM project by explicitly scoping their patent
  contributions with this license
* Eliminate the schism between runtime libraries and the rest of the compiler
  that makes it difficult to move code between them
* Ensure that LLVM runtime libraries may be used by other open source and
  proprietary compilers

This project involves sensitive legal issues and has been a multi-year
effort. The primary public discussions have included these mailing list threads:

* October 19, 2015: [Initial license draft proposal](http://lists.llvm.org/pipermail/llvm-dev/2015-October/091536.html)
* September 12, 2016: [Second license draft](http://lists.llvm.org/pipermail/llvm-dev/2016-September/104778.html)
  , resolving GPL2 compatibility concerns
* April 17, 2017: [Third license draft](http://lists.llvm.org/pipermail/llvm-dev/2017-April/112142.html)
  , which resolved concern about use of LLVM runtimes with proprietary
  toolchains
* August 7, 2017: [LLVM Developer Policy wording](http://lists.llvm.org/pipermail/llvm-dev/2017-August/116266.html)

Beyond that, these topics have also been discussed by, and include contributions
from, over a dozen lawyers and key LLVM contributors, and have been discussed
informally with hundreds of people in the LLVM Developer Meeting BoFs. The
effort has been overseen by Heather Meeker, who is the LLVM Foundation’s legal
counsel. If you have questions or concerns about the content of this document,
please email the [llvm-dev mailing
list](http://lists.llvm.org/cgi-bin/mailman/listinfo/llvm-dev) or the [LLVM
Foundation Board](mailto://board@llvm.org) depending on the sensitivity of your
email.

## Status and Documents

At this point, we have achieved community consensus on:

* The goals of the relicensing effort
* License Full Name: "Apache 2.0 with LLVM Exception"
* [SPDX License Identifier](https://spdx.org/licenses/):
  "Apache-2.0 WITH LLVM-exception"
* The license text itself. This is [the expected LICENSE.TXT file](/relicensing/LICENSE.txt)
* The revised LLVM [developer policy patch](/relicensing/devpolicy.patch)

We also have worked with our legal counsel to build several more boring pieces:

* A new top-of-file header block that is minimal and includes the relevant and
  important information about the new license
* An individual agreement to relicense and a form to collect information
  necessary for completing the relicensing
* A corporate agreement to relicense that is available for companies to sign
  and has begun to be distributed to some of the known and/or large contributors

We currently plan to install the new developer policy and add the new license in
January 2019 after the LLVM 8.0 release has branched.

Once that is done, we will still need need to:

* Enact a process for getting 100% of existing code relicensed with the above
  agreements or rewrite/remove the code
* Drop the old license when the entire codebase is covered under the new
  license

## New File Header

The new file header will be:

    //===-- file/name - File description ----------------------------\*- C++ -\*-===//
    //
    // Part of the LLVM Project, under the Apache License v2.0 with LLVM Exceptions.
    // See https://llvm.org/LICENSE.txt for license information.
    // SPDX-License-Identifier: Apache-2.0 WITH LLVM-exception
    //
    //===----------------------------------------------------------------------===//

Some notable aspects of the new header:

* There is no explicit copyright notice -- these had little value and tended
  to not be maintained

* It is designed to be as compact and minimalist as possible while having the
  critical information: that it is part of LLVM, what license it is under,
  where to find that license, and the machine-scrapable SPDX markup to help
  people doing license audits

## Individual Relicensing Agreement

Individuals need to complete [a web
form](https://goo.gl/forms/X4HiyYRcRHOnTSvC3) that we will use to drive the
relicensing process. Part of that form will prompt them with a DocuSign
agreement that they can sign online to cover anything they personally
contributed. It will also collect any companies or academic institutions that
may own right to some of their contributions so that we can cover them with the
corporate agreement below.

We do ask that individuals generally sign the individual agreement even if they
think their contributions are probably covered by a corporate agreement. It will
be fairly expensive for us to validate each case where an individual has not
signed that \*all\* of their contributions are covered by a corporate
agreement. The individual agreements let us not spend time and money on this by
covering things either way. We think this is likely simpler and definitely less
expensive. Still, we are leaving all of the options open.

Feel free to send questions concerns about this to the [Foundation mailing
list](mailto://llvm-foundation@lists.llvm.org).

## Corporate Relicensing Agreement

Corporations may sign an agreement to relicense their contributions to LLVM
under the new license [with DocuSign](https://na3.docusign.net/Member/PowerFormSigning.aspx?PowerFormId=5a2bb38c-41c4-4ce0-a26e-52a7eb8ae51c)
. This is our preferred mechanism for collecting signatures. However, if your
company requires it, you can print out [this PDF of the agreement](https://drive.google.com/open?id=1FiHyH__qqr6Ki2RXDEAcP7SEYFhsawNo)
, sign it, scan it, and send the signed version as a PDF attachment to the [LLVM
Foundation Board](mailto://board@llvm.org). Further, if your company has a
specific concern or issue with the agreement, please reach out to the [the
board](mailto://board@llvm.org) and we'll try to help.

**Companies that have Signed:**

{{< expand >}}

* 3DExcite GmbH
* AMD
* ARM
* Access Softek
* Andes Technology
* Apple
* Argonne National Laboratory
* Autodesk
* Azul Systems, Inc.
* BUGSENG srl
* Barcelona Supercomputing Center
* Battelle Memorial Institute Pacific Northwest Division operator of Pacific
  Northwest National Laboratory
* Bluware Inc.
* CERN
* Ceemple Ltd.
* Cisco
* Citus Data
* Cobham Gaisler AB
* CodeWeavers
* Codeplay
* Cray
* Embecosm Limited
* EnterpriseDB
* Ericsson
* Facebook
* Fermi Research Alliance, LLC, operator of Fermi National Accelerator
  Laboratory
* Google
* GrammaTech, Inc
* Graphcore
* Huawei
* IBM
* Imagination Technologies
* Imperial College London
* Intel
* JetBrains
* Julia Computing, Inc.
* Linaro
* Linguamatics
* M-Labs Limited
* Mentor Graphics Corporation
* Microsoft
* Mozilla
* Newton Nordic
* Nvidia
* Octasic Inc.
* PTScientists GmbH
* Qualcomm
* QuarksLab
* RT-RK Computer Based Systems LLC
* RWTH Aachen University, ITC
* Red Hat
* RemObjects Software
* SAP SE
* SAS Institute Inc.
* ST Microelectronics
* Sony
* Synopsys, Inc.
* The Aerospace Corporation
* The FreeBSD Foundation
* The Linux Foundation
* The NetBSD Foundation
* The Qt Company
* UIUC
* UT-Battelle, LLC (operating Oak Ridge National Laboratory)
* Uberchord Engineering GmbH
* Wave Computing, Inc. (owner of MIPS, etc.)
* lowRISC
* XMOS

{{< /expand >}}

A list of companies that have been contacted about relicensing is below. This is
primarily intended to avoid duplicate work within these companies trying to get
things signed and set up.

{{< expand >}}

* INRIA
* LLNL
* MIT
* Path Scale
* Samsung

{{< /expand >}}

## Next Steps and Schedule Estimate

Our goal is to openly and transparently communicate our process, including the
expected next steps and a timeframe that can be used for planning. That said, we
are dealing with a lot of unknowns, so while we believe the following schedule
is achievable, this is not a guarantee:

* ~January 2019: Coincident with the final release branch date for LLVM 8.0,
  we will install the new developer policy. To ensure that all contributors
  have agreed to the terms of the new developer policy, we will rescind commit
  access from all contributors who are not covered by a corporate or
  individual agreement at that point. We will develop a policy for affected
  contributors to regain commit access.

When these steps are done, all new contributions will be under the new license
structure, and we expect that a significant amount of prior contributions will
be relicensed under the new structure. At that point, we will scope and define
the process for chasing down the long tail of prior contributions that are not
covered and resolve them on a case-by-case basis.
