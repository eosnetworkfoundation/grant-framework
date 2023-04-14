# EOS Network Foundation Grant Proposal

- **Project Name:** Jungle Testnet Ecosystem
- **Team Name:** CryptoLions (Fire Labs Limited)
- **EOS Payment Address:** cryptolions1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/EOS-Jungle-Testnet

## Contact

- **Contact Name:** Sudip Banerjee (CEO), Artem Radchenkо (PO/PM)
- **Contact Email:** roar@cryptolions.io
- **Website:** https://cryptolions.io




## Project Overview

### Overview

- **Name:** Jungle Testnet Ecosystem. Stage I

- **Brief Description:** Jungle Ecosystem — is a next stage, a higher level of interaction and infrastructure, that can be built on top of and around the Jungle Testnet to provide proper UX, support and development to existing EOS community and newcomers, encourage BPs and contributors, meet new partners and colleagues. The final product will help onboard people easier, build teams and projects much faster and efficiently, test new theories and rate the work of others in a more fun and comfortable way. As a new offering we see more than one “branches” of Jungle Testnet. And a big part of the Ecosystem will take new web-application, provided instead of outdated Jungle Monitor. Read mode in the Google Presentation: https://docs.google.com/presentation/d/1L4DUnPQO4oxTccsR8J6dqt7R5wsfdIPrRoQGXrsmWRI/edit?usp=sharing (the access is/will be provided to the ENF Committee members).

- **Relationship to EOSIO:** The Jungle Testnet was initiated by CryptoLions and has served as a sandbox for many dev teams and Block Producers since the birth of EOS. It played a cornerstone role in the EOS launch and now as the network matures and grows it provides a reliable test environment for EOS-based dapps. Many critical errors have been found and fixed in Jungle before they could make their way to the mainnet, and many EOS dapps and features were developed and tested there.

- **Reason for Interest:** CryptoLions Team, is an EOS block-producer and developer from the EOS beginning. In 2018 we launched the initial version of Jungle Testnet, one of the first testnets on EOS, and made it available to the community. We constantly contribute our effort, and as a result the 4th version of the Jungle was released recently. We are glad to have a lot of supporters who join our path and we have an ambitious plan to extend Jungle brand to Jungle Ecosystem. We hope you see the value of what we are doing and consider the possibility of giving us a grant for the development of the Jungle Ecosystem. Our goal is to create a finished modern product, aligned with ENF strategy and EOS mainnet updated vision, to make the ecosystem as self-sufficient as possible, but we understand that we cannot sustain the project financially alone. Therefore, **we seek long-term cooperation and support from ENF to bring this product to the EOS community**.


### Project Details

**Mock-ups/designs of any UI components**

Links to the Figma wireframes and description of the sub-projects provided in the presentation (see link in the ​​Brief Description).

**Data models of the core functionality**

Work on the detailed data model will be done at the beginning of Milestone 1. We plan to use email as the user ID in My Jungle; it will simplify onboarding new people. To store data, we will use a database and also utilize tables in smart-contracts on Jungle “branches” (for short-term storage of test assets) and on the EOS Mainnet (for long-term storage of ecosystem assets).

**API specifications of the core functionality**

During Stage I, we will not provide any new API or API specifications, except for those that already exist (such as the SimpleAssets API on new Jungle "branches").

**An overview of the technology stack to be used**

Antelope software for Jungle Testnet “branches”. MongoDB and smart-contract tables to store data. C++ for smart-contracts. HTML, CSS, JS and ReactJS, Redux for the frontend. There is no static decision on programming language and framework for the backend. Possibly it will be NodeJS, if so then Passport.js that helps to develop authentication using a username and password, Facebook, Twitter, and more. SendGrid, Mailerlite or Mailgun to send notifications and informational emails, and probably promo emails in the distant future. Matomo (or GA) and Hotjar (or Sentry) for UX analytics. Also can be used AWS or Hetzner for hosting and Docker for containerization. SimpleAssets on EOS Mainnet to create/mint on demand Animal NFTs and Jungle NTTs.

