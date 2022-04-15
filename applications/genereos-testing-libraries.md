 # EOS Network Foundation Grant Proposal

- **Project Name:** EOSIO Smart Contract Testing Libraries
- **Team Name:** GenerEOS Pty Ltd
- **EOS Payment Address:** aus1genereos
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3

## Project Overview

This application is to support an existing proposal put forward on [Pomelo](https://pomelo.io/grants/sclibraries) to reach its funding and therefore product/feature objectives..

As highlighted in the [CORE+ Blue Paper](https://medium.com/eos-network-foundation/core-blue-paper-80c26db532b6), smart contract unit-testing and code validation is an essential part of the modern software development process and it is seriously lacking in the EOS and EOSIO development world. There are two main tools that are limited in functionality that have been developed by the community for this purpose but sadly they have been abandoned and are no longer fit for purpose due to a lack of funding and their uncompetitiveness in the wider market.

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

- **Name:** Javascript based EOSIO Smart Contract Testing and Validation Libraries
- **Brief Description:** Develop three Javascript based EOSIO smart contract testing libraries - unit-testing, code coverage and security and code style validation
- **Relationship to EOSIO:** Testing and validation libraries are a critical tool for developers to develop robust and secure smart contracts for EOSIO based applications such as Defi
- **Reason for Interest:** The team behind GenerEOS have built many smart contract based applications on EOS and EOSIO based chains as well as on Ethereum and saw a clear gap in the testing and validation space on EOS and EOSIO in comparison to Ethereum


### Project Details

**Unit-test** 
The unit-test library will be built with Javascript leveraging eosio-core built by Greymass giving you the ability to dockerize a light EOSIO node that can run on any system. This allows the ability for the user to host it on their system easily and automated with the ability to test for multiple EOSIO based chains i.e EOS, WAX, TELOS, PROTON, FIO and UX. It also allows for each project to simply set up CI/CD and seed table data without modifying the contracts. All code will be open sourced under MIT so it is free for the community to use, creating no barrier to entry for developers. 
 
**Features**
* Open-source MIT license
* Ability to init/reset table data
* Ability to test accounts and permissions
* Built with Javascript
* Dockerize a light EOSIO node that can be run on the users system automatically
* Ability to test multiple EOSIO(EOS/WAX/TELOS) networks with links to public snapshots.
* Simplified method to setup CI/CD
 
**Code coverage**

Code coverage, first devised in the 1960s, encapsulates the idea that tests should ‘touch’ all of the code under test. If the tests execute all of your code, and the results from the tests are as expected, it is less likely your code contains unforeseen bugs. Sadly, there is no available code coverage library in EOS and EOSIO. After studying existing code coverage libraries in Ethereum such as [solidity-coverage](https://github.com/sc-forks/solidity-coverage) we think it might be possible to bridge this over to the EOS and EOSIO world for native developers to leverage. This library will be built with javascript.
 
 
Here is a list of rewrite rules we will consider to apply for our code coverage library. These are subject to change when development of the project commences. 
 
**rewrite rules**

```If```

```loop```

```return```

```statements```

```conditional```

```function```

```expressions```
 
**Security and code style validation**

Security is critical when it comes to smart contracts especially with the rise in Defi applications. The Ethereum community has seen a number of linter tools such as [solcheck](https://github.com/federicobond/solcheck) and [ethlint](https://github.com/duaraghav8/Ethlint) that are used for checking security rules and verifying compliance with style guides. This is a huge benefit for developers in the Ethereum community. Sadly, there are no available linter tools in the EOS and EOSIO space to assist developers. Our goal is to provide a linter library that consists of three functions: Security Rules, Best Practice Rules & Style Guide Rules.

 The following rules will be considered to be included; and are subject to change during development. This library will be built with javascript.
 
**Security Rules: rule-id**

```missing-authorization-check```

```missing-assertion```

```check-forged```

```token-transfer```

```fake-notification```

```receipt-bad-randomness```

```re-entrancy-attack```

```unchecked-action-arguments```
 
 
**Best Practice Rules: rule-id**

```code-complexity```

```function-max-lines```

```max-line-length```

```no-empty-blocks```

```no-unused-vars```

```reason-string```

 
**Style Guide Rules: rule-id**

```quotes```

```const-name```

```contract-name```

```func-name```

```func-param-name```

```private-vars```

```table-name```

```var-name```



### Ecosystem Fit

These three libraries are aimed at developers and entrepreneurs to give them the tools needed to create secure and robust smart contracts for their tools or products to be built on EOS and EOSIO. As illustrated in the overview, and in the CORE+ Blue Paper, there is a clear gap missing with these tools in the EOS and EOSIO development world which places EOS at a disadvantage compared to other chains.  

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

This project has not begun development yet and is in the architecting and research phase. Please reference our [Pomelo Pitch](https://pomelo.io/grants/sclibraries) for more details around reasoning and justification. We will be building off of similar projects in the Ethereum world as explained in previous sections. One concern that we currently have is around the C / C++ parser instrumentation library, in our Pomelo pitch, we assumed we could make a workaround similar to what was achieved with previous Ethereum libraries - however - it might be a more difficult task than was anticipated and therefore could cause a roadblock for milestone 2 & 3.

## Development Roadmap


### Overview

- **Total Estimated Duration:** Duration of the whole project is 3 months effort and total delivery time of 6 months which includes testing and documentation. This is based on the assumption of building a workaround for the C / C++ parser instrumentation library - refer to deliverable 1 milestone 2.
- **Full-Time Equivalent (FTE):**  4.3
- **Total Costs:** $135000 USD, payment can be made in EOS. Note, that the total amount raised in the Pomelo proposal will be deducted from the final milestone payment - currently ~$20,000 USD.

### Milestone 1 — Unit-test library

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


### Milestone 2 — Code Coverage library

- **Dependencies:** workaround for an C / C++ parser instrumentation library (see deliverable 1)
- **Estimated duration:** 1 month effort and 2 months total delivery duration including testing and documentation
- **FTE:**  5
- **Costs:** $49500 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial and operating instructions that explains how to have transparent coverage of nodejs unit tests, instrumentation/ reporting of files in batch mode for browser tests and server side code coverage for nodejs |
| 0c. | Testing Guide | NA - the testing guide will be included in the documentation as the library is testing in nature. |
| 0d. | Docker | NA - docker detailed in deliverable 3 |
| 0e. | Article | N/A - included on the milestone 3 deliverable.
| 1. |Research/analysis and documentation about all parser/rewrite rules of eosio smart contracts | C / C++ parser nodejs module for eosio smart contract. This functionality is critical to the success of milestones 2 and 3. This proposal is based on the assumption we can make a fast workaround that is robust enough for the functionality. However, it is likely that this will not be the case and a fully functioning C / C++ parser or instrumentation library will need to be developed which would be a roadblock for milestones 2 and 3. |  
| 2. | Precompile: Read contract source code and rewrite the source so the code execution path can be tracked| Some mechanisms to analysis/parse the source code; A javascript module to apply rewrite rules to the smart contract|  
| 3. | Compile contract and run unit-tests using instrumented artifacts | Dockerize eosio compiler; Compile modified source code|  
| 4. | Generate coverage reports | NodeJS module to generate code coverage report via command line| 


### Milestone 3 — Security and code style validation library

- **Dependencies:** workaround for an C / C++ parser instrumentation library (see milestone 2, deliverable 1)
- **Estimated duration:** 1 month effort and 2 months total delivery duration including testing and documentation
- **FTE:**  4
- **Costs:** $40500 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial and operating instructions that explains installation, usage and configuration, writing a core rule, developing a shareable config and developing a plugin. |
| 0c. | Testing Guide | NA - the testing guide will be included in the documentation as the library is testing in nature. |
| 0d. | Docker | NA - docker provided in milestone 1 & 2. |
| 0e. | Article | We will publish an article that explains the work completed on all three libraries through grant funding with the content geared towards our target audience of developers and entrepreneurs in the EOS and EOSIO ecosystem.
| 1. |Base plugin to allow to define new plugin rule and report script | Base plugin pattern to add new plugin rule; Nodejs Script to generate rule report|  
| 2. | Style Guide Rules| Add new rule plugins for following:```quotes```; ```const-name```; ```contract-name```; ```func-name```; ```func-param-name```; ```private-vars```; ```table-name```; ```var-name``` |  
| 3. | Security Rules | Add new rule plugins for following: ```missing-authorization-check```; ```missing-assertion```; ```check-forged```;```token-transfer```; ```fake-notification```; ```receipt-bad-randomness```; ```re-entrancy-attack```; ```unchecked-action-arguments```| 
| 4. | Best Practice Rules | Add new rule plugins for following:```code-complexity```;```function-max-lines```;```max-line-length```;```no-empty-blocks```;```no-unused-vars```;```reason-string```| 


## Future Plans

* We intend to continually look at the market and add competitive features to all three libraries working with developers to better understand the features needed for their projects. Note; this depends on subsequent funding for this level of support.  
* We plan on maintaining the open source code base to ensure that it is up to date with the latest various third-party libraries, frameworks, and software that it uses. Note; this depends on subsequent funding for this level of support. 


## Additional Information

**How did you hear about the Grants Program?** Personal recommendation.

We have worked alongside the ENF since inception and have been a part of the EOS and EOSIO community since genesis and have identified this as a critical piece of missing tooling that creates friction for developers.

![image](https://user-images.githubusercontent.com/25791287/163632619-77f53152-e0f5-4fe9-8e18-eff4c1da94ca.png)
