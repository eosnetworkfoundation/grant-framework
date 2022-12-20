# EOS Network Foundation Grant Proposal



- **Project Name:** EOS Domains
- **Team Name:** VisionTech, Inc.
- **EOS Payment Address:** domains.hufi
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** https://pomelo.io/grants/eosdomains
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/EOSDomains/EOS-Domains

## Contact

- **Contact Name:** Cy Dai
- **Contact Email:** eosdomains@foxmail.com
- **Website:** N/A


## Project Overview


### Overview


- **Name:** EOS Domains
- **Brief Description:** The EOS Domains is a distributed, open, and extensible naming system based on the Trust EVM. 
- **Relationship to EOSIO:** With the development of EOSIO ecology, domain name service has become one of the essential infrastructure of blockchain.
- **Reason for Interest:** We are bullish on about the future development of EOSIO ecology and want to help EOSIO build the important infrastructure of domain name service to connect people, information, assets, and applications in the digital world through EOS domain names.

### Project Details

The EOS Domains registry consists of a single smart contract that maintains a list of all domains and subdomains, and stores three critical pieces of information about each:

(1) The owner of the domain

(2) The resolver for the domain

(3) The caching time-to-live for all records under the domain


The owner of a domain may be either an external account (a user) or a smart contract. A registrar is simply a smart contract that owns a domain and issues subdomains of that domain to users that follow some set of rules defined in the contract.


Owners of domains in the EOS Domains registry may:

(1) Set the resolver and TTL for the domain

(2) Transfer ownership of the domain to another address

(3) Change the ownership of subdomains


The EOS Domains registry is deliberately straightforward and exists only to map from a name to the resolver responsible for it.

Resolvers are responsible for the actual process of translating names into addresses. Any contract that implements the relevant standards may act as a resolver in EOS Domains. General-purpose resolver implementations are offered for users whose requirements are straightforward, such as serving an infrequently changed address for a name.

Each record type - cryptocurrency address, IPFS content hash, and so forth - defines a method or methods that a resolver must implement in order to provide records of that kind. New record types may be defined at any time via the EIP standardization process, with no need to make changes to the EOS Domains registry or to existing resolvers in order to support them.

Resolving a name in EOS Domains is a two-step process: First, ask the registry what resolver is responsible for the name, and second, ask that resolver for the answer to your query.


- One SDK for All

Fast implementation: To corner a market, we not only need features that support users, but also that support partners. It is through their integrations that our product can really grow and reach new eyes and use cases. 

Name service aggregator: EOS Domains has TLDs that can be used to resolve other domains and name services. This means developers only have to integrate our SDK in order to have integrated with all the other main name services out there. No more having to integrate more than one name service while having to keep an eye open on new name services to stay relevant.


- Mock-ups/designs of any UI components

