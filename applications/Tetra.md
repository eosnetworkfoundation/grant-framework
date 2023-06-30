# EOS Network Foundation Grant Proposal

- **Project Name:** Tetra
- **Team Name:** Tetra Team
- **EOS Payment Address:** godsolislove
- **Level:** 1
- **Pomelo Grant(s):** [killerapp](https://pomelo.io/grants/killerapp)
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/tetragrids

## Contact

- **Contact Name:** Douglas James Butner
- **Contact Email:** dougbutner@gmail.com
- **Website:** https://tetra.earth



## Project Overview

Tetra brings you humanity's "creme of the crop" daily in an abundant economic system using geopolitical maps and Gregorian timeframes to churn content, projects, and people in a way that brings people together in a mutual-benefit system. 

Tetra operates as an economic layer on top of existing web 2 and web 3 content, including the Atomic Assets NFT standard, with the benefit of additional financial mechanisms, including tokenized exposure, infinite-cycle project funding, zero-interest microloans that replay themselves over time, and IRL templates local leaders can follow to organize events.  

This grant is to start to build the underlying tech, and we will apply to continue for a level 2 and level 3 grant to continue to make this a reality on Antelope.

Components
- Map + Chart based UI mapping content by location created
- UI: Users arrange lists of 1) Social 2) Commercial and 3) Personal projects they want to support in their **local area**.
- Backend: Stores table of user's chosen projects in the three categories

**Tetra Distributes a token (liquid for attention) to the projects on citizens' lists**

- Projects can use the token to accrue and advertise themselves at key moments, or as financial fuel.
- Anyone can organize a project, share a personal project like art
- Personal projects can be for one's self
- Tetra rewards voters for actively voting + participating with projects
- As rewards are distributed, an equal amount of exposure is given to that content. The rewards collected can be spent for an equal amount of exposure at any time in the future.
- Content is only discoverable if it has received an upvote during the time period a user is viewing, and was created where a user is viewing on the geopolitical map. 
    - This mechanism gives power to new and relevant content. 
    - Creators are incentivized to stimulate the abundant economy with token-voted from votes on their contact 

 
Tetra does this by creating scarcity in attention when displaying the top content. 

**The Bottom Line**
Tetra's grid system increases the value people receive from online advertising because they can "spike" global reach for a short time, and also get paid directly from the system if their advertising changes positive opinion in their direction.   


### Scope of Grant

We hope to build this alongside the ENF over the coming months, and will be applying for additional grants as we go. 

The scope of this grant is to create: 

**XMS:  Extensible Metadata Standard**

- Takes the work out of parsing of memos within contract actions.

All Antelope developers will be able to use the standard to declare custom memos that allow them to receive new information from their supporters and create Blockchain enabled businesses with higher functionality without the technical knowledge.

Future projects will benefit by being able to implement contracts with higher functionality, better usability, at a lesser technical debt.


**Tokenized on-chain Referral System**

- Creates time-limited invitation structure where assets are used to track and award those who act honestly and bring new users on in a high-context way.
- End result is a list of consenting accounts that can rev\
- This may seem strange, but it's a mergance of social convention and technology that's needed to onboard the next wave of Antelope users

### Organization Overview

Douglas James Butner is founder and CTO
Alejandro Lozada is the co-founder

Tetra 

### Overview

- **Name:** Tetra
- **Brief Description:** 

- **Relationship to EOS Network / Antelope:** Team lead is also the lead of cXc.world, a project on WAX blockchain, and wants to continue on the technology. Douglas is a member of EOSIO community since 2020, and Eden member #100. Tetra requires a robust chain without fees to be successful for all members. It only makes sense for us to be on Antelope.

- **Reason for Interest:** I'm grateful to the ENF for providing what I see as the best blockchain tech out there, and want to contribute to that stack. I believe has a disproportionately small share of impact compared with other blockchains. I want to build the apps that create that impact to benefit the lives of all. I can only do that on-chain with this tech stack to the best of my knowledge. I'm also tired of trying to earn a living as a teacher distracting me from coding, so I'd like to join up and walk together with the ENF and community in this way.


### Project Details


- Mock-ups/designs of any UI components

These are from cXc Beta's User Interface. 

