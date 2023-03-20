
# EOS Network Foundation Grant Proposal
-   **Project Name:** EVMNS (EVM Name Service)
-   **Team Name:** EVMNS Labs
-   **EOS Payment Address:** evmnsdomains
-   **Level:** 3
-   **Pomelo Grant(s):** N/A
-   **Project is Open-Source:** Yes
-   **Project was part of Token sale:** No
-   **Repository where Project resides:** https://github.com/evmns/EVMNS

# Contact
- **Contact Name:** Harry Davis
- **Contact Email:** evmns_manager@outlook.com
- **Website:** N/A

# Project Overview
**EVMNS (EVM Name Service) is a distributed, open and extensible multi-chain DID domain naming system built on EVM and EOS,** relying on the high performance, security and reliability of EOS to better and seamlessly connect people, information, assets, dApps, etc. in the WEB3 world.<br/><br/>
EVMNS domains use the ERC721 protocol standard with .evm as the domain suffix, such as abc.evm, 123.evm, jack.evm, etc., to map human-readable and easy-to-remember names with all kinds of content at the same time, including but not limited to EVM addresses, EOS addresses, other cryptocurrency addresses, content hashes, URLs, and metadata.<br/><br/>
### Overview
- **Name:** EVMNS (EVM Name Service)<br/>
- **Brief Description:** A distributed, open and extensible multi-chain DID domain naming system built on EVM and EOS.<br/>
- **Relationship to EOSIO:** EVMNS's multi-chain layout will bring more new users to EOS and EVM, because it helps users of other chains to know and understand EOS and EVM, and to enjoy the unique advantages of EOS (industry-leading transaction speeds, high TPS and low transaction cost), and help EOS to expand its positive influence in the WEB3 world.<br/>
- **Reason for Interest:** WEB3 trend is developing rapidly, a set of DID domain naming system with perfect function, multi-chain layout and good user experience is the "identity infrastructure" of WEB3 application, and it can be confirmed that DID is like an avatar, which is the basic and essential element and the identity of WEB3 world. For more information, see our research **< Why DID is needed\>** in Additional Information at the end of this article.<br/><br/>

### Project Details
- **Mock-ups/designs of any UI components**<br/><br/>
   We will build the official website, including project introduction, domain registry and management, and explanatory documents, etc., to provide users with a complete one-stop experience.<br/><br/>
