# EOS Network Foundation Grant Proposal

- **Project Name:** NFT Collection Manager Stage 2
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
- **Brief Description:** An interface to the AtomicAssets standard which makes it easy to manage your own Atomic NFT Collections, and plugins to ensure high quality releases and gamification integration.
- **Relationship to EOSIO:** FACINGS has been launching AtomicAssets NFTs  since its inception in early 2021. Its parent company and initial investor, Detroit Ledger Technologies (formerly EOS DETROIT), has been in the Antelope/EOSIO ecosystem since its inception as a pioneer block producer on EOS and other Antelope blockchains.
- **Reason for Interest:** Our team and experience combined with the need for an open-source creator that is friendlier to use makes for a perfect fit. The lack of development on EOS for NFTs and gamification resources makes it a necessity going forward.


### Project Details

**Mock-ups/designs of any UI components**

These designs are from past prototypes, to give an example, but does not represent the final product: 
https://drive.google.com/drive/folders/1iN2bQJhB_w_A_fKXC8-iYr3Re2-rbqSt

**Data models of the core functionality**

The data model will be largely based on the AtomicAssets [schema](https://github.com/pinknetworkx/atomicassets-contract/wiki/Tables).

**API specifications of the core functionality**

We seek to implement the entirety of the [AtomicAssets](https://github.com/pinknetworkx/atomicassets-contract/wiki/Actions) allowed actions in the NFT Collection Manager, bringing together the power of existing actions into the EOS framework for implementation with complex collections and gamification.


**An overview of the technology stack to be used**

The NFT Collection Manager is a client-side app built in NextJS and talks directly with public blockchain API nodes. Our goal is to minimize dependencies. Therefore we intend for all of the data to be stored on-chain, with IPFS being used to store all NFT images.


**Documentation of core components, protocols, architecture, etc. to be deployed**

- Jungle4 EOS testnet support
- Data handling/validation
- TypeScript implementation
- Plugin Architecture
  - Data standard & import functionality
  - Smart Airdrops


**PoC/MVP or other relevant prior work or research on the topic**

We have an internal proof of concept that was shared in our previous grant application. The creator is currently hosted at https://creator.facings.io. You can see the details of our previous grant here: https://github.com/eosnetworkfoundation/grant-framework/blob/main/applications/facings-nft-collection-manager.md


**What your project is _not_ or will _not_ provide or implement**

Stage 1 was designed to generate a proof of concept working feature set on which we are immediately following up with a Stage 2 grant proposal to maximize the use and effectiveness of the Collection Manager and add feature sets toward our goals of easy collection management and gamification. Our project will not include or promote NFT sales, token creation, token backing, or the staking of NFTs. No drops will be possible with Stage 2 of the project, aside from airdrops and basic transfers.


### Ecosystem Fit

**Where and how does your project fit into the ecosystem?**

The only NFT creator on EOS is AtomicHub, which is closed source and allows collection owners to publish NFTs. Our project will provide an open source solution for EOS that is easy to use. Another relevant project is NeftyBlocks; they have many advanced features but their UI is also closed-source and only available on WAX. Advancing NFTs, play & earn, and GameFi on EOS with an easy to use, functional collection manager fills a void in the EOS NFT ecosystem.


**Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**

Our target audience consists of game developers, creators, and members of the EOS community and other Antelope chains. We aim to encourage members of other chains to create on EOS in the future. By leveling the playing field on EOS with improved tooling, there is a compelling argument for game producers and collection enthusiasts to develop and launch on EOS.


**What need(s) does your project meet?**

The AtomicHub creator is a barebones UI integrating directly to a blockchain node, as well as their own internal IPFS node for file storage. It is available to everyone and anyone may publish without limits using their own resources. Nefty’s creator is much more complex with features like Pack Generation and Blending. However, neither of these platforms are open source.

We have created an open-source NFT collection manager which is both fully functional on its own, and represents a reference implementation of the AtomicAssets standard across the Antelope ecosystem as an open-source alternative to the other two choices. On top of the core functionality, we are excited to enable advanced workflows and gamification with a plugin system. By leveraging the existing Atomic standard, anyone is able to produce feature rich NFTs and manage them seamlessly, creating a launchpad for gamification that can be a boon to the EOS network. EOS has the opportunity to be a big player in the gaming market which is struggling to find operating chains that fulfill all of the utility of blockchain with decentralized NFT ownership. The market is ripe to take the next step and EOS is poised to be the platform of choice.


**Are there any other projects similar to yours in the EOSIO ecosystem?**

There are no viable open source projects meeting this need.


## Team

### Team members

- **Team Leader:** Rob Konsdorf (Robrigo), CEO
- Keir Kleinknecht (Banana), COO
- Roadscape, Software Engineer
- Felblob, Product Manager
- Marcelo Souza, UI Engineer
- Elton Ponglio, Product Designer
- Marcos Moreira, DevOps Engineer


### Legal Structure
- **Registered Legal Entity:** FACINGS, Inc.
- **Registered Address:** 1570 Woodward Ave. FL 3 Detroit, MI 48226

### Team Experience

The FACINGS team brings multidisciplinary experience to the table. It is led by Rob Konsdorf, a co-founder of Detroit Ledger Technologies and blockchain technologist, and Keir Kleinknecht, a multi-technology, seasoned traditional exec and GameFi NFT analyst. The team has experience shipping software together, having created a “white-glove” NFT collection launch product and process responsible for shipping over 700,000 WAX NFTs for early collection partners, and generating over $500,000 in gross sales. Our research and first hand experience shipping in the NFT space makes us uniquely qualified to build tools to make the lives of NFT collection owners easier.

Specific successes and experience from our team include the success of projects on Telos and WAX, including WAX Labs and the OIG Election portal, both led by Rob Konsdorf. Keir has run over 13 successful startup companies, been an executive Board member for 3 Public Companies and ran several VC firms with net assets over $300 MM. Roadscape our Sr Software Engineer developed interface products at Steemit Inc, including the site that would become hive.blog, as well as leading the project for a content scaling layer called Hivemind. Collectively our engineers bring a vast amount of experience to and from web3 and are poised to execute this project with efficiency.

Recently, we completed and delivered the first stage of this project as an ENF grant on time and on budget.


### Team Org Repos

- https://github.com/facings
- https://github.com/FACINGS/eospyo

### Team Member Repos

- https://github.com/robrigo
- https://drive.google.com/drive/folders/1OfEwjO_ho5QTB9dfrbjMk2IUPEZ6iq6m?usp=sharing
- https://github.com/roadscape
- https://github.com/felsin
- https://github.com/mr-souza
- https://github.com/pongilo
- https://github.com/mmoreirasantosdev


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/robertkonsdorf/
- https://www.linkedin.com/in/keirkleinknecht/
- https://www.linkedin.com/in/mr-souza/
- https://www.linkedin.com/in/marcos-moreira-51285b16/


## Development Status

We recently delivered Stage 1 of this project as an ENF grant and have been preparing for Stage 2 of development, having started  research and preliminary design of the plugin system, and developing numerous UX and usability improvements, as well as progress on TypeScript implementation.


## Development Roadmap


### Milestone Summary

- **Total Estimated Duration:** 4.5 months
- **Full-Time Equivalent (FTE):** 4 FTE
- **Total Costs:** 180,000 USD


### Milestone 1 — TypeScript, UX, and Plugins Core

- **Estimated duration:** 2 months
- **FTE:**  4
- **Costs:** 80,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | GPLv3 |
| 0b. | Documentation | We will provide an updated ‘Getting Started’ guide and deployment instructions. We will document how to add, configure, and build new plugins. We will add a comprehensive User Guide. |
| 0c. | Testing Guide | (1) Two methods of quickly verifying completion of typescript migration; (2) walkthrough to test each new UI feature; (3) a step-by-step guide for adding a plugin |
| 0d. | Docker | We will provide a Dockerfile that can be used to launch a UI instance and test all the functionality delivered with this milestone. |
| 1. | TypeScript Implementation | Converting all components to TypeScript to improve maintainability and reliability. This has been requested by the EOS community. |
| 2. | UX Improvements | (1) Jungle4 EOS testnet support<br />(2) Airdrop - allow minting to multiple accounts<br />(3) Transfers - filter NFTs by name or collection<br />(4) Upgrade navigation / breadcrumbs and small screen optimization<br />(5) IPFS updates - manual address entry, previews, validation, view originals<br />(6) Metadata handling - new social links for collection, better defaults for schema, allow blank immutable fields, improved input validations |
| 3. | Plugin Architecture | Design and implement a client-side plugin framework which allows for added functionality at the collection level in the UI. The plugin system itself adds no external dependencies while increasing modularity and flexibility of the app. It also allows maintainers to inject functionality (and API integrations) while retaining a common core to contribute back to. |



### Milestone 2 — Data Import Plugin

- **Estimated Duration:** 1.5 months
- **FTE:**  4
- **Costs:** 60,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | GPLv3 |
| 0b. | Documentation | We will document the portable data standard used by the import system and provide usage instructions. |
| 0c. | Testing Guide | A testing script with sample data files will be provided to demonstrate usage of the import plugin; one sample will demonstate how validation failures are treated; the other will demonstate the success case. The test can be performed locally or via our hosted instance. |
| 0d. | Docker | We will provide a Dockerfile that can be used to launch a UI instance and test all the functionality delivered with this milestone. |
| 1. | Import Function | - Development of an AtomicAssets CSV standard<br />- Ability to import a CSV to create a schema and templates and submit the transactions in batches<br />- Minimal data validation to help detect user errors |
| 2. | Advanced Validation | - Improved validation results/reporting<br />- Data validation heuristics upon import: (a) Uniqueness; (b) Completeness; (c) Datatype optimization |


### Milestone 3 — Airdrop Plugin

- **Estimated Duration:** 1 month
- **FTE:**  4
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | GPLv3 |
| 0b. | Documentation | We will provide an Airdrop guide with general usage instructions, as well as documentation of the Airdrop plugin itself. |
| 0c. | Testing Guide | A step-by-step script to demonstrate the airdrop functionality locally or via our hosted instance. |
| 0d. | Docker | We will provide a Dockerfile that can be used to launch a UI instance and test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an article describing the work we performed as part of the grant, introduce the plugin system, and highlight the new possibilities and sample plugins. |
| 1. | Airdrop Plugin Core | - Specify single & multiple recipients<br />- Specify drop assets by (a) minting a specific Template ID; or (b) transfer multiple Asset IDs<br />- Randomize recipients (i.e. mint numbers) using random.org<br />- Batch submits |
| 2. | Airdrop API Queries | Look-up Queries:<br />- everyone who has specific template<br />- everyone who doesn’t have specific templates within a collection<br />- everyone who has any item from a collection<br /><br />Unique Queries:<br />- option to send single or multiple assets to matched accounts |


## Future Plans

As indicated in the Development Status section, FACINGS set out to build a fully custodial NFT launchpad which serves as a bridge into web3 for brands, creators, and games looking to integrate NFTs into their product offerings. Our vision is to streamline access to tools for managing composable NFT use cases, and abstract away the complexity of tapping into them for entities that do not have a pre-existing knowledge of web3, or may not be technical in nature. In some cases with big firms, they may not have a policy for accounting for crypto even, making participation that requires holding and securing tokens difficult.

The NFT Collection Manager is a stepping stone towards realizing that vision, setting the foundational elements of our content management experience for publishers, and making them available for all to use and build upon.

Our goal is to create a platform that leverages EOS’s robustness and attracts gaming studios to a more simplistic and user friendly launch. We believe the integration of the creator UI with additional features down the road will be a very compelling choice, turning EOS into the premier gamification center, while maintaining excitement for other trends and collections. 

FACINGS envisions sustaining our business with a premium tier of features built on top of the open source core, with a usage-based business model (pay-as-you-publish). Premium features incorporated as plugins could include facilitation of sales, redeemable NFTs, composable crafting, and support for mint on demand and preminted packs.

The integration of the plugin system further opens up this project to growth and contributions which can be leveraged by any fork or maintainer. By allowing new functionality to be added as encapsulated plugins, it becomes safer and simpler to create and share new features without requiring modifications to the core, nor new forks or diverging codebases.

Future features that could also be valuable to prioritize work on includes integrating best-of-breed onboarding experiences, automatic collection microsite generation (configurable sales sites), enabling purchasers to pay for their own on-chain account with a credit card in the purchasing flow, and richer functionality to support the needs of NFT-integrated games including event triggers for mutable data.


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

Robrigo has been following the ENF since its inception and saw the blog announcement for the grants framework. After brainstorming with the team, we crafted our initial proposal for this project. This proposal represents a continuation of the development started in stage 1.