You can look at the latest trends (Monthly, Weekly, Daily, etc) or look into the past.* *Default is all-time.*
<p align="center"><a href="https://music.cxc.world" target="_blank" alt="Experience cXc Music">
  <img width="100%" height="auto" src="https://github.com/currentxchange/purple-explainer/blob/master/Images/Temporal-Selected.png"></a>
</p>

You can see trends for any nation. *Default is Global.*
<p align="center"><a href="https://music.cxc.world" target="_blank" alt="Experience cXc Music">
  <img width="100%" height="auto" src="https://github.com/currentxchange/purple-explainer/blob/master/Images/Geo-France.png"></a>
</p>



UI will be loosely based on the concepts of [Mapps](https://docs.google.com/document/d/1YppJ2EYumRI2j0UHYdZh7NJMObMI_NfHgaFRLbjgBtw/preview) and Team Lead's previous UIs including cXc.world



- Data models of the core functionality

[Web4 Metadata Standard](https://github.com/dougbutner/Geotemporal-NFT-Standard)

This standard works with Atomic Assets and is generally extended throughout the system to serve as a route for the creation as well as to enable and explicitly declare what actions are available for any piece of data or person within the system.

Further data structures include collections of arrays which indicate which projects as well as what percentage of the users funding should be directed to those projects.

From their tables of records will be created, similar to what we did in [ups.cpp](https://github.com/dougbutner/beta-pseudo/blob/main/real-contracts/ups.hpp)

- API specifications of the core functionality
We don't have a public API yet. In the future this will be uses to allow users to set their lists of the projects and people they support, and claim their rewards. 

- An overview of the technology stack to be used

C++ smart contracts for EOSIO / Antelope using official CLI and using the eosio.token standard, as well as extensions of that standard. 

Creation currencies will be stored just like any other eosio.token contract, in a table, and we will use tables for all forms of voting in rewards. 

Outside of the grant's scope, the app UI uses Leaflet.js, waxjs, and node.js.

- Documentation of core components, protocols, architecture, etc. to be deployed

Current documention is in-code. 

[Tetra / Web4 NFT Documentations](https://github.com/dougbutner/Geotemporal-NFT-Standard)


- PoC/MVP or other relevant prior work or research on the topic

cXc.world's [unreleased geotemporal functionality](https://youtu.be/coNc4iJB7OM?t=138)




- What your project is _not_ or will _not_ provide or implement

Our project is not intended to implement any sort of image hosting, music hosting, or any type of media hosting. 

In the scope of the grant, we focus on C++ and Javascript, and only promise helper functions in the context of building a Javascript application interacting with eosjs, or developing a smart contract to deploy on the antelope network.








### Ecosystem Fit

- Where and how does your project fit into the ecosystem? 

Tetra is the killer app Antelope has been waiting for, with a use case of cultivating culture through mutual benefit relationships in and sets up cycles that integrate with peoples lives, meaning the revisit the app and use it often. We benefit from the efficiency and speed of Antelope. 

Our benefit to the ecosystem is that we empower NFT creators using Atomic Assets, developers by making it easier for them to empower the memo to get new information into and between contracts in a ways that others can expect and understand.   

- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?

The problem that we solve is one of attention distribution, curation. Our project target audience is all those who wish to take part as well as benefit in such a system. The audience for our deliverables in the scope of this grant are developers Looking to integrate either easier user experience into their contracts, or who wish to virally grow their app using our system, as well as the same people who will participate in the referral system.

- What need(s) does your project meet?

Our project meets an ideological need for systems of creation that are both transparent and geared towards fostering relationships in the long term. 

In the scope of this grant, our project meets the needs of developers to easily be able to digest information sent in a memo, so they can receive tokens and instructions at the same time, with minimal development 


- Are there any other projects similar to yours in the EOS Network / Antelope ecosystem?

The project management aspect has a small overlap with Hypha's rolling seasonal system. 

cXc.world's [unreleased geotemporal functionality](https://youtu.be/coNc4iJB7OM?t=138) is similar to Tetra's.

  - If so, how is your project different?

Tetra is not a DAO-like system like Hypha, but a curation system that has an effect of project funding. Our seasons allow for reporting of projects' progress. 

Tetra is different from cXc in the nature of content and curation. Tetra allows listing of Commercial and Social projects, not available on cXc.world.

  - If not, are there similar projects in related ecosystems?
  N/A


## Team

### Team members

- **Team Leader:** Douglas James Butner


### Legal Structure
- **Registered Legal Entity:** Douglas James Butner
- **Registered Address:** 489 Collier Rd, Accident, MD 21520

Tetra is currently legally considered an unincorporated non-profit. Douglas James Butner is the current responsible party. 

### Team Experience

Team Lead
- Douglas has 15 years as a webmaster + full-stack developer, starting with building a social networking website and deploying it at age 16 (2008)
- Built + maintained over a dozen Wordpress and Drupal sites 
- I built and launched WAX dapp cXc.world in 3 months in 2018 using jQuery, leaflet.js and PHP and a relational database. App launched with an integration to cross-post on Steemit, later with WAX Music NFT capabilities
- I maintained cXc.world for nearly 5 years, and lead our project's marketing, community and tech development

Alejandro Lazado
- Alejandro is experienced as a leader and creative director
- He in working directly with Spanish-speaking employees and managing human aspects of the project 


### Team Org Repos

**Profiles**
- https://github.com/TetraGrids


### Team Member Repos

- https://github.com/dougbutner

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/douglasbutner/

## Development Status

Tetra builds on years of development of cXc.world, launched December 2018.

Development in Ideas + Data structures
- Web4 Paper
- Mapps Paper

Development in Code
- Smart Contracts

Tetra hasn't been developed in public yet, but will be in the future after the project is publicly announced.


# Demo of current progress
Here's a demo of the system built by our Team Lead that is the precursor to Tetra. Also see `Work you have already done.` below.

https://www.youtube.com/watch?v=coNc4iJB7OM&t=136

And an example of an NFT integration can be seen live at [cXc.world/f/nft](https://cXc.world/f/nft)



## Development Roadmap

### Milestone Summary

Summary: Tetra Team will start to develop in public with the ENF, test, and publish Extensible Metadata Standard along with documentation and tutorials for Antelope developers. Result: Memos on Antelope Blockchains will become more useful and easier to understand. 

Developers with less developer experience or knowledge of the tech stack to create their own basic applications, as they will be able to store and act upon on-chain data in a simpler way.


- **Total Estimated Duration:** 2 months 
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 10,000 USD



### Milestone 1 - Extensible Metadata Standard

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:**  5,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | I will document the metadata standard to show the functionality and how an end user (Antelope dapp developer) would implement In a smart contract and in a Javascript application. I will document in-code where appropriate and in a README.md for the repo. |
| 0c. | Testing Guide | I will include unit testing in the code in a node.js project. |
| 0e. | Article | I will publish an article on Hive and Medium that explains the technical aspects of the XMS system and hpp for an Antelope developer audience. I will publish second article announcing the system with the benefits for a wider developer community, as the standard will be able to be used in different contexts. I will encourage developers to use the technology, and link to relevant Antelope developer docs. |
| 1. | Smart Contract Implementation | I will create a memo-specific implementation in C++ that can be included as a header file in any Antelope dapp developers project in the future. This will enable contract developers to listen for transfer memos and have a tool kit to decipher these memos, giving them an easy way to inter face with tokens that other's will understand.  |  
| 1. | Smart Contract Implementation | I will create a rosio.token::transfer memo-specific implementation in C++ that can be included as a header file in any Antelope dapp developers project in the future. This will enable contract developers to listen for transfer memos and have a tool kit to decipher these memos, giving them an easy way to inter face with tokens that other's will understand.  |  
| 2. | Node Package | I will launch a npm package for XMS. This new package will allow people to use the extensible meta-data standard to interact with the block chain in their applications, including given them the tools to make sense of application specific information based only on tx memos. This will empower people to build front ends on top of blockchains in the Antelope ecosystem. |  
| 3. | Audits + Release | The code will be audited and released. Docker image may be released depending if warranted by the complexity of the environment. | 


Other's works used: [Atomic Assets](https://github.com/pinknetworkx/atomicassets-contract) header file. Builds on previous work from team.


### Milestone 2 - Viral Global Invite System

Summary: I will create an unseen-on-Antelope on-chain invite system with leaderboards that utilizes scarcity as well as location to create a viral and valuable economy to get people ready (and on Antelope) for Tetra when we launch our full economy.

Antelope projects can use this in the future to build awareness and hype. Through the system, referrals will grow slowly and naturally because of game functions of a time limiting factor, as well as a top chart function/

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 5,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | I will document in-code and in a README.md for the repp which will contain instructions on use. |
| 0c. | Testing Guide | I will include unit testing in the project and instruct users how to test in the README. I will update the READMEs when needed. |
| 0e. | Article | I will publish an article on Hive and Medium that explains the technical aspects of the referral system and contract for a technical audience. I will publish second article announcing the system with the benefits for a general audience. I will encourage developers to use the technology, and link to relevant Antelope developer docs. |
| 1. | Develop Contract | I will build a referral system that allows the user to invite a limited amount of people per day, and rewards them for inviting people, as well as for inviting people who invite people. There will be no cost for the invitee, and the inviter and invitee will both be rewarded with assets that allow them to better-utilize Tetra on launch. Features include time-limiting the amount of invites, extra incentives for inviting people who invite others, and a top-chart of referrals. |
| 2. | Simple UI Funnel | I will create a way to interact with the referral system through a UI. This will be a part of a funnel that allows a user to display interest and start to make small meaningful interactions with Tetra. |  
| 3. | Audits + Release | The code will be audited and released. Docker image will be shared for the contract development. | 

## Future Plans

- how you intend to use, enhance, promote and support your project in the short term

Tetra is currently finalizing up our logo variations, branding documents and online presence. 

Douglas is currently holding programming tests to hire 2 key developers (React + C++) for Tetra. 

We plan to announce these tools + articles in the Antelope telegram group, as well as to promote the article in both the Tetra and cXc social media. In the short term. we will keep our ears open, and listen for any good ideas to incorporate in the future, as well as anything we should remove that is insecure or inefficient. Team will stay active in reviewing pull requests.

- the team's long-term plans and intentions in relation to it.

My launch promo strategy is to use cXc's userbase and brand recognition as catalyst for inviting people to use the invite system (Milestone 2) building Tetra up for launch.

Our technical strategy is to build the foundations as open-source tech through grants, and when we are ready, launch the project contracts. We will launch individual aspects on WAX testnet first. 

We plan to continue to develop Tetra in future grants to build a solid relationship with the ENF. This is something I neglected to do with cXc, failing to recognize the importance of asking for help and working together, naively believing that good tech and systemic design means a successful system. Now I understand it's important to take each actor's needs into account and serve all as best as possible.

We will continue to market, develop, and expand Tetra, projects we support like Hypha, and Antelope as the shining technology to enable these systems.


## Additional Information

**How did you hear about the Grants Program?** 

From the Antelope Developers telegram.

- Work you have already done.

I started designing Tetra in 2020, staying longer-than-expected in Barranquilla for the pandemic, [already thinking about ways](https://github.com/dougbutner/effective-collective) to make the system I had created for cXc better. I've been working in the background on tetra for this time, creating the ideological grounds. This culminated in understanding thoroughly what the component technologies were I would need, and starting to build those through the ENF grant program. 

In the past: 

I built another project [cXc.world](https://cxc.world) and [PURPLE](https://github.com/currentxchange/purple-explainer) and developed the concept of [Mapps](https://docs.google.com/document/d/1YppJ2EYumRI2j0UHYdZh7NJMObMI_NfHgaFRLbjgBtw/preview)

And the Ups contracts: 
https://github.com/dougbutner/beta-pseudo/blob/main/real-contracts

Both of which are groundwork tech relevant to Tetra.

- If there are any other teams who have already contributed (financially) to the project.

The project has been personally funded by Team Lead Douglas Butner. 

- Previous grants you may have applied for.

We applied first for [funding for cXc](https://github.com/dougbutner/grant-framework/blob/main/applications/cXc_ups.md) but were unable to continue because cXc had a token sale. 

With Tetra 

Pomelo grant [killerapp](https://pomelo.io/grants/killerapp)

Other grants our team members have applied for: 

[musicnfts](https://pomelo.io/grants/musicnfts), [nftmedia](https://pomelo.io/grants/nftmedia), [democracy](https://pomelo.io/grants/democracy), and [evmxideathon](https://www.youtube.com/watch?v=ggHqQgSNXHg)