- **Implementation Overview**<br/><br/>
   EVMNS has two principal components. **Registry and Resolvers.**<br/>
   ![](https://github.com/evmns/evm_name_service/blob/main/registry.png?raw=true )
  - **EVMNS Registry**<br/><br/>
      The EVMNS registry is a smart contract that maintains a list of all domains and subdomains and stores three critical pieces of information about each domain: the owner of the domain, the resolver for the domain, and the caching time-to-live for all records under the domain.<br/><br/>
      The owner of a name can be an external account (a user) or a smart contract. A registrar is a smart contract that owns a top-level domain and distributes subdomains of that domain to users according to the rules in the contract.<br/><br/>
      The domain owner in the EVMNS registry is capable of:<br/>
      1.Set the resolver and TTL for the domain;<br/>
      2.Transfer ownership of the domain to another address;<br/>
      3.Change the ownership of subdomains;<br/><br/>
      The EVMNS registry exists simply to map domains to the resolver responsible for resolving that domain.<br/><br/>
  - **Resolvers**<br/><br/>
      The resolver is responsible for converting domains to addresses. Any smart contract that meets the criteria related to resolvers can be used as a resolver program in EVMNS.<br/><br/>
      Each record type (EVM address, content hash, etc.) defines one or more methods that the resolver must implement in order to provide such records. Adding a new record type does not require changes to the EVMNS registry or to existing resolvers.<br/><br/>
      Resolving a domain in EVMNS requires two steps: the first step is to ask the registry which resolver is responsible for the domain; the second step is to query that resolver for the result.<br/><br/>
      Let's say we want to find the EVM address pointed by "abc.evm". First, we ask the registry which resolver is responsible for resolving "abc.evm"; then, we ask that resolver for the address of "abc.evm".<br/><br/>
  - **About Namehash**<br/><br/>
      Resource constraints in smart contracts make it inefficient to interact directly with readable names, so EVMNS uses only fixed length 256-bit cryptographic hashes. In order to generate hashes from names while still retaining their hierarchical nature, EVMNS uses an algorithm called Namehash, which is used only to represent names within EVMNS.<br/><br/>
      Namehash is a recursive process that generates a unique hash for any valid name. Starting from the Namehash of any name (e.g., the Namehash of "abc.evm"), one can derive the Namehash of any subname (e.g., the Namehash of "ab. abc.evm"), and the derivation process does not require knowledge of or processing of the readable original name "abc.evm". It is this feature that allows EVMNS to be a hierarchical system without having to deal with readable text strings internally. <br/><br/>
      Before using Namehash for hashing, the name first needs to be normalized with the help of the UTS-46 standard to ensure that the letters in the name are case-insensitive and to prohibit the use of invalid characters. Any hashing and resolving of names must first be normalized to ensure that all users get consistency of EVMNS.<br/><br/>
### Ecosystem Fit
- **Where and how does your project fit into the ecosystem?**<br/><br/>
    EOS has integrated short domain name function in the main chain since its launch, and naturally supports user-defined account name, which is the first to achieve a good experience of human readability and easy to remember, **It would be a great pity if this advantage is not continued on EVM,** As we know, EVMNS, as a DID domain naming system, can fulfill the requirement well and help EVM to better continue the convenience and efficiency of EOS.<br/><br/>
Considering the better integration of EVM and EOS users, EOS mainnet users will have the privilege to register EVM domains (5-digit and above length domains) at a special price, **which not only fills the gap in the EOS ecological DID domain system, but also further helps the growth of EOS user scale** (more new users will create EOS accounts in order to get the privilege to register EVM domain at a special price). In addition, it also helps EOS users to have the same experience of EOS account name on EVM, and EOS users can also create their own decentralized super business cards, personal decentralized WEB3 homepage/website. It's a multi-benefit!<br/><br/>
What's more, EVMNS will also provides free technical support to holders of existing short names on the EOS mainnet to assist them in issuing corresponding DID domain service agreements in the EVM, such as assisting holder of short name ‘eos’ to issue domain protocol with the suffix .eos on EVM, contributing to the ecological prosperity of EOS and the EVM together.<br/><br/>
- **Who is your target audience ?**<br/><br/>
    Our users are positioned as WEB3 ecological users, corresponding to blockchains including but not limited to EOS, EVM, ETH, BSC, etc.<br/><br/>
- **What need(s) does your project meet?**<br/><br/>
    **One identity accessible to multiple blockchains.** There is no doubt that we are moving towards a multi-chain future, where each WEB3 user travels through different blockchains and dApps, having and managing multiple identities, multiple usernames, multiple sets of identity information, full of tedium and inconvenience and lacking a good experience.<br/><br/>
With EVMNS, you can ensure that one universal identity remains intact, not only for all applications, but for all blockchains. You will only have to manage one set of identities, such as your profile, Email, Twitter, Telegram, ETH address, EOS address, EVM address, etc. How wonderful it will be to be able to sync to all chains with one edit.<br/><br/>
EVMNS will also meet these needs: human readable and memorable WEB3 usernames, a more user-friendly experience in WEB3 world, decentralized super business cards, and personal decentralized WEB3 homepage/website. For more information, see our research **< Why DID is needed>** in Additional Information at the end of this article.<br/><br/>
- **Are there any other projects similar to yours in the EOSIO ecosystem?**<br/><br/>
There are no other projects on EOS and EVM ecosystem that are similar to EVMNS for now.<br/><br/>
But there are similar DID projects in other blockchains, such as ENS on ETH, SPACE ID on BSC, Bonfida on Solana, EVNS on Evmos, PNS on Polka, and cross-chain DID service‘.bit’, etc. The DID domain naming service protocol has become one of the basic projects on every blockchain, showing a blossoming market. See our research **< DID Market Analysis>** in Additional Information at the end of this article for more details on the market.<br/><br/>
Compared to other DID domain projects, EVMNS has a special feature. Benefited from EOS's industry-leading transaction speeds (0.5 seconds), high TPS and low transaction costs, users will have an unparalleled experience when using EVMNS. They will be able to confirm the successful modification of their identity information in seconds, without worrying about block congestion or the cost of interacting with the chain, and will be able to enjoy the WEB3 world more smoothly, which will be an important advantage of EVMNS.<br/><br/>
# Team
### Team members
- **Team Leader: Harry Davis**<br/>
- Allen Harris<br/>
- Frank Lee <br/>
### Legal Structure
- **Registered Legal Entity:** Jump Dream PTE. LTD.<br/>
- **Registered Address:** 5001 Beach Road#07-37, Golden Mile Complex, Singapore 199588<br/>
### Team Experience
The core members of EVMNS Labs are the first ecological participants of EOS, who experienced and witnessed the launch of EOS and are still deeply involved in the ecological construction.<br/><br/>
Team members have participated in several medium to large scale EOS projects before and after, and also developed ENS (Ethereum Name Service) related domain Exchange, domain bulk registry protocol, etc. We are not only EOS loyalists, but also ENS heavy players, with good understanding of DID domain naming system.<br/>
### Team Member Repos
- Allen Harris, https://github.com/sutaiyi
- Frank Lee, https://github.com/chenminmin4

# Development Roadmap
### Milestone Summary
- **Total Estimated Duration:** 12 weeks
- **Full-Time Equivalent (FTE):** 6 FTE
- **Total Costs:** 195,000 USD
### Milestone 1 - Requirements Analysis and official website
- **Estimated duration:** 2 weeks
- **FTE:** 2
- **Costs:** 20,000 USD

| ID  | Deliverable  |Specification|
| ------------ | ------------ | ------------ |
| 0a.   |License   | MIT License  |
| 0b.  | Documentation  | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles.  |
| 0c.  | Testing Guide  | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file.  |
| 0d.  | Docker  | Use Docker to start a container that runs a local nodevm instance where specific users and contracts are deployed for developer testing. This ensures that developers have the same environment when using EVMNS.  |
| 1  | Demand Analysis  | Unpacking requirements, developing business process diagrams, planning business modules, standardizing development documentation and testing processes, etc.  |
| 2  | Release official website  | Including project introduction, Roadmap and other content.  |<br/><br/>
### Milestone 2 - Smart Contracts
- **Estimated duration:** 4 weeks
- **FTE:** 5
- **Costs:** 100,000 USD

| ID  | Deliverable  |Specification|
| ------------ | ------------ | ------------ |
| 0a.  | License  | MIT License  |
| 0b.  | Documentation  | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles. |
| 0c.  | Testing Guide  | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file.  |
| 0d.  | Docker  | Use Docker to start a container that runs a local nodevm instance where specific users and contracts are deployed for developer testing. This ensures that developers have the same environment when using EVMNS.  |
| 1  | Core Contracts  | At the core of EVMNS is a smart contract that maintains a list of all domains and sub-domains and stores three key pieces of information about each domain: the owner of the domain, the resolver of the domain, and the cached time to live (i.e., TTL) for all records under the domain.  |
| 2  | Domain registrar  | EVMNS allows domain owners to manage all their domains, including sub-domain registrations. We will provide standard domain registration contracts and interfaces, allowing all compliant contracts to access and renew, transfer and other operations for domains.  |
| 3  | Root Node Management  | Completing the design of the root node, EVMNS will lock the control of the root node so that the root owner cannot influence the ownership of the .evm domain and set the root node to be held jointly by the community in a multi-signature contract, guaranteeing all the power of the user.  |
| 4  | Domain Resolver  | Resolvers are responsible for the actual process of translating names into addresses. Any contract that implements the relevant standards may act as a resolver in EVMNS. |<br/><br/>
### Milestone 3 - Key Systems and Components
- **Estimated duration:** 3 weeks
- **FTE:** 3
- **Costs:** 45,000 USD

| ID  | Deliverable  |Specification|
| ------------ | ------------ | ------------ |
| 0a.  | License  | MIT License  |
| 0b.  | Documentation  | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles. |
| 0c.  | Testing Guide  | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file.  |
| 0d.  | Docker  | Use Docker to start a container that runs a local nodevm instance where specific users and contracts are deployed for developer testing. This ensures that developers have the same environment when using EVMNS.  |
| 1  | Domain Manager  | The Domain Manager in EVMNS is a domain management contract that allows domain owners to manage the domains they own, change names in the registry and transfer ownership to anyone else.  |
| 2  | Reverse resolver  | The reverse resolver in EVMNS provides the ability to declare reverse records for use in configuring records as a convenient feature most commonly used as a way to specify address specification names.  |
| 3 | Metadata Storage Management System  | Store the domain metadata independently in the metadata management system and access the corresponding metadata through api.  |
| 4  | Domain Management System  | Build EVMNS domain management system to realize administrators capability of financial review, daily log maintenance review, emergency management, etc. for EVMNS.  |<br/><br/>
### Milestone 4 - In-depth testing
- **Estimated duration:** 2 weeks
- **FTE:** 2
- **Costs:** 20,000 USD

| ID  | Deliverable  |Specification|
| ------------ | ------------ | ------------ |
| 0a.  | License  | MIT License  |
| 0b.  | Documentation  | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles. |
| 0c.  | Testing Guide  | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file.  |
| 0d.  | Docker  | Use Docker to start a container that runs a local nodevm instance where specific users and contracts are deployed for developer testing. This ensures that developers have the same environment when using EVMNS.  |
| 1  | In-depth test  | Automated unit tests with 100% coverage and multiple rounds of functional testing are completed internally to ensure functionality and robustness.  |
| 2  | dApp Development Documentation  | Establish a perfect dApp development documentation system to meet and support the quick access of dApp developers.  |<br/><br/>
### Milestone 5 - Deployment Test Network
- **Estimated duration:** 1 weeks
- **FTE:** 2
- **Costs:** 10,000 USD

| ID  | Deliverable  |Specification|
| ------------ | ------------ | ------------ |
| 0a.  | License  | MIT License  |
| 0b.  | Documentation  | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles. |
| 0c.  | Testing Guide  | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file.  |
| 0d.  | Docker  | Use Docker to start a container that runs a local nodevm instance where specific users and contracts are deployed for developer testing. This ensures that developers have the same environment when using EVMNS.  |
| 0e. | Article| We will publish an English article about the project on medium.com, explaining how smart contracts work and how the project will be used. Also, we will illustrate the goals and outcomes set through the grant.|
| 1  | New version of the official website  | Including project introduction, domain registration and management, instruction documents, etc.  |
| 2  | Deployment of test networks  | Deploy the test environment and conduct public testing to further ensure the smooth launch and security of the system  |<br/><br/>

#### Multi-Chain Ecology
Multi-chain ecology is the focus of the second phase of development, and we will prioritize the completion of the first phase of development (the above five milestones) to maximize the assurance that EVMNS can be launched and run stably at the first time after the official launch of EVM.<br/><br/>
Therefore, the development content, duration and cost of the multi-chain ecology will be separately defined before the launch of the second phase.<br/><br/>
# Future Plans
- Multiple rounds of in-depth testing will be carried out first after the testnet is deployed. When all the problems found in the test are fixed, we will start the security audit of the smart contract to further ensure security. On the premise that the security audit is completely passed, it will finally be deployed to the mainnet and the project will be officially launched. It is estimated that it will take about 1 month to complete the above items.<br/><br/>
- We will build EVMNS DAO, realize community management, and promote the implementation of decentralized operation and R&D of EVMNS.<br/><br/>
- Register WEB2 domain with .evm suffix with DNS operators for domain resolution and binding services for traditional browsers so that users can directly access websites/personal homepages corresponding to .evm domain in Chrome, Edge and other browsers to achieve good interoperability between WEB3 and WEB2.<br/><br/>
- Develop EOS plug-ins and browser plug-ins belonging to EVMNS to help users manage their EVMNS domains more easily through plug-ins, quick access, collection management of EVMNS domains of other users, etc.<br/><br/>

# Additional Information
### How did you hear about the Grants Program? 
We learned of the program by following announcements on ENF’s Twitter and other channels.<br/>
### Some of our research
#### What is DID
   DID is the abbreviation of ‘Decentralized Identity’ , which is a kind of digital identity without a centralized institution as the final guarantee, and is an extension and expansion in WEB 3 of the concept of "user portrait" in WEB2.<br/><br/>
The final form of DID development may be that each user has a unique network-wide identity, and multiple local identities for segmented scenarios. Users remember and identify DIDs through domains, manage DIDs and interact with applications through wallets, and integrate different credentials and local identities on multiple chains through wallets.<br/><br/>
#### Why DID is needed
- **Human readable and easy to remember WEB3 username**<br/><br/>
  Although each of us has a unique ID number, in our daily life, we generally use 'name' as an identifier of one's identity (although there will be renames) because it is easier for daily communication.<br/><br/>
The world of WEB3 has the same problem: while people currently interact primarily based on wallet addresses, no one wants to remember that long string of characters. If the digital identity of WEB3 needs a 'name', then what EVMNS is doing is hoping to be that 'name'.<br/><br/>
- **A more user-friendly WEB3 experience**<br/><br/>
  In WEB2 world, digital identity is platform-centered, and different products within the same group are connected through an account system. For example, Tencent's mailbox, games and finance can all use the same account; Google, Facebook and other top Internet enterprises also have their own account systems. Although this kind of identity system is easy to build, its disadvantages have been widely known: the accounts between platforms do not interoperate with each other, and users have no way to control their own identity data.<br/><br/>
  In WEB3 world, user interaction is mainly based on wallet address, so a series of activities related to the address constitute the most native decentralized digital identity DID of WEB3, and it can be naturally interoperable between different dApp applications without barriers. In this way, users can quickly find their acquaintance and friends when they enter new applications and games, without having to re-add them back by themselves like in WEB2 world.<br/><br/>
  Imagine a peer-to-peer chat where you can find the desired contact by simply searching for xxx. evm instead of an 18-digit irregular address starting with 0x. What a wonderful experience, and each EVM domain is unique so you don't have to worry about matching the wrong person.<br/><br/>
  Moreover, by using a DID name to connect to various cryptocurrency addresses, you can receive cryptocurrency payments from others through that domain name without having to copy and paste long addresses.<br/><br/>
- **Decentralized Super Business Card**<br/><br/>
  Each DID domain is a unique NFT, and the owner is free to set the content they wish to map or record, in addition to the common EVM wallet address, other cryptocurrency addresses, but also avatars/pictures, Email, Website, profile, Twitter/Telegram accounts and other content, no one can tamper or delete the information, the user has full control of his or her identity information. A DID may seem like a simple domain name, but it contains unlimited content, and **is a super business card for the WEB3 world.**<br/><br/>
- **Personal decentralized WEB3 homepage/website**<br/><br/>
  EVMNS allows users to create personal decentralized homepages/websites and upload them to the Interplanetary File System (IPFS), a global network of storage protocols that allow computers around the world to store and share data in a peer-to-peer fashion.<br/><br/>
In short, EVMNS and IPFS can help users to establish personal homepages/blogs and websites, with functions similar to the combination of RSS feeds + WEB3 Medium. **Users will have full ownership, including domain name, content and data,** completely avoiding the possibility of being deleted by registrars/data operators.<br/><br/>
- **WEB3 Infrastructure**<br/><br/>
  DID is also known as the "identity infrastructure" of WEB3 applications. As discussed above, it is basically determined that DID and avatar are the basic and essential elements of WEB3, being the identity of the WEB3 world.<br/><br/>
  
#### DID Market Analysis
- **ENS(Ethereum Name Service)**<br/><br/>
  ENS was launched on May 4, 2017 by Alex Van de Sande and Nick Johnson of the ETH Foundation. In November 2021, ENS issued its own governance token and launched an airdrop. At the same time, ENS established the ENS DAO to enable community governance, where token holders will participate in the management of the assets, as well as voting on DAO proposals and co-voting on the use of the vault.<br/><br/>Earlier in the interview Vitalik said, "**The Ethereum Domain Name Service ENS is by far the most successful non-financial ETH application,** which can basically be compared to a decentralized phone book."<br/><br/>
As of November 27, 2022, **the total amount of ENS domain  registration reached 2.79 million** and the number of Ethereum addresses holding ENS domains reached 609,000. Since November 2021, the number of monthly ENS registrations has shown explosive growth, reaching a peak of 437,000 monthly registrations in September 2022.<br/><br/>
**Total registration revenue of ENS domains has exceeded $60 million,** of which nearly $50 million has been realized so far in 2022 alone. Total secondary market transactions have reached 112.39K ETH and $197 million.<br/><br/>
![](https://github.com/evmns/evm_name_service/blob/main/t2.png?raw=true )
<div align="center">（Data source dune.com/makoto/ens)</div><br/>

![](https://github.com/evmns/evm_name_service/blob/main/t3.png?raw=true )
<div align="center">（Data source NFTGO.io)</div><br/>
Whether it is the registration scale, transaction scale, or the number of holder’s addresses, ENS is far ahead of similar projects, occupying the absolute leading position and having the strongest community consensus.<br/><br/>
The following is the partial sales of historical.<br/>
paradigm.eth, 420ETH<br/>
000.eth, 300ETH<br/>
Opensea.eth, 99.89ETH<br/>
Nike.eth, 60ETH<br/>
Samsung.eth, 60ETH<br/><br/>

- **SPACE ID (BNB Chain Name Service)**<br/><br/>
  SPACE ID is a decentralized domain naming service protocol developed based on BNB Chain, officially launched in August 2022, with .bnb as the domain suffix, essentially the same as ENS, and dedicated to building a common name service network that seamlessly connects people, information, assets and applications across the blockchain. And by allowing users to bind their identities across multiple chains, communities can build their own domain naming services through SPACE ID's network. To date, more than 40 applications have announced that they have enabled integration of the SPACE ID protocol.<br/><br/>
**A seed round of funding led by Binance Labs was completed on September 2nd, 2022 for an undisclosed amount.**<br/><br/>
As of November 27, 2022, SPACE ID domain name total registrations reached 304,000, the total number of holders’ addresses reached 98,700, and **the total registration revenue was 14,700 BNB, USD 4.42 million** (1 BNB = USD 300). The total secondary market transaction size was about 22,000 BNB, 6.60 million USD.<br/><br/>
![](https://github.com/evmns/evm_name_service/blob/main/t4.png?raw=true )
<div align="center">（Data source dune.com/spaceid/spaceid）</div><br/>
At present, WEB3 domain services like ENS and SPACE ID are also BNS on Binance, Bonfida on Solana, EVNS on Evmos, PNS on Polka, and cross-chain DID service‘.bit’, etc. The DID domain naming service protocol has become one of the basic items of every blockchain, showing a blossoming market state.
