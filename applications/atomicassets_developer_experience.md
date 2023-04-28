


# EOS Network Foundation Grant Proposal


- **Project Name:** AtomicAssets Developer Experience
- **Team Name:** pink.gg Solutions GmbH dba AtomicHub
- **EOS Payment Address:** pinknetworkx
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/pinknetworkx/atomicassets-contract

## Contact

- **Contact Name:** Jona Wilmsmann
- **Contact Email:** jona@pink.gg
- **Website:** https://pink.gg


## Project Overview

### Overview

- **Name:** AtomicAssets Developer Documentation
- **Brief Description:** We intend to make it easier for developers to take part and start building in the Antelope NFT ecosystem. For this, we plan to improve the developer journey and increase usability of the AtomicAssets NFT standard by creating robust documentation and examples, which are currently missing from our ecosystem
- **Relationship to EOS Network / Antelope:** AtomicAssets is by far the most widely adopted NFT standard for Antelope chains. Since its creation in 2020, more than 367,000,000 NFTs have been created across the WAX, EOS, Proton and Telos blockchains, and thousands of collections have been created.
- **Reason for Interest:** The user experience that can be offered by NFT projects utilizing AtomicAssets on an Antelope chain far surpasses the user experience any other blockchain can offer to-date. However, as of today, most of the largest and highest-profile NFT projects still choose other blockchains like Ethereum or Solana to build on. We believe a big reason for this is the less mature developer ecosystem on Antelope chains, which leads to NFT projects often not considering Antelope. We want to address these issues with a goal of bringing significant, high-quality NFT projects into the Antelope ecosystem. The best way to do this is through education.

### Project Details

The core of the project, being the AtomicAssets NFT standard, already exists in a fully finished and battle-tested state.

A basic documentation of the AtomicAssets smart contract is available in the [AtomicAssets GitHub Wiki](https://github.com/pinknetworkx/atomicassets-contract/wiki). However, compared to the vast amount of information available for EVM-based NFTs, this is insufficient for inexperienced developers to get started. We recognize that many  developers will not only be new to AtomicAssets, but also new to Antelope in general. We want to remove friction for new projects, and provide structural support (clear reference documentation & code samples) for them to get started. We believe that a significant investment in developer resources is needed to make Antelope NFTs a compelling choice for new developers.

We plan to not just create resources for the smart contract itself, but also for the other components needed to build a full AtomicAssets dapp, in particular the open source [AtomicAssets API](https://github.com/pinknetworkx/eosio-contract-api) that we also developed and the [atomicassets-js](https://github.com/pinknetworkx/atomicassets-js) Javascript library. This will consist of

1) Documentation of the AtomicAssets Smart Contracts
2) Documentation of the AtomicAssets API (using eosio-contract-api)
3) Beginner guides, including covering Antelope basics
4) Examples, covering the full AtomicAssets stack from building custom smart contracts to using the API and integrating it in Dapps using atomicassets-js

We expect this to be an ongoing effort, and plan to adapt to market trends to put out relevant and valuable information.

### Ecosystem Fit

We view NFT technology as one of the most obviously valuable innovations that blockchain technology brings - Enabling true digital ownership for the first time. We expect that NFT based projects, e.g. gaming or collectibles projects, or other innovations we haven’t even contemplated, will have a leading impact in shaping the web3 landscape and mainstream entertainment in the years to come.

AtomicAssets is already widely adopted within the Antelope ecosystem, and has established itself as the go-to standard for NFTs. More than 367MM NFTs have been created by more than 2,500 whitelisted (as in checked by us to ensure quality and originality standards) collections on the WAX and EOS blockchains alone.

AtomicAssets is used by some of the biggest dapps (e.g. AlienWorlds / Splinterlands) in the world and some of the biggest brands (e.g. Topps MLB, Funko). It has been interacted with by millions of users to-date. However, adoption rates by projects, businesses and developers has lagged behind other blockchains because the value proposition of AtomicAssets VS ERC-721 is not readily apparent, and the ecosystem support is vastly inferior. We hope to address all of that with this initiative.

## Team

### Team members

- **Team Leader:** Jona Wilmsmann (Co-Founder)
- Fabian Emilius (Co-Founder)
- Jeffrey Haas (Chief Revenue Officer)
- Technical Writer (To be hired)

### Legal Structure
- **Registered Legal Entity:** pink.gg Solutions GmbH
- **Registered Address:** Tölzer Straße 1, 82031 Grünwald, Germany

### Team Experience

Jona and Fabian are the two co-founders of the company. They founded the company in 2019, while studying Computer Science at the Technical University of Munich. They started out by building multiple smaller tools for the Antelope (back then named ‘eosio’) ecosystem and became block producers on the WAX blockchain. A plan to build an NFT based game led to them creating the AtomicAssets NFT standard and building the hub and trading platform AtomicHub.

Jona created all the smart contracts used by the company to date, including the AtomicAssets standard.

