 # EOS Network Foundation Grant Proposal

- **Project Name:** EOSIO Smart Contract Testing Libraries
- **Team Name:** GenerEOS Pty Ltd
- **EOS Payment Address:** aus1genereos
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3

## Project Overview

This application is to support an existing proposal put forward on [Pomelo](https://pomelo.io/grants/sclibraries) to reach its funding and therefore product/feature objectives..

As highlighted in the [CORE+ Blue Paper](https://medium.com/eos-network-foundation/core-blue-paper-80c26db532b6), smart contract testing is an essential part of the modern software development process and it is seriously lacking in the EOS and EOSIO development world. There are two main tools that are limited in functionality that have been developed by the community for this purpose but sadly they have been abandoned and are no longer fit for purpose due to a lack of funding and their uncompetitiveness in the wider market.

**Existing tools**

[EOSFACTORY](https://github.com/tokenika/eosfactory)
 
**Advantages**

* Open source and free to use

**Disadvantages**

* Convoluted instructions with unnecessary steps where developers need to compile the eosio source code and then build and install eosfactory. 
* Local node runs in background mode which can cause issues with different EOSIO configurations or software versions.
* Difficulty testing multiple smart-contracts due to needing a data table for each contract.
* Difficult to setup CI/CD for projects 
 
[HYDRA](https://docs.klevoya.com/hydra/about/getting-started/)
 
**Advantages**

* The framework is developed with Javascript which is simple to install and run. 
* Simplified setup of CI/CD
* Ability to init table data for each smart contract. This reduces code review time to understand how to insert data to each table. 

**Disadvantages**

* Closed source code
* Hosts EOSIO node on the user server side which can reduce performance and adds friction
* Paid service. 
* To init table data the smart contract needs to be updated. The unit-test framework and smart contact code should be independent. 


### Overview

- **Name:** Javascript based EOSIO Smart Contract Testing Library
- **Brief Description:** Develop a Javascript based EOSIO smart contract testing library
- **Relationship to EOSIO:** Testing libraries are a critical tool for developers to develop robust and secure smart contracts for EOSIO based applications
- **Reason for Interest:** The team behind GenerEOS have built many smart contract based applications on EOS and EOSIO based chains as well as on Ethereum and saw a clear gap in the testing and validation space on EOS and EOSIO in comparison to Ethereum


### Project Details

**Smart Contract Testing Library** 
The smart contract testing library will be built with Javascript leveraging eosio-core built by Greymass giving you the ability to dockerize a light EOSIO node that can run on any system. This allows the ability for the user to host it on their system easily and automated with the ability to test for multiple EOSIO based chains i.e EOS, WAX, TELOS, PROTON, FIO and UX. It also allows for each project to simply set up CI/CD and seed table data without modifying the contracts. All code will be open sourced under MIT so it is free for the community to use, creating no barrier to entry for developers. 
 
**Features**
* Open-source MIT license
* Ability to init/reset table data
* Ability to test accounts and permissions
* Built with Javascript
* Dockerize a light EOSIO node that can be run on the users system automatically
* Ability to test multiple EOSIO(EOS/WAX/TELOS) networks with links to public snapshots.
* Simplified method to setup CI/CD


### Ecosystem Fit

This library is aimed at developers and entrepreneurs to give them the tools needed to create secure and robust smart contracts for their tools or products to be built on EOS and EOSIO. As illustrated in the overview, and in the CORE+ Blue Paper, there is a clear gap missing with these tools in the EOS and EOSIO development world which places EOS at a disadvantage compared to other chains.  

## Team

### Team members

* Team Lead: Tim Weston - Co-founder and Head of Product. 
* Devops Lead: Ralf Weinand - Co-founder and Head of Infrastructure
* Technical Lead: Rob Dewilder - Senior Technical Lead 
* Senior Fullstack Developer: Quoc Le - preferred languages C++/Nodejs/Solidity
* Smart Contracts Developer/Backend: Tung - preferred languages Nodejs
* Smart Contract/Backend Developer: Quy - preferred languages C++/Nodejs
* Frontend/Nodejs Developer: Liem - preferred languages Nodejs


### Contact

- **Contact Name:** Tim Weston
- **Contact Email:** tim@genereos.io
- **Website:** https://genereos.io/

### Legal Structure
- **Registered Legal Entity:** GenerEOS Pty Ltd - ABN 80 628 307 853
- **Registered Address:** 64 Churchill St, Jamberoo, NSW, Australia 2533

### Team Experience

GenerEOS are top 21 genesis block producers on the EOS mainnet and have been building and growing out the EOS and EOSIO ecosystem since 2018. We have a strong team of passionate developers and entrepreneurs that love to operate on the bleeding edge of technology. We were the original developers of the open-sourced web-wallet EOSToolkit.io and are the developers behind Genpool.io a staking rewards platform built on EOS. Our Technical Lead Rob Dewilder is the ex-CTO of Worbli and IT Director of Sony Music, he is a full stack developer that is a very well-respected technology professional with 20 years of experience in engineering and management roles. He is capable of managing large-scale infrastructures, highly technical backend projects, global supply chains and has vast experience with EOSIO and smart contract development. Quoc Le, is a senior developer with 8 years of experience, currently working as a senior engineer at WAX building out internal testing frameworks and core code development along with their suite of NFT related projects. 

### Team Org Repos

- https://github.com/generEOS>


### Team Member Repos

- https://github.com/timmwest>
- https://github.com/rdewilder>
- https://github.com/RalfWeinand>
- https://github.com/quocle108>


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/ralfweinand/>
- https://www.linkedin.com/in/robert-dewilder-6b83311/>


## Development Status

This project has not begun development yet and is in the architecting and research phase. Please reference our [Pomelo Pitch](https://pomelo.io/grants/sclibraries) for more details around reasoning and justification. We will be building off of similar projects in the Ethereum world as explained in previous sections. 

## Development Roadmap


### Overview

- **Total Estimated Duration:** Duration of the whole project is 1 month effort and total delivery time of 2 months which includes testing and documentation. 

- **Full-Time Equivalent (FTE):**  4
- **Total Costs:** $40500 USD, payment can be made in EOS. Note, that the total amount raised in the Pomelo proposal will be deducted from the final milestone payment - currently ~$7,000 USD.

### Milestone 1 — Smart Contract Testing library

- **Estimated duration:** 1 month effort and 2 months total delivery duration including testing and documentation
- **FTE:**  4
- **Costs:** $40500 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial and operating instructions that explains; Setup of a testing environment; Config and write unit-test; API reference |
| 0c. | Testing Guide | NA - the testing guide will be included in the documentation as the library is testing in nature. |
| 0d. | Docker | NA - included on deliverable 1 |
| 0e. | Article | N/A as its on the milestone 3 deliverable. However, if milestone 2 & 3 are roadblocked (ref milestone 2, deliverable 1) the article will be published at this milestones completion.
| 1. | Dockerize a light EOSIO node that can be run on the users system automatically. With several options on initial chain state for different chains e.g. EOS/TELOS/WAX | Dockerfile to setup each chain; shell script to initialize smart contract/data; docker image stored in docker hub |  
| 2. | Provide all core functionalities for unit-test| Javascript API to interact with the docker container within the testing scripts; Javascript Core APIs for developer to interact with chain for example: set contract, push action, get table and an array of wrapped functions that allow developers to quickly interact with blockchain; Assertion library for smart contract testing|  
| 3. | Provide some advanced functionalities | Nodejs modules and docker shell scripts to manipulate blockchain state and time for special testing purposes e.g. booting the chain with an arbitrary time; Init/reset smart contract table data with minimal modification of smart contract; Functionalities to test accounts/permission|  


## Future Plans

* We intend to continually look at the market and add competitive features to the smart contract testing library working with developers to better understand the features needed for their projects. Note; this depends on subsequent funding for this level of support. Additionally, we are currently investigating Clang to build a code coverage and code validation library which was a part of our initial proposal but has dropped out due to the complexity. It is our hope that we can find a solution and add these libraries back in and build them later in the year.

* We plan on maintaining the open source code base to ensure that it is up to date with the latest various third-party libraries, frameworks, and software that it uses. Note; this depends on subsequent funding for this level of support. 


## Additional Information

**How did you hear about the Grants Program?** Personal recommendation.

We have worked alongside the ENF since inception and have been a part of the EOS and EOSIO community since genesis and have identified this as a critical piece of missing tooling that creates friction for developers.

