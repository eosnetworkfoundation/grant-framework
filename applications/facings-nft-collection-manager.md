# EOS Network Foundation Grant Proposal

- **Project Name:** NFT Collection Manager Stage 1
- **Team Name:** FACINGS, Inc.
- **EOS Payment Address:** facings
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** https://pomelo.io/grants/eospyo
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/FACINGS/collection-manager


## Contact

- **Contact Name:** Rob Konsdorf
- **Contact Email:** rob@facings.io
- **Website:** https://facings.io


## Project Overview

Our goal with the NFT Collection Manager is to create a publishing platform that leverages EOS’s robustness and attracts gaming studios to a more simplistic and user friendly launchpad. We believe the integration of the Collection Manager with additional features down the road will be a very compelling choice, supporting EOS in its endeavor to become a premier gaming blockchain, while maintaining excitement for other trends and collections. 

### Overview

- **Name:** NFT Collection Manager
- **Brief Description:** An interface to the AtomicAssets standard which makes it easy to manage your own Atomic NFT Collections, with draft mode and collaboration features to ensure high quality releases and gamification integration.
- **Relationship to EOSIO:** FACINGS has been launching AtomicAssets NFTs  since its inception in early 2021. Its parent company and initial investor, Detroit Ledger Technologies (formerly EOS DETROIT), has been in the EOSIO ecosystem since its inception as a pioneer block producer on EOS and other EOSIO blockchains.
- **Reason for Interest:** Our team and experience combined with the need for an open-source creator that is friendlier to use makes for a perfect fit. The lack of development on EOS for NFTs and gamification resources makes it a necessity going forward.


### Project Details

**Mock-ups/designs of any UI components**

These designs are from past prototypes, to give an example, but does not represent the final product: 
https://drive.google.com/drive/folders/1iN2bQJhB_w_A_fKXC8-iYr3Re2-rbqSt

**Data models of the core functionality**

