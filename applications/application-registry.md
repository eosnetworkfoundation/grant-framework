# EOS Network Foundation Grant Proposal

- **Project Name:** Application Registry
- **Team Name:** Rewired.one
- **EOS Payment Address:** rewired11111
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** https://pomelo.io/grants/keyproof
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/Rewired-one/Application-Registry

## Contact

- **Contact Name:** DJ Kruitbosch
- **Contact Email:** dj@rewired.one
- **Website:** https://www.rewired.one

## Project Overview

This grant request is in response to the Wallet+ Blue Paper section titled: Application Registry.

### Overview

- **Name:** Application Registry
- **Brief Description:** The Application Registry is an on-chain repository of applications available on the EOS Mainnet. It will provide input to wallets and other applications to increase user experience and enhance security, including the associated governance. Four main deliverables are part of this project: 1) On-chain Application Registry (smart contract), 2) Indexing Service, 3) Web Application.
- **Relationship to EOSIO:** No common Application Registry exists today for EOS Mainnet. This project will create a common Application Registry,and an interface that can connect to EOS Mainnet (and in the future to other EOSIO chains as well)  in order to query the applications.
- **Reason for Interest:** Rewired.one has been building and successfully implementing EOSIO solutions into large businesses for more than 2 years. We have partnered with community projects, implementers and block producer teams during this time. We have an active Pomelo Grant open for Keyproof, our Enterprise Signing Portal, which would also have an element of an Application Registry.

### Project Details

The project would deliver the following three elements of the Application Registry; the registry itself, an indexing service and a web frontend.

One of the first tasks will be to  come to consensus between EOS mainnet wallets on what data is to be stored in the Application Registry and how this would be presented back to the wallets.

These data standards have to be defined first, in order to have a clear way forward.

We need to agree on:
- What app data to capture and store in the registry
- What are the specifications of the app manifest
- What activity metrics will be gathered from the applications and their associated EOS accounts
- What contract name will we use (blue paper recommends eosio.apps)
- Who will be the gatekeepers/validators of the app updates

Suggested wallet providers, who will be asked to put forward a representative::
- Anchor
- Wombat
- Tokenpocket
- (Unico)

Once we have these defined, we can start building the actual smart contract. Initially the app manifests and graphics will be stored either in externally hosted sites or on IPFS, but this can later be further enhanced by adding the Asset Hosting and Asset Proxy service as described in the Wallet+ Blue Paper.

The indexing service will put the indexes in place to give insights into the data stored on the Application Registry. In addition it will show activity metrics for the accounts associated with the applications in order to show usage metrics.

The last part of the project will build the Frontend, which will focus on the three different users: application developers, administrators/validators and end users.

While application developers can submit, update and delete their apps, administrators/validators will be the ones validating the information and confirming that all data is valid, the rules are adhered to and that the app can be published/updated. The end users will be able to browse the Application Registry pretty much like an app store, where different application categories can be browsed, where data from the Application Registry and Indexing Service will be displayed. The Frontend will be built using React.js.

