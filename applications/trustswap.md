# EOS Network Foundation Grant Proposal

- **Project Name:** TrustSwap
- **Team Name:** TrustSwap
- **EOS Payment Address:** trustswap111
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A

## Contact

- **Contact Name:** Esteban Saá B.
- **Contact Email:** steban@gmail.com
- **Website:** https://trustswap-testnet.web.app/

## Project Overview

TrustSwap is a decentralized crypto exchange build on top of the Trust EVM Blockchain; it bring an easy to use yet poweful Web3 interface. The code is forked from Uniswap V2. This grant will fund the development of a new frontend, as well as the deployment of the correspondent smart contracts on the TrustEVM blockchain. 

### Overview

- **Name:** TrustSwap
- **Brief Description:** TrustSwap is an open source decentralized exchange structured to work on top of TrustEVM Blockchain. It delivers a fast, secure and easy to use EVM20 token trading. 
- **Relationship to EOSIO:** TrustSwap is built on top of Trust, an EVM compatible blokchain of EOSIO.
- **Reason for Interest:** We are looking to create the most scalable and easy to use swap service. Trust EVM provides a solid foundation to build on. 

### Project Details

- Our project is early on its development process, this allows us to align our decision making with the best interests of the IOS community.
- We compiled a few ideas for the designs here: https://www.figma.com/file/IPrFq5RrP0V3cSMO1IwJrv/Swap-branding-and-logo . We are still early on the process of creating a brand. Most of our work so far has been devoted to deploying, testing and adapting to the inerworking of TrustEVM. 
- Our code comes from the Uniswap project, the following links contains broad documentation on the project: https://docs.uniswap.org/protocol/V2/reference/API/overview
- We will be reusing many of the components of the code where our project is forked from. This includes frameworks as REACT for the frontend: https://reactjs.org/. For the back end we are using the MERN stack to build a static site. MERN includes tools such as: https://github.com/nodejs/node. The resulting code is static HTML that we host at Google Firebase, it includes several functions such as CDN, so we can substain highloads maintaing good quality of service, and defend from DDOS attacks. Further the hosting platform allows us to implement CD/CD pilelines and optimize our deployment methodologies. 
- While we are very early on our development process we have deployed several smart contracts and their respective interfaces. 
- https://trustswap-testnet.web.app/ is the frontend to our decentralized exchange. It curently makes use of the TrustEVM testnet.
- https://trustswap-farm.web.app/ is our farm contract, it accepts LP deposits from our decentralized exchange and pays out testnet token. 
- https://docs.trustswap-farm.web.app/ is our documentation site, it includes general information of our platform. We are using Gitbook for it, will be connected once our domain name is decided. 
- https://www.npmjs.com/settings/trustevm/packages , we have published an SDK to npmjs.com, this will make it easy for other developers to connect to our smart contract. There are multiple use cases for this, for instance market makers and arbitragers can use our SDK to make their systems work. 
  - TrustSwap will not divert far from the orignal source code we initially forked from, instead we will adapit it to TrustEVM. We start with the open source version of the Uniswap V2, and will upgrade to V3 once the license allow is. 
 - As part of our initial work we have deployed two extremely important smart contracts that will provide a backbone to the upcoming deployments from other teams. These are the WrappedEVM contract, and the Multicall2 contract. These contracts are fundamental building blocks of any EVM ecosystem. We plan to coordinate work with the main devs of the project, so that the deployment of these contracts can be done securely for mainnet. 

### Ecosystem Fit
 
- We believe in a future where value flows freely accross decentralized networks. This means that TrustEVM needs a way to receive, swap and send away value to other networks, coins, tokens and NFTs.
- Our target audience is a world of crypto users looking to safely trade their crypto currencies, with a focus on those not expert with decentralized  platforms. We specially aim to make things easy. 
- The project solves the need of users to trade among multiple crypto currencies; also the need to obtain tokens of new projects and swap for stable currencies. 
-  There are multiple crypto decentralized exchanged on our ecosystem, yet we are the first one available on the upcoming Trust EVM EOS blockchain. There are currently no other decetralized exchanges built for Trust EVM.

## Team

### Team members

- **Team Leader:** Esteban Saá Barona

### Legal Structure
- **Registered Legal Entity:** We are in the initial process of registration
- **Registered Address:** N/A

### Team Experience

We have been working for over 25 years with highly scalable network platforms with a focus on Linux servers and network security. Our skills include developing highly scalable LAMP platforms. Discovered Bitcoin on 2012 and inspired on satoshidice, created satoshicode, a word finding game that was popular for a while, only to be killed when fees made it inpossible to play. We were early supporters and users of mastercoin/omni, this interest also was killed by BTC high fees. The high fees of Bitcoin switched our attention to building on Ethereum, where we partcipaided anonymously for devevelopment of security testing tools. During the market bull runs switched focus into trading and investing; we gained a lot of experience but ultimatelly discovered that the passion  that motivate us is writing code and creating products.  We see a future where the world runs around decentralized technolgies and cryptopgraphy.  We were critical  on the early days of Ethereum for its plans of switching to  PoS, https://twitter.com/estebs/status/614086876165705728 , eventually we understood its merits, and saw many of our concerns solved by dPoS. 

### Team Org Repos

- This is our main code repository: https://github.com/evm20

### Team Member Repos

- https://github.com/steban1

### Team LinkedIn Profiles (if available)

- Esteban Saá B. Linledin: https://www.linkedin.com/in/esteban-s-988b6457/

- Telegram Group: https://t.me/jointrustswap
- Twitter: https://twitter.com/joinTrustSwap

## Development Status

We have a fully functional decentralized exchange working on the TrustEVM testnet, we have also deployed a functioning staking farm. Both are being actively tested by the EOS community. Further we have deployed multisig bridge contracts, an evm20 faucet, several evm20 tokens, wrapped EVM20 contract, and Multicall contract. We are the first team deploying contracts and actively testing the TrustEVM. 

## Development Roadmap

### Overview

- **Total Estimated Duration:** The frontend design and mainnet deployment of smart contract will take 2 months of work, plus one month of testing and debugging. We plan to be ready for the first day of TrustEVM mainnet with a production ready and fully functional decentralized exchange.

### Milestone 1  — Implement redesigned Swap frontend

- **Estimated duration:** 3 months
- **FTE:**  2
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License |  MIT  |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how to configure TrustEVM and use TrustSwap |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Deployment | We will provide a repository with instructions on how to deploy the frontend. |
| 0e. | Article | We will publish an **article** that explains how the different components of the platform are connected to make the platform work |


## Future Plans

- We will be updating our core contracts to Version 3 of Uniswap as soon as the license allows us. There are other several contracts we are working on, they include bridging services and lending. We will be maintaining the core DEFI contracts, wEVM and Multicall.


## Additional Information

**How did you hear about the Grants Program?** personal recommendation
It was mentioned in our telegram channel by a member of our community. We were early to respond to the EOS community building an EVM,  we understand the smart contract we are deploying are important to the sucess of the TrustEVM.