**Documentation of core components, protocols, architecture, etc. to be deployed**

At the end of Stage I, we will create basic documentation that describes main functionality developed during this stage, in order to cover key workflows.

**PoC/MVP or other relevant prior work or research on the topic**

We have already established proof of concept with the existing version 4 of Jungle and the Jungle Monitor at https://monitor4.jungletestnet.io/. However, we see opportunities for further improvements, based on received feedback from EOS and Jungle communities. In addition, we have some functionality in mind that we plan to develop during Stage III, if we receive the necessary grant in the future — we are going to show the MVP during the call with ENF Grant representatives.

**What your project is _not_ or will _not_ provide or implement**

During Stage I, our focus is on creating the core features of "My Jungle" and implementing "branches" and access to them. After this stage, we plan to apply for grants to further maximize and improve the efficiency of the Jungle Ecosystem, as well as add new features to achieve our goals of managing test accounts, expanding useful functionality for developers, and implementing "gamification" to improve networking and work relationships within the EOS and Jungle communities. We will not provide or implement anything beyond the scope of Stage I within the estimated cost of development. However, we are open to considering additional proposals for Stages II or III. Maintenance of the developed software will not be provided at the expense of funds received under this grant (we will submit a separate application).


### Ecosystem Fit

**Where and how does your project fit into the ecosystem?**

Jungle Ecosystem will complement the EOS Ecosystem by simplifying workflows for developers and testers. In addition, it can be a useful tool for onboarding newcomers who want to understand how EOS works, but are not yet ready to purchase EOS tokens or spend on RAM and CPU. The concept of having multiple "branches" of Jungle blockchains can help to separate daily tests made by dapp developers from stress tests by block producers, among other operations, and simplify the overall smart-contract operations for everyone involved.

**Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**

Our main target audience for Jungle Ecosystem includes EOS dapp developers and testers, as well as stakeholders who have invested in these dapps and are looking to find an employer or colleague. Our secondary target audience includes any specialist familiar with other Antelope-based blockchains. We believe that the assets of the Jungle Ecosystem being on the EOS Mainnet will make it easier to onboard developers who have not yet worked on the EOS blockchain. This presents an opportunity for ENF to gain developers from other chains as well, using the Jungle Ecosystem as a "bridge".

**What need(s) does your project meet?**

Testing fast in a comfortable way, creating and managing test wallets easier than it's possible now, generating test assets, etc. (Stage I). More needs we can cover in Stage II and Stage III under separate grants (see description of Stages II and II in the presentation).

**Are there any other projects similar to yours in the EOSIO ecosystem?**

There is no project that offers the concept of testnet "branches" under one product or a comprehensive testnet ecosystem.




## Team

### Team members

- **CEO:** Sudip Banerjee
- **CTO:** Bohdan Kossak
- **PO/PM:** Artem Radchenkо
- **Tester:** Taras Kob
- **DevOps:** Andrii Bobrovych and Oleksii Zhukov 
- **Smart-contract Developer:** Olexiy Nahornyak
- **Frontend Developer:** TBD
- **Backend Developer:** TBD
- **Copywriter (part-time):** TBD
- **Technical Writer (part-time):** TBD
- **Community Manager (part-time):** TBD
- **Illustrator (part-time):** TBD

### Legal Structure

- **Registered Legal Entity:** Fire Labs Limited
- **Registered Address:** Quijano Chambers, P.O. Box 3159, Road Town, Tortola, British Virgin Islands.


### Team Experience

The CryptoLions team has experience and expertise in the blockchain industry. We have successfully launched and maintained block production nodes for various chains on the Antelope (EOSIO) software, including EOS. Additionally, we have developed and launched several own dapps, such as MSIG.app, the NFT game "Kolobok Adventures", NFT MarketPlace, NFT Tools, Redemption Bank and others. 

