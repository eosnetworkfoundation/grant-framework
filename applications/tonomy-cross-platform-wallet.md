# EOS Network Foundation Grant Proposal

- **Project Name:** EOSIO cross-platform wallet
- **Team Name:** Tonomy Foundation
- **EOS Payment Address:** tonomyaccou1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/Tonomy-Foundation/tonomy-id

## Contact

- **Contact Name:** Jack Tanner
- **Contact Email:** jack@tonomy.foundation
- **Website:** https://tonomy.foundation

## Project Overview

We submit this grant proposal for feedback about the design and fit for the EOS and EOSIO ecosystems. We are happy to work with you to fix problems in the ecosystem related to identity and be connected with others doing so. We want to align with the community reasonably before moving forward with developing something to ensure it can be used, easily and have the greatest impact for EOS and EOSIO. Your support and funding helps us achieve this goal!

### Overview

We are building a cross-platform mobile blockchain and SSI wallet for EOSIO public chains like EOS, Telos and WAX. This can be used to s send tokens, sign dApp transactions, passwordless sign into web2 and web3 apps and share credentials. We plan to build several non-custodial recovery mechanisms: social recovery, security questions and hardware recovery. This recovery will allow users to recover both keys as well as sovereign data. Our experience in sovereign identity and design gives us the confidence needed to say we can do this.

We see this project as an extension of the Wallet+ blue paper. We want to support the work of these new EOSIO/Mandel SDK's by integrating early releases and giving feedback and potentially contributing to the development. We had already considered several of the features proposed in this blue paper: application registry, hardware wallets, account recovery and asset proxy/hosting service. While the initial proposal of Wallet+ is to support web applications, we will be able to adopt the JavaScript/typescript packages for our application as well as we are using React Native for the mobile wallet. This will also give the added benefit of providing a mobile testing ground for the Wallet+ deliverables.

The mobile wallet will be fully open source (MIT or Apache 2.0 license) and provide a reference For other developers. This will be the first open-source self-sovereign identity EOSIO mobile client and the first identity solution using the EOSIO DID method. We make useability one of our highest priorities, ensuring that cryptography and blockchain are hidden from mainstream users as much as possible. We take a design first approach going through several rounds of increasing fidelity design prototypes and testing before starting development to ensure alignment with users and ecosystems.

Due to the limited funding from only being at level 1 ($10,000), this grant proposal only seeks funding to support the development of its first recovery mechanism - social recovery. Other work is not covered in this proposal. We will be self-funding as well as receiving external European Horizon 2027 and other funding for the release of the first beta edition of the wallet. In future ENF and Pomelo proposals we aim to extend the features of this application and after a proper production launch offered it as a software as a service model for public and private chains.

- **Name:** EOSIO cross-platform wallet
- **Brief Description:**  Build a new EOSIO cross-platform mobile client with advanced features such as recovery and SSI
- **Relationship to EOSIO:** Our application is built on top of the EOSIO blockchain framework. It will be compatible with any pure-EOSIO blockchain. We will use tools set out in the Wallet+ paper and support their development.
- **Reason for Interest:** We want to support the public EOS, Telos and WAX ecosystems. In the future, we plan to take this software and provide it in a software as a service model to industry and enterprise use cases.

### Project Details

- **Our process and values**

For technical development we value usability, security, privacy of personal information and sovereign control of your account. None of these should be compromised in an identity wallet.

Our process:
1. Brainstorm and concept development
2. User reasearch
3. Design hypersprint - a UX workshop where we discover flows and priorities
4. Mockups and testing - creating a low fidelity click-through design that we conduct in person testing with users
5. High-fidelity prototype - creating A high fidelity click-through design prototype that we conduct in pursing testing with users
6. Research of technologies and architecture
7. Development

Deployed per chain or app.

- **Mockups/designs of any UI components**
  - Figma prototype access available upon request. Please email jack@tonomy.foundation
  - See video here: TODO

- **Data models of the core functionality**

Application architecture

