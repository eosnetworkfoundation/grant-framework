<img src="img/enf-header.png" />

# EOS Network Foundation Grant Framework

> **Sunset Notice**
> 
> This initiative has been sunset, and we are no longer accepting grant applications. 
> 
> If you want to pursue funding for EOS projects you can reach out to [EOS Labs](https://www.eoslabs.io/) or [EOS Network Ventures](https://eosnetworkventures.com/).

As part of the EOS Network Foundation's (ENF) charter to grow and support the EOS ecosystem, the ENF has developed a multi-level grant program to help power research, software development, and maintenance of the [Antelope](https://antelope.io/) code base.  For more information about the ENF, please visit our [website](https://eosnetwork.com/funding/) or [YouTube account](https://www.youtube.com/c/EverythingEOS).

## Grant Guidelines
Individuals, small teams, and companies are all permitted to apply for grants. The purpose of the grants is to enable developers, businesses and individuals to build on EOS.  Grants [vary in size](#grant-levels) based on the size and scope of the initiative.  All forms of projects are open for submission, core chain modifications, tools, libraries, etc. as long as they are fully open-source.  Strong technical projects that clearly add to the Public Good are preferred.
The odds of getting your project approved increase if you follow our [acceptance recommendations](docs/acceptance-recommendations.md).  In all cases, you must meet the following [minimum requirements](docs/minimum-requirements.md).
## Grant Levels
The EOS Network Foundation (ENF) funds development grants for "Public Good" as well as those to “for profit” entities - with the goal that all grants will enhance the EOS community. Grants proposals are accepted in three levels, each having different amounts and acceptance criteria.  ENF Grants have guidelines, an application process, and a multi-stage approval process.  They also have a milestone based pay-out system.
<table width="100%">
  <tr><th>&nbsp;</th><th>Individual / Small</th><th>Team / Medium</th><th>Company / Large</th></tr>
  <tr><td><b>Amount</b></td><td align="center">Up to $10,000</td><td align="center">Up to $50,000</td><td align="center">Up to $200,000</td></tr>
  <tr>
    <td valign="top"><b>Requirements</b></td>
    <td valign="top"><ul><li>No prior Pomelo grant required</li><li>Selection by Grant Committee</li><li>2 Grant Evaluator approvals</li></ul></td>
    <td valign="top"><ul><li>Prior <a href="https://pomelo.io/">Pomelo grant</a> required</li><li>Selection by Grant Committee</li><li>3 Grant Evaluator approvals</li></ul></td>
    <td valign="top"><ul><li>Special KYC process</li><li>Selection by Grant Committee</li><li>4 Grant Evaluator approvals</li><li>Prior <a href="https://pomelo.io/">Pomelo grant</a> recommended</li><li>Grants > $100k - ENF Approval</li></ul></td>
  </tr>
  <tr>
    <td valign="top"><b>Benefits</b></td>
    <td valign="top"><ul><li>Feedback during application process and evaluation</li><li>Introduction to related teams and projects</li></ul></td>
    <td valign="top"><ul><li>All benefits from Level 1</li><li>Milestone support and engagement</li><li><a href="docs/grant-badge.md">ENF Grant Program Badge</a></li><li><a href="docs/co-promotion.md">Co-promotion on Twitter</a></li></ul></td>
    <td valign="top"><ul><li>All benefits from Levels 1 and 2</li><li>Introductions to ENF Ventures VC partners*</li></ul></td>
  </tr>
</table>
* ENF Ventures will be established at a future date in 2023.

## Three Grant Types
There are three types of grants that the ENF considers. Some are originated by the community itself, and some are 
proposed in the form of an RFP by the ENF.

### 1. New Proposal
Most grant applications will take the form of a "New Proposal" from a member of the EOS community.
These projects range from core chain enhancements, SDKs, tools, and applications. These are initiated by members of the 
community and run through the standard [Grant Process](#grant-process) below.

> ⚠ **Grants are meant to kickstart your project, not sustain it**
>
> Our grant program is designed to provide initial support to projects so that they can become self-sustaining. 
> We do not provide long-term funding, and if a project fails to become self-sustaining after reaching the minimum 
> viable product (MVP) stage, we may consider it uninteresting to the wider community and stop approving grants for it.
> 
> This rule does not apply to grants that focus on components that should not have a business model, 
> such as core chain enhancements, developer tooling, and so on. Those will always be evaluated based on the value
> they bring to the community they are targeted at.

### 2. Maintenance Grant
Maintenance grants are also initiated by the community to bring back support for a library, SDK or tool that has fallen 
out of maintenance. These proposals are more limited in scope and milestone to ensure proper progress is made.  
Maintenance grants should not be used to add feature or functionality to existing code, but to bring it up to current 
levels of the chain, operating system, or programming language levels.  New functionality to existing projects can be 
applied via a "New Proposal". Read more about [Maintenance Grants](docs/maintenance-grants.md).

### 3. RFP Response
From time to time, the ENF will propose a work request to the community in the form of an RFP.  All community members, teams and companies are welcome to reply to the RFP.  Responses from multiple teams are expected.  The ENF will then select the best RFP response and award the work to the team that submitted it. [Read more on RFPs and how to reply to them](docs/rfp_info.md).

<br/><br/>

## Grant Process (for New Proposals)
The Grant Process consists of four major components: the Application Process, the Approval Process, Milestone Reporting, and Payment(s).  Payments will be made in EOS to the wallet specified in the Grant Application.  The processes must be completed in order and there may be feedback loops in some of the processes as described below.
### 1. Application Process
The application process is completed through Github.  You will need to fork the repository, change one of the forms, and submit it via a Pull Request as outlined in the steps below:
1. [Fork](https://github.com/eosnetworkfoundation/grant-framework/fork) this repository
2. In your fork, create a copy of the Grant Application template [(applications/application-template.md)](applications/application-template.md). If you're using the GitHub web interface, you will need to create a new file and copy the contents of the template inside the new one. **Please make sure you do not modify the template file directly.**
3. Name the new file after your project: `myproject_name.md`. Please make sure to put it in the `applications` directory. Make sure your filename does not have any spaces in it and ends with the `.md` extension.
4. Fill out the template with the details of your project. The more information you provide, the faster the review. Please refer to our [Grant guidelines for most popular grant categories](docs/grant_guidelines_per_category.md) and make sure your deliverables present a similar level of detail. To get an idea of what a strong application looks like, you can have a look at the following examples: [1](./applications/greymass-web-client-sdk.md), [2](./applications/oci-transaction-lifecycle.md). If you are applying for a smaller grant that solely consists of UI work, for example, you do not need to provide as much detail.
6. When your application is complete, create a Pull Request.  Please note, the Pull Request should only contain _one new file_—the Markdown file you created from the template.
7. You will see a comment template that contains a checklist. You can leave it as is and tick the checkboxes once the pull request has been created. Please read through these items and check all of them.
8. Sign off on the [terms and conditions](docs/T&Cs.md) presented by the [CLA assistant](https://github.com/claassistantio) bot as a Contributor License Agreement. You might need to reload the pull request to see its comment.
9. Your Grant Application is now complete.  The ENF Committee or Evaluators will contact your for next steps.

### 2. Approval Process
The Grant Approval Process consists of a review by the Grant Committee to check if the application fits the needs of the EOS Network community.  If the Committee approves the application, it is then sent on to the Grant Evaluators for technical approval. Please remember, your application will have a higher chance of acceptance and move through the process more quickly if you follow our [acceptance recommendations](docs/acceptance-recommendations.md) and meet all of our [minimum requirements](docs/minimum-requirements.md).  The approval process is outlined in the steps below:
1. The [Grant Committee](#grant-committee) may issue comments and request changes on the pull request.
2. Clarifications and amendments made in the comments _must be included in the application_. 
   - You may address feedback by directly modifying your application and leaving a comment once you're done. 
   - Generally, if you don't reply within 2 weeks, the application will be closed due to inactivity, but you're always free to reopen it as long as it hasn't been rejected.
3. When all requested changes are addressed and the terms and conditions have been signed, your application will be marked as `ready for review` and shared internally with the rest of the committee.
4. Once the Grant Committee has agreed the application meets the needs of the EOS Network Community, it will be shared with the [Grant Evaluators](#grant-evaluators) for technical evaluation.  If it is determined that the application does not meet the needs of the EOS Community, it will be rejected with a reason as to why it did not meet those needs.
5. Similarly to the Grant Committee process, the Grant Evaluators may issue comments and request more information on your pull request.
6. Clarifications and amendments to the above comments and request for information _must be included_ in the application.
7. Once the application has received the required number of Evaluator approvals, it will be accepted and merged.
8. Applications may be rejected by the Grant Evaluators as being overly ambitious, improper architecture/design or inadequate architecture/design documentation.
9. Unless specified otherwise, the day on which the application is accepted will be considered the starting date of the project, and will be used to estimate delivery dates.

### 3. Milestone Reporting
Milestones are to be delivered on the [Grant Milestones](https://github.com/eosnetworkfoundation/grant-milestones/) repository following the [process](https://github.com/eosnetworkfoundation/grant-milestones#milestone-delivery-process) described therein.

### 4. Payments
Payments are made in EOS at the time of milestone sign off up to and including the final deliverable milestone.

## Changes to a Grant After Approval
- Accepted grant applications can be amended at any time. However, this _necessitates a reevaluation by the committee_ and the same number of approvals as an application (according to the [levels](#grant-levels)). If your application has been accepted and, during development, you find that your project significantly deviates from the original specification, please open a new pull request that modifies the existing application. This also applies in case of significant delays.
- If your _delivery schedule_ significantly changes, please also open a pull request with an updated timeline.
- If your deliveries are significantly delayed and we cannot get a hold of you, we will terminate the grant (3 approvals required, regardless of level. If a member of the committee creates the termination PR, only 2 more approvals are required).

## Grant Teams
There are three teams that drive the process for ENF Direct Grants: Committee, Evaluators, and Operations

### Grant Committee
The Grant Committee are senior members of the EOS community that know the priorities of the ecosystem and can make required initial funding decisions based upon the guidelines of the grant program.  This committee is more business focused than technically focused but they understand the technical nature of the desired future.
- [Yves La Rose](https://github.com/YvesLaRose)
- [Aaron Cox](https://github.com/aaroncox)
- Dafeng Guo
- Fu Pan
- Peter Watt
- Van Kai
- Wen Huaqiang
- Damian Byeon

### Grant Evaluators
The Grant Evaluators review applications approved by the Grant Committee for technical merit and achievability.   They are more technical in nature and are more concerned with whether the proposal solves the problem optimally, is realizable in the specified time frame, and utilizes proper processes as required for the milestone achievement metrics.
- [Bart Wyatt](https://github.com/wanderingbort)
- [Areg Hayrapetian](https://github.com/arhag)
- [Matt Witherspoon](https://github.com/spoonincode)
- [Bucky Kittinger](https://github.com/larryk85)
- [Nathan James](https://github.com/nsjames)
- [Denis Carriere](https://github.com/DenisCarriere)

### Grant Operations
The Grant Operations team manages the overall workflow of the ENF Grant process including: application acceptance and routing, notification of acceptance or rejection, monitoring of milestones and distribution of payments.
- [Ted Cahall](https://github.com/tedcahalleos)
- [Jeff Werner](https://github.com/jeffwerner00)

## License
[Apache License 2.0](docs/LICENSE) © EOS Network Foundation