Fabian created the AtomicAssets API and built the first version of AtomicHub almost entirely himself. Today, he leads the technical and product teams at pink.gg.

Jeffrey has a track record of joining startups early (i.e. PokerStars and DraftKings) and helping scale them into becoming large companies. At pink, he leads the growth efforts, with a particular focus on partnerships with game studios and IP holders that aim to bring new exciting content into the ecosystem, and a large new user base together with that.

### Team Org Repos

- https://github.com/pinknetworkx
- https://github.com/pinknetworkx/eosio-contract-api
- https://github.com/pinknetworkx/atomicassets-contract
- https://github.com/pinknetworkx/atomicmarket-contract
- https://github.com/pinknetworkx/atomicpacks-contract
- https://github.com/pinknetworkx/atomicassets-js
- https://github.com/pinknetworkx/atomicmarket-js

### Team Member Repos

- https://github.com/fabian-emilius
- https://github.com/jona-wilmsmann

### Team LinkedIn Profiles (if available)

- https://linkedin.com/in/jona-wilmsmann-8834661b5/
- https://linkedin.com/in/fabian-emilius/
- https://linkedin.com/in/jeffreyhaas/

## Development Status

As mentioned before, AtomicAssets already exists and is widely adopted, but the existing technical documentation is still rather rudimentary.

## Development Roadmap


### Milestone Summary

- **Total Estimated Duration:** ~14 months 
- **Full-Time Equivalent (FTE):** ~1.36 FTE
- **Total Costs:** 167,500 USD




### Milestone 1 — Recruit a technical writer

- **Estimated duration:** 3 months
- **FTE:**  1
- **Costs:** 30,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | N/A |
| 0b. | Documentation | N/A |
| 0c. | Testing Guide | N/A |
| 1. | Job Listing & Advertising | To achieve our goal of creating compelling developer docs, we will need to recruit a dedicated technical writer as a FTE for the duration of the project. We will be looking for a candidate with an existing understanding of blockchain technology and NFTs. |
| 2. | Recruitment & Signing | We will utilize both internal HR resources as well as external recrutiers to find suitable candidates. Work with external recruiters will incur costs. We note that depending on the  candidate's availability and previous commitments, it may take up to an additional 3 months for them to start working for us, though we will prioritize quicker starters. |
| 3. | Training | We will train the technical writer and have  them familiarize themselves with AtomicAssets before they start with creating content. |



### Milestone 2.1 — Introduction to Antelope & Comparison with other major blockchains


- **Estimated duration:** 2 weeks
- **FTE:**  1.2
- **Costs:** 4,500 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Article | We will create an article introducing readers to Antelope from a developer's perspective and compare Antelope to other major blockchains, in particular EVM based chains. |




### Milestone 2.2 — Introduction to AtomicAssets & Comparison with other major NFT standards


- **Estimated duration:** 2 weeks
- **FTE:**  1.2
- **Costs:** 4,500 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Article | We will create an article introducing readers to AtomicAssets from a developer's perspective and compare AtomicAssets to other major NFT standards, in particular ERC721. |




### Milestone 2.3— Guide: Getting started with Antelope & AtomicAssets


- **Estimated duration:** 3 weeks
- **FTE:**  1.2
- **Costs:** 6,750 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Guide | We will create a guide that will help readers get started building with AtomicAssets on Antelope. We aim to position this as a go-to resource for developers new to the space, and feature an overview of relevant Antelope blockchains (including testnets), an account creation guide including the basic use of wallets, and we will compile an overview of existing available documentation, available APIs including public endpoints, and common packages used for Antelope and AtomicAssets development. |




### Milestone 3.1— Design and build atomicassets.io


- **Estimated duration:** 1 month
- **FTE:** 2
- **Costs:** 16,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | We will not document the code for the website itself |
| 0c. | Testing Guide | N/A |
| 1. | Website | We will design and build atomicassets.io - A website that will feature an introduction to AtomicAssets, advantages that it has over other NFT standards, easy reference of documentation and useful links. For this we will involve our team of UX/UI designers and frontend engineers as well as the technical writer. |




### Milestone 3.2— Update AtomicAssets documentation


- **Estimated duration:** 1 week
- **FTE:**  1.2
- **Costs:** 2,250 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Update Documentation | We will update the existing AtomicAssets documentation and bring it into the same format that we will use for all other documentation as part of this project. |




### Milestone 3.3— Update AtomicMarket documentation


- **Estimated duration:** 1 week
- **FTE:**  1.2
- **Costs:** 2,250 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Update Documentation | We will update the existing AtomicMarket documentation and bring it into the same format that we will use for all other documentation as part of this project. |




### Milestone 3.4— Introduction to using AtomicAssets in custom smart contracts


- **Estimated duration:** 1 month
- **FTE:**  1.2
- **Costs:** 9,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Guide | We will create a step by step guide to building custom smart contracts that build on top of AtomicAssets. We will briefly touch on the general Antelope smart contract development approach but will otherwise link to existing resources on Antelope smart contracts. We will include code examples to follow and end up with a simple example smart contract. |