![Web 1920 – 1](https://user-images.githubusercontent.com/120728170/208610091-7ae7f559-6181-461b-873f-df048b139ac3.jpg)

![Web 1920 – 4](https://user-images.githubusercontent.com/120728170/208610185-78f445a4-796c-4774-82fb-05a8b59d6829.jpg)

![5](https://user-images.githubusercontent.com/120728170/208610358-9511bcfa-e7bb-4fb7-bed5-fb2d4526d479.jpg)

![6](https://user-images.githubusercontent.com/120728170/208610378-4369a1fa-e4e6-4be4-b96b-5462155d848d.jpg)

![7](https://user-images.githubusercontent.com/120728170/208610393-1199d3ec-a8de-4056-9594-0b93e1c4c7f0.jpg)

![Web 1920 – 8](https://user-images.githubusercontent.com/120728170/208610421-82818409-5191-48b2-96d0-64a2d96813e8.jpg)



### Ecosystem Fit



- Where and how does your project fit into the ecosystem?

As you known, domain name service has become one of the essential infrastructure of blockchain. Through EOS Domains, the users of EOSIO can have their own domain name account on the Antelope, ending in “.eos”.
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?

The users of EOSIO are our target audience, including the users of DeFi, GameFi, NFTs on EOSIO.
- What need(s) does your project meet?

There is no secret to the fact that social interactions have been the root cause for the latest internet boom. People want identity interactions, they want to be recognized: display their names in leaderboards, chat windows, wallet holdings, NFT listings, etc. They want to interact with people, and not addresses, to become a brand themselves. We help people trade cryptos, lend tokens, mint NFTs, and buy tickets or even homes in the future highly decentralized world easier by using EOS Domains.
- Are there any other projects similar to yours in the EOSIO ecosystem?

We are not aware of other projects similar to this in the EOSIO ecosystem.
  - If not, are there similar projects in related ecosystems?
  
  Yes, Ethereum Name Service（ENS）.

## Team

### Team members

- **Team Leader:** Cy Dai
- Moffat
- Gary
- Never Zhang
- Judy
- Icey
- Tom
- Jason
- Nic
- Kevin
- Martin
- Arron
- Mia
- Amy

### Legal Structure
- **Registered Legal Entity:** VisionTech Inc.
- **Registered Address:** Room 201, Building 1, No. 200, Tianfu Fifth Street, High-tech Zone, Chengdu, China

### Team Experience
- Cy Dai, Team Leader. NFT collector; Co-Founder of OVO META, Ex Co-Founder of FPX META, Founder of Fight 4 Climate; Climate Reality Leader, Founding Member of Meta Time DAO; Alumni of CGIU, Global Honorary Follow of Zhejiang University; G20YEA Social Influence Elite, Startup Member of China Young Entrepreneurs Association, 2019 Outstanding Social Entrepreneur, former China Regional Director of 2030 Youth Force of UNDP Asia Pacific.
- Moffat, FullStack Developer. Core Member @MarsDAO_,Web3 Builder, Developer @soldiamondheads, FullStack Developer.
- Gary, Smart Contract Engineer. Fourteen years of mobile Internet practitioners. Six years of game development and co-founder. A single game has more than 10 million downloads. Developed some NFT tools. Be optimistic about NFT for a long time, invest and collect NFT. A staunch supporter of blockchain technology, all in web3.
- Never Zhang, Product Manager. 8 years of working experience, senior Web2 product manager.
- Judy, Head of Brand. Futurist, Investor, MBA degree in Luxury Management while in France. Currently studying at EAC Arts Management MBA in France.
- Icey, Smart Contract Engineer. Blockchain contract expert, back-end engineer, OpenDAO core contributor, 721 Club Technology OG.
- Tom, Front-end Engineer. Grand front-end engineer, Lark's open capability architect.
- Jason, FullStack Developer. Web/JavaScript full stack engineer, author of WebCell open source front-end framework, Microsoft MVP, Ali Cloud MVP, FCC Global Top 100 volunteer, FCC Chengdu community leader, open source community director.
- Nic, Front-end Engineer. Web/JavaScript front-end engineer, excellent volunteer of Open Source Club, volunteer of TEDxChengdu, core organizer of FCC Chengdu Community.
- Kevin, BD. Studied abroad and lived in Singapore, engaged in fintech for 7 years, crypto trading experience for 5 years, angel investor, contemporary art and NFT collector enthusiast, 5 years BD experience.
- Martin, User Growth Operations Officer. Good at operating mainstream we-media channels such as Discord, Twitter, ins, mirror for Crypto projects.
- Arron, Community Manager. Streamline Technologies NFT Project Manager, 2 years of community management experience.
- Mia, UI Designer. Familiarity with software development processes using Agile methodologies. Knowledgeable in interaction design and information architecture. Experienced with design software, such as Figma, Adobe XD.
- Amy, Graphic Designer. 3 years of graphic design experience, good command over design techniques and visual elements.



### Team Org Repos

- https://github.com/EOSDomains
- https://github.com/EOSDomains/EOS-Domains



## Development Status

We are familiar with the EOSIO ecology and code framework through desk research. At present, we are sorting out the product function list and designing the product prototype.

- previous interface iterations, such as mock-ups and wireframes.

![Web 1920 – 3](https://user-images.githubusercontent.com/120728170/208610141-38459110-f267-473f-80f3-7f3e972baef6.jpg)

## Development Roadmap


### Milestone Summary


- **Total Estimated Duration:** 2 months 
- **Full-Time Equivalent (FTE):** 14 FTE
- **Total Costs:** 125,000 USD


### Milestone 1 — Market analysis & User analysis & Platform analysis(Trust EVM)

- **Estimated duration:** 1 week
- **FTE:**  4
- **Costs:** 5,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | Unlicense |
| 0b. | Documentation | Documentation for total team |
| 0c.	| Testing Guide | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file |
| 1. | Market analysis | Analyze the market data of the most popular did projects |  
| 2. | User analysis | Analyze the user behavior data of the most popular did projects |  
| 3. | Platform analysis | Analyze the basic data of each public chain, including the number of users and daily activity |  
| 4. | Feasibility report | Get the feasibility of developing the did project on Trust Evm blockchain |  



### Milestone 2 — Product design

- **Estimated Duration:** 1 week
- **FTE:**  6
- **Costs:** 40,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles |
| 0c. | Unit tests | Unit tests for the logic |
| 1. | Core function design | What users can do with our products |  
| 2. | Front-end interaction design | For the convenience and safety of user operations, which data of the user needs to be saved and processed on the server |  
| 3. | Backend design | For the convenience and safety of user operations, which data of the user needs to be saved and processed on the server |  
| 4. | Contract design | Cooperate with functional design to realize a safe and efficient contract structure |  


### Milestone 3 — Coding

- **Estimated Duration:** 3 weeks
- **FTE:**  7
- **Costs:** 50,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles |
| 0c. | Unit tests| Unit tests for the developers & test engineers |
| 1. | Front-end coding and development | Realize the previously planned layout, interaction, fluency, and interact with the backend and contract |  
| 2. | Backend coding and development | Provide the functional interface required by the front end, provide data display and storage, and logical calculation |  
| 3. | Contract code and development | For the convenience and safety of user operations, which data of the user needs to be saved and processed on the server |  
| 4. | Function development | Use solidity for contract function development |  


### Milestone 4 — Alpha test

- **Estimated Duration:** 1 week
- **FTE:**  5
- **Costs:** 10,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles |
| 0c.	| Testing Guide | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file |
| 1. | Internal Testing In The Development Department | Developers swap testing other developers' features with a clear rationale |  
| 2. | Testing Department | Complete test |  
| 3. | Partner Test | Open to partner testing |  


### Milestone 5 — Beta testing and whitelist activity

- **Estimated Duration:** 1 week
- **FTE:**  8
- **Costs:** 10,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance for users in our articles |
| 0c.	| Testing Guide | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file |
| 1. | Deploy Testnet | Users can register .eos domain names on the testnet |  
| 2. | Sweepstakes | Users who participate in the registration have the opportunity to obtain the white list qualification for pre registration |  
| 3. | Feedback | Users who report valid questions have the opportunity to pre register |  


### Milestone 6 — Mainnet launch

- **Estimated Duration:** 1 week
- **FTE:**  7
- **Costs:** 10,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance for users and whitelists in our articles |
| 0c.	| Testing Guide | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file |
| 0e. | Article | We will publish an English article about the project on medium.com, explaining how smart contracts work and how the project will be used. Also, we will illustrate the goals and outcomes set through the grant | 
| 1. | Pre-register | For whitelisted users |  
| 2. | Public Sale | Anyone can start registering/resolving/transferring/trading .eos domain names |  
| 3. | Announcement Of Partners And Projects Cooperation | Empower the eos domain name to reflect the value of the domain name |  




## Future Plans


- how you intend to use, enhance, promote and support your project in the short term, and

We plan to work with as many of Trust EVM's eco-programs as possible, build a network of partnerships, and invest more resources in marketing to engage early adopters through whitelist campaigns.

- the team's long-term plans and intentions in relation to it.

Connect your identifiers: EOS Domains will let you connect your identities from the Web2 world. Your Twitter handle, email address, Github account.
VisionTech intends to bid on future ENF projects through the Grant Framework.

## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation staff recommendation


