# EOS Network Foundation Grant Proposal

- Project Name: bountyblok Distribution Tool - Extended Features
- Team Name: bountyblok
- EOS Payment Address: bountyblokio
- [Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels): 2

## Project Overview

This application is to support an existing proposal put forward on [Pomelo](https://pomelo.io/grants/bountyblok) to reach its funding.

bountyblok is built for NFT Artists, brands and various projects who want to engage their followers with a set of tasks while earning rewards. Also built for developers who want to add gaming mechanics inside their projects. 

### Overview

- **Name:** bountyblok Distribution Tool

- **Brief Description:** We are looking to expand our features and offer what we have right now on the WAX version and some of these features include:
  - Ability to query accounts who completed entire sets
  - Ability to query accounts via schema attributes 
  - Staking - a lot of projects stake their NFTs to earn rewards, for example "wombatmaster"
  - Floor Sweeping (ability to buy a large number of the cheapest listed assets)
  - Accounts by Instagram comments
  - and many more

  The costs below include on-going maintenance, and customer support for the next 12 months. We offer support via telegram and email 7 days a week.


- **Relationship to EOSIO:** We rely heavily on the EOSIO tech, from its chain APIs to the atomicassets smart contract.

- **Reason for Interest:** We have had a growing demand to provide some our successful tools that are currently on WAX onto EOS. Working closely with projects from Stephane, Seth, Byron to name a few, we clearly see the benefits it can have in launching our distribution tool onto EOS.

### Project Details

Our feature-rich distribution tool allows you to easily distribute thousands of NFTs to your followers in just a few clicks. Reward users who completed a typeform, engaged with a Tweet, are holding certain NFTs, completed entire sets, and more.

- Mockups/designs of any UI components:  We have a minimal version already on https://eos.drop.bountyblok.io but the final version is yet to be designed.

- An overview of the technology stack to be used
  - [EOSIO](https://eos.io) is a highly performant open-source blockchain platform, built to support and operate safe, compliant, and predictable digital infrastructures.
  - C#/.NET
  - PostgreSQL/MS SQL
  - Node.js/angular.io/vue.js


- Documentation of core components, protocols, architecture, etc. to be deployed
* We will provide an article / tutorial on how to use the tool.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?
  bountyblok fits into the category of Ecosystem Growth.
  
  
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
	Games, artists, brands and various projects looking to engage their community by rewarding them with NFTs/FTs

- What need(s) does your project meet?
  It is a free tool which allows projects on EOS to help them grow their community and user-base 

- Are there any other projects similar to yours in the EOSIO ecosystem?
  Not that I am aware
  
   
## Team

We are mostly a tech-strong group of guys based in Montreal, Canada
You can view our team on slide #3 https://bountyblok.io/deck.pdf

### Team members

* Dimitri Nikolaros: Software Developer/Team Lead, holds B.Eng from Concordia University in Computer Engineering.
* Jan Bui: Software Architect, holds a B.Comm from McGill University in Management Information System and Accountancy.
* Saddam Tahir: Software Developer, holds a Masters from Concordia University in Computer Science.
* Noman Mirza: Software Developer, holds a Masters from Concordia University in Computer Science .
* Jackie Chao: Software Developer, holds B.Eng from Concordia University in Software Engineering.
* Mike Barwick: UX/UI Designer

### Contact

* **Contact Name:** Dimitri Nikolaros
* **Contact Email:** dimitri.nikolaros@inlinefx.com
* **Website:** https://eos.drop.bountyblok.io

### Legal Structure

* **Registered Address:** 3770 rue Jean-Paul-Sartre Laval (Québec) H7P0E4 Canada
* **Registered Legal Entity:** inlineFX Software (9278-3521 Québec inc.)

### Team Experience

The bountyblok team carries a strong technical background in various areas of engineering from front end to backend development, EOSIO and various blockchain technologies. 

* Jan Bui:

  With over 2 decades' experience in technical leadership and a sound vision of the delicate balance between technology and business, Jan has positioned inlineFX at the forefront of the technology landscape. He has worked previously in Montreal, Zurich and London, working and managing high-level teams of front-office software developers at various banks and brokerages such as Credit Suisse, Morgan Stanley and BGC Partners.

* Dimitri Nikolaros:

  As Co-Founder and lead programmer, Dimitri focuses on delivering quality and functional software. He has developed websites that have processed millions of transactions and currently used by thousands of avid users. In addition, Dimitri focuses on client-relationship management and other strategic initiatives.

### Team Member Repos

* https://github.com/bountyblok 
* https://github.com/diminiko

### Team LinkedIn Profiles (if available)

* https://www.linkedin.com/in/dnikolaros/ Dimitri Nikolaros
* https://www.linkedin.com/in/jan-bui-4b62383/ Jan Bui

## Development Status

The distribution tool went live on EOS in Q4 2021: https://eos.drop.bountyblok.io. However, this version went live with a limited set of features as we required additional infrastructure at the time.

## Development Roadmap

### Overview

We are looking to expand our features and offer what we have right now on the WAX version and some of these features include:

* Ability to query accounts who completed entire sets
* Ability to query accounts via schema attributes 
* Staking - a lot of projects stake their NFTs to earn rewards, for example "wombatmaster"
* Floor Sweeping (ability to buy a large number of the cheapest listed assets)
* Accounts by Instagram comments
* and many more

The costs below include on-going maintenance, and customer support for the next 12 months. We offer support via telegram and email 7 days a week.


- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):**  4
- **Total Costs:** 100,000 USD

### Milestone 1 SETUP INFRA + BACKEND

- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 30,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 
| 0b. | Documentation | Not applicable here |
| 0c. | Testing Guide | Not applicable here |
| 0d. | Docker | Not applicable here |
| 0e. | Article | Not applicable here |
| 1. | EOS SHIP Setup | We will setup infrastructure and run our own EOS SHIP nodes |  
| 2. | Atomicassets DB | We will setup infrastructure in order to run our own Atomicassets DB and API | 
| 3. | New Backend | Deploy a new backend instance |   

### Milestone 2 UI Components

- **Estimated duration:** 1 month
- **FTE:**  4
- **Costs:** 70,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 
| 0b. | Documentation | Not applicable here |
| 0c. | Testing Guide | Not applicable here |
| 0d. | Docker | Not applicable here |
| 0e. | Article | We will provide an article which contains a tutorial on how to use the tool |
| 1. | SQL Bridge | Implement and deploy our SQL module to query the atomicassets SQL DB |  
| 2. | UI Features | Implementation of the various components and features on the UI |  
| 3. | Fresh Design | New Home Page that reflect the EOS projects and marketplace | 




## Future Plans

-  We will continue to work closely with the projects on EOS because of the constant feedback they provide (Stephane, Byron, Seth, etc)
-  We understand that this industry constantly changes and evolves and we strive to adapt to the changes as much as possible. That being said, we are genuinely excited about the EVM coming to EOS and plan to support this tech within our tools. We will have capabilities to handle ERC-1155 and help attract EVM based projects from other chains
-  We have a strong industry recognition across other chains and believe can attract new projects looking to expand across other chains, especially EVM-based


## Additional Information

**How did you hear about the Grants Program?** 

- From Zack at the ENF
