# EOS Network Foundation Grant Proposal

- **Project Name:** EOSIO cross-platform wallet part 1 - social recovery TODO
- **Team Name:** Tonomy Foundation
- **EOS Payment Address:** tonomyaccou1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/Tonomy-Foundation/tonomy-id

## Contact

- **Contact Name:** Jack Tanner
- **Contact Email:** contact@tonomy.foundation
- **Website:** https://tonomy.foundation

## Project Overview

> If this is an application for a follow-up grant (the continuation of an earlier, successful ENF grant), please provide name and/or pull request of said grant on the first line of this section.

### Overview

- **Name:** EOSIO cross-platform wallet with advanced features such as recovery and SSI
- **Brief Description:**

We are building a cross-platform mobile blockchain and SSI wallet for EOSIO public chains like EOS, Telos and WAX. This can be used to s send tokens, sign dApp transactions, passwordless sign into web2 and web3 apps and share credentials. We plan to build several non-custodial recovery mechanisms: social recovery, security questions and hardware recovery. This recovery will allow users to recover both keys as well as sovereign data. Our experience in sovereign identity and design gives us the confidence needed to say we can do this.

We see this project as an extension of the Wallet+ blue paper. We want to support the work of these SDK's by integrating early releases and giving feedback and potentially contributing to the development. We had already considered several of the features proposed in this blue paper: application registry, hardware wallets, account recovery, asset proxy/hosting service. While the initial proposal of Wallet+ is to support web applications, using react native we should be able to adopt the JavaScript/typescript packages for our application as well. This will also give the added benefit of providing a mobile testing ground for the Wallet+ deliverables.

The mobile Wallet will be fully open source (MIT or Apache 2.0 license) and provide a reference For other developers. This will be the first open-source self-sovereign identity mobile client and the first identity solution using the EOSIO DID method.

Due to the limited funding from only being at level 1, this grant proposal only seeks funding to support the development of its first recovery mechanism. Other work is not covered in this proposal. We will be self-funding as well as receiving external European Horizon 2027 and other funding for the release of the first beta edition of the wallet. In future ENF and Pomelo proposals we aim to extend the features of this application and after a proper production launch offered it as a software as a service model for public and private chains.

- **Relationship to EOSIO:** Our application is built on top of the EOSIO blockchain framework. It will be compatible with any pure-EOSIO blockchain.
- **Reason for Interest:** We want to support the public EOS, Telos and WAX ecosystems. In the future, we plan to take this software and provide it in a software as a service model to industry and enterprise use cases.

### Project Details

- Mockups/designs of any UI components
Figma prototype access available upon request. Please email jack@tonomy.foundation
See video here:
TODO

- Data models of the core functionality

- API specifications of the core functionality

- An overview of the technology stack to be used

