# EOS Network Foundation Grant Proposal

- **Project Name:** TrustSwap
- **Team Name:**TrustSwap
- **EOS Payment Address:** trustswap111
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A

## Contact

- **Contact Name:** Esteban Saá Barona
- **Contact Email:** steban@gmail.com
- **Website:** https://trustswap-testnet.web.app/

## Project Overview

TrustSwap is a decentralized crypto exchange build on top of the TrustEVM Blockchain.

### Overview

- **Name:** TrustSwap
- **Brief Description:** TrustSwap is a fork of the Uniswap open source project, it is built to work on top of TrustEVM Blokchain and deliver fast, secure and easy to use token trading. 
- **Relationship to EOSIO:** TrustSwap is built on top of TrustEVM, an EVM compatible side chain of EOSIO.
- **Reason for Interest:** We are looking to create the most scalable, and easy to use swap platform.

### Project Details

- Mockups/designs of any UI components
- https://www.figma.com/file/IPrFq5RrP0V3cSMO1IwJrv/Swap-branding-and-logo
- Data models / API specifications of the core functionality
- https://docs.uniswap.org/protocol/V2/reference/API/overview
- An overview of the technology stack to be used
- https://reactjs.org/
- NodeJS , 
- ....
- Documentation of core components, protocols, architecture, etc. to be deployed
- ... documentation link
- PoC/MVP or other relevant prior work or research on the topic
- https://trustswap-testnet.web.app/
- https://trustswap-farm.web.app/
  - TrustSwap will not write new contract code, instead follow the path marked by the open source Uniswap project. We start with the open source version of the Uniswap V2, and will upgrade to V3 once the license allow is.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem? 
The future is EVM...
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
A world of crupto users looking to trade their crypto currencies.
- What need(s) does your project meet?
The need of users to switch among multiple crypto currencies.
- Are there any other projects similar to yours in the EOSIO ecosystem?
There are multiple crypto decentralized exchanged on the ecosystem, we are the first one available on the upcoming TrustEVM side chain.
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?

## Team

### Team members

- **Team Leader:** Esteban Saá Barona

### Legal Structure
- **Registered Legal Entity:** We are in the initial process of registration
- **Registered Address:** N/A

### Team Experience

I have been working for over 25 years with computers, most of them dedicated to Linux servers. Have xperience, started Butcoin on, worked ...

### Team Org Repos

- https://github.com/evm20

### Team Member Repos

- https://github.com/steban1

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/estebansaa

## Development Status

> If you've already started implementing your project or it is part of a larger repository, please provide a link and a description of the code here. In any case, please provide some documentation on the research and other work you have conducted before applying. This could be:

- links to improvement proposals or [RFPs](https://github.com/eosnetworkfoundation/grant-framework/tree/main/docs/rfps) (requests for proposal),
- academic publications relevant to the problem,
- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to this project with anyone from the EOS Network Foundation,
- https://t.me/jointrustswap
- previous interface iterations, such as mock-ups and wireframes.
- https://www.figma.com/file/IPrFq5RrP0V3cSMO1IwJrv/Swap-branding-and-logo

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
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our EOSIO nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)


## Future Plans

- As we are a fork of Univswap, we are currently limited to Version 2 of the protocol. Version 3 includes several important improvements, and we plan to update to it as soon as the license allows us. 


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.
It was mentioned in our telegram channel by a member of our community.