![Application architecture](https://drive.google.com/uc?export=view&id=1HepZr9w9BxJ0EpGp2CZLeA7QtTjd1Ps9)

We plan to use the EOSIO account model hierarchy for recoverability. This is an example of what an account might look like
![Account model example](https://drive.google.com/uc?export=view&id=1Jm7xwBnM6x4lRJRxOEMaSVAxEeIrwvY5)

This UML diagram shows several of the datatypes and structures stored in the mobile wallet

![UML of data stored in the mobile wallet](https://drive.google.com/uc?export=view&id=12jOcSy39lk4im-ODADsasiu7jl3fhcrm)

- **API specifications of the core functionality**

Draft public interfaces (typescript) for applications integrating with Tonomy ID:

[Identity](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/blob/master/src/integration/identity.type.ts) - Sign in and log out of your application with your Tonomy ID.

[Credentials](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/blob/master/src/integration/credentials.type.ts) - Create and share verifiable credentials and store credentials in your sovereign storage

[Transactions](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/blob/master/src/integration/transaction.type.ts) - Sign EOSIO transactions

[Communication](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/blob/master/src/integration/communication.type.ts) - Send a message to another EOSIO account

- **An overview of the technology stack to be used**

  - See Application architecture diagram above
  - Mobile client: React Native
  - Key storage: [react-native-keychain](https://www.npmjs.com/package/react-native-keychain) (which uses key enclaves on the mobile device if available)
  - Transport layer: QR codes and DIDComm
  - Data models: EOSIO signing request (ESR), verifiable credentials with [schema.org](https://schema.org) structures
  - Blockchain: EOSIO

- **Documentation of core components, protocols, architecture, etc. to be deployed**

This project is creating the following softwares

**[Tonomy ID](https://github.com/Tonomy-Foundation/Tonomy-ID)** - the cross-platform mobile wallet (Android and iOS) for public and private EOSIO blockchains

**[Tonomy ID SDK](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK)** -  the typscript library used in Tonomy ID to interact and call with the EOSIO blockchain and services. It is also used as the public API for integration by applications to do single sign-on, share credentials and sign transactions.

**Tonomy ID demo app** - a reactjs application showing demo flows applications can integrate with Tonomy ID To sign transactions, share credentials and consent and sign into their web2 or web3 application.

**Tonomy ID integration** - and integration repository used to run the above three applications in a developer environment for integration and automated testing.

- **PoC/MVP or other relevant prior work or research on the topic**

The following work was done by project lead Jack Tanner during his consulting and employment with [Gimly](https://www.gimly.io/). These experiences have led him to understand the identity landscape and create a design that will enable EOSIO chains to deliver one of the most advanced and empowering identity solution for web3:
- Architecting and developing the entire [Myd](https://europechain.io/identity/myd-missing-piece-puzzle-ssi/) sovereign (not self-sovereign) identity solution for Europechain. See [myd.online](https://myd.online/).
- Running the [EOSIO identity working group](https://www.gimly.io/eosio-identity) in which we researched and built the EOSIO DID in collaboration with the community and Block One.
- Writing the [EOSIO DID spec](https://github.com/Gimly-Blockchain/eosio-did-spec)
- Leading the development of the [EOSIO DID resolver](https://github.com/Gimly-Blockchain/eosio-did-resolver)
- Leading and writing the W3C standard [Verifiable Conditions](https://github.com/w3c-ccg/verifiable-conditions) to allow EOSIO and other DID methods to suitably expose multi-key material and delegated authorizations in DID Documents. This was then incorporated in the EOSIO DID.
- Researching recovery techniques, sovereign storage, locking protocols and more for the research deliverable for EU funded project [Gimly ID](https://www.gimly.io/gimly-id). This research survey existing technologies needed to build a fully self sovereign identity system.

Additionally, Jack has been in independently involved in several relevant prior works:
- Co-writing the [EOSIO Privacy report](https://eos.io/news/blockchain-privacy/) in collaboration with the EOSIO community and Block One. I led the research into existing privacy architectures, very relevant for understanding and leading architecture of SSI applications.
- Leading the development of the [Civic Participation Tool](https://theblockstalk.medium.com/civic-participation-tool-upgrade-to-openstad-e7aed01c5271#c5a3) in which our team created a direct democracy tool on EOSIO with an SSI identity integration.
- Organising and running many [EOSIO workshops](https://theblockstalk.medium.com/the-eosio-blockchain-developer-workshop-now-available-on-youtube-ddeba54f0d94) - in person and online - and writing education and pratcical EOSIO material on [Medium](https://theblockstalk.medium.com/), [Github](https://github.com/theblockstalk) and [Twitter](https://twitter.com/theblockstalk).
- Jack has been technically involved in blockchain since 2016 learning from Matthew Di Ferrente and Nick Johnson (core Ethereum Foundation developers) as a developer, auditor, educator and technical influencer. He has worked on many blockchain protocols and dApp architectures.

- **What your project is _not_ or will _not_ provide or implement**

Tonomy ID offers a range of features:
1. EOSIO blockchain tx signing
2. EOSIO blockchain multi-sig signing
3. Social recovery
4. Hardware recovery
5. Security question recovery
6. Non-custodial third party recovery ("guardians in Wallet+ paper)
7. Verifiable Credential sharing
8. Peer-to-peer EOSIO account communication network
9. SSO login to web2 and web3 applications
10. Sovereign data cloud storage (client-side encrypted using a recoverable key)

This grant proposal **only seeks funding for #3, social recovery feature**. Other features will be funded through a mixture of self funding, EU grants and additional ENF and Pomelo grants in combination with revenue from our SaaS offering to industry.

To be clear, we would prefer to receive more than $10,000 if possible to fund the development of this application.

### Ecosystem Fit

- **Where and how does your project fit into the ecosystem**

We are developing an identity solution that can be used on public and private EOSIO blockchains. Users of each EOSIO chain will then be able to sign transactions on dApps securely from their mobile wallets. We aim to offer this as a SaaS and/or DIY with support package to industry as well as host and run a identity app for EOS, Telos and WAX.

As previously mentioned, we see ourselves collaborating closely with the Wallet+ team to deliver an extended set of SDKs and services for wallets. We hope to provide a mobile testing ground for their software and likely assist in development ( probably through issue creation and PRs to fix bugs).

We are excited to be 1st to truly bring a generic self-sovereign identity (SSI) solution to EOSIO. Other solutions like [OmniOne](https://omnione.net/en/main) and [Infra Blockchain](https://infrablockchain.com/en/posts/vaccine-passport-bclabs-notice) Do not maintain full EOSIO compatibility. Our solution develops the required libraries as well as a reference identity application which can be used by others. This is of tremendous value to the EOSIO ecosystem as it brings a highly adopted set of technologies and community with it that can then be available to EOSIO dApps including:
  - credential sharing - Allow users to share their identity data privately with other users. This is a privacy-preserving alternative approach to the Wallet+ "profiles"
  - interoperability - All credential data standards across all did methods (Bitcoin, Ethereum, Polkadot, EOSIO, etc) are interoperable meaning that they can be validated even from another chain. This brings a level of interoperability between chains (between EOSIO chains and externally). With transnational companies like Microsoft and IBM and national government adoption of SSI this means EOSIO chains will be ready to use identities created by such institutions (even if not done using EOSIO).
  - sovereign data - The SSI architecture allows full control over data without any third party storing your data.
  - privacy and compliance - Ensuring identity data does not live on the block chain or any server significantly improves privacy andd ensurres that data compliance is built in.
  - scalability - Moving identity off the blotting and into web or mobile clients improve scalability of the block chain
  - communication - SSI tools like DIDComm allow a cross chain communication system to exist without having to trust third parties. This could be there in easy IBC solution for inter-dApp communication
If you are unfamiliar with SSI we would be happy to Point you to some articles or give a brief introduction to SSI.

- **Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**


chains for identity
EOS, telos, WAX
dapps for tx signing, SSO and other features
ourself

- **What need(s) does your project meet?**

useability
recoverability
privacy
security
sovereignty
scaleability


- **Are there any other projects similar to yours in the EOSIO ecosystem?**
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?

## Team

### Team members

- **Team Leader:** Jack Tanner
- Chris Veroef
- Mikhail Rusanov
- Carrie Ann Smith
- Jordan Fisher
- Mia Jacobson

### Legal Structure
- **Registered Legal Entity:** Tonomy Stichting
- **Registered Legal Country:** Netherlands
- **Registered Address:** Thorbecke Laan, Baarn, Utrecht 3741TR, Netherlands

### Team Experience

> Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past. For research-related grants, references to past publications and projects in a related domain are helpful. If you applied for a Pomelo grant in the past, please be sure you listed them in the section above and mention them in detail in this section.

> If anyone on your team has applied for a grant at the EOS Network Foundation previously, please list the name of the project and legal entity here.

Myd, EOSIO DID, EOSIO identity working group, gimly, Verifiable Conditions, W3C CCG, DIF
EOSIO training
ethereum
other from other teammates?

### Team Org Repos

- https://github.com/Tonomy-Foundation
- https://github.com/Tonomy-Foundation/civic-participation

TODO add Chris and Carrie?

### Team Member Repos

- https://github.com/theblockstalk
- https://github.com/theblockstalk/eosio-contracts
- https://github.com/theblockstalk/awesome-eosio (added several tools in some [PRs](https://github.com/DanailMinchev/awesome-eosio/pull/70))
- https://github.com/theblockstalk/eosworkshop1
- https://github.com/theblockstalk/eosio-sovereign-contract-poc
- https://github.com/theblockstalk/funnels
- https://github.com/kamitor
- https://github.com/carrie2240

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/jack-tanner/
- https://www.linkedin.com/in/christiaanverhoef/
- https://www.linkedin.com/in/rusanovmp/
- https://www.linkedin.com/in/carrie-ann-smith-95240899/
- https://www.linkedin.com/in/jordanelizabethfisher/
- https://www.linkedin.com/in/mia-jacobson-012218139/

## Development Status

> If you've already started implementing your project or it is part of a larger repository, please provide a link and a description of the code here. In any case, please provide some documentation on the research and other work you have conducted before applying. This could be:

- links to improvement proposals or [RFPs](https://github.com/eosnetworkfoundation/grant-framework/tree/main/docs/rfps) (requests for proposal),
- academic publications relevant to the problem,
- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to this project with anyone from the EOS Network Foundation,
- previous interface iterations, such as mock-ups and wireframes.

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

> :zap: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** Duration of the whole project (e.g. 2 months)
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project throughout its duration (see [Wikipedia](https://en.wikipedia.org/wiki/Full-time_equivalent), e.g. 2 FTE)
- **Total Costs:** Requested amount in USD for the whole project (e.g. 12,000 USD). Note that the acceptance criteria and additional benefits vary depending on the [level](../README.md#grant-levels) of funding requested. This and the costs for each milestone need to be provided in USD; if the grant is paid out in EOS, the amount will be calculated according to the exchange rate at the time of payment.

### Milestone 1 Example — Implement EOSIO Sub-module

- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our EOSIO nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)
| 1. | EOSIO Sub-module: X | We will create a EOSIO module that will... (Please list the functionality that will be implemented for the first milestone) |  
| 2. | EOSIO Sub-module: Y | We will create a EOSIO module that will... |  
| 3. | EOSIO Sub-module: Z | We will create a EOSIO module that will... |  
| 4. | EOSIO chain | Sub-modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |  


### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1
- **Costs:** 4,000 USD

...


## Future Plans

> Please include here

- how you intend to use, enhance, promote and support your project in the short term, and
- the team's long-term plans and intentions in relation to it.


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

> Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
