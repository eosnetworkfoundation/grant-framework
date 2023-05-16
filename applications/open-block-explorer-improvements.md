# EOS Network Foundation Grant Proposal

- **Project Name:** Open Block Explorer Improvements
- **Team Name:** Detroit Ledger Technologies
- **EOS Payment Address:** detroitfunds
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 2
- **Pomelo Grant(s):** https://pomelo.io/grants/obeconfig, https://pomelo.io/grants/eosexplorer, https://pomelo.io/grants/smartcontrac, https://pomelo.io/grants/nodesuiteimp
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/FACINGS/collection-manager


## Contact

- **Contact Name:** Adam Zientarski
- **Contact Email:** adam@detroitledger.tech
- **Website:** https://detroitledger.tech


## Project Overview

### Overview

- **Name:** Open Block Explorer Improvements
- **Brief Description:** Open Block Explorer (OBE) is an open source block explorer serving the Antelope ecosystem. The goal of this grant is to develop most of the remaining features needed to bring Open Block Explorer to feature parity with the most mainstream block explorer, Bloks.
- **Relationship to EOS Network / Antelope:** Block Explorer / Block Producer
- **Reason for Interest:** Detroit Ledger Technologies began as a pre-launch block producer candidate on EOS. Over the years, we have witnessed the various closed source block explorers being launched only for those platforms to gradually degrade in quality as the contributions that voters valued shifted and maintaining those platforms became unprofitable and burdensome.


### Project Details

**Mock-ups/designs of any UI components**

The mockups for the custom name portal with EOS branding can be found here: https://www.figma.com/file/qN1INaxvwed8HoEgJpqCJs/OBE?type=design&node-id=401-650&t=UCpfxuwWbShTijuJ-0

The create account view will be inspired by the create account view page on Bloks found at the following links:
Simple view: https://bloks.io/wallet/create-account
Advanced view: https://bloks.io/wallet/create-account/advanced 

**An overview of the technology stack to be used**

Open Block Explorer uses VueJS/Quasar and Typescript.

Open Block Explorer relies on Hyperion and Antelope RPC to display chain data. OBE also will also use a custom indexer developed by the Telos Network that may need to be modified to aggregate EOS chain statistics. Currently no pages use this indexer to display data. DLT will commit to hosting the indexer for the EOS network.


**Documentation of core components, protocols, architecture, etc. to be deployed**

The following functionality will be deployed to a multichain block explorer. The team suggests it is hosted at https://explorer.antelope.io. If that is not possible the team will acquire another domain.

*Adding a view/page for a user to create an account and pay the fee from an existing* account.
- Simple mode
- Advanced mode

*Adding an interface for viewing, searching, and placing bids on custom account names*
- Current list of bids
  - Only needs to be the top 50 as opposed to all outstanding name bids since only the highest bid is awarded.
  - Current examples are clunky.
  - List when bid was placed.
- Timer showing when the current auction concludes and list the date/time in plaintext.
- Name availability lookup
 - Easily search any name and get a quick response on availability.
   - Taken
   - Available
- Show currently owned names and make creating the account streamlined (leverage new Create Account UI).

*Adding an interface for wrapping and sending tokens across Antelope chains using IBC*

*Cross reference transactions to the other chains of that same transaction within OBE and provide a link to the transaction on the opposite network.*


**PoC/MVP or other relevant prior work or research on the topic**

The Telos only version of Open Block Explorer can be found at: https://explorer.telos.net

**What your project is _not_ or will _not_ provide or implement**

This proposal will not implement Wharfkit because most of the work that needs to be performed has already been completed by Greymass - https://github.com/telosnetwork/open-block-explorer/pull/646

However, the team will make UI adjustments needed to accommodate the Wharfkit integration.


### Ecosystem Fit

**Where and how does your project fit into the ecosystem?**

A reliable block explorer that both displays accurate transaction data and provides users of varying skill levels with quality of life functionality that makes interacting with system level smart contracts a breeze has been lacking from the ecosystem. This grant seeks to add some of the missing features that are required to reach feature parity with Bloks.io as well as new tools that leverage the recent IBC addition to Antelope. Being that the explorer is open source, it can be maintained by a greater pool of community members and the EOS network will never be without an option for a block explorer.


**Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**

The end-user target audience is EOS ecosystem users at large. The overall designs and implementations need to be simple enough for newer or less technical users, but also offer some advanced views for power users. Another large target audience for the platform is dapps/dapp developers to form partnerships for the Dapps to link out to transaction and account information on the EOS version of OBE as opposed to existing block explorers.

**What need(s) does your project meet?**

Currently, Open Block Explorer is one of two open source block explorers in the Antelope ecosystem.Of those two OBE is the more feature rich, offering various tools to interact with the chain rather than only displaying high level network data.

By having an open source solution, actors in all of the Antelope networks can contribute, significantly lowering the resources per network required to maintain a vital tool going forward.

**Are there any other projects similar to yours in the EOS Network ecosystem?**

There has historically been a number of block explorers in the ecosystem that are maintained to varying degrees. Only one of the following block explorers is open source.