Some initial documentation and design thoughts have been put together in [this document](https://github.com/Rewired-one/Application-Registry/blob/c6850763b8d65e800f5a07d092174e5b5e9366a0/docs/grant-supplemental-information.pdf).

### Ecosystem Fit

- The Application Registry is a true added value for EOS Mainnet and for later inclusion into the wider EOSIO ecosystem
- Target Audience: EOS Mainnet wallet and application developers, but also EOS Mainnet users
- The need for the Application Registry was defined as part of the Wallet+ Blue Paper and to our knowledge, no other project teams are working on this


## Team

### Team members

- **Team Leader:** Torbene Anderson
- Rewired.one Sponsor: Torben Anderson
- Advisory Lead: Brendon Ross
- Business Analyst Scott Owen (TBC)
- Blockchain Developer: Ian Docolin (TBC)
- Smart Contract Developer: Erick Casanova (TBC)
- Frontend Developer: Collin Wang (TBC)
- Lead Project Manager: DJ Kruitbosch


### Legal Structure
- **Registered Legal Entity:** Consulting Rewired Limited
- **Registered Address:** 63/66 Hatton Garden, Fifth Floor Suite 23, London, EC1N 8LE


### Team Experience

The Rewired.one team has been involved with EOSIO since its founding in 2018. We developed the worker proposal system for Telos where we worked for Douglas Horn. We helped Ashe Oro on the TokenYield product for almost a year and we have now been working almost two years with Emanate, a Music3 platform built on EOS Mainnet. We work with both Startups and Enterprise Clients to build solutions that fit their needs, which include E2E Project Management, Consulting, Solution Architecture, Design through to  implementation, including Smart Contract development and private Blockchain implementations for enterprise. For that matter we also contributed to the Core+ Bluepaper where we took ownership of the Enterprise section.


### Team Org Repos

- https://github.com/Rewired-one
- https://github.com/Emanate-official
- https://github.com/modadao
- https://github.com/eosphere/heyfio


### Team Member Repos

- https://github.com/torbenanderson
- https://github.com/interwebcoding
- https://github.com/IanMendozaJaimes
- https://github.com/tlacloc
- https://github.com/superstar391
- https://github.com/djkruitbosch


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/torbenanderson1/
- https://www.linkedin.com/in/interwebcoding/
- https://www.linkedin.com/in/ian-mendoza-jaimes/
- https://www.linkedin.com/in/erick-alejandro-casanova-cort%C3%A9s-2a549010a/
- https://www.linkedin.com/in/collin-wang-1362a51b0/
- https://www.linkedin.com/in/djkruitbosch/


## Development Status

- No development work has started as of this submission
- EOS Wallet+ Blue Paper
- Grant proposal reviewed by Greymass team, pre-requisites for further development will be captured under Milstone 1
- Grant route followed after discussion with and recommendation by Yves


## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 16 weeks 
- **Full-Time Equivalent (FTE):**  2.4 FTE
- **Total Costs:** 229,000 USD
- 

### Milestone 1 — Initiate Project & Agree on governance structure and Application Registry metadata

- **Estimated duration:** 3 weeks
- **FTE:**  0.9
- **Costs:** 18,081 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | License | MIT |
| 2. | Project Governance setup | Team setup, governance setup, stakeholder mapping complete. |
| 3. | Governance agreement | Agreement on how the EOS Mainnet will provide governance on how Application developers can register their applications into the Application Registry. This includes a list of validators who will ensure that apps are following the defined rules.
This also defines the rules that apps have to comply with, what metrics they have to support/report and how the app can be updated or deleted.
Part of the governance will also consider user input based on their experience with apps. If an app is not behaving as per guidelines, it can be reported.
We propose to use a 3/5 multisig with a dedicated governing body. We suggest these are the following entities: greymass, tokenpocket, ENF, ultra and rewired.
Part of this deliverable we will also define the application data standards, such as title, description, category, icon, URL, app manifest, etc. |


### Milestone 2 — Build Application Registry

- **Estimated Duration:** 15 weeks
- **FTE:**  1.2
- **Costs:** 106,081 USD *

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide documentation as part of the source code and a handbook on how wallet or application developers can use the Application Registry smart contract. It will contain how to build and deploy the code, how to interact with the contract, how to use EOSJS. |
| 0c. | Testing Guide | We will provide automated Smart Contract test cases using DUNE. |
| 1. | Application Registry (Smart Contract) | The Smart Contract will be built in such a way that it considers the governance as defined in an earlier step and will allow the Application metadata to be stored on-chain. The Smart Contract will be designed to be deployed on any EOSIO chain. |  

* Additional sub-milestones may be required to support effective cash flow for the project team


### Milestone 3 — Build Application Registry

- **Estimated Duration:** 7 weeks
- **FTE:**  0.5
- **Costs:** 23,783 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide documentation on the available indexes and what data is being represented. |
| 0c. | Testing Guide | We will provide test scripts that can verify that the indexes are populated and return results. |
| 1. | Application Registry (Smart Contract) | The Smart Contract will be built in such a way that it considers the governance as defined in an earlier step and will allow the Application metadata to be stored on-chain. The Smart Contract will be designed to be deployed on any EOSIO chain. |  


### Milestone 4 — Application Registry Web Frontend

- **Estimated Duration:** 9 weeks
- **FTE:**  1.4
- **Costs:** 81,115 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial that explains how the various functions of the Frontend work for each user type. These user types are app developers, validators, end users and administrators. |
| 0c. | Testing Guide | We will provide test procedures on how to verify that all functionality is working as expected. |
| 1. | Application Registry Web Frontend | This is the Web Portal where users can browse the Application Registry. Application developers will be able to register their applications and will be able to make changes to existing Application Registry entries. Validators and Administrators will be able to validate Application Registry requests. Users are also able to “report” applications that are not behaving as they should, in order for a Validator to take the necessary action, which could be to warn the Application developer about this unwanted behavior or to remove the Application from the Registry completely. |  


## Future Plans

- Integration of the Asset Hosting Service or Asset Proxy Service, as outlined in the Wallet+ Blue Paper.
- Allow users to leave App reviews and Application ratings. A strong system needs to be built around this to avoid fraud and manipulation of these ratings.


## Additional Information

**How did you hear about the Grants Program?** We were recommended to use the Grant application by Yves, since no formal RFP exists coming out of the EOSIO Coalition.

We already had some alignment meetings with Aaron Cox and his team, who were the primary responsible team for the Wallet+ Blue Paper. Aim was to ensure that the Grant Application captured the scope and spirit of the white paper.
