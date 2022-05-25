# EOS Network Foundation Grant Proposal

- **Project Name:** TrustSwap
- **Team Name:** TrustSwap
- **EOS Payment Address:** trustswap111
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A

## Contact

- **Contact Name:** Esteban Saá Barona
- **Contact Email:** steban@gmail.com
- **Website:** https://trustswap-testnet.web.app/

## Project Overview

TrustSwap is a decentralized crypto exchange build on top of the Trust EVM Blockchain.

### Overview

- **Name:** TrustSwap
- **Brief Description:** TrustSwap is an open source decentralized exchange structured to work on top of TrustEVM Blockchain. It delivers a fast, secure and easy to use EVM20 token trading. 
- **Relationship to EOSIO:** TrustSwap is built on top of Trust, an EVM compatible side chain of EOSIO.
- **Reason for Interest:** We are looking to create the most scalable, and easy to use swap service. Trust EVM provides a solid platform to build on.

### Project Details

- We compiled a few ideas for the design here,  https://www.figma.com/file/IPrFq5RrP0V3cSMO1IwJrv/Swap-branding-and-logo . We are still early on the process of creating a brand-
- Most of our code comes from the Uniswap project, the following links contains broad documentation on the project- https://docs.uniswap.org/protocol/V2/reference/API/overview
- We will be reusing many of the components of the code where our project is forked from. This includes frameworks as react for the frontend: https://reactjs.org/. For the back ebd we are using https://github.com/nodejs/node
- Documentation of core components, protocols, architecture, etc. to be deployed
- ... https:
- While we are very early on our development process we have deployed several smart contracts and frontends to them. 
- https://trustswap-testnet.web.app/ Is the frontend to a decentralized exchange. It curently makes use of the TrustEVM testnet-
- https://trustswap-farm.web.app/ is a farm contract, it accepts LP deposits from our decentralized exchange and payrs out our testnet roken TRT. 
- https://docs.trustswap-farm.web.app/ is our documenation site, it includes general information of our platform. 
  - TrustSwap will not write new contract code, instead follow the path marked by the open source Uniswap project. We start with the open source version of the Uniswap V2, and will upgrade to V3 once the license allow is.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem? 
The future is EVM...
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
A world of crypto users looking to trade their crypto currencies.
- What need(s) does your project meet?
The need of users to switch among multiple crypto currencie, obtain tokens of new projects, swaps for stable currencies. 
- Are there any other projects similar to yours in the EOSIO ecosystem?
There are multiple crypto decentralized exchanged on the ecosystem, we are the first one available on the upcoming Trust EVM EOS side chain. There are currently no other decetralized exchanges built for Trust EVM.

## Team

### Team members

- **Team Leader:** Esteban Saá Barona

### Legal Structure
- **Registered Legal Entity:** We are in the initial process of registration
- **Registered Address:** N/A

### Team Experience

We have been working for over 25 years with highly scalable network platforms with a focus on Linux servers. Have a lot experience developmeing with LAMP framework. Started teaching Linux at College, with a first class being what were initially my teachers for other scholl classes. Discovered Bitcoin on 2012, inspired on satoshidice, created satoshicode, a word discovery game that was popular for a while, only to be killed when fees made it inpossible to play. Was an early user of mastercoin/omni, this interest also was killed by BTC high fees. The high fees switiched my attention to building on Ethereum, where Ipartcipaided anonymously for devevelopment. During the bull runs, Switched interests into trading and investing, I learned a lot of experience but ultimatelly dkiscovered hthat may pation was on writing code and creating products.  I see afuture where the worl runs around decentralized technolgies and cryptopgraphy.  

I was very critical of Ethereum for its plans of being PoS, https://twitter.com/estebs/status/614086876165705728 , eventually I understood its merits, and saw many of my concerns solved by dPoS. 


### Team Org Repos

- https://github.com/evm20

### Team Member Repos

- https://github.com/steban1

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/esteban-s-988b6457/

## Development Status

- https://t.me/jointrustswap
- https://www.figma.com/file/IPrFq5RrP0V3cSMO1IwJrv/Swap-branding-and-logo
- https://twitter.com/joinTrustSwap
- https://t.me/jointrustswap

## Development Roadmap

For each milestone,

- make sure to include a specification of your software. _Treat it as a contract_; the level of detail must be enough to later verify that the software meets the specification.
- include the amount of funding requested _per milestone_.
- include documentation (tutorials, API specifications, architecture diagrams, whatever is appropriate) in each milestone. This ensures that the code can be widely used by the community.
- provide a test suite, comprising unit and integration tests, along with a guide on how to set up and run them.
- commit to providing Dockerfiles for the delivery of your project.
- indicate milestone duration as well as number of full-time employees working on each milestone.
- **Deliverables 0a-0c are mandatory for all milestones**, and deliverable 0e at least for the last one. If you do not intend to deliver one of these, please state a reason in its specification (e.g. Milestone X is research oriented and as such there is no code to test).

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

- We will be updating our core contracts to Version 3 of Uniswap as soon as the license allows us.


## Additional Information

**How did you hear about the Grants Program?** personal recommendation
It was mentioned in our telegram channel by a member of our community. We were early to respond to the EOS community building an EVM,  we understand the tools we are building are important to the sucess of the platform.
