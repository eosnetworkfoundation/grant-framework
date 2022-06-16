# EOS Network Foundation Grant Proposal

- **Project Name:** EdenEOS-Smart-contract-Elections
- **Team Name:** EOS Support LLC 
- **EOS Payment Address:** rorodev.gm
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** https://pomelo.io/grants/rneyu
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/Eossupport/Eden.git

## Contact

- **Contact Name:** Randall Roland
- **Contact Email:** ranroland@eossupport.io
- **Website:**Eossupport.io

## Project Overview

Write new smart contract for EdenEOS organization and Help community run an elections x1

Blockchain has set the stage for a new age where communities can organize and pursue the freedom of wealth to create a society equal for all. To succeed in pursuing freedom of wealth, communities have to find a way to organize. To organize, people worldwide would require applications to allow for members of different communities, or organizations to gather and reach consensus to select the best ideas to help people build wealth. Therefore, the experiment to help organization deploy edenos is very important. 

### Overview

- **Name:** EdenOS-smart-contract-Election.
- **Brief Description:** EdenOS is an open-source code. The code is used to run an election for organizations. Genesis edeneos needs written smart contract for their organizaiton and run an election on July 9th,2022. Our goal is to write smart contract and run an election for EdenEOS organization. 
- **Relationship to EOSIO:** EdenOS runs on the EOS mainnet 
- **Reason for Interest:** We are interested in helping organizations run elections and integrate the edeonOS code. The need for decentralized autonomous software to help developers, investors, and communities make decisions is needed more today than ever. Working on such a project is very exciting and refreshing.  

### Project Details
In this project, we are asking for funds for our time spent to studying the edenOS code, updating documentations, including concepts of the edenOS code. We are also asking for funds to cover the time spent to come up with concepts, to write a new smart contracts, testing codes, and running an election for the EdenEOS community. Some of the project details are:

- studying EdenOS and its code logic
- Setup notion for Eden organizations and keep the concepts of political playoffs and true democracy uptodate.
- Setup own test infrastructure and write test codes
- Run complete testing on the edenOS software
- Setup own production infrastructure
- Write smart contract:
  - change election time
  - change donation fees
  - eliminate sortition pay
  - Find a way to make all CD receive same pay, ineffect increasing pay of delegates
  - implement 14 days time delay for when bylaws can be proposed and approved onchain
  - Remove Electsettime restriction.
  
- What your project is _not_ or will _not_ provide or implement
  - Project doesn't come with IP, and social media accounts.
  - Implementing and deploying EdensOS for other organizations.
  - Doesn't include maintenance of EdenEOS code

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?
The project fits under Community project.
  
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
Dapp

- Are there any other projects similar to yours in the EOSIO ecosystem?
This project was started by Fractally team. Currently there is no other edenOS type of consensus building software.
  - If so, how is your project different?
  This project was started by Fractally team. They built the original open-source code. 
  - If not, are there similar projects in related ecosystems?
  At the moment, there is no similar project in the eos ecosystem.

- What need(s) does your project meet?
Governance, WPS

## Team

### Team members

- EOS support Team
- RORO Technology Team

### Legal Structure
- **Registered Legal Entity:** EOS Support LLC
- **Registered Address:** 21693 FM 1314 suite 500, Porter Tx

### Team Experience

- EOS Support ran the Last edenEOS elections
- We have set up EdenEOS notion for the community 
- Builders of EOS Support platform and organizations smart contract
- Team that provides Live support and how-to guides for the EOS community
- Lead blockchain developer (dev of EosTools)

### Team Org Repos
- https://github.com/Eossupport
- https://github.com/RoRo-TechnologyPLLC

### Team Member Repos

- N/A

### Team LinkedIn Profiles (if available)

- N/A

## Development Status

The smart contract updates has been written and compiled. Currently in testing phase.
Deployed code on testnet on June 11th,2022

## Development Roadmap
- Wrote about the opportunity to start building Daos on eos using EdenOS (https://bywire.news/articles/eos-as-a-network-of-daos) in march, 2022
- Started learning about the edenOS code ~ 3 months ago. Learned from fractally team and helped ran a successful eden election in April, 2022
- Started working and transfered EdenEOS notion into EOS support notion so that community can have access to EdenOS documentations (May, 2022)
- Discussed with CEO/founder of ENF regarding the opportunity to write smart contracts for eden communities and help organizations run elections
- Started EdenOS experimentation and code modifications in May, 2022

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

------

### Overview

- **Total Estimated Duration:** 3 months 
- **Full-Time Equivalent (FTE):** 7 FTE
- **Total Costs:** 75,000 USD

### Milestone 1 — EdenOS V0.3.4

- **Estimated duration:** ~ 1 month (started working on this in May 2022)
- **FTE:**  3 (whole EOS support team)
- **Costs:** 50,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | The documetnation of the previous version of EdenOS will remain. Some content will be modified to reflect modified code. We will also add some content to make the documentation more complete and comprehensive. |
| 0c. | Testing Guide | Eden has complete test code implemented with github actions, which will run automatically when project is packaged with github actions. Some of these parameters will be modified so that it fits modified projects |
| 0d. | Docker | N/A |
| 0e. | Article | Write how-to guides for users and EdenEOS community
| 1. | Change election time
| 2. | Change donation fees 
| 3. | update distribution pay
| 4. | implement 14 days time delay
| 5. | Remove Electsettime restriction

### Milestone 2 — Additional features
- preparing and helping EdenEOS get ready to run an election
- **Estimated Duration:** 2 weeks
- **FTE:**  4
- **Costs:** 15,000 USD

### Miletone 3 - Additional features
- set up testing infra
- set up production infra (AWS, zoom, powerup fees, RAM cost, IPF cost)
- **Estimated Duration:** 2 weeks
- **FTE:**  2
- **Costs:** 10,000 USD


## Future Plans:

Eos support and Roro Technology intends to continue research and development to improve the edenOS code. In addition, we intend to:

- Run elections for organizations that have integrated iterated versions of EdenOS
- Host and Deploy edenOS for organizations
- Maintain EdenOS iterated code for organizations
- continue to iterate edenOS software for organizations
- Develop dispute resolution
- Hire another full time blockchain developer to help us with building features


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website and Directly from the ENF

- We have been working on the eden notion, studying the code for ~ 3 months
- We ran the last edenEOS elections for the EdenEOS community
- We have helped with the eden user onbaroding of EOS
- Creating how-to guides and articles for EdenEOS
- Educating users on social media, telegram, facebook, reddit about EdenOS, and the concepts of fractal democracy

  
