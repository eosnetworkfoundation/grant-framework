# EOS Network Foundation Grant Proposal


- **Project Name:** Msig.app
- **Team Name:** Fire Labs Limited
- **EOS Payment Address:** cryptolions1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 2
- **Pomelo Grant(s):** https://pomelo.io/grants/msig.app
- **Project is Open-Source:** Yes. All is open-sourced.
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/CryptoLions/MSIG_tool (public) https://github.com/orgs/CryptoLions/repositories (private, will be open-sourced when project will be release)

## Contact

- **Contact Name:** Taras Kob, Sudip Banerjee
- **Contact Email:** roar@cryptolions.io
- **Website:** https://cryptolions.io


## Project Overview


### Overview


- **Name:** Msig.app - simplify multisig for novice and expert
- **Brief Description:** It is too complicated for a novice to manage multi signatures. We will solve this! And for experts - we have templates that make your daily multisig transactions easy. Save your time for more important things! Blockchain gives us a new sense of personal ownership. Now we also move into group ownership, DAO, cooperation, making decisions together with somebody, etc. We are developing MSIG app (https://msig.app/jungle), which helps both new and pro users to manage multi-signature transactions. 
Note, this is a Partial open-source project. Everything is open sourced, including smart-contract calls from FE extracted as a separate module at npmjs for easy reusage by other projects. Only the design of UI is a Closed Source.
- **Relationship to EOSIO:** It uses EOSIO system contracts. It is intended for daily usage by each EOSIO user who needs multi signatures, and this number of users is growing because of DAO and other collective-usage use cases.
- **Reason for Interest:** We are well-known experts in msig topic, creating dozens of complex msigs including starting a few EOSIO blockchains and the famous Jungle. So we saw the intersection of our expertise and the user's needs. In addition, we partnered with a great user-experience expert to make it look nice and simple to use.

### Project Details


Part of the work is already done. Please have a look at this screencast of the UX and you will be able to see our UI components and UX - https://drive.google.com/file/d/1LSUQGZhlpXDpeuYwc51OyMBK_0Edrn35/view?usp=sharing
You can also view the same on youtube here: https://www.youtube.com/watch?v=xLrGSM_VvcY

We use React for FrontEnd, it will be a web application at msig.app domain.
We have more Documentation and can provide it on demand.
What your project is_not_ or will _not_ provide or implement
  - This is an open question. We have a clear definition of what will be included in the 1st version of our app. But as for the next versions, it is not clear yet, because we also have feedback gathering and R&D phases in our roadmap (details below), so we will decide what else we include in this project later.

### Ecosystem Fit


- Where and how does your project fit into the ecosystem? 
Can be used for several use cases: 
1. For anybody, including novice users, who need to create msig transactions.
2. For experts that want to simplify their daily msig operations. We have templates.
3. We can predict some DAO-related cooperations, we already have an interest from DAO tools.
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
Potentially any EOSIO user who need msig transaction, and this number is groving because of DAO and other collective-usage use cases.
- What need(s) does your project meet?
Novice users need a simple tool to create their 1st msig, it is too complicated without our msig.app.
Experts need some tool to simplify their day-to-day msig operations, e.g. payments ect. We have templates for them
Even Experts have a hard time creating different complex msigs, our templates help them also.
DAO tools may use us in the future.
Our app makes EOSIO look more user-friendly, nice-looking interface, and also more professional for new users.
- Are there any other projects similar to yours in the EOSIO ecosystem?
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?
We do not know about similar projects in EOSIO ecosystem released yet. Users may use bloks.io for msigs or directly call smart contracts in a command-line style, etc. We've not done competitor analysis regarding other chains, but our partner user-experience designer has huge experience in related topics and probably did some analysis, we can continue this analysis in the next phases also.


## Team

### Team members

- **Team Leader:** Sudip Banerjee
- Steve Floyd
- Taras Kob
- Rost
- Danny
- and many others

### Legal Structure
- **Registered Legal Entity:** Fire Labs Limited
- **Registered Address:** Quijano Chambers, P.O. Box 3159, Road Town, Tortola, British Virgin Islands.

### Team Experience

For msig expertise: www.cryptolions.io - we are well-known experts in EOSIO msig topic, and took part in starting several EOSIO chains, including many complex msig work that is needed for this. We also have many other EOSIO products listed there.
For user-experience expertise: https://www.blocktower.app/ form https://www.linkedin.com/in/stevefloyds/ who has huge UX and design expertise.
For Front-end expertise: https://forages.studio/ E.g. https://arkinfernum.io/ and many other nice-looking and professionally executed web apps.
We have many other projects in our portfolio, we can provide on demand.

### Team Org Repos

- https://github.com/orgs/CryptoLions/repositories

### Team Member Repos

- https://github.com/Vilchynskyi
- https://github.com/stevefloyd
- https://github.com/TarasCL
- https://github.com/orange1337

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/vilchynskyi-roman
- https://www.linkedin.com/in/stevefloyds/
- https://www.linkedin.com/in/taraskob

## Development Status

Part of the work is already done. Please have a look at this screencast of the UX and you will be able to see our UI components and UX - https://drive.google.com/file/d/1LSUQGZhlpXDpeuYwc51OyMBK_0Edrn35/view?usp=sharing
- references to conversations you might have had related to this project with anyone from the EOS Network Foundation,
Yes, Sudip had a conversation in August with ENF and to very positive feedback and an invitation to ask for a grant.
- previous interface iterations, such as mock-ups and wireframes.
Yes, already mentioned above, duplicating here: https://www.youtube.com/watch?v=xLrGSM_VvcY

## Development Roadmap

### Milestone 1

- **Estimated duration:** 1.5 month
- **FTE:**  3.5
- **Costs:** 50,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | One of these: MIT / Apache 2.0 / GPLv3  |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can use our open-source module. |
| 0c. | Testing Guide | If necessary, the core functions will be covered by unit tests to ensure functionality and robustness. |
| 0d. | Docker | If necessary, we will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. But it may be not necessary because our open-source module is in the npmjs |
| 0e. | Article | We will publish an **article**/workshop that explains what was done/achieved as part of the grant. (Content, language and medium should reflect your target audience described above.)
| 1. | The open-source npmjs module (and code) and all the rest Front-end code and design etc. | This can be reused by anybody to create similar projects. The calls from UI to the system smart-contracts will be wrapped in npmjs module so it should be even easier to reuse. |  
| 2. | Released web application on www.msig.app | User can create, save (for future reuse), and export msigs in a step-by-step user-friendly manner for the next 7 tx types (templates): Custom Transaction; Transfer Token; Deploy Contract; Change Permissions; Vote for a BP; Buy / Sell RAM; Delegate CPU / NET  |  

## Future Plans

We plan to maintain the app and gather feedback from users and then later maybe add new features based on that feedback and also based on our RnD and expertise. Also, we plan to promote the app through Twitter and through our communities. And also do some level of user support as we do for the rest of our projects (e.g. kolobok.io).

## Additional Information

**How did you hear about the Grants Program?** Twitter, and also directly from ENF member

- Previous grants you may have applied for.
We got ENF Recognition Grant for Jungle Testnet, here is the respective tx: https://bloks.io/transaction/c1530324d1da4cf894e21a667521351a7ad7a8ec879b3add65fa5d4b95089e68?tab=traces