*Bloks.io*<br>
Bloks has historically been the go-to block explorer for the Antelope ecosystem. The block producer team that created Bloks was acqui-hired by Metallicus. As the Metallicus team shifted their engineering focus to other products, Bloks gradually fell into disrepair. Various basic functionality such as paginating/filtering account transactions, vote totals, and signing/executing multi-sigs work in a limited or inconsistent manner across various chains because of a failure to maintain updated api endpoints. Despite this, Bloks still continues to see significant usage. The project is not open source.

*EOS Authority*<br>
The second most used block explorer is provided by EOS Authority. This block explorer is perhaps the most feature rich of all of the block explorers and does some things better than Bloks. For example, its custom name bidding interface is much easier to use than Bloks. This block explorer is not open source and receives an inconsistent level of maintenance.

*Antelope Tools*<br>
The other open source block explorer on the market, Antelope Tools by Edenia, is a newer block explorer that focuses on block producer tools and information. This includes statistics around block producer pay, number of block producers out of compliance, a bp.json generator and more. The actual block explorer on Antelope Tools, while from a design is an improvement over more commonly used block explorers, lacks various expected functionality. For example, account lookups only provide a limited snapshot of information, no history, and no way to actually execute actions such as voting for block producers, executing smart contracts, and more.

*EOSQ*<br>
This powerful block explorer functions the best of the popular block explorers when it comes to querying, however it lacks the ability for users to interact with smart contracts. The UI code can be improved by displaying the transaction information closer to how Bloks and EOS Authority display it. EOSQ also relies on dfuse, a history solution which is more demanding and costly to support compared to hyperion.

*EOSX*<br>
The platform has some unique features when compared to its competitors such as token swaps and Defi pools for Antelope native tokens (VIG, etc). The team behind EOSX also solves user experience learning curves in a practical way by providing guides on how to perform certain functions. The platform also supports a large number of Antelope networks. EOSX falls short on its UI/UX to other explorers.

*EOS Flare Explorer*<br>
Another simple explorer, the only difference of note is that some of the stats that it displays on the home page such as RAM price relative to EOS or liquid vs staked EOS, voted vs not voted EOS, etc. This explorer is rarely used.

*EOS Tracker*<br>
EOS Tracker displays slightly more information that some of the other rudimentary explorers in the list, but various information on the website is incorrect and some features, such as the list of most recent actions associated with account on the account profile page do no work, indicating that the website is sparsely maintained.

*Miscellaneous*<br>
There are additional block explorers on other chains in the ecosystems. DLT believes these explorers can be used for inspiration and are highly unlikely to offer an EOS explorer in addition to their native chain. For example, WAX’s block explorer that was developed in-house, https://waxblock.io.


## Team

### Team members

- **Team Leader:** Adam Zientarski
- **Advisor:** Jesse Schulman
- **Engineering Manager:** Karyne Mayer
- **Senior UI/UX Engineer:** Elton Pongilo
- **Senior UI/UX Engineer:** Alexandre Santos
- **Senior UI/UX Engineer:** Eduardo Jaeger


### Legal Structure
- **Registered Legal Entity:** EOS Detroit, Inc.
- **Registered Address:** 1570 Woodward Ave. FL 3 Detroit, MI 48226

### Team Experience

Throughout its history as a block producer, Detroit Ledger Technologies has built or contributed to a number of network-focused applications. These projects have included the WAX OIG Election Portal, WAX Labs, Telos RFP, and more. DLT has spent the last year contributing to Open Block Explorer by building various features such as the multi-signature interface for power users, providing design work for future features, bug fixes, and other minor improvements.

DLT also participated in the FACINGS NFT Collection Manager Stage 1 under the legal name FACINGS INC. by providing the UI/UX designs and some of the frontend engineering work for the project. Elton Pongilo was the designer and he is also participating in this proposal as a designer and engineer.

Prior to joining the Web3 space, DLT’s engineering team worked at a wide variety of firms, from startups to Fortune 500 companies such as Hewlett-Packard (HP).

During Season 4 of Pomelo, DLT submitted two grant applications that were related to Open Block Explorer (one for multi-chain functionality and the other infrastructure). These grants were underfunded due to their late submission. Those Pomelo grants can be found at the beginning of this submission. During Season 6 of EdenOnEOS, Adam Zientarski was elected to a Level 1 Delegate position on the campaign platform of using funding awarded to finish the work required for finishing the multi-chain functionality and to update the branding for the EOS portal in the block explorer. The approximately 1200 EOS from the Pomelo grants and 3250 EOS awarded from EdenOnEOS was used towards this work.


### Team Org Repos

- https://github.com/eosdetroit
- https://github.com/eosdetroit/nodesuite
- https://github.com/telosnetwork/telos-rfp, https://github.com/telosnetwork/telos-rfp-ui
- https://github.com/worldwide-asset-exchange/wax-labs-ui
- https://github.com/eosdetroit/govboard


### Team Member Repos