### Milestone 4.1— Update and document atomicassets npm package


- **Estimated duration:** 1 month
- **FTE:**  1.5
- **Costs:** 12,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Update package | We will bring the existing atomicassets npm package up to date, which already is working and public but has not been updated for a while. |
| 2. | Documentation | We will thoroughly document the package, replacing the existing barebones documentation. |




### Milestone 4.2— Update and document atomicmarket npm package


- **Estimated duration:** 1 month
- **FTE:**  1.5
- **Costs:** 12,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Update package | We will bring the existing atomicmarket npm package up to date, which already is working and public but has not been updated for a while. |
| 2. | Documentation | We will thoroughly document the package, replacing the existing barebones documentation. |




### Milestone 4.3— Guide: Example mini game dapp


- **Estimated duration:** 2 months
- **FTE:**  1.5
- **Costs:** 32,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Build dapp | We will build an example on chain NFT mini game. It will feature a custom smart contract, a website using the AtomicAssets API to get data, and full wallet integration for users to log in and interact with the game |
| 2. |  Guide | We will create a step by step guide that will walk through the process of creating a dapp build on top of AtomicAssets from start to finish. It will serve as an example that developers can use as a starting point for their own project, and will allow us to explain all aspects of AtomicAssets development in an interesting and non abstract way. |




### Milestone 5.1— Update and document AtomicAssets API


- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 16,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | AGPL 3.0 |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Update | We will update the existing AtomicAssets API, and in particular work on making the code easier to read and understand. |
| 2. | Documentation | We will thoroughly document the API, adding documentation both for the API endpoints and for how to run the API. |




### Milestone 6.1— Creator Beginner Guide


- **Estimated duration:** 1 week
- **FTE:**  1.2
- **Costs:** 2,250 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Guide | We will create a guide targeting creators that aren't necessarily developers. It will explain the basic AtomicAssets structure and concepts and include a step by step guide of using the NFT Creator on AtomicHub. |




### Milestone 6.2— Advanced Creator Guide


- **Estimated duration:** 2 weeks
- **FTE:**  1.2
- **Costs:** 4,500 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Guide | We will create guides targeting advanced creators, explaining commonly used attributes with special handling (e.g. "img" for main image), how to set up AtomicHub market filters, how to create a collection catalog and an introduction to IPFS. |




### Milestone 7.1 — Hosting a blockchain node


- **Estimated duration:** 3 weeks
- **FTE:**  1.2
- **Costs:** 6,750 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Guide | We will create a guide for how to host an Antelope blockchain node, either with or without state history. We will also go into considerations like which hardware is required, best practices for high availability and common problems. |




### Milestone 7.2 — Hosting the AtomicAssets API


- **Estimated duration:** 2 weeks
- **FTE:**  1.2
- **Costs:** 4,500 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Guide | We will create a guide for how to host the AtomicAssets API. We will also go into considerations like which hardware is required, best practices for high availability and common problems. |




### Milestone 7.3 — Hosting an IPFS node


- **Estimated duration:** 1 week
- **FTE:**  1.2
- **Costs:** 2,250 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT for all code / code examples |
| 0b. | Documentation | Self explanatory |
| 0c. | Testing Guide | N/A |
| 1. | Guide | We will create a guide for how to host an IPFS node. We will also go into considerations like which hardware is required, best practices for high availability and common problems. |



## Future Plans

Our success as a company relies on the wide adoption of NFT technology, in particular on our "home" (Antelope). To date, we have almost entirely* self-funded the development of the AtomicAsset standard and supporting infrastructure across the Antelope ecosystem.

- In the short term, we will continue to provide support to creators and collectors on both the EOS and WAX networks. As the primary marketplace for the EOSIO community, we ensure that essential services such as discovery, trading, auctions, selling, and buying are operational on our platform. 
- In the long term, we strive to make the AtomicAsset standard more accessible to prospective developers, particularly AAA gaming studios aiming to incorporate blockchain technology. We want to increase the visibility, usability and adoption of NFTs on Antelope.
- We hope that after the milestones covered by this grant are completed, the ecosystem will have matured and developed so much that we can justify keeping the technical writer on our payroll using our own funds.


## Additional Information

**How did you hear about the Grants Program?** Yves (ENF CEO) and Zack (ENF CCO) met with Jona and Jeffrey in Q4 2022 and invited us to consider applying as part of this conversation.

The milestones are grouped by category. Since they are mostly independant from one another, we do not intend to work on them in the order we listed them. Instead, we plan to work on the foundational milestones first, before starting with the more sophisticated and integrated milestones. In general, we plan to listen to feedback regarding which information and format is most useful and act accordingly.

*External funding has come from WAX in 2020 through a grant of roughly $10K for the creation of AtomicAssets. Our team has also received a $100K Recognition Grant in 2021 from the EOS Network Foundation. Otherwise, no external funding has been used to capitalize the business to-date since the initial seed capital from the founders. 
