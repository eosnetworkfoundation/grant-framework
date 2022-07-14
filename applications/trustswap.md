# EOS Network Foundation Grant Proposal
- **Project Name:** TrustSwap
- **Team Name:** TrustSwap
- **EOS Payment Address:** trustswap111
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A

## Contact
- **Contact Name:** Esteban Saá B.
- **Contact Email:** steban@gmail.com
- **Website:** https://www.trustswap.finance

## Project Overview
TrustSwap is a decentralized crypto exchange built on top of the Trust EVM Blockchain; it connects an easy to use Web3 interface with solidity written smart contracts forked from the Uniswap project. This grant will fund the development of a new frontend, as well as the deployment of the correspondent smart contracts on the Trust EVM blockchain. 

### Overview
- **Name:** TrustSwap
- **Brief Description:** TrustSwap is an open source decentralized exchange designed to work on top of the Trust EVM Blockchain. It delivers fast, secure and easy to use EVM20 tokens trading. 
- **Relationship to EOSIO:** TrustSwap is built on top of Trust, an EVM compatible blockchain of EOS.
- **Reason for Interest:** We are looking to create the most scalable and easy to use swap service. Trust EVM provides a solid foundation to build on. 

### Project Details
- https://www.trustswap.finance/ is the frontend to our decentralized exchange. It currently makes use of the Trust EVM testnet.
- https://farm.trustswap.finance/ is our farm contract, it accepts LP deposits from our decentralized exchange and distributes testnet tokens. 
- https://docs.trustswap.finance/ is our documentation site, it includes general information about our platform.
- https://www.npmjs.com/package/@trustevm/sdk , we have published an SDK to npmjs.com, this will make it easy for other developers to connect to our smart contract. There are multiple use cases for this, for instance market makers and arbitrageurs can use our SDK to connect their tools to our platform. 
- TrustSwap will not divert far from the original source code we initially forked from, instead we will adapt it to Trust EVM. We start with the open source version of the Uniswap V2, and will upgrade to V3 once the license allows it. 
- As part of our initial work we have deployed two extremely important smart contracts that will provide a backbone to the upcoming deployments from other teams. These are the WrappedEVM contract, and the Multicall2 contract. These contracts are fundamental building blocks of any EVM ecosystem. We plan to coordinate work with the main devs of the project, so that the deployment of these contracts can be done securely for mainnet.
- Our project is early in its development process, this allows us to align our decision making with the best interests of the EOS community.
- We compiled a few ideas for the designs here: https://www.figma.com/file/IPrFq5RrP0V3cSMO1IwJrv/Swap-branding-and-logo . We are still early in the process of creating a brand. Most of our work so far has been devoted to deploying, testing and adapting to the inner workings of Trust EVM. 
- Our code comes from the Uniswap project, the following links contains broad documentation on the project: https://docs.uniswap.org/protocol/V2/reference/API/overview
- We will be reusing many of the components of the code where our project is forked from. This includes frameworks as REACT for the frontend: https://reactjs.org/. For the back end we are using the MERN stack to build a static site. MERN includes tools such as: https://github.com/nodejs/node. The resulting code is static HTML that we host at Google Firebase, it includes several functions such as CDN, so we can maintain good quality of service, and defend from DDOS attacks. Further the hosting platform allows us to implement CI/CD pipelines and optimize our deployment methodologies. 
- While we are very early in our development process we have deployed several smart contracts and their respective interfaces. 

### Ecosystem Fit
 
- We believe in a future where value flows freely across decentralized networks. This means that Trust EVM needs a way to receive, swap and send away value to other networks, coins, tokens and NFTs.
- Our target audience is a world of crypto users looking to safely trade their crypto currencies, with a focus on those not expert with decentralized  platforms. We specially aim to make things easy. 
- The project solves the need of users to trade among multiple crypto currencies; also the need to obtain tokens of new projects and swap for stable currencies. 
-  There are multiple crypto decentralized exchanges on our ecosystem, yet we are the first one available on the upcoming Trust EVM blockchain. There are currently no other decentralized exchanges built for Trust EVM.

## Team

### Team members

- **Team Leader:** Esteban Saá Barona

### Legal Structure
- **Registered Legal Entity:** We are in the initial process of registration
- **Registered Address:** N/A

### Team Experience

We have been working for over 25 years with highly scalable network platforms with a focus on Linux servers and network security. Our skills include developing highly scalable LAMP platforms. Discovered Bitcoin in 2012 and inspired by satoshidice, created satoshicode, a word finding game that was popular on the early bitcoin days, only to be killed when fees made it impossible to play. We were early supporters and users of mastercoin/omni, this interest also was killed by BTC high fees. The high fees of Bitcoin switched our attention to building on Ethereum, where we participated anonymously for development of security testing tools. During the market bull runs switched focus into trading and investing; we gained a lot of experience but ultimately discovered that the passion that motivates us is writing code and creating products.  We see a future where the world runs around decentralized technologies and cryptography.  We were critical  on the early days of Ethereum for its plans of switching to  PoS, https://twitter.com/estebs/status/614086876165705728 , eventually we understood its merits, and saw many of our concerns solved by dPoS. 

### Team Org Repos

- This is our main code repository: https://github.com/evm20

### Team Member Repos

- https://github.com/steban1

### Team LinkedIn Profiles (if available)

- Esteban Saá B. LinkedIn: https://www.linkedin.com/in/esteban-s-988b6457/
- Telegram Group: https://t.me/jointrustswap
- Twitter: https://twitter.com/joinTrustSwap

## Development Status

We have a fully functional decentralized exchange working on the Trust EVM testnet, we have also deployed a functioning staking farm. Both are being actively tested by the EOS community. Further we have deployed multisig bridge contracts, an EVM20 faucet, several EVM20 tokens, wrapped EVM20 contract, and Multicall contract. We are the first team deploying contracts and actively testing the Trust EVM. 

## Development Roadmap

### Overview

- **Total Estimated Duration:** The frontend design and mainnet deployment of smart contract will take 2 months of work, plus one month of testing and debugging. We plan to be ready for the first day of Trust EVM mainnet with a production ready and fully functional decentralized exchange.

### Milestone 1  — Deploy contracts to the Trust EVM testnet

- **Estimated duration:** 1 months
- **FTE:**  2
- **Costs:** 5,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License |  MIT  |
| 0b. | Repository | We will provide a repository with instructions on how to deploy the frontend. |
| 0c. | Swap  | We will deploy a testnet version of TrustSwap. |
| 0d. | Farm | We will deploy a testnet version of the farming contract. |


### Milestone 2  — Implement redesigned Swap frontend and mainnet contract deployment

- **Estimated duration:** 2 months
- **FTE:**  2
- **Costs:** 5,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License |  MIT  |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how to configure Trust EVM and use TrustSwap |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 1. | Swap  | We will deploy a mainnet version of the swap contract. |
| 2. | Farm | We will deploy a mainnet version of the farming contract.|
| 3. | Contracts | We will verify that the bytecode of the repository code matches the deployed bytecode. |
| 4. | Frontend | We will deploy and updated frontend design. |

## Future Plans

- We will be updating our core contracts to Version 3 of Uniswap as soon as the license allows us. There are other several contracts we are working on, they include bridging services and lending. We will be maintaining the core DEFI contracts, wEVM and Multicall.

## Additional Information

**How did you hear about the Grants Program?** personal recommendation
It was mentioned in our telegram channel by a member of our community. We were early to respond to the EOS community building an EVM,  we understand the smart contract we are deploying are important to the success of the Trust EVM.