- Adam Zientarski: N/A
- Jesse Schulman: https://github.com/poplexity
- Karyne Mayer: https://github.com/karynemayer
- Elton Pongilo: https://github.com/pongilo
- Alexandre Santos: https://github.com/AlexandreSSJr
- Eduardo Jaeger: https://github.com/jaegerfe


### Team LinkedIn Profiles (if available)

- Adam Zientarski: https://www.linkedin.com/in/adamzientarski/
- Jesse Schulman: https://www.linkedin.com/in/jesse-schulman/
- Karyne Mayer: https://www.linkedin.com/in/karyne-mayer/
- Elton Pongilo: https://www.linkedin.com/in/pongilo/
- Alexandre Santos: https://www.linkedin.com/in/alexandressj/
- Eduardo Jaeger: https://www.linkedin.com/in/eduardofjaeger/

## Development Status

The Telos only version of OBE is deployed in production at https://explorer.telos.net

Development work on finalizing multi-chain functionality, refactoring hard coded variables, and EOS network branding is already underway. The URL routing is currently being upgraded. The first pull requests for finishing multi-chain functionality can be found here: https://github.com/telosnetwork/open-block-explorer/pull/692, https://github.com/telosnetwork/open-block-explorer/pull/698

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 50,000 USD


### Milestone 1 — Custom Name Portal

- **Estimated duration:** 2 months
- **FTE:**  2 FTE
- **Costs:** 33,333.22 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic written and video tutorial that explains how a user can perform the create account and custom name portal functionality. The documentation on how to deploy OBE is already available in the public repository and the team will add any needed updates. |
| 0c. | Testing Guide | Documentation of the intended functionality/outcomes of each feature subset will be provided. Robust error messages will be provided in the UI/UX as a part of the milestone. Unit tests will be written in Jest. |
| 1. | Frontend / User Interface | Create Account (1 sprints) <uL><li>Simple view: https://bloks.io/wallet/create-account</li><li>Advanced view: https://bloks.io/wallet/create-account/advanced</li></ul>  |
| 2. | Frontend / User Interface | Custom Name Portal (3 sprints) <ul><li>Current list of bids</li><ul><li>Probably only needs to be the top 50 as opposed to all outstanding name bids since only the highest bid</li><li>Current examples are clunky</li><li>List when bid was placed</li></ul><li>Timer showing when the current auction concludes and list the date/time in plain text</li><li>Name availability lookup</li><ul><li>Easily search any name and get a quick response on availability</li><ul><li>Taken</li><li>Available</li></ul></ul><li>Show currently owned names and make creating the account streamlined (leverage new Create Account UI)</li></ul> |


### Milestone 2 — IBC Tools & Information

- **Estimated Duration:** 1 month
- **FTE:**  2 FTE
- **Costs:** 16,666.66 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic written tutorial that explains how a user can perform the create account and custom name portal functionality. The documentation on how to deploy OBE is already available in the public repository and the team will add any needed updates. |
| 0c. | Testing Guide | Documentation of the intended functionality/outcomes of each feature subset will be provided. Robust error messages will be provided in the UI/UX as a part of the milestone. Unit tests will be written in Jest. |
| 0d. | Article | We will publish an article that explains the new account creation, custom name portal, and IBC Tools functionality and how they came to be with support from the ENF. |
| 1. | Additional UI functionality | IBC Tools and Information - Adding an interface for wrapping and sending tokens across chains using IBC - Cross reference transactions to the other chains of that same transaction within OBE and provide a link to the transaction on the opposite network. |

## Future Plans

In the short term, the best thing that we can do to increase awareness of multi chain OBE is to partner with Dapp developers to link to OBE for referencing transaction metadata or network accounts from within their platform (similar to how AtomicHub links off to account pages on waxblock.io from the header of the AtomicHub user profile). Driving traffic to the general explorer and having the ability to demonstrate substantial traffic will allow the explorer to be monetized through banner ads and other sponsorship sales. We envision that the proceeds from multi chain will be split between reinvesting in maintaining OBE through capitalizing decentralized entities on each network via a consortium model (i.e. Eden On EOS “Circles”, etc.) which will continue to contribute to development of OBE and/or fund additional projects.

The Telos Core Development (TCD) team is also committed to providing the resources to maintain the Open Block Explorer in the long-term, as well as provide funding for new features and enhancements as time allows. Detroit Ledger Technologies will continue to support the Open Block Explorer initiative in coordination with the TCD. A number of other features have been added to the future roadmap, such as RAM pricing / historical RAM pricing, robust chain history exports, EOS PowerUp, Proxy Portal, CI/CD updates, Enhanced Block Producer Profiles, additional language support, and more!


## Additional Information

**How did you hear about the Grants Program?** 

DLT has previously submitted a grant. Most likely the original announcement through Twitter.

**What has your team already contributed to the project?**

DLT has contributed to the development of Open Block Explorer in some manner for the past year. The teams contributions are as follows:
- Multisig Proposal Portal (Creation/View/Sign/Execute)
- Ongoing maintenance and bug fixes 
- Finish multi-chain functionality (Pt. 1 complete, URL routing improvements in progress)
- EOS explorer branding UI update
