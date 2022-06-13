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

#### **Our process and values**

For technical development we value usability, security, privacy of personal information and sovereign control of your account. None of these should be compromised in an identity wallet.

Our process:
1. Brainstorm and concept development
2. User reasearch
3. Design hypersprint - a UX workshop where we discover flows and priorities
4. Mockups and testing - creating a low fidelity click-through design that we conduct in person testing with users
5. High-fidelity prototype - creating A high fidelity click-through design prototype that we conduct in pursing testing with users
6. Research of technologies and architecture
7. Development

#### **Mockups/designs of any UI components**
  - Figma prototype access available upon request. Please email jack@tonomy.foundation
  - See video here: TODO

#### **Data models of the core functionality**

Application architecture

![Application architecture](https://drive.google.com/uc?export=view&id=1HepZr9w9BxJ0EpGp2CZLeA7QtTjd1Ps9)

We plan to use the EOSIO account model hierarchy for recoverability. This is an example of what an account might look like
![Account model example](https://drive.google.com/uc?export=view&id=1Jm7xwBnM6x4lRJRxOEMaSVAxEeIrwvY5)

### **API specifications of the core functionality**

Draft public interfaces (typescript) for applications integrating with Tonomy ID:

[Identity](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/blob/master/src/integration/identity.type.ts) - Sign in and log out of your application with your Tonomy ID.

[Credentials](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/blob/master/src/integration/credentials.type.ts) - Create and share verifiable credentials and store credentials in your sovereign storage

[Transactions](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/blob/master/src/integration/transaction.type.ts) - Sign EOSIO transactions

[Communication](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/blob/master/src/integration/communication.type.ts) - Send a message to another EOSIO account

#### **An overview of the technology stack to be used**

  - See Application architecture diagram above
  - Mobile client: React Native
  - Key storage: [react-native-keychain](https://www.npmjs.com/package/react-native-keychain) (which uses key enclaves on the mobile device if available)
  - Transport layer: QR codes and DIDComm
  - Data models: EOSIO signing request (ESR), verifiable credentials with [schema.org](https://schema.org) structures
  - Blockchain: EOSIO

#### **Documentation of core components, protocols, architecture, etc. to be deployed**

This project is creating the following softwares

**[Tonomy ID](https://github.com/Tonomy-Foundation/Tonomy-ID)** - the cross-platform mobile wallet (Android and iOS) for public and private EOSIO blockchains

**[Tonomy ID SDK](https://github.com/Tonomy-Foundation/Tonomy-ID-SDK)** -  the typscript library used in Tonomy ID to interact and call with the EOSIO blockchain and services. It is also used as the public API for integration by applications to do single sign-on, share credentials and sign transactions.

**Tonomy ID demo app** - a reactjs application showing demo flows applications can integrate with Tonomy ID To sign transactions, share credentials and consent and sign into their web2 or web3 application.

**Tonomy ID integration** - and integration repository used to run the above three applications in a developer environment for integration and automated testing.

#### **PoC/MVP or other relevant prior work or research on the topic**

See our Team Experience below. Very specific for this proposl is
1. We have already built a self sovereign identity at on EOSIO - Myd
2. We have led and developed the core components needed for EOSIO SSI in the EOSIO identity working group and EOSIO DID work, this also shows our willingness to collaborate openly with the ecosystem
3. We have researched various technical building blocks and protocols relevant for making this product as part of the EU funded Gimly ID project
4. We have built a prototype direct democracy dApp on EOSIO leading us to further understand the requirements of web3 identity - the Civic Participation Tool
5. We have a deep and varied knowledge and commercial of both EOSIO and other blockchains and SSI technologies, tools and communities

#### **What your project is _not_ or will _not_ provide or implement**

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
10. Sybil protection
11. Sovereign data cloud storage (client-side encrypted using a recoverable key)

This grant proposal **only seeks funding for #3, social recovery feature**. Other features will be funded through a mixture of self funding, EU grants and additional ENF and Pomelo grants in combination with revenue from our SaaS offering to industry.

To be clear, we would prefer to receive more than $10,000 if possible to fund the development of this application.

Our goal is to ensure that we develop something that is suitable for each of the open EOSIO public blockchains. That involves collaboration with the EOS, Telos and WAX, Working with the Wallet+ SDK team (greymass) and of course with the EOS network foundation and the EOSIO coalition.

### Ecosystem Fit

#### **Where and how does your project fit into the ecosystem**

We are developing an identity solution that can be used on public and private EOSIO blockchains. Users of each EOSIO chain will then be able to sign transactions on dApps securely from their mobile wallets. We aim to offer this as a SaaS and/or DIY with support package to industry as well as host and run a identity app for EOS, Telos and WAX.

As previously mentioned, we see ourselves collaborating closely with the Wallet+ team to deliver an extended set of SDKs and services for wallets. We hope to provide a mobile testing ground for their software and likely assist in development ( probably through issue creation and PRs to fix bugs).

We are excited to be 1st to truly bring a generic self-sovereign identity (SSI) solution to EOSIO. Other solutions like [OmniOne](https://omnione.net/en/main) and [Infra Blockchain](https://infrablockchain.com/en/posts/vaccine-passport-bclabs-notice) Do not maintain full EOSIO compatibility. Our solution develops the required libraries as well as a reference identity application which can be used by others. This is of tremendous value to the EOSIO ecosystem as it brings a highly adopted set of technologies and community with it that can then be available to EOSIO dApps including:
- credential sharing - Allow users to share their identity data privately with other users. This is a privacy-preserving alternative approach to the Wallet+ "profiles"
- interoperability - All credential data standards across all did methods (Bitcoin, Ethereum, Polkadot, EOSIO, etc) are interoperable meaning that they can be validated even from another chain. This brings a level of interoperability between chains (between EOSIO chains and externally). With transnational companies like Microsoft and IBM and national government adoption of SSI this means EOSIO chains will be ready to use identities created by such institutions (even if not done using EOSIO).
- sovereign data - The SSI architecture allows full control over data without any third party storing your data.
- privacy and compliance - Ensuring identity data does not live on the block chain or any server significantly improves privacy andd ensurres that data compliance is built in.
- scalability - Moving identity off the blotting and into web or mobile clients improve scalability of the block chain
- communication - SSI tools like DIDComm allow a cross chain communication system to exist without having to trust third parties. This could be there in easy IBC solution for inter-dApp communication

If you are unfamiliar with SSI we would suggest [you start here](https://github.com/animo/awesome-self-sovereign-identity), or we can give a brief introduction to SSI.

#### **Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**

The Tonomy ID product will be targeted for EOSIO blockchains. As a revenue stream, we see ourselves mainly reaching out to industries or current industry EOSIO chains as a solution for them.

We also plan to host a solution on at least one of the major EOSIO public chains: EOS, Telos and WAX. We hope to get the support of the foundations/communities in launching these. We expect these to to be white labelled to some degree, e.g. EOS ID, Telos ID etc for their branding... The adoption on a chain basis depends on the support from their community. We also plan to support account creation and as this depends on each chain, will need to collaborate further with each ecosystem.

As part of our efforts to increase adoption and get feedback about software, We will additionally target dApps in EOS, Telos and WAX. For example, we are already talking with Hypha DAO on Telos about creating an identity solution for them on Telos. By talking to dApps we can discuss the specific features that they need for their application.

#### **What need(s) does your project meet?**

Our strategy prioritises usability without compromising security or privacy. We aim to create a user-friendly chain specific identity application in which users do not need to know or see aany cryptography or even watching information. This addresses a major usability issue in most EOSIO chain ecosystems.

Our additional features such as recoverability or credential sharing provide the means for dApps to decentralise their identity and onboarding process in a way that the whole ecosystem can trust.

With self sovereign identity, we ensure current dApps meet human privacy rights and important compliance regulations such as Europe's GDPR, California's CCPA and general KYC regulations. Just as important, SSI provides a large scalability improvement by moving data off the blockchain / IPFS and into the hands of the people can then share it peer-to-peer.

#### **Are there any other projects similar to yours in the EOSIO ecosystem?**
Contact us for a more detailed market analysis.
![Market analysis](https://drive.google.com/uc?export=view&id=1S_YVQp8MoK6Ornk2q_hmGaT-YnnteViA)

In addition to the above, we want to make the distinction between Tonomy ID and Anchor (the leading EOSIO wallet) clear:
  - we are building an application that can be deployed for each chain instead of a generic multi-EOSIO-chain specific wallet like Anchor. The reason we are doing this is to simplify the design and flows for users and create a better user experience.
  - both Tonomy ID and Anchor have a EOSIO transaction signer
  - Tonomy ID has built in SSI support, allowing for personal information ( who you are, health and more) to be privately stored and shared with consenting parties. This is a different approach to Anchor which has proposed "profiles" as a feature in Wallet+ which puts this information on the blockchain.
  - Tonomy ID has several built in recovery mechanisms that do not rely on any third parties. Anchor has as planned a semi-custodial recovery technique with "guardians"
  - Tonomy ID is planning to build a variety of plug-in sybil attack prevention modules
  - Tonomy ID Allows single sign-on (SSO) login to applications, like Anchor. Where Tonomy ID this is is that it can authorise a public key on the block chain which can then be used by the sign in application without needing to go back to Tonomy ID for every transaction that needs to be signed. This is an optional feature, if applications want everything signed by the active key a will need to use Tonomy ID to sign this. This allows applications to decide the usability/security balance for their applications needs.

## Team

### Team members

- **Team Leader:** Jack Tanner
- Chris Veroef
- Mikhail Rusanov
- Carrie Ann Smith
- Jordan Fisher
- Mia Jacobson
- Suneet Bendre
- Rebal Alhaqash

### Legal Structure
- **Registered Legal Entity:** Tonomy Stichting
- **Registered Legal Country:** Netherlands
- **Registered Address:** Thorbecke Laan, Baarn, Utrecht 3741TR, Netherlands

### Team Experience

The following work was done by project lead Jack Tanner during his consulting and employment with [Gimly](https://www.gimly.io/). These experiences have led him to understand the identity landscape and create a design that will enable EOSIO chains to deliver one of the most advanced and empowering identity solution for web3:
- Architecting and developing the entire [Myd](https://europechain.io/identity/myd-missing-piece-puzzle-ssi/) sovereign (not self-sovereign) identity solution for Europechain. See [myd.online](https://myd.online/).
- Running the [EOSIO identity working group](https://www.gimly.io/eosio-identity) in which we researched and built the EOSIO DID in collaboration with the community and Block One.
- Writing the [EOSIO DID spec](https://github.com/Gimly-Blockchain/eosio-did-spec)
- Leading the development of the [EOSIO DID resolver](https://github.com/Gimly-Blockchain/eosio-did-resolver)
- Leading and writing the W3C standard [Verifiable Conditions](https://github.com/w3c-ccg/verifiable-conditions) to allow EOSIO and other DID methods to suitably expose multi-key material and delegated authorizations in DID Documents. This was then incorporated in the EOSIO DID.
- Researching recovery techniques, sovereign storage, locking protocols and more for the research deliverable for EU funded project [Gimly ID](https://www.gimly.io/gimly-id). This research survey existing technologies needed to build a fully self sovereign identity system.

Additionally, Jack has been in independently involved in several relevant prior works:
- Co-writing the [EOSIO Privacy report](https://eos.io/news/blockchain-privacy/) in collaboration with the Suneet and the EOSIO community and Block One. I led the research into existing privacy architectures, very relevant for understanding and leading architecture of SSI applications.
- Leading the development of the [Civic Participation Tool](https://theblockstalk.medium.com/civic-participation-tool-upgrade-to-openstad-e7aed01c5271#c5a3) in which our team created a direct democracy tool on EOSIO with an SSI identity integration.
- Organising and running many [EOSIO workshops](https://theblockstalk.medium.com/the-eosio-blockchain-developer-workshop-now-available-on-youtube-ddeba54f0d94) - in person and online - and writing education and pratcical EOSIO material on [Medium](https://theblockstalk.medium.com/), [Github](https://github.com/theblockstalk) and [Twitter](https://twitter.com/theblockstalk).
- Jack has been technically involved in blockchain since 2016 learning from Matthew Di Ferrente and Nick Johnson (core Ethereum Foundation developers) as a developer, auditor, educator and technical influencer. He has worked on many blockchain protocols and dApp architectures.

TODO add something about Suneet

### Team Org Repos

- https://github.com/Tonomy-Foundation
- https://github.com/Tonomy-Foundation/civic-participation

### Team Member Repos

- https://github.com/theblockstalk
- https://github.com/theblockstalk/eosio-contracts
- https://github.com/theblockstalk/awesome-eosio (added several tools in some [PRs](https://github.com/DanailMinchev/awesome-eosio/pull/70))
- https://github.com/theblockstalk/eosworkshop1
- https://github.com/theblockstalk/eosio-sovereign-contract-poc
- https://github.com/theblockstalk/funnels
- https://github.com/kamitor
- https://github.com/carrie2240
- https://github.com/bendre
- https://github.com/Rebal67

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/jack-tanner/
- https://www.linkedin.com/in/christiaanverhoef/
- https://www.linkedin.com/in/rusanovmp/
- https://www.linkedin.com/in/carrie-ann-smith-95240899/
- https://www.linkedin.com/in/jordanelizabethfisher/
- https://www.linkedin.com/in/mia-jacobson-012218139/
- https://www.linkedin.com/in/suneet-bendre/
- https://www.linkedin.com/in/rebal-alhaqash-683b0b174/

## Development Status

We have currently finished a clickable prototype.

We are currently in the process of creating the final design. We have begun setting up some of the repositories needed.

As mentioned previously, Jack Tanner has conducted a large amount of research into protocols and Technical components needed to create this application during his contracting and employment with Gimly. He has also been involved with the EOSIO community since the EOS public block chain launch. An example of this is the publishing of the Data Privacy Research report. See **Team Experience** for more information.

## Development Roadmap

This section purely describes the development roadmap for Tonomy ID that is relevant for this grant proposal - the feature of social recovery.

Please reach out was and we can set up a time to discuss the rest of the roadmap if needed.

For each milestone,

- make sure to include a specification of your software. _Treat it as a contract_; the level of detail must be enough to later verify that the software meets the specification.
- include the amount of funding requested _per milestone_.
- include documentation (tutorials, API specifications, architecture diagrams, whatever is appropriate) in each milestone. This ensures that the code can be widely used by the community.
- provide a test suite, comprising unit and integration tests, along with a guide on how to set up and run them.
- commit to providing Dockerfiles for the delivery of your project.
- indicate milestone duration as well as number of full-time employees working on each milestone.
- **Deliverables 0a-0c are mandatory for all milestones**, and deliverable 0e at least for the last one. If you do not intend to deliver one of these, please state a reason in its specification (e.g. Milestone X is research oriented and as such there is no code to test).

### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):**  50 hours work from 1 FTE developer (Jack, Rebal and Suneet)
- **Total Costs:** $10,000

### Milestone 1 — Implement of social recovery

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code |
| 1. | Social Recovery - React Native | We will build the reacts native screens needed to setup social recovery and then recover the users account. This will be in our Tonomy ID repository |  
| 2. | Social Recovery - SDK | We will build the reacts native screens needed to setup social recovery and then recover the users account. This will be in our Tonomy ID SDK repository |  


### Milestone 2 — Testing and demo (part of generic Tonomy ID testing)

- **Estimated Duration:** 1 month
- **FTE:**  1
- **Costs:** 2,000 USD
- 
| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | UAT | Items relevant to social recovery will be checked in the user acceptance test (UAT) which was created at the end of our design phase. |
| 2. | Linting | Items relevant to social recovery will be checked in the user acceptance test (UAT) which was created at the end of our design phase. |
| 3. | Demo | We will provide a video showing a person using the social Recovery feature of Tonomy ID. |
| 4. | Article | We will publish an article that explains what we have achieved. |

At a later stage, when the Tonomy ID MVP is completed ( including social recovery) we will deploy this to a public EOSIO chain and broadcast this to current users so that they may start adopting. This production launch and marketing is not covered as part of this grant proposal.

## Future Plans

Tonomy ID is part of a application suit designed to fit the needs of "ecosystems of trust. This will be an integrated environment with the following applications
- Tonomy ID (Identity)
- Tonomy Gov (Governance portal for the ecosystem)
- Tonomy Money (A token factory)
- Tonomy Organizations (A DAO factory)

## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Medium and Twitter I think
