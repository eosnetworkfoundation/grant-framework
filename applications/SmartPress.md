# EOS Network Foundation Grant Proposal

- **Project Name:** SmartPress
- **Team Name:** SmartPress
- **EOS Payment Address:** 0xD8BC1BcA4f1D4A0c1d35E3ef177fF2ef1f548eA8
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 2
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** No
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/crokau/smartpressau

## Contact

- **Contact Name:** Lachlan Greenbank
- **Contact Email:** smartpressau@gmail.com
- **Website:** https://smartpress.ai

## Project Overview

### Overview

> Please provide the following:

- **Name:** SmartPress - Most advanced smart contract building platform (powered by AI and EVM infrascructure).
- **Brief Description:** Prompt, write, compile, test, fix, deploy all in one streamlined flow.
- **Relationship to EOS Network / Antelope:** EOS_EVM is currently a main focus chain on the SmartPress platform, and we want to make it even more so the premiere chain for SmartPress users default when building on the EVM.
- **Reason for Interest:** We want to onboard a million new developers to EOS_EVM by working more closely with the ENF.

### Project Details

SmartPress's goal has always been to make creating your own smart contracts achievable for anyone. However, most developers face struggles in getting started with smart contract development and bringing their visions to life.

Born out of the EOS global hackathon in 2018, SmartPress envisions an easy-to-use smart contract building platform powered by AI. It simplifies contract writing, compilation, deployment to EOS_EVM, and verification processes—making smart contract development a breeze.

Try it today at https://smartpress.ai

The vision is to empower users to express their ideas and receive tangible results effortlessly, similar to Remix but without the complexity.

The goal is to onboard thousands of new developers to the EOS developer ecosystem by providing a user-friendly platform for prototyping and deploying ideas. SmartPress streamlines EOS development, with EOS_EVM network forefront in our wallet's network selector. Additionally, we assist users in setting up wallets and provide guides on obtaining testnet faucet tokens specifically for EOS.

To illustrate SmartPress's capabilities, we asked it to create a smart contract for this grant process. You can find the results at [this link](https://www.smartpress.ai/create/ai/results/e0ed18b5-a3dc-42a9-88d4-afd8d064f805) and verified on EOS_EVM testnet [here](https://explorer.testnet.evm.eosnetwork.com/address/0x425974edf0381bd2bF6a18412c3D8553280A07a8/contracts#address-tabs).

Prompt: "Create a system that manages grant applications for funding, where applications fall into three tiers of funding: 10,000 USD, 50,000 USD, and 200,000 USD. Users should propose their projects and upload a link to the git commit of their project proposal. Specified voters set up in the contract can vote on the proposal, with 2 votes required for a 10,000 USD proposal, 3 votes for 50,000 USD, and four votes for 200,000 USD."

We are open to Open Sourcing all our code if we get the opportunity to work with the ENF on this grant.

Architecture diagram

![Screenshot 2023-05-30 at 4 38 29 pm](https://github.com/crokau/grant-framework/assets/71380821/5521c955-6810-42aa-bf4a-6030e3d23de4)

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?
- Developer tool for coders and non coders to create anything at all EVM. This is a ecosystem growth tool for EVM chains.

- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
- Developers, management of web3 companies, researchers, people looking to get their feet wet with smart contracts.

- What need(s) does your project meet?
- Without this project, if someone wants to get into smart contract development it would take years... With this project they can start experimenting in minutes. 
  
- Are there any other projects similar to yours in the EOS Network / Antelope ecosystem? No
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?
- There are projects like ChainGPT (with a token attached), their tech that is miles behind SmartPress, no compiling, no fixing, no deploying, no sharing.. and a lot of other things. They seem to be going nowhere fast (in terms of what we are trying to acheive with Smartpress), good luck to them.
- Platforms like Thirdweb That offer a lot of contract templates, but they are prebuilt and static and dont offer the creativity available by Smartpress's ai/infrasctructure architecture.

## Team

### Team members

- **Team Leader:** Lachlan Greenbank

### Legal Structure
- **Registered Legal Entity:** Private (to be shared)
- **Registered Address:** Private (to be shared)

### Team Experience

Lachlan lead the engineering team that built the first globally regulated and fully backed stock exchange on Ethereum, SOMA.finance, expected to launch in 2023.

He won the EOSIO global hackathon in Sydney in 2018 and has been building smart contracts since 2016, experiencing the pain points and pitfalls firsthand.

### Team Org Repos

- https://github.com/crokau

### Team Member Repos

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/lachlan-g-99185789/

## Development Status

Working product - smartpress.ai

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

### Milestone Summary

### Milestone 1 Example — New must have features asked for by EOS_EVM users

- **Estimated duration:** 2 month
- **FTE:**  1
- **Costs:** 15,000 USD

| ID | Deliverable | Specification | 
| ----- | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) create and deploy a contract using the new features added |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | N/A - we dont use docker |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)
| 1. | Build a feature that allows bringing and upgrading preexisting contract.
| 2. | Upgrade wallet system to allow the use of any local dev chains.
| 3. | UX changes that push users towards EOS EVM testnet and mainnet over than other chains (faucet enhancements etc).
| 4. | AI function re-architecture for improved code generations.



### Milestone 2 Example — Non smart contract code generations and enhancements

- **Estimated Duration:** 2 month
- **FTE:**  1
- **Costs:** 15,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) create and deploy a contract using the new features added |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | N/A - we dont use docker |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)
| 1. | Automatic Generation of frontend code based on created contracts.
| 2. | Wallet login and added privacy features
| 3. | Support for more smart contract libraries in code generations, Chainlink, more OpenZepplin contracts, etc.
| 4. | Ongoing maintenance to ensure a seamless platform experience.


## Future Plans

> Please include here:

Our long term plans are to onboard millions of new developers and deploy billions of contracts. As Smart contracts become more and more used in everyday life, and AI code generation only gets better over time,
We see smartpress as a building block to the new web economy.

We wend a lot of tweets out daily about new creations and features, we also reply and reach out to a lot of prominent people in the crypto space constantly to raise brand awareness and garner new users.

## Additional Information

**How did you hear about the Grants Program?** personal recommendation.
