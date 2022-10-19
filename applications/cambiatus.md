# EOS Network Foundation Grant Proposal

- **Project Name:** Roles and Permissions
- **Team Name:** Cambiatus
- **EOS Payment Address:** luizhadadeos
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 2
- **Pomelo Grant(s):** https://pomelo.io/grants/cambiatus
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/cambiatus


## Contact

- **Contact Name:** Luiz Hadad
- **Contact Email:** luiz@cambiatus.com
- **Website:** https://cambiatus.com/

## Project Overview

This is a followup-grant from a successful Pomelo Grant: https://pomelo.io/grants/cambiatus

## Overview

- **Name:** Roles and Permissions
- **Brief Description:** Use Roles & Permissions to make our users grow as they interact with a collaborative business / DAOs.
- **Relationship to EOSIO:** Our users already use EOSIO as their blockchain.
- **Reason for Interest:** EOSIO is great because of speed, easy contracts to delegate, stake and build in multisig, but it lacks capacity to contextualize user achievements and permissions on a DAO. We intend to solve that pain.

### Project Details

- [Mental map](https://miro.com/app/board/uXjVOBYRrXc=/)
- [Storytelling Presentation in Figma](https://www.figma.com/proto/N724ADHvSImTQkYYnIPOoh/Proposta-ENF_Roles-%26-Permissions?page-id=0%3A1&node-id=26%3A49&viewport=957%2C254%2C0.29&scaling=contain&starting-point-node-id=26%3A49)
- [Storytelling Presentation in PDF](https://drive.google.com/file/d/1ba9zNnsYe2pBF_5lB5VfuGA1ekvz_WNC/view?usp=share_link)
- [Mock-ups/designs of any UI components](https://www.figma.com/file/IYaSqUD58quAZMIhqdi7WA/Roles-%26-Permissions?node-id=508%3A3181&t=DYGyoE0p7cT4WYFW-0)
- [Wireframe in production](https://drive.google.com/file/d/1yr7H5RMlMqKqgawuBTvsnA9f_1otgQ90/view?usp=share_link)


This grant builds on top of another successful [grant](https://pomelo.io/grants/cambiatus) we worked on. Because of that, we already have some data models and documentation, which can be found [here](https://github.com/cambiatus/contracts/blob/master/community/community.hpp) and in the following code snippets:

```cpp
  /**
   * Roles is a way to identify people's relation with their community.
   * It can be used to allow people to be recognized by their role in the whole of the community, to give them awards or to help them to identify themselves.
   * They can be customized with a color and can have a name
   *
   * Roles can also be atttached with permissions that gives them abilities within the community such as the ability to invite new people in, to sell goods and services and more
   *
   * The initial abilities that we offer are:
   *  invite: invite new users `netlink`
   *  claim: allow claiming actions `claimaction`
   *  order: create new orders `transfersale`
   *  verify: verify autenticity on claims `verifyclaim`
   *  sell: sell items on the shop `createsale` `updatesale` .
   *  award: awards an action `verifyaction` (`award`)
   *
   * All of those roles are used from within the contract to mediate the usage of some actions.
   *
   * Roles are scoped by community.
   */
  TABLE role
  {
    eosio::name name;
    std::vector<std::string> permissions;

    std::uint64_t primary_key() const { return name.value; }

    EOSLIB_SERIALIZE(role, (name)(permissions));
  };
```

```cpp
enum permission
{
  invite,
  claim,
  order,
  verify,
  sell,
  award,
  transfer
};
```

```cpp
  TABLE member
  {
    eosio::name name;
    eosio::name inviter;
    std::string user_type;
    std::vector<eosio::name> roles;

    std::uint64_t primary_key() const { return name.value; }

    EOSLIB_SERIALIZE(member,
                     (name)(inviter)(user_type)(roles));
  };
```

**API specification from the contract**

We will provide helper functions to help verify if the user has the required role:

```cpp
  /// @abi action
  /// Upserts roles in a community
  ACTION upsertrole(eosio::symbol community_id, eosio::name name, std::string color, std::vector<std::string> & permissions);

  /// @abi action
  /// Sets a number of roles for a user
  ACTION assignroles(eosio::symbol community_id, eosio::name member, std::vector<eosio::name> & roles);
  
  // Convinience methods
  bool is_member(eosio::symbol community_id, eosio::name user);
  bool has_permission(eosio::symbol community_id, eosio::name user, permission e_permission);
  std::string permission_to_string(permission e_permission);
```

### An overview of the technology stack to be used
It's an on-chain functionality so everything will be handled locally with the libraries we will provide. We also will provide our [smart contract source code](https://github.com/cambiatus/contracts/blob/master/community/community.hpp).


#### We will also provide reference for:
- Ingesting blockchain data using [Elixir](https://elixir-lang.org/) and [Broadway](https://elixir-broadway.org)
- Serving blockchain data using [GraphQL](https://graphql.org)
- Interacting with relevant smart contract action using Javascript and [Elm](https://elm-lang.org)
- [Our architecture](https://www.figma.com/file/i4Azmx3APcQulJ1zmHNLIV/Cambiatus-Architecture?node-id=0%3A1), which can help other projects decide on their own path

### PoC/MVP or other relevant prior work or research on the topic
Our current structure includes the following roles: members, validators and admins. These roles are being used by our over 9000 users since 2018:

- Members: `buy`, `sell`, `claim`
- Validator:  `approve` or `reject` claims (voting)
- Admin: Configure community settings, and perform admin only tasks: manage objectives, actions, enable features, publish internal communications, configure tokenomics and more.

### What your project is not or will not provide or implement
We already have the intent to extend this data structure for different horizons. But for now we will *not* provide:
- Integration with multi signatures,
- Onchain and Offchain propositions,
- Decision making tools,
- User journeys,
- Weighted voting for different roles.

All of the above will be addressed in future versions.

Our end goal is to allow communities to decide with different voting strategies that take into consideration their history on the community instead of simply having a proportional voting weight based on the amount of tokens the user holds. 

To achieve this we propose the following steps:

1. Provide structure for adding context/metadata to a user participation in a community. Roles will provide this, allowing users to earn or receive roles based on their history / reputation, on and off chain. 
2. Some of those achievements will provide them with permissions, effectively allowing them to "work their way" into more responsibilities and permissions on a community. This will be provided by permissions. This means certain eosio actions will only be processed by people of certain roles within the community that have the appropriate permission.
3. After having this basic contextualization, we will create tools for decision making inside a community. This will allow users to vote and multisig with their votes and roles. 
4. From here, we will have to define what our communities need the most. Some ideas are a more refined voting system with weighted voting based on roles, exploring external reputation systems like [POAPs](https://poap.xyz), creating User Journeys to allow communities to promote internal learning and capacitation.

For this grant we intend to start walking that path, building steps 1 and 2.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?
    - We develop a software that helps communities create their own tokens and have a set of DAO tooling for that. Our focus is to onboard users with no blockchain knowledge or familiarity to use it. Communities can create their own complementary currencies and use it to help them connect, trade and save their other fiat/crypto money for other interactions. 
    - We are open source and a participant in the EOS ecosystem since 2019.
    - We run our own EOSIO private network with the help of EOS Rio block producer as our tech partners.
    - People from our team are long time learners and teachers of the ecosystem (our team facilitated 3 EOS hackathons and many meetups in Brazil since 2018).
    - In 2022 we got the first financial support from the EOS Community via Pomelo, when we reached the top 10 projects with the roles and permissions feature, base work for what we are talking about on this grant. 

<br/>

- Who is your target audience?
    - The whole EOSIO/ Antelope compatible ecosystem (Wax, Ultra, Telos, etc),
    - Our 8 communities in production, its leadership teams and their 9k+ users from Costa Rica, Brazil and Ethiopia,
    - Dapp developers trying to add a comprehensive permission tool to their smart contracts,
    - DAOs facing the limitations of a simple holder whale taking important decisions,
    - Users with little to no blockchain experience

<br/>

- What need(s) does your project meet?
  - **Decentralization:** using Roles & Permissions, community leaders will be able to assign roles and permissions to other people involved in community leadership and by doing so, taking the decision/task away from just one person.
  - **Decentralized governance:** allowing decision-making to be inclusive and collaborative, facilitating a scenario in which people can exercise their voting power based on their history of living within the community, instead of having their voting power stipulated only by the number of tokens you own. New leaderships can emerge as time progresses. 
  - **Education:** Expanding access to the community based on learning: as a user learns, commits and collaborates with the community, they earn more access. This also helps to avoid trolls or fake Sybyl accounts, as it takes time to be able to participate fully.
  - **Engagement:** As the person learns, interacts and contributes to the growth of the community, they are recognized, gaining Roles & Permissions that reflect their good engagement within the community.

### Similar projects 
Hypha is a similar product within the EOSIO ecosystem. They're an organization-in-a-box solution and we believe they’re better suited for communities that already have a deeper blockchain knowledge and know what a DAO is, how to use a DAO toolkit, and most of their features are thought for advanced users. 

Hypha looks like a high-end application, with many different features, that requires a broader / deeper knowledge to use. We’d love to see both projects coexisting, learning and collaborating in the EOS ecosystem. Since both projects are open source, it will be great to see how both projects unfold. Cambiatus focuses on ease of use, and being an entryway for many people, enabling them to further their interactions with the broader EOSIO community and projects. 

From other blockchains and ecosystems we find another set of tools that may look similar:
- Aragon
- Colony
- DAOStack
- 1HiveDAO
- DAOHaus
- Socialstack
- Closer.earth


## Team

### Team members
- Co-founders: Karla Córdoba-Brenes, Ranulfo Paiva Sobrinho;
- Community Building Team: Luiz Hadad, Criscia Cesconetto, Luisa Calixto;
- Developers Team: Julien Lucca, Henrique Buss, Matheus Buss;
- UI/UX Team: Juliana Ramos, Rafa Chadud;
- Data Science: Helton Ramos.

#### Team Leaders: 
- Community Building Team Leader: Luiz Hadad;
- Developers Team Leader: Julien Lucca;
- UI/UX Team Leader: Juliana Ramos

### Legal Structure
- **Registered Legal Entity:** Cambiatus OPC
- **Registered Address:** PO Box 2510, Grand Cayman KY1-1104, Cayman Islands


### Team Experience
Our team has been building on EOSIO for 4 years now. We've done our pilot in a community in Costa Rica. We've been part of every major announcement since before Block.one released version 1.0. Since then we've deployed and maintained our own private network, developed several features into our app, including [smart contract](https://github.com/cambiatus/contracts), [backend](https://github.com/cambiatus/backend), [infrastructure](https://github.com/cambiatus/backend#nginx-setup), wallet integrations, [frontend](https://github.com/cambiatus/frontend) and finally our own wallet inside our app.

Although we admire and like projects like Hypha, Cambiatus is different because our main focus is on social currencies and financial resiliency to foster planetary regeneration. This is shown through our actions, such as choosing to develop a mobile-first webApp because many of our members don’t have enough memory space in their smartphones to download an app, others don't have access to a PC/laptop and others yet have a slow and unreliable internet connection. These actions are reflections of our goals and learnings with our partner communities which are located in Latin America and Africa.

We also have translations to portuguese, spanish, catalan, amharic and english. Our educational content is in english, translated to portuguese and spanish - and we have community support in those three languages. Being pluricultural and language inclusive to our communities is a must.

Our biggest differential to our communities is that they're all provided with assisted tokenomics co-design sessions - we don’t assume they know how to create a currency or develop their own tokenomics. We added a human layer to enable our partner communities to use our tools and be able to promote change in their economic context. It's a constructivist method, allowing co-creation, co-organization and aligning objectives under a group.

[Our methodology starts with a learning path](https://www.cambiatus.com/learningpath) that helps community leaders understand what is money, how money is created, what are social currencies, examples, and then we start explaining about crypto, blockchain, DAOs, collaborative businesses and evolved Coops using blockchain technologies.

Only after this we start the co-design sessions, and we take the educational approach very seriously, because at the end of the day, it’s a mindset change.

We believe Cambiatus is a tool that is more accessible for “normies”, especially the ones that don’t have much understanding about crypto or communities that don’t speak fluent english (the language barrier is HUGE in Latam). One example is that we’re doing a co-design process with the Paiter Surui Indigenous community, aiming to create the first blockchain-based social currency in their tribe. How would they be able to use Hypha? We believe Cambiatus is easier to use than Hypha, with the most essential tools, and still helps communities create their own organizations to exchange value and coordinate themselves towards financial resiliency.

Cambiatus is the first step for many people entering the crypto ecosystem and discovering how to use social tokens and collaborate with DAOs. We already have [partner communities](https://www.cambiatus.com/communities) doing this like [Muda](https://www.instagram.com/mudaoutraseconomias/) and [Play4Change](https://www.play4change.io/), empowering people from favelas in Brazil, [Verdes](https://verdesmonteverde.com/) in Costa Rica and [Agelgil](https://www.cambiatus.com/agelgil) in Ethiopia. Our newest community called [Paiter Coin](https://www.cambiatus.com/povo-paiter-surui), co-created with the Paiter Suruí Indigenous People, in the quest to involve the people in community actions in the village and have their economy independent with their own currency.

- **Karla:** MSc Community Development, Cambiatus co-founder, Shuttleworth Foundation Alumni and first Latinamerican Grantee, Singularity University Alumni, Asoblockchain Costa Rica Board Member, TEDx Costa Rica speaker.  Past experience:  10+ years working in community development and environmental projects in Costa Rica, supporting local communities, facilitating development and organizational processes. 2+ years collaborating with Enlivening Edge Magazine as a team member, an holacratic organization focused on Next-Stage Organizations. 5+ years developing and implementing Cambiatus Methodology and co-design processes. Co-organized the first EOS Hackathon in Brazil. Currently supporting the strengthening of the Costa Rican blockchain ecosystem.  Speaker focused on Impact, Governance, and ReFi. [Full CV](https://docs.google.com/document/d/1ayR6cLJppXk-9YHpFVSyw_EQ7zDvtT69JPVuLgH-PJI/edit?usp=sharing) 

- **Ranulfo:** PhD in Economics, Post Doc in Crypto Assets applied to Conservation. Cambiatus co-founder and vagabond master [Full CV](https://docs.google.com/document/d/1xnL1sOqLcduWJUTyiSFuu-l3ZwI_eOxfs4ELnwjCFmo/edit?usp=sharing) 

- **Lucca:** Full stack software developer, collaborated on one of the first games on EOS, [MonsterEOS](https://github.com/MonsterEOS/monstereos) a tamagotchi like platform. Working for 5 years with blockchain, mainly Ethereum and EOS. 3+ years working with mobile app development, 10+ years working with backend development. I have teached on 4 universities on free courses and participated on boostraping dev communities, like [Ethereum São Paulo](https://www.meetup.com/pt-BR/ethsaopaulo/) (2k members) and [Elixir User Group in São Paulo](https://www.meetup.com/pt-BR/elug_sp/) (1k members). Published two ERC20 tokens into mainnet with some use and also helped auditing for [PixEOS](https://gallery.pixeos.art/) smart contracts

- **Luiz Hadad:** Former head of community @ EOS Rio, helped organize several hackathons, meetups and conferences in Brazil.  Currently is an advisor at Ethereum Brasil, helping organize Ethereum Rio and Ethereum São Paulo events this year. Speaks at the main crypto conferences in Brazil - was the opening speaker at Ethereum Rio and showcased the Cambiatus use case. Lead researcher for the Sherlock Communications Blockchain Report Latam. Member of the Founders Circle at ReFi DAO

### Team Org Repos
- https://github.com/cambiatus
- https://github.com/cambiatus/frontend
- https://github.com/cambiatus/contracts
- https://github.com/cambiatus/backend
- https://github.com/cambiatus/event-source

### Dev Team Member Repos
- https://github.com/lucca65 
- https://github.com/henriquecbuss 
- https://github.com/MatheusBuss

### Related work from our team
- https://github.com/henriquecbuss/elm-eos
- https://github.com/MonsterEOS/monstereos
- https://github.com/lucca65/ex_coin
- https://github.com/lucca65/thedapp

### Team LinkedIn Profiles (if available)
- https://www.linkedin.com/in/muguika/
- https://www.linkedin.com/in/ranulfosobrinho/
- https://www.linkedin.com/in/luiz-eduardo-abreu-hadad-9b493033/ 
- https://www.linkedin.com/in/julienlucca/ 
- https://www.linkedin.com/in/henrique-buss-5b85801b4/ 
- https://www.linkedin.com/in/matheus-da-cunha-buss-0236b9164/
- https://www.linkedin.com/in/julianacristineramos/
- https://www.linkedin.com/in/lcalixxto/
- https://www.linkedin.com/in/rafaela-chadud/
- https://www.linkedin.com/in/heltonramos/


## Development Status 

Development has already started with smart contract implementation, which can be seen here: https://github.com/cambiatus/contracts or with a little more depth in the PR: https://github.com/cambiatus/contracts/pull/33. 

Basic planning for the next steps can be seen here: https://github.com/orgs/cambiatus/discussions/669

This feature will require interactions on: 
- Smart Contracts, which is already done;
- UX/UI, which is on progress;
- Backend ingestion, which has not started yet
- API, which has not started yet
- Frontend, which has not started yet

Some resources:
- [Figma reference with some discussion (in brazilian portuguese)](https://www.figma.com/file/IYaSqUD58quAZMIhqdi7WA/Roles-%26-Permissions?node-id=0%3A1)
- [Slides for the presentation of Role and Permissions](https://www.figma.com/proto/N724ADHvSImTQkYYnIPOoh/Proposta-ENF_Roles-%26-Permissions?page-id=0%3A1&node-id=26%3A49&viewport=957%2C254%2C0.29&scaling=contain&starting-point-node-id=26%3A49)
- [Mental map](https://miro.com/app/board/uXjVOBYRrXc=/)
- Storytelling Presentation in PDF: [Roles&Permissions.pdf](https://drive.google.com/file/d/1ba9zNnsYe2pBF_5lB5VfuGA1ekvz_WNC/view?usp=share_link)
- [Mock-ups/designs of any UI components](https://www.figma.com/file/IYaSqUD58quAZMIhqdi7WA/Roles-%26-Permissions?node-id=551%3A7694&t=vO3s9hMAqvU7jIPd-1)
- Wireframe in production: [Wireframe Roles and Permissions.pdf](https://drive.google.com/file/d/1yr7H5RMlMqKqgawuBTvsnA9f_1otgQ90/view?usp=share_link)


## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 7 months
- **Full-Time Equivalent (FTE):** 6 FTE
- **Total Costs:** $50,000 

Note: This grant interacts with several existing Github repositories, all of them already have instructions on how to run and test. To test, aside of automated tests and pull requests, its possible to check live on https://demo.cambiatus.io. This is our demonstration environment and contains deployed backend, frontend and contract. You can also use our [block explorer](https://local.bloks.io/account/cambiatus.cm?nodeUrl=demo.cambiatus.io&coreSymbol=SYS&systemDomain=eosio)

### Milestone 1 — Provide structural changes for adding context / metadata to a user participation in a community, mostly backend work with no visible changes
- **Estimated duration:** 1 month
- **FTE:** 6
- **Costs:** 8,500.00 USD
- **License:** GNU Affero General Public License v3.0
- **Documentation:** All documentation on this milestone is delivered by code and release notes, as its intended to be consumed by code
- **Testing Guide:** Core functions will be fully covered by unit tests to ensure functionality and robustness. Related repos will contain testing instructions. Test setup and instructions are already present in our [backend repository](https://github.com/cambiatus/backend), only new tests will be added. Existing instructions will cover them
- **Application interface to EOSIO:** We will create an integration layer, consisting of a blockchain sync solution like demux implementation or similar to digest blockchain data into our own centralized database, for caching
- **Front-End / User Interface:** Minor adjustments to comply with the new data structures, but no new screens or other visible changes
- **Caching layer	/ API Interface:** Minor adjustments to comply with new data structures:
    - Provide new entities like role and permission
    - Updating existing entities like network and user

This Milestone is partially completed and can be checked on some Pull Requests:
- https://github.com/cambiatus/contracts/pull/33
- https://github.com/cambiatus/contracts/pull/40
- https://github.com/cambiatus/backend/pull/200
- https://github.com/cambiatus/frontend/pull/676
- https://github.com/cambiatus/event-source/pull/34
- https://github.com/cambiatus/event-source/pull/36

**How to assert correctness:**  This milestone will contain no visible changes. A [block explorers](https://local.bloks.io/account/cambiatus.cm?nodeUrl=demo.cambiatus.io&coreSymbol=SYS&systemDomain=eosio) will be needed to check its correctness. 

### Milestone 2 - Allow users to earn or receive roles manually from the community admin. Including visible changes
- **Estimated duration:** 1 month
- **FTE:** 3
- **Costs:** 8,300.00 USD
- **Design:** Design screens to experiment with how we are going to allow admins to manage roles inside an community:
  -  Create, Update, Delete roles
  -  Assign Roles
  -  Display roles in profile and related pages
  -  Display community roles
  -  Designs are partially done and can be seen [here]((https://www.figma.com/file/IYaSqUD58quAZMIhqdi7WA/Roles-%26-Permissions?node-id=508%3A3181&t=DYGyoE0p7cT4WYFW-0))
- **Backend:** Based on the screens, develop GraphQL APIs to better serve those screens. Including adding both database and GraphQL entities like `user_roles`, `community_roles`, permissions enums
- **Frontend:** 
  - Add hover for role public view
  - Add modal for viewing role modal
  - Add links to modals: profile page, community page, user hover, profile modal
  - Role cards on the community page
  - Role wide cards for the new "Our Roles Page"

**How to assert correctness:** This milestone have frontend screens, so it will be possible to:

- Check the demonstration environment to see if it matches the designs linked above;
- Try doing the operations described related to roles. You will need to be an community admin. Create your own on: https://demo.cambiatus.io/community/new
- Run tests on the backend with `mix test`, after following the [setup tutorial](https://github.com/cambiatus/backend/blob/master/.github/contributing.md)

### Milestone 3 - Gather feedback on the first round of implementations. No code on this milestone, mostly community building, showcasing and learning sessions to use the newly added feature.
- **Estimated duration:** 2 months
- **FTE:** 6
- **Costs:** 8,300.00 USD
- **Testing Guide:** Use of navigable prototypes to carry out concept and usability tests with key people (administrators and other members of the community) in order to raise and define hypothesis and mitigate possible functionality errors. We will make adjustments to interfaces based on test results
- **Documentation and Testing Guide:** We will use our test environment to test the main functionalities and the proposed design. We will provide both inline documentation of the code and a basic tutorial that explains how a user can use it within their communities. We will also publish our platform tutorials [here](https://medium.com/cambiatus-tutorials)
- **Feedback gathering and tutorials:** We will do live meetings and workshops to showcase basic usage and how existing communities could use this. Meetings will be in english, spanish and portuguese, languages that our communities use. With feedback we can prioritize upcoming features and adjust as needed
- **Design:** Prepare for the next milestone: 
  - Basic interface for creating common automations with triggers for number of claims, or specific claims, or selling an item on the shop
  - Screen to display automations enabled
  - Create and validate mockups

**How to assert correctness:** This milestone is focused on community building with no code artifacts. In order to assert that this plan was indeed followed, please participate on our community sessions. Please get in touch with our community building team: luiz@cambiatus.io. Also, our findings will be posted on our [Medium](https://medium.com/cambiatus).  


### Milestone 4 - Automatically give roles based on onchain triggers. This milestone is more vague, as we need to study how to better implement this. Research phase will be done together with milestone 3, if possible.
- **Estimated duration:** 1 month to 2 months
- **FTE:** 6
- **Costs:** 8,300.00 USD
- **Research:** Study tools like Chainlink and LiquidApps to check on how we enable oracle-like structure and decentralized automation systems. 
Depending on our findings, plan out a centralized alternative. We can use multisigs to initiate automatic transactions on communities, requiring admins to approve them
- **Contract:** Actions to authorize Chainlink (or LiquidApps) to our communities to setup automation
- **Backend:** No further work will be required if we manage to do this with a solution similar to Chainlink. If not, we will need to develop a similar, centralized one. It must allow for **triggers** based on our contract ACTIONs:
  - `upsertactions` (when actions are changed in a community)
  - `upsertobjectives` (when objectives are changed in a community)
  - `claimaction` (when a user initiates a request for claiming an action)
  - `verifyclaim` (when other users vote to approve/reject a claim)
  - `reward` (when admins reward users a certain amount of tokens) 
  - with the following **Effects**:
    - `assignrole`
  - under available **Conditions**:
    - Count: a certain number of times a trigger must be activated
    - Time scope: a limit date like "5 days, 1 month" and so on
    - Existing roles: a filter that makes sure the affected users have necessary roles
- **Extensive tests for those workers:** Given its complexity, it will required thoughtful testing
- **Frontend:** 
  - Screens for assigning roles, managed by community admins
  - Rework our notification center, to better display events live 
  - Commemorative modal for achieving a role
  - Admin screens to display existing automation
  - Admin screens to enable automation
  - Admin screens to create, edit and delete automation

**How to assert correctness:** Follow the [setup tutorial](https://github.com/cambiatus/backend/blob/master/.github/contributing.md) and try creating automations using our [GraphQL playground](https://demo.cambiatus.io/api/graphiql)

You can also try to do the same using our demonstration environment. This requires you to be an admin for a community, create one [here](https://demo.cambiatus.io/community/new).



### Milestone 5 - Implement roles scoping for our action claim flow. Only certain roles can validate actions. This is a refactor of an existing feature. Can be done in a different order, as we already have all the requisites on our code. 
- **Estimated duration:** 1 month
- **FTE:** 5
- **Costs:** 8,300.00 USD
- **Contract:** 
  - Adjust action/claim flow to use a role as a validator instead of a list of users
  - Allow optional specific validator role; Migrate existing contract data to the new usage of role
  - Clean up old data to minimize RAM footprint
- **Backend:**
  - Migrate existing database to use new role structure for actions
  - Adjust GraphQL entities
- **Frontend:** 
  - Adjust forms to use roles
  - Adjust multiple usages of actions/claims that display a list of validators to display a role instead
  - Adjust forms to comply with new contract action params

**How to assert correctness:** This milestone affects an existing feature on the platform. Currently, in order to mint/issue new tokens, you need to do an action for your community. Actions are default way of minting tokens. Today, when creating actions, you'll need to assign a list of user that are the validators for that action. This milestone aims to change that. Instead of assigning a list of unique users, you will instead choose a role.

In order to test, you'll need to be a community admin, you can create your own community [here](https://demo.cambiatus.io/community/new). Then, access your community, click on the cog icon, located next to your notifications, on the top right corner of the app. Then go to "Objectives and Actions" -> "Create new objective" -> Fill in the requested data -> Select your newly created objective -> "Create new action". 

You will see a form. Fill the data in. On the section "Does it need verification?" choose "Manual". You'll be able to select roles on the section that appeared. Save your objective.

Now, you will need to:

1. Have the necessary role. You can assign yourself a role on the admin screen (accessible from the cog used earlier)
2. Open a new claim. That can be done on the community screen, accessible on your Homescreen -> How to earn
3. After claiming, you should see a new section on your Homescreen: "Actions for analysis".
4. You should be able to vote on a claim correctly.


### Milestone 6 - Test, gather feedback and adjust for errors or unexpected edge cases. Final interaction on the feature before its considered done.
- **Estimated duration:** 1 month
- **FTE:** 6
- **Costs:** 8,300.00 USD
- **Testing Guide:** pre-implementation tests analyzing functionality and usability along with the proposed design
- **Documentation:** We will provide both inline documentation of the code and a basic tutorial that explains how a user can use it within their communities. We publish our platform tutorials [here](https://medium.com/cambiatus-tutorials)
- **Feedback gathering and tutorials:** We will do live meetings and workshops to showcase basic usage and how existing communities could use this. Meetings will be in English, Spanish and Portuguese, languages that our communities use. With feedback we can prioritize next features and adjust as needed

**How to assert correctness:** This milestone is focused on community building with no code artifacts. In order to assert that this plan was indeed followed, please participate on our community sessions. Please get in touch with our community building team: luiz@cambiatus.io. Also, our findings will be posted on our [Medium](https://medium.com/cambiatus).  

## Future Plans
Our first intent is to use the Roles & Permissions feature within the Cambiatus ecosystem. Our communities will be called to experiment with the feature and our Data Team will be able to gather some insights about how it's been used. We would like to evolve this feature and decouple it from Cambiatus, allowing other Antelope based applications to use it as a way to improve their DAO toolkit. This will be addressed in future versions, but since we are open source, our insights, learnings and how-tos will always be available to anyone interested, and free use under GNU Affero General Public License v3.0.

With our Roles & Permissions implemented, we will address decision making next. We intend to implement a set of decision-aid methodologies to support our members by leveraging vast practical and theoretical experiences in the field of applied decision making that one of our co-founders has. We want to adapt and develop new methodologies to support decentralized governance processes, not only for Cambiatus members but also for other DAOs. Tools include voting and doing weighted multi signatures based on roles. We will provide some starter voting strategies like simple majority and qualified majority (qualifying and weighting votes based on roles acquired).

During the year 2022, we've also started an internal training with our team and some key members of our communities using some decision making methodologies so we can get up to speed with how it's done before starting using roles to scope and implement decision making tools. Results have shown promise and motivated our team to continue learning and apply the Cambiatus decision making process.

As we progress, we wish to build more refined voting systems, exploring POAPs/NFTs as achievement badges and ways to back up a member’s reputation in a certain community. With Roles & Permissions, we are allowed to explore different paths to decentralized decision making, using not only the amount of tokens one account has, but their history / relationship / collaboration within a certain DAO. Effectively moving away from giving governance power to those with more votes and instead valuing a member vote based on their learning, participation, history, relationship and collaboration with a certain community or DAO. We believe this to be a more human-like approach than what is commonly done in our industry.

We also wish to build a tool to allow admins to create "User Journey"', a role based path that walks users through how to participate more in their community, earn roles and grow together with their communities. User Journeys could also be used to promote learning paths inside a community, by setting a learning path that guarantees participants to have certain roles. For example, users that take all the decision making courses, publish their findings publicly and help new users to onboard could take the role of "Voter", effectively allowing them to vote on DAO decisions. 

## Additional Information

Luiz Hadad, our lead for community building, is an active member of the EOS community since its launch. He worked at EOS Rio leading community building from 2018 until 2019, participated in many EOS conferences and kept an eye on the development of the EOS ecosystem. Since the launch of ENF, we have been willing to participate more in the community. We participated in the Pomelo Grants season 3 and saw on twitter that the grants program was happening. Then Luiz asked Yves La Rose for some information/guidance on the process through telegram, and we got into this stage.


### Members that contributed financially to the project
Some of our members also help Cambiatus financially by contributing to our Liquidity Pool, here are some of them:

- [Satisfied Vagabonds LLC](https://www.satisfiedvagabonds.com)
- Helena Stewart: MUDA leader and impact investor
- Karla Córdoba-Brenes & Ranulfo Paiva Sobrinho: Cambiatus co-founders.
- [Shuttleworth Foundation](https://shuttleworthfoundation.org)
- Cambiatus team members and community team leaders

Approximate total contribution from start to date: $350K USD

Previous grants you may have applied for:

- We got a $1M USD grant from Shuttleworth Foundation, executed from 2018-2021 and that actually served as Cambiatus Seed Funding. 
- We applied for a grant on Pomelo Season 3, being a top 10 project for the season.
- We also applied for grants in other ReFi initiatives, such as Celo and Future Quest.

