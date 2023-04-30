# EOS Network Foundation Grant Proposal

- **Project Name:** Scry Protocol
- **Team Name:** Keychain INC
- **EOS Payment Address:**
EOS876ZWzPTGr4dEczLdZJrJDZmCfGj3Swt6Eqmtbi3pZ99opAc44
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** [https://github.com/ScryProtocol](https://github.com/ScryProtocol/)

## Contact

- **Contact Name:** JD Burger
- **Contact Email:** pr0@keychain.me
- **Website:** [scry.finance](https://docs.scry.finance/)

## Project Overview

### Overview
- **Name:** Scry Protocol - Permissionless framework for onchain data
- **Brief Description:**
An Open, Decentralized and Permissionless Framework for Bringing On-Demand Web2 Data to Web3
Morpheus is a framework that allows developers to request any API from web2, directly onchain for their web3 apps. This tool enables real-time data requests, any API and data to be used, and can be used on any EVM network. Morpheus has been designed to make it easier for developers to build decentralized applications that can interact with the real world, thereby bridging the gap between web2 and web3.
- **Relationship to EOS Network / Antelope:** 
EOS is severly underserved by other oracle networks such as Link, with no real feeds by the largest oracle providers, which even then all being provided by only a few signers, creating not only limited data for devs and projects but all being unable to be custom for projects with their own data sources to ensure security and ability to deploy new feeds and scale. Alternatives are usually just Link forks or also have a token required in the model, cannot deploy own oracles, cannot access custom data or are not simple to use.

The data available to devs directly limits use cases which can be deployed, you can’t deploy insurance without data about whats being insured, you cant deploy financial markets thats not crypto exclusive without access to traditional finance data. By allowing high scale, easy to deply oracles that supports new feeds in real time, projects can scale not just the transactions but the capbilities.
- **Reason for Interest:** 
Trying to expand to every EVM based network and help them scale both in throughput and use cases.
### Project Details
- Mock-ups/designs of any UI components
https://base.dapp.scry.finance/
https://morpheus.scry.finance/
- Data models of the core functionality
https://github.com/ScryProtocol/Morpheus
- API specifications of the core functionality
https://docs.scry.finance/docs/morpheus/use-request-feeds
- An overview of the technology stack to be used
Solidity/react/JS
- Documentation of core components, protocols, architecture, etc. to be deployed
https://docs.scry.finance/docs/
- PoC/MVP or other relevant prior work or research on the topic
https://docs.scry.finance/docs/morpheus/build-your-own-oracle
- What your project is _not_ or will _not_ provide or implement
  We will not be trying to create oracles ourselves or maintaining them, though we are able to if the foundation wish, we want to simply create tool to allow anyone to create their OWN oracles. See for the mission
  https://scryprotocol.substack.com/p/introducing-data-lps

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?
Data LPs (Data Liquidity Providers) are essentially decentralized marketplaces for data. They provide a way for developers to source data from a variety of different sources, while also providing incentives for individuals and entities to contribute their data to the marketplace. In a Data LP, anyone can contribute their data and earn rewards for doing so. Developers can then purchase the data they need from the signers they choose. Scry is a pioneering a decentralized and open market data approach with Morpheus that allows anyone to easily set up and operate their own oracle and node with no technical expertise.

By enabling anyone to fill requests for data, Scry allows developers and projects to choose where they source their data based on reputation for who they feel will be honest, as well as even source the data from their own community.
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
Devs for protocols
- What need(s) does your project meet?
Oracles and data
- Are there any other projects similar to yours in the EOS Network / Antelope ecosystem?
  - If so, how is your project different?
One of the biggest issues with data and oracle infrastructure in crypto is that it is monopolized by players like Chainlink, and all alternatives suffer from the same closed systems for data through set signers or a single token as the core security. This results in a centralized approach to data, which goes against the very ethos of decentralization.

By enabling anyone to fill requests for data, Scry allows developers and projects to choose where they source their data based on reputation for who they feel will be honest, as well as even source the data from their own community.

Morpheus nodes, which are self-hosted oracles, are a key component of the Scry ecosystem. They are able to accept requests for data from any API endpoint on any EVM network, directly onchain. This enables real-time requests for any data instantly and with the signers they choose.
  - If not, are there similar projects in related ecosystems?
See above
## Team

### Team members
- **Team Leader:** JD Burger
- Mario Johannson

### Legal Structure
- **Registered Legal Entity:** Keychain INC
- **Registered Address:** 16192 Coastal Highway, Lewes, DE 19958

### Team Experience
In Crypto since 2011. Cofounded Keychain,  Cryptodevs.
Previously studied Neuroscience before going full time crypto in 2019.
Notables: EIP 5075 Author, First NFT DAO fragmentation implementation, made an AMM before Uniswap.
Repos
https://github.com/ConjureFi

### Team Org Repos
https://github.com/ScryProtocol/
https://github.com/ScryProtocol/contracts/
> Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

### Team Member Repos
https://github.com/pr0toshi

### Team LinkedIn Profiles (if available)

## Development Status
- academic publications relevant to the problem,
https://scryprotocol.substack.com/p/understanding-scrys-hashranch-vrf
https://docs.scry.finance/docs/morpheus/vrf-hash-ranch
- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
https://scryprotocol.substack.com/
- references to conversations you might have had related to this project with anyone from the EOS Network Foundation,
@nsjames on Discord
- previous interface iterations, such as mock-ups and wireframes.
https://base.dapp.scry.finance/
https://morpheus.scry.finance/

Alpha
https://docs.scry.finance/docs/morpheus/build-your-own-oracle

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

> :zap: If any of your deliverables is based on someone else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Milestone Summary

- **Total Estimated Duration:** 3 months 
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 150,000 USD

### Milestone 1 Implement EOS Application and Front End
- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 45,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT / Apache 2.0 / GPLv3 / Unlicense |
| 0b. | Documentation | We will provide both **documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our oracle nodes and send test transactions, which will show how the new functionality works. This will be EOS specific with preset RPC|
| 0d. | Binaries | We will provide binaries that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains the full process for deployment and about the infrastructure for EOS (what was done/achieved as part of the grant).
| 1. | Application interface to EOS EVM | We will create prebuilt setup for EOS with preset RPCs in the repo
| 2. | Front-End / User Interface | We will create a UI that connects to shows authorised oracles to explore |  
| 3. | Pull based oracle  | We will create a pull based oracle for EOS devs with the EOS teams help to allow teams to use oracles with preset update frequencies, see
https://base.dapp.scry.finance/
This will also allow us to do a hire for support/business outreach/general nondev help

### Milestone 2 VRF Research
- **Estimated Duration:** 1 month
- **FTE:**  2
- **Costs:** 25,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT / Apache 2.0 / GPLv3 / Unlicense |
| 0b. | Documentation | We will provide both **documentation** of the code and a basic **tutorial** that explains how a user can use VRFs for their apps and the security guarantees. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 1. | VRF Verifier | We will create a open source verifier for the VRF
| 2. | VRF and Protocol audit | We will audit the contracts and VRF - $15k bounty

### Retroactive Milestone 3 All that we've built
- **Estimated Duration:** 1 year
- **FTE:**  2
- **Costs:** 40,000 USD
Am requesting a grant for retroactive purposes for what we've built, having spent resources, time, lost opportunities as well as effectively having delivered core tools already without even asking for any funding before we built it showing our commitment to the project and creating value before requesting funds. As such this request is just us requesting if the foundation want to compensate for the tools we've made and find them valuable. We will also port all the below tools to be on the network or available.
| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT / Apache 2.0 / GPLv3 / Unlicense |
| 0b. | Documentation | We have provided both **documentation** of the code and a deep **tutorials** that explains how a user can use Morpheus and Scry as well as VRFs for their apps and with high security guarantees / permissionless deployment being able to self deploy. |
| 1. | VRF | We have created a open source VRF mechanism
https://scryprotocol.substack.com/p/understanding-scrys-hashranch-vrf
https://docs.scry.finance/docs/morpheus/vrf-hash-ranch
| 2. | Open Oracle Framework | 1 Contract Many Feeds
Oracles can have a single feed or have 1 contract and submit many feeds/prices available, allowing submitFeed(uint[] feedIDs, uint[] values) to save gas for large feed sets. This allows large players to easily submit multiple feeds with 1 call and not need to manage multiple transactions/calls to multiple contracts. | 
Monetization and Incentives
Because oracles have upkeep costs, the oracles can charge a small fee in ETH. This way they can deploy many feeds as long as they are worth the upkeep, and because we compact many feed updates into single calls, efficiency couldn’t be better. Users can then shop around for the best feed or can choose based on price, depending on risk tolerance. This creates an open oracle marketplace and revenue model and allows projects to quickly bootstrap feeds they need from providers. Oracles can then price their feeds based on upkeep and cost as well as deprecate unused feeds. | 
Containerization
Oracles are created as single contracts which are owned by the oracle parties that submit feeds, these oracles then create an id for every feed they want to create, which allows for users to explore feeds offered by an oracle and select based on id, while having each oracle be completely contained, such that bad oracles do not affect good oracles and users can choose providers that are good for them. | 
Scalability
OOF was designed for projects, users and providers to easily create new feeds and oracles for Ethereum and other networks to have access to offchain data in a decentralized and open market model. By allowing for anyone to create an oracle with minimal knowledge and time, and setting up decentralized providers | 
Oracles key features
- Autonomous oracle system where devs can self deploy own feeds/oracles and use custom signers for permissionless, decentralized and secure deployment with self-controllable feed creation using custom APIs for rapid development. The nodes are able to be deployed in <15m on any EVM by devs with 0 code needed and update feeds supported in realtime as needed.
- 200+ different feed updates with 1 tx (high scale data). Scaled with Layer 2s.
- Use any API with a highly robust parse engine, controlled by a simple spreadsheet, just put the URL, the parse for the json to be expected and basic info and the feed will be ready to use and submitted on chain by all signers.
- Data lookup for historical data for all feeds natively, allows for both immutable data access, TWAP construction and onchain analytics.
- Allows for various monetization structures at a feed level, oracle providers can charge for certain feeds to earn revenue as well as provide others for public use, subscription models for data requests at the feed level and oracle level.
- Largest data provider for Goerli, Sepolia, Optimism, Canto, polygon and providing 3x the data Link are able to, with the ability to scale to 100x by simply updating the APIs pulled from. Stress tested with up to 500 feeds with just 1 tx, which is 10x Links entire oracle network for any Layer 2, and more than matches all oracle feeds for mainnet they offer, in 1 tx.
- Fully decentralized and open source, the Front End, Node and Contracts are all open source and can be self hosted by teams and networks | 
https://base.dapp.scry.finance/ -will be ported
https://github.com/scryprotocol/NodeDeploy

| 3. | 
Morpheus | 
An Open, Decentralized and Permissionless Framework for Bringing On-Demand Web2 Data to Web3 | 
Morpheus is a framework that allows developers to request any API from web2, directly onchain for their web3 apps. This tool enables real-time data requests, any API and data to be used, and can be used on any EVM network. Morpheus has been designed to make it easier for developers to build decentralized applications that can interact with the real world, thereby bridging the gap between web2 and web3. | 
One of the most significant advantages of Morpheus is its ability to access any API endpoint. This means that developers can now easily request data from sources such as social media platforms, weather APIs, and financial data APIs directly on the blockchain. This makes it possible to build applications that are more relevant to the real world such as insurance, synthetics, social dapps and that can provide more value to users. | 
Morpheus is also designed to be network-agnostic, which means that it can be used on any EVM network. This makes it easier for developers to build applications that are not limited to a particular blockchain, but that can be used on any network that supports EVM. | 
Morpheus is an exciting new tool that is set to revolutionize the way developers build decentralized applications. By enabling real-time data requests and access to any API endpoint, Morpheus makes it easier to create applications that are more relevant to the real world. With its network-agnostic design, Morpheus can be used on any EVM network, making it a powerful tool for developers looking to build decentralized applications. | 
- Anyone can run a data provider and earn fees from requests
- Creates a data market and lets devs choose their oracle sources at the signer level and batch many for redundancy
- Any API endpoint in realtime for any data
- Custom highly secure VRF with simple verification
- 0 Code setup and deployment, takes <60s to set up and have an operational node
- Out of the box nodes, contract deployment and verifiers and front end  | 
https://github.com/ScryProtocol/Morpheus/
https://docs.scry.finance/docs/morpheus/morpehus


### Milestone 4 Community Support
- **Estimated Duration:** 1 month
- **FTE:**  2
- **Costs:** 40,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 1. | Bring devs onto the platform with support for deploying their own oracles | We will create channels for support for devs to come and delpoy their own oracles and get any support they need in deploying and running their oracles. This milestone is for helping the community use the tools and bring projects on as oracles creating a decentralized data market. Includes development, further docs, guides, private help, outreach.
| 2. | Hackathon sponsorships and bounties - 20k optional
## Future Plans
Short-term Plans:
Enhance the Scry Open Oracle Framework (OOF) and Morpheus by implementing new features, improving performance, and fixing bugs to increase usability and adoption.
Promote and support the project by creating comprehensive documentation, tutorials, and guides to make it easy for developers to integrate Scry OOF and Morpheus into their projects.
Engage with the developer community through webinars, workshops, and hackathons to raise awareness about the project and gather valuable feedback.
Collaborate with other projects in the ecosystem to identify potential synergies and partnerships that can help increase adoption and expand the project's reach.
Long-term Plans:
Establish Scry OOF and Morpheus as the go-to solution for decentralized oracles and data access in the blockchain ecosystem.
Foster a thriving community of developers, data providers, and users who contribute to the growth and success of the project.
Continuously research and develop new technologies and methodologies to improve the robustness, scalability, and security of the Scry OOF and Morpheus platforms.
Explore and develop new use cases and applications for decentralized oracles and data access in various industries, such as finance, supply chain, healthcare, and more.

## Additional Information

**How did you hear about the Grants Program?** personal recommendation by nsjames

- Work you have already done. See retroactive milestone
- If there are any other teams who have already contributed (financially) to the project.
No
- Previous grants you may have applied for.
None from EOS
