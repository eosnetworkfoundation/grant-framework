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

TrustSwap is a decentralized crypto exchange build on top of the Trust EVM Blockchain; it bring an easy to use, yet poweful Web3 interface. 

### Overview

- **Name:** TrustSwap
- **Brief Description:** TrustSwap is an open source decentralized exchange structured to work on top of TrustEVM Blockchain. It delivers a fast, secure and easy to use EVM20 token trading. 
- **Relationship to EOSIO:** TrustSwap is built on top of Trust, an EVM compatible side chain of EOSIO.
- **Reason for Interest:** We are looking to create the most scalable, and easy to use swap service. Trust EVM provides a solid platform to build on.

### Project Details

- Our project is early on its development process, this allows us to allign our decision making with the best interests of the IOS community.
- We compiled a few ideas for the designs here: https://www.figma.com/file/IPrFq5RrP0V3cSMO1IwJrv/Swap-branding-and-logo . We are still early on the process of creating a brand. Most of our work so far has been devoted to deploying, testing and adapting to the inerworking of TrustEVM. 
- Our code comes from the Uniswap project, the following links contains broad documentation on the project: https://docs.uniswap.org/protocol/V2/reference/API/overview
- We will be reusing many of the components of the code where our project is forked from. This includes frameworks as REACT for the frontend: https://reactjs.org/. For the back end we are using the MERN stack to build a static site. MERN includes tools such as: https://github.com/nodejs/node. The resulting code is static HTML code that we host at Google Firebase, it includes several functions such as CDN, so we can substain veyr hgih loads maintaing good quality of service, and defend from DDOS attacks. Further the hosting platform allows us to implement CD/CD pilelines and optumize our deployment methodologies. 
- While we are very early on our development process we have deployed several smart contracts and their respective interfaces. 
- https://trustswap-testnet.web.app/ is the frontend to a decentralized exchange. It curently makes use of the TrustEVM testnet-
- https://trustswap-farm.web.app/ is a farm contract, it accepts LP deposits from our decentralized exchange and pays out testnet token. 
- https://docs.trustswap-farm.web.app/ is our documenation site, it includes general information of our platform. We are using Gitbook for it, will be connected once our domain name is decided. 
- https://www.npmjs.com/settings/trustevm/packages , we have published an SDK to NPMKS.com, this will make it easy for other developers to connect to our smart contract. There are multiple use cases for this, for instance market makers and arbitragers can use our SDK to make their bots work. 
  - TrustSwap will not divert far from our orignal code source, instead adapt to TrustEVM the open source Uniswap project. We start with the open source version of the Uniswap V2, and will upgrade to V3 once the license allow is. 
 - As part of our initial work we have deployed two extremely important smart contracts that will provide a backbone to the upcoming contract from other teams. These are the WrappedEVM contract, and the Multicall2 contract. These contracts are fundamental building blocks of any EVM ecosystem. We plan to coordinate work with the main devs of the project, so that the deployment of these contracts can be done securely for mainnet. 

### Ecosystem Fit

- Where and how does your project fit into the ecosystem? 
We believe in a future where value flows freely accross decentralized networks. This means that TrustEVM needs a way to receive, swap and send away value to other networks, coins, tokens and NFTs.
- Who is your target audience?
A world of crypto users looking to safely trade their crypto currencies, with a focus on those not expert with decentralized technology platforms. We specially ait to make things easy. 
- What need(s) does your project meet?
The need of users to switch among multiple crypto currencie, the need to obtain tokens of new projects and swaps for stable currencies. 
- Are there any other projects similar to yours in the EOSIO ecosystem?
There are multiple crypto decentralized exchanged on out ecosystem, yet we are the first one available on the upcoming Trust EVM EOS side chain. There are currently no other decetralized exchanges built for Trust EVM.

## Team

### Team members

- **Team Leader:** Esteban Saá Barona

### Legal Structure
- **Registered Legal Entity:** We are in the initial process of registration
- **Registered Address:** N/A

### Team Experience

We have been working for over 25 years with highly scalable network platforms with a focus on Linux servers and network security. Our skills include developing highly scalable LAMP platforms. Discovered Bitcoin on 2012 and inspired on satoshidice, created satoshicode, a word finding game that was popular for a while, only to be killed when fees made it inpossible to play. We were early supporters and users of mastercoin/omni, this interest also was killed by BTC high fees. The high fees of Bitcoin switiched out attention to building on Ethereum, where we partcipaided anonymously for devevelopment of security testing code. During the bull runs switched focus into trading and investing; we gained a lot of experience but ultimatelly discovered that the passion  that motivate us is writing code and creating products.  We see a future where the world runs around decentralized technolgies and cryptopgraphy.  We were critical  on the early days of Ethereum for its plans of being PoS, https://twitter.com/estebs/status/614086876165705728 , eventually we understood its merits, and saw many of my concerns solved by dPoS. 

### Team Org Repos

- https://github.com/evm20

### Team Member Repos

- https://github.com/steban1

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/esteban-s-988b6457/

## Development Status

- Telegram Group: https://t.me/jointrustswap
- Figma sketches: https://www.figma.com/file/IPrFq5RrP0V3cSMO1IwJrv/Swap-branding-and-logo
- Twitter: https://twitter.com/joinTrustSwap

## Development Roadmap

### Overview

- **Total Estimated Duration:** The frontend deployment and mainnet deployment of smart contract will take 2 months of work, plus one month of testing and debugging. 

### Milestone 1  — Implement redesigned Swap frontend

- **Estimated duration:** 3 months
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

- We will be updating our core contracts to Version 3 of Uniswap as soon as the license allows us. There are other several contracts we are working on, they include bridging services and lending. We will be maintaining core defi contract, wEVM and Multicall.


## Additional Information

**How did you hear about the Grants Program?** personal recommendation
It was mentioned in our telegram channel by a member of our community. We were early to respond to the EOS community building an EVM,  we understand the smart contract we are deploying are important to the sucess of the EVM.