-- Mobile client: React Native
-- Key storage: [react-native-keychain](https://www.npmjs.com/package/react-native-keychain) (which uses key enclaves on the mobile device if available)
-- Transport layer: QR codes and DIDComm using EOSIO signing request (ESR) and verifiable credentials
-- Blockchain: EOSIO

- Documentation of core components, protocols, architecture, etc. to be deployed

- PoC/MVP or other relevant prior work or research on the topic
[https://europechain.io/identity/myd-missing-piece-puzzle-ssi/](https://europechain.io/identity/myd-missing-piece-puzzle-ssi/)

- What your project is _not_ or will _not_ provide or implement
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious

### Ecosystem Fit

> Help us locate your project in the EOSIO landscape and what problems it tries to solve by answering each of these questions:

- Where and how does your project fit into the ecosystem?
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
- What need(s) does your project meet?
- Are there any other projects similar to yours in the EOSIO ecosystem?
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?

## Team

### Team members

- **Team Leader:** Jack Tanner
- Chris Veroef
- Mikhail Rusanov
- Carrie Ann Smith
- Jordan Fisher
- Mia Jacobson

### Legal Structure
- **Registered Legal Entity:** Tonomy Stichting
- **Registered Address:** Thorbecke Laan, Baarn, Utrecht 3741TR, Netherlands

### Team Experience

> Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past. For research-related grants, references to past publications and projects in a related domain are helpful. If you applied for a Pomelo grant in the past, please be sure you listed them in the section above and mention them in detail in this section.

> If anyone on your team has applied for a grant at the EOS Network Foundation previously, please list the name of the project and legal entity here.

Myd, EOSIO DID, EOSIO identity working group, gimly, Verifiable Conditions, W3C CCG, DIF
EOSIO training
ethereum
other from other teammates?

### Team Org Repos

- https://github.com/Tonomy-Foundation
- https://github.com/Tonomy-Foundation/civic-participation

TODO add Chris and Carrie?

### Team Member Repos

- https://github.com/theblockstalk
- https://github.com/theblockstalk/eosio-contracts
- https://github.com/theblockstalk/awesome-eosio (added several tools in some [PRs](https://github.com/DanailMinchev/awesome-eosio/pull/70))
- https://github.com/theblockstalk/eosworkshop1
- https://github.com/theblockstalk/eosio-sovereign-contract-poc
- https://github.com/theblockstalk/funnels
- https://github.com/kamitor
- https://github.com/carrie2240

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/jack-tanner/
- https://www.linkedin.com/in/christiaanverhoef/
- https://www.linkedin.com/in/rusanovmp/
- https://www.linkedin.com/in/carrie-ann-smith-95240899/
- https://www.linkedin.com/in/jordanelizabethfisher/
- https://www.linkedin.com/in/mia-jacobson-012218139/

## Development Status

> If you've already started implementing your project or it is part of a larger repository, please provide a link and a description of the code here. In any case, please provide some documentation on the research and other work you have conducted before applying. This could be:

- links to improvement proposals or [RFPs](https://github.com/eosnetworkfoundation/grant-framework/tree/main/docs/rfps) (requests for proposal),
- academic publications relevant to the problem,
- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to this project with anyone from the EOS Network Foundation,
- previous interface iterations, such as mock-ups and wireframes.

## Development Roadmap

This section should break the development roadmap down into milestones and deliverables. To assist you in defining it, we have created a document with examples for some grant categories [here](../docs/grant_guidelines_per_category.md). Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**. In the descriptions, it should be clear how your project is related to the EOS ecosystem. We _recommend_ that teams structure their roadmap as 1 milestone ≈ 1 month.

For each milestone,

- make sure to include a specification of your software. _Treat it as a contract_; the level of detail must be enough to later verify that the software meets the specification.
- include the amount of funding requested _per milestone_.
- include documentation (tutorials, API specifications, architecture diagrams, whatever is appropriate) in each milestone. This ensures that the code can be widely used by the community.
- provide a test suite, comprising unit and integration tests, along with a guide on how to set up and run them.
- commit to providing Dockerfiles for the delivery of your project.
- indicate milestone duration as well as number of full-time employees working on each milestone.
- **Deliverables 0a-0c are mandatory for all milestones**, and deliverable 0e at least for the last one. If you do not intend to deliver one of these, please state a reason in its specification (e.g. Milestone X is research oriented and as such there is no code to test).

> :zap: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** Duration of the whole project (e.g. 2 months)
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project throughout its duration (see [Wikipedia](https://en.wikipedia.org/wiki/Full-time_equivalent), e.g. 2 FTE)
- **Total Costs:** Requested amount in USD for the whole project (e.g. 12,000 USD). Note that the acceptance criteria and additional benefits vary depending on the [level](../README.md#grant-levels) of funding requested. This and the costs for each milestone need to be provided in USD; if the grant is paid out in EOS, the amount will be calculated according to the exchange rate at the time of payment.

### Milestone 1 Example — Implement EOSIO Sub-module

- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our EOSIO nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)
| 1. | EOSIO Sub-module: X | We will create a EOSIO module that will... (Please list the functionality that will be implemented for the first milestone) |  
| 2. | EOSIO Sub-module: Y | We will create a EOSIO module that will... |  
| 3. | EOSIO Sub-module: Z | We will create a EOSIO module that will... |  
| 4. | EOSIO chain | Sub-modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |  


### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1
- **Costs:** 4,000 USD

...


## Future Plans

> Please include here

- how you intend to use, enhance, promote and support your project in the short term, and
- the team's long-term plans and intentions in relation to it.


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

> Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
