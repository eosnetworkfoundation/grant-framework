# EOS Network Foundation Grant Proposal

> This document will be part of the terms and conditions of your agreement and therefore needs to contain all the required information about the project. Don't remove any of the mandatory parts presented in bold letters or as headlines! Lines starting with a `>` (such as this one) can be removed.
>
> See the [Grant Framework Process](https://github.com/eosnetworkfoundation/grant-framework#grant-process-for-new-proposals) on how to submit a proposal.

- **Project Name:** The Lost Diamond
- **Team Name:** Time2Discover
- **Payment Address:** time2discovr (EOS Mainnet)
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1

> ⚠️ *The combination of your GitHub account submitting the application and the EOS account address above will be your unique identifier during the program. Please keep them safe.*

## Project Overview

This application is in response to an RFP. (Open application process)

### Overview

The Lost Diamond is a real-world P2E adventure race where the goal is to find The Lost Diamond by conquering checkpoints all around the world.

This 90 second intro video will give a good overview: https://youtu.be/3BKr1uY6nZ8

The EOS Mainnet is the only technology platform available that has the requirements needed to make TheLostDiamond race work: instant transactions to anyone in the world with no fees for the users and the option to transfer EOS-tokens to Coinbase/Binance to let the users spend the money earned by using a crypto debit card. 

Our team has been involved in EOS since 2018 and we want to contribute to the ecosystem's growth and teach non-tech people how blockchain technology can be used in a fun and educational way.


### Project Details

We expect the teams to already have a solid idea about your project's expected final state. Therefore, we ask the teams to submit (where relevant):

- Mockups/designs of any UI components
- Data models / API specifications of the core functionality
- An overview of the technology stack to be used
- Documentation of core components, protocols, architecture, etc. to be deployed
- PoC/MVP or other relevant prior work or research on the topic
- What your project is _not_ or will _not_ provide or implement
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious

### Ecosystem Fit

The main goal of TheLostDiamond project is ecosystem growth.

The EOS Mainnet has solved one of the biggest problems in the world - how to transfer money instantly to anyone in the world as easy as sending an email.

The EOS-community needs ambitious projects that can show that advantage to a larger audience.  

The EOS Mainnet has 5 millions accounts. Important EOS-projects, e.g. the implementation of the EVM, will probably get a lot of users from the 40 million accounts on Ethereum. Our target audience is the 150 million users hunting virtual monsters on PockémonGo.

EOS has the opportunity and technology to replace virtual monsters with real money. And the EOS ecosystem needs projects that are targeting non-tech users in an order of magnitude from outside the smaller crypto community.

We are not aware of other similar projects in the EOSIO or other related ecosystems. 


## Team

### Team members

- Team leader: Bjørn Omsland
- Team members: Ann Magrit Monhof, Siv Anne Balslev, Jørn Balslev

### Contact

- **Contact Name:** Bjørn Omsland
- **Contact Email:** bomsland@gmail.com
- **Website:** thelostdiamond.io

### Legal Structure
- **Registered Legal Entity:** Time2Discover AS (Norway) https://w2.brreg.no/enhet/sok/detalj.jsp?orgnr=925474746
- **Registered Address:** Rosenholmveien 25, 1414 Trollåsen, Norway

### Team Experience

We are four creative outdoor enthusiasts from Norway with backgrounds in the travel industry, logistics, project management and programming.

We have hosted several Lost Diamond events in Norway, utilizing the EOS-Mainnet, for more than 1,000 users to test and improve TheLostDiamond race.


### Team Code Repos

- https://github.com/bjornomsland
- https://github.com/bjornomsland/CaptainBlackBillSmartContract

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.
N/A

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/bjornomsland/
- https://www.linkedin.com/in/ann-magrit-monhof-55785610/
- https://www.linkedin.com/in/jorn-balslev/
- https://www.linkedin.com/in/sivbalslev/

## Development Status

We have a working MVP that has been used for testing the application in several single-event races in Norway. https://cptblackbill.com/

The smartcontract is located on the EOS-Mainnet account cptblackbill. The code is available at https://github.com/bjornomsland/CaptainBlackBillSmartContract

The frontend is developed in NodeJs and hosted on Google Clouds. 

Different single-event races can have different unique domain names. E.g. our biggest single-event race is “Discover Oslo Adventure Race”. We will host our third Discover Oslo Adventure Race on June 11th. https://opplevoslo.app The feedback from our Discover Oslo participants has been exceptionally good. 98% say they will participate in the upcoming Discover Oslo race.

Development, testing and feedback from all the single-event races is the foundation for our main goal - launching The Lost Diamond 24/7 Global Adventure Race. The Lost Diamond 24/7 Global Adventure Race is ready for Test Marketing, where the goal is to find out how many people will participate in a pure crypto-based adventure race and see if we can obtain a 22% monthly growth rate. 


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
- **Deliverables 0a-0d are mandatory for all milestones**, and deliverable 0e at least for the last one. If you do not intend to deliver one of these, please state a reason in its specification (e.g. Milestone X is research oriented and as such there is no code to test).

> :zap: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** One month (for the first milestone)
- **Full-Time Equivalent (FTE):**  1 FTE
- **Total Costs:** 10,000 USD (for the first milestone. The whole project will take years and estimated total need for funding is 500,000 USD)

### Milestone 1 Example — Implement EOSIO Sub-module

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our EOSIO nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)
| 1. | EOSIO Sub-module: X | We will create a Substrate module that will... (Please list the functionality that will be implemented for the first milestone) |  
| 2. | EOSIO Sub-module: Y | We will create a Substrate module that will... |  
| 3. | EOSIO Sub-module: Z | We will create a Substrate module that will... |  
| 4. | EOSIO chain | Sub-modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |  


### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1
- **Costs:** 4,000 USD

...


## Future Plans

Please include here

- how you intend to use, enhance, promote and support your project in the short term, and
- the team's long-term plans and intentions in relation to it.


## Additional Information

**How did you hear about the Grants Program?** EOS Fireside chat

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