We have collaborated with industry leaders on several EOS blockchain projects and provided consultation and code-review for various EOS and Antelope projects. The CryptoLions team consists of members with extensive experience across multiple fields and technologies. Since 2018, we have been active in the EOS and Antelope (EOSIO) communities, continuously working to improve our experience and the blockchain industry in general.

Moreover, our team takes pride in developing the first NFT standard for EOS, SimpleAsset and maintain Jungle Testnet during years, the testnet where ENF perform its tests https://medium.com/eos-network-foundation/eos-evm-launches-on-jungle-testnet-with-full-ethereum-and-rpc-compatibility-f741485b5577.

The CryptoLions team played a key role in identifying a critical issue on the EOS Mainnet just a few days before its launch. Specifically, the Jungle Testnet had crashed instead of the EOS Mainnet. This incident was documented by the EOS Metal team in their blog (https://medium.com/coinmonks/thats-how-we-broke-jungle-testnet-twice-in-a-row-eleven-days-before-1-0-eosio-release-ef996495df). After the EOS launch, there were 2-3 occasions when the Jungle Testnet was disrupted and crashed instead of the EOS Mainnet (for example canceled deferred transactions, found by the WeCan team). During these incidents, the CryptoLions team was actively involved in testing, communication and investigating the causes of the problems.



### Team Org Repos

- https://github.com/CryptoLions
- https://github.com/EOS-Jungle-Testnet


### Team Member Repos

- https://github.com/jtf420 - Sudip Banerjee
- https://github.com/ansigroup - Bohdan Kossak
- https://github.com/rskaskiw - Roman Skaskiw
- https://github.com/po-pm - Artem Radchenkо
- https://github.com/TarasCL — Taras Kob


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/sudipbanerg/ - Sudip Banerjee
- https://www.linkedin.com/in/bohdan-kossak-a25b722/ - Bohdan Kossak
- https://www.linkedin.com/in/roman-skaskiw-300a6671/ - Roman Skaskiw
- https://www.linkedin.com/in/andriibobrovych/ - Andrii Bobrovych
- https://www.linkedin.com/in/artemradchenko/ - Artem Radchenkо
- https://www.linkedin.com/in/taraskob — Taras Kob
- https://www.linkedin.com/in/oleksiyzhukov — Oleksiy Zhukov




## Development Status

Currently, we have spent time gathering feedback from the EOS and Jungle communities to understand their needs and wishes for the existing EOS Testnet (Jungle). We have prepared a Jungle Ecosystem concept, which is presented in our proposal (see presentation), and created initial wireframes to estimate the approximate time and cost of development. 

We divided our development plan for the ecosystem into three stages: Stage I — "Core", Stage II — "Pro", and Stage III — "Extended". Also we moved the budget for maintenance, BPs rewards, and promotions to individual grant applications.

This application was written to get grant funds for the Stage I (“Core”).

Additionally, we have also created an MVP for one of the ecosystem's sub-products, which we would like to develop in Stage III ("Extended"), in case if we receive the necessary grant for that stage (please find description and the link in the presentation).




## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 8 months 
- **Full-Time Equivalent (FTE):** 6.5 FTE
- **Total Costs:** 150,000 USD


### Milestone 1 — Initial implementation of the Jungle "branches", detailed planning, UI/UX design

- **Estimated duration:** 2 month
- **FTE:** 4 FTE
- **Costs:** 50,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | No documentation on this milestone |
| 0c. | Testing Guide | No testing guides on this milestone |
| 0d. | Docker | No Docker files on this milestone |
| 0e. | Article | We will publish a post or an article that explains what was done/achieved as part of the 1st milestone after getting this part of the grant to inform EOS and Jungle Communities. A draft of the post/article will be coordinated with ENF before publication |
| 1. | Detailed planning, UI/UX | We will work on detailed planning and UI/UX, based on the initial ideas and wireframes |  
| 2. | Jungle Style Guidelines | We will work on a new Jungle logo, style guides (as shown in the presentation), and guidelines for UI, illustrations, and visual language overall to make the Jungle Ecosystem look more modern and fresh |  
| 3. | "Branches" | We will start setting up infrastructure for "branches" |  
| 4. | Jungle BPs | We will begin working on the framework for BPs  |  
| 5. | Illustrations, icons, NFTs and NTTs | We will begin work on illustrations, icons, and images for NFTs and NTTs |   
  


### Milestone 2 — Initial implementation frontend, backend, etc.

- **Estimated duration:** 3 month
- **FTE:** 6.5 FTE
- **Costs:** 50,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT  |
| 0b. | Documentation | We will start writing basic documentation |
| 0c. | Testing Guide | No testing guides on this milestone |
| 0d. | Docker | No Docker files on this milestone |
| 0e. | Article | We will publish a post or an article that explains what was done/achieved as part of the 2nd milestone after getting this part of the grant to inform EOS and Jungle Communities. A draft of the post/article will be coordinated with ENF before publication |
| 1. | Frontend | We will begin implementing the UI/UX in code, based on the designs from milestone 1 |  
| 2. | "Branches" | We will connect the frontend with the "branches" |  
| 3. | Jungle BPs | We will continue working on the framework for BPs and start developing a Discord bot to test it  |
| 4. | Illustrations, icons, NFTs and NTTs | We will continue working on illustrations, icons, and images for NFTs and NTTs |   
| 5. | Backend | We will start developing the backend for the functionality designed in milestone 1  |  



### Milestone 3 — Completion work of Stage, testing, preparation for launch

- **Estimated duration:** 3 month
- **FTE:** 6.5 FTE
- **Costs:** 50,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT  |
| 0b. | Documentation | We will finalize work on writing basic documentation for this milestone |
| 0c. | Testing Guide | We will work on testing guides for this milestone |
| 0d. | Docker | We will provide a Dockerfile for this milestone |
| 0e. | Article | We will publish a post or an article that explains what was done/achieved as part of the 3rd milestone after getting this part of the grant to inform EOS and Jungle Communities. A draft of the post/article will be coordinated with ENF before publication |
| 1. | Frontend | We will finalize work on the frontend and test it |   
| 2. | Jungle BPs | We will finalize work on the Discord bot and test it |   
| 3. | Illustrations, icons, NFTs and NTTs | We will finalize work on illustrations, icons, and images for NFTs and NTTs |   
| 5. | Backend | We will finalize work on the backend and test it |    



## Future Plans

As part of Stage I, our plan is to launch the web app and gather user feedback. We will prioritize fixing critical issues, and based on the feedback and our R&D and expertise, we may (or may not) include them into the next grant applications.

Once we have completed our obligations for Stage I and received the final tranche of the grant, we will apply for grants for Stage II and Stage III to further develop the ecosystem into a more comprehensive platform (to make the ecosystem more like an “ecosystem” with more than one app).

We will also apply for grants to cover cost of the first year of maintenance, rewards for BPs (see presentation) and promo (promo is optional, if ENF can promote Jungle Ecosystem we would be happy, or we need a grant to do that on our side to pay for paid ads in SM, creation of images, texts, etc.).




## Additional Information

**How did you hear about the Grants Program?**

ENF Social Media channels, directly from ENF member

**Previous grants you may have applied for**
- In 2021 was received the "ENF Recognition Grant" for Jungle Testnet, see this tx: https://bloks.io/transaction/c1530324d1da4cf894e21a667521351a7ad7a8ec879b3add65fa5d4b95089e68?tab=traces
- In December 2022 we applied for a grant for MSIG.app, and this grant was rejected: https://github.com/eosnetworkfoundation/grant-framework/actions/runs/3687536834