The data model will be largely based on the AtomicAssets [schema](https://github.com/pinknetworkx/atomicassets-contract/wiki/Tables).

**API specifications of the core functionality**

We seek to implement a large portion of the [AtomicAssets](https://github.com/pinknetworkx/atomicassets-contract/wiki/Actions) allowed actions in the NFT Collection Manager UI bringing together the power of existing actions into the EOS framework for implementation with complex collections and gamification.


**An overview of the technology stack to be used**

The NFT Collection Manager will use React/JS. Our goal is to minimize dependencies. Therefore we intend for all of the data to be stored on-chain. In the future, IPFS will be used to store all NFT images and a testnet is used to stage draft collections.

The NFT Collection Manager will be a client-side app built in React and talking directly with public blockchain API nodes.


**Documentation of core components, protocols, architecture, etc. to be deployed**

- Base Implementation (MVP/Core functionality)
  - Home page: featured collections and an “about” section
- Login functionality. When logged in, show:
  - Logged in user’s account name and profile photo
  - Option to log out
  - RAM/Resource usage
- Account page: list user’s collections
- Basic collection viewer (Collection, Schemas, Templates, Assets)
- Basic collection manager
  - Create/Edit Collections
  - Create/Extend Schemas
  - Create Templates
  - Create Assets
  - Lock template
  - Burn asset
- Basic Collection explorer
  - Discovery features (trending or featured collections)
  - UI polish of collection viewer
- Airdrops: basic airdrop functionality


**PoC/MVP or other relevant prior work or research on the topic**

We have an internal POC that can be shared with EOS.


**What your project is _not_ or will _not_ provide or implement**

Stage 1 is designed to generate a proof of concept working featureset on which we plan to immediately follow up with a Stage 2 grant proposal to maximize the use and effectiveness of the Collection Manager and add feature sets toward our goals of collection management and gamification. Our project will not include or promote NFT sales, token creation, token backing, or the staking of NFTs. No drops will be possible with stage 1 of the project, aside from airdrops.


### Ecosystem Fit

**Where and how does your project fit into the ecosystem?**

The only NFT creator of EOS is AtomicHub, which allows collection owners to publish NFTs. Our project will provide an open source solution for EOS that is easy to use. The one other important project is NeftyBlocks; they have many advanced features but their UI is also closed-source and only available on WAX. Advancing play & earn and GameFi on EOS with an easy to use, functional collection manager captures a large void that EOS cannot afford to ignore.


**Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**

Our target audience consists of game developers, members of the current EOS and derivative chains. We also hope to encourage members of other chains to create on EOS in the future. By leveling the playing field for EOS with improved tooling, there is a compelling argument for game producers and collection enthusiasts to develop and launch on EOS.


**What need(s) does your project meet?**

The AtomicHub creator is a barebones UI integrating directly to a blockchain node, as well as their own internal IPFS node for file storage. It is available to everyone and anyone may publish without limits using their own resources. Nefty’s creator is much more complex with features like Pack Generation and Blending. However, many of their features are gated behind a staking mechanism.

We would like to create an open-source NFT collection manager which would be both fully functional on its own, and would represent the “reference implementation” for the AtomicAssets standard across the EOS family and be an open-source alternative to the other two choices. On top of the core functionality, we are excited to enable collaborative workflows and also to add the ability to work on drafts and review your entire collection before publishing it. Game publishers have a need to stage launches and manage NFTs to correlate with their actual release and for testing. This is not currently feasible on EOS in an efficient manner. By leveraging the existing Atomic standard, we are able to produce feature rich NFTs and manage them seamlessly, creating a launchpad for gamification that has yet to be seen on any EOS chain. EOS has the opportunity to be a big player in the gaming market which is struggling to find operating chains that fulfill all of the utility of blockchain with decentralized NFT ownership. The market is ripe to take the next step and EOS is poised to be the platform.


**Are there any other projects similar to yours in the EOSIO ecosystem?**

There are no viable open source projects meeting this need.


## Team

### Team members

- **Team Leader:** Rob Konsdorf (Robrigo), CEO
- Keir Kleinknecht (Banana), CTO
- Roadscape, Software Engineer
- Felblob, Product Manager
- Marcelo Souza, UI Engineer
- Alex Klein, Support Engineer
- James Alonso, Product Designer
- Marcos, DevOps Engineer


### Legal Structure
- **Registered Legal Entity:** FACINGS, Inc.
- **Registered Address:** 1570 Woodward Ave. FL 3 Detroit, MI 48226

### Team Experience

The FACINGS team brings multidisciplinary experience to the table. It is led by Rob Konsdorf, a co-founder of EOS DETROIT and blockchain technologist, and Keir Kleinknecht, a multi-technology, seasoned traditional exec and GameFi NFT analyst. The team has experience shipping software together, having created a “white-glove” NFT collection launch product and process responsible for shipping over 700,000 WAX NFTs for early collection partners, and generating over $500,000 in gross sales. Our research and first hand experience shipping in the NFT space makes us uniquely qualified to build tools to make the lives of NFT collection owners easier.

Specific successes and experience from our team include the success of projects on Telos and WAX, including WAX Labs and the OIG Election portal, both led by Rob Konsdorf. Keir has run over 13 successful startup companies, been an executive Board member for 3 Public Companies and ran several VC firms with net assets over $300 MM. Roadscape our Sr Software Engineer developed interface products at Steemit Inc, including the site that would become hive.blog, as well as leading the project for a content scaling layer called Hivemind. Collectively our engineers bring a vast amount of experience to and from Blockchain and are poised to execute this project with efficiency.


### Team Org Repos

- https://github.com/facings
- https://github.com/FACINGS/eospyo

### Team Member Repos

- https://github.com/robrigo
- https://drive.google.com/drive/folders/1OfEwjO_ho5QTB9dfrbjMk2IUPEZ6iq6m?usp=sharing
- https://github.com/roadscape
- https://github.com/felsin
- https://github.com/mr-souza
- https://github.com/mewmix
- https://heyjames.design/
- https://github.com/mmoreirasantosdev


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/robertkonsdorf/
- https://www.linkedin.com/in/keirkleinknecht/
- https://www.linkedin.com/in/mr-souza/
- https://www.linkedin.com/in/marcos-moreira-51285b16/


## Development Status

Some initial interface designs are included in the project details above. Beyond that work, our team has spent considerable time researching the landscape and spec’ing components related to building a fully custodial NFT launchpad on top of the AtomicAssets standard, so we understand the problem domain well. The NFT Collection Manager is a self-custody and simpler version of the product we originally set out to build. Our interest in building this is to fill the void we see in robust collection management solutions, to provide a well-scoped utility for the EOS ecosystem to start benefiting from, and to ship an MVP that we can start getting feedback and traction with in the short term.


## Development Roadmap


### Milestone Summary

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):** 4 FTE
- **Total Costs:** 80,000 USD


### Milestone 1 — Account Login & View Collections

- **Estimated duration:** 1 month
- **FTE:**  4
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | GPLv3 |
| 0b. | Documentation | We will provide a ‘Getting Started’ guide, deployment instructions, as well as inline documentation of the code. |
| 0c. | Testing Guide | Documentation for a walkthrough of the UI as described and the intended outcome of each subset will be provided along with expected feedback results. FACINGS UI standards including visibility of system status, user control and freedom, consistency, error prevention, recognition over recall, flexibility and efficiency, minimalistic design, error recovery and documentation will all be implemented. |
| 0d. | Docker | We will provide a Dockerfile that can be used to launch a UI instance and test all the functionality delivered with this milestone. |
| 1. | Base Implementation | Home page: show featured collections, “about” section, and login link. |
| 2. | Login & Account | When logged in, show: (a) logged in user’s account name and profile photo, (b) Option to log out, (c) RAM/Resource usage, and (d) list of user's collections. |
| 3. | Collection viewer | Ability to explore/examine Collections, Schemas, Templates, Assets. |  



### Milestone 2 — Create/Edit Collections

- **Estimated Duration:** 1 month
- **FTE:**  4
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | GPLv3 |
| 0b. | Documentation | We will provide a ‘Getting Started’ guide, deployment instructions, as well as inline documentation of the code. |
| 0c. | Testing Guide | Documentation for a walkthrough of the UI as described and the intended outcome of each subset will be provided along with expected feedback results. FACINGS UI standards including visibility of system status, user control and freedom, consistency, error prevention, recognition over recall, flexibility and efficiency, minimalistic design, error recovery and documentation will all be implemented. |
| 0d. | Docker | We will provide a Dockerfile that can be used to launch a UI instance and test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an article describing the work we performed as part of the grant, introduce our app, and highlight the features which make it valuable. |
| 1. | Collection Manager | Handle fundamental operations: (1) Create/Edit Collections, (2) Create/Extend Schemas, (3) Create Templates, (4) Create Assets, (5) Airdrop assets to list of accounts |  
| 2. | Additional functions | Lock template, burn asset |  
| 3. | Deployment | We will host the UI and it will be privately available for alpha testing. |  



## Future Plans

As indicated in the Development Status section, FACINGS set out to build a fully custodial NFT launchpad which serves as a bridge into web3 for brands, creators, and games looking to integrate NFTs into their product offerings. Our vision is to streamline access to tools for managing composable NFT use cases, and abstract away the complexity of tapping into them for entities that do not have a pre-existing knowledge of web3, or may not be technical in nature. In some cases with big firms, they may not have a policy for accounting for crypto even, making participation that requires holding and securing tokens difficult.

The NFT Collection Manager is a stepping stone towards realizing that vision, setting the foundational elements of our content management experience for publishers, and making them available for all to use and build upon.

In the short term, we will work with NFT projects specific to EOS in order to create a feedback loop from real users. We will also leverage surveys to gather feedback anonymously and from other types of users as well. We will use this feedback to prioritize maintenance and improvements on the core.

Our goal is to create a platform that leverages EOS’s robustness and attracts gaming studios to a more simplistic and user friendly launch. We believe the integration of the Collection Manager with additional features down the road will be a very compelling choice, turning EOS into the premier gamification center, while maintaining excitement for other trends and collections. 

We envision sustaining our business with a premium tier of features built on top of the open source core, with a usage-based business model (pay-as-you-publish). Some of these premium features include facilitation of sales, redeemable NFTs, composable crafting, and support for packs. We have also envisioned a multi-level open source model where we create customer acquisition through open source channels and convert add ons for profit as a continuously evolving and growing market. Both market strategies are sustainable and FACINGS is poised to operate opportunistically and nimbly.

Future avenues that may also be critical to prioritize work on includes integrating best-of-breed onboarding experiences, automatic collection microsite generation (configurable sales sites), enabling purchasers to pay for their own on-chain account with a credit card in the purchasing flow, and richer functionality to support the needs of NFT-integrated games.


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

Robrigo has been following the ENF since its inception and saw the blog announcement for the grants framework. After brainstorming with the team, we crafted this proposal.
