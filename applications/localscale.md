# EOS Network Foundation Grant Proposal

- **Project Name:** LocalScale
- **Team Name:** LocalScale PBC
- **EOS Payment Address:** localscaleos
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/localscale


## Contact

- **Contact Name:** Steph Osmont
- **Contact Email:** steph@localscale.org
- **Website:** https://localscale.org

## Project Overview


### Overview

- **Name:** Globalizing Local Resilience
- **Brief Description:** LocalScale is a public benefit organization focusing on the development of resilient and sustainable local economies through the use of technology, science and regenerative activities.
- **Relationship to EOS Network / Antelope:** The platform already works with the Telos blockchain. Our integration with Hphha's tools would benefit from an integration to EOS. 
- **Reason for Interest:** Our platform's purpose is to be blockchain-agnostic, while supporting the blockchains that will allow interoperability with our direct partners.

### Project Details


- See our attached presentation, slide 22 
- See our attached presentation, slide 6
- See https://localscale.readme.io/reference/getting-started-with-your-api-1 for some of our open APIs
- Java, NodeJS, C++ (backend), Javascript, React, Flutter (front-end & mobile) - AWS Cloud and multiple services being leveraged
- See our attached presentation
- Platform is in production at https://localscale.org/
- Our platform is not a financial tool

### Ecosystem Fit

- The LocalScale platform provides an ecosystem integrating web3 tools (coins, DAOs, wallets) for local communities
- Our target audience is local ecosystem designers wanted to provide autonomy and resilience for local communities
- Among other tools, the platform provides marketplace tools needed by other web3 ecosystem players, allowing their users to exchange value locally and solidify their zones of resilience
- Hypha is a similar project in the EOS network but focuses on providing DAOs, while LocalScale focuses on providing marketplace-centric tools for those DAOs

## Team

### Team members

- **Team Leader:** Steph Osmont
- Nadim Hamdan
- Cliff Johnson
- António Cascalheira
- Gilles Bonugli
- Rieki Cordon
- Chuck Harrisson
- Jeff Quintero

### Legal Structure
- **Registered Legal Entity:** LocalScale PBC
- **Registered Address:** 15 Campolindo Rd, Point Reyes Station, CA 94956, USA

### Team Experience

- I (Steph Osmont) am a serial-entrepreneur who had multiple successful exits on technologies I created (please see my LinkedIn). I am currently co-founder of a SAAS company called Hostfully, for a platform I created in 2016, which is today a multi-million dollars company with over 80 employees.
- Cliff Johnson was the co-founder of Vacasa, the largest Vacation Rental Management Company in the world. He is also an impact entrepreneur and investor involved in many regenerative projects.

### Team Org Repos

- https://github.com/localscale

### Team Member Repos

- https://github.com/cascalheira
- https://github.com/chuck-h

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/stephaneosmont/
- https://www.linkedin.com/in/cascalheira/
- https://www.linkedin.com/in/johnsoncliff/
- https://www.linkedin.com/in/rieki-cordon777/
- https://www.linkedin.com/in/hamdan-itm/

## Development Status

- Academic esearch to which we participated on local resilience https://localscale.org/research/en/intro_summary.jsp?uid=97p8290f3eea52d4c40cd4b904d594ad
- Blog posts at https://localscale.org/blog/index.jsp
- See the MOU signed with Hypha, which triggered the integration project with EOS https://dao.hypha.earth/localscale/proposals/46812

## Development Roadmap

This section should break the development roadmap down into milestones and deliverables. To assist you in defining it, we have created a document with examples for some grant categories [here](../docs/grant_guidelines_per_category.md). Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**. In the descriptions, it should be clear how your project is related to the EOS ecosystem. We _recommend_ that teams structure their roadmap as 1 milestone ≈ 1 month.

For each milestone,

- make sure to include a specification of your software. _Treat it as a contract_; the level of detail must be enough to later verify that the software meets the specification.
- include the amount of funding requested _per milestone_.
- include documentation (tutorials, API specifications, architecture diagrams, whatever is appropriate) in each milestone. This ensures that the code can be widely used by the community.
- provide a test suite, comprising unit and integration tests, along with a guide on how to set up and run them.
- commit to providing Dockerfiles for the delivery of your project.
- indicate milestone duration as well as number of full-time employees working on each milestone.
- **Deliverables 0a-0c are mandatory for all milestones**, and deliverable 0e at least for the last one. If you do not intend to deliver one of these, please state a reason in its specification (e.g. Milestone X is research oriented and as such there is no code to test).

### Milestone Summary

- **Total Estimated Duration:** 5.5 months 
- **Full-Time Equivalent (FTE):** 3.5 FTE
- **Total Costs:** 190,000 USD

### Milestone 1 — Implement EOS Support in LocalScale core framework

- **Estimated duration:** 2 month
- **FTE:**  3.5
- **Costs:** 65,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT
| 0b. | Documentation | We will provide documentation that explains the implementation of the different sub-components that are required to process transactions on EOS and retrieve associated data. |
| 0c. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0d. | Article | We will publish an **article** that explains our extended architecture and how it can support EOS-based transactions.
| 1. | Core connectors to EOS  | We will extend our architecture to allow transactions to be validated by the EOS network. This involves a lot of the core tools such as transaction signers, transaction retrieval, user authorization, and all the core components that require communication to the EOS network.   
| 2. | Caching layer  | We will extend our caching layer to be able to store data coming from EOS.  
| 3. | Back-end  | We will extend our data model to accommodate transactions to a different blockchain. |
| 4. | Authorization Model and User Management | We will extend our user management authorization model to accommodate EOS-based accounts. This includes UI so that EOS-based accounts can log into LocalScale using their favorite wallet app. |
| 5. | APIs | We will create internal APIs for our different services to communicate with the EOS connectors outlined above. |
| 6. | Design, Architecture and Testing | The estimation for this milestone takes into account time spend on product design, product architecture, project management, testing and release management. |



### Milestone 2 — Implement EOS Support in LocalScale vertical tools 

- **Estimated Duration:** 1.5 month
- **FTE:**  3
- **Costs:** 40,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT 
| 0b. | Documentation | We will provide documentation explaining how the different tools provided by LocalScale implement support for the EOS network. |
| 0c. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0d. | Article | We will publish an **article** that explains how the LocalScale bioregional tools now support EOS-based transactions.
| 1. | Marketplace Support | This includes the ability to conduct EOS-compatible transactions on the different marketplaces provided on LocalScale: local, global and virtual farmers market. |  
| 2. | Seed Exchange System support of EOS | This includes the ability to conduct EOS-compatible transactions on the Seed Exchange System, for bioregions that will select an EOS-based currency for their exchanges. This includes back-end, middle-tier and front-end work in the ability for a bioregional entity to also select among different networks. |  
| 3. | Local Exchange Trading System  |Similar as above but applied to the LETS module. |  
| 4. | Design, Architecture and Testing | The estimation for this milestone takes into account time spend on product design, product architecture, project management, testing and release management. |




### Milestone 3 — Implement EOS Support in LocalScale mobile app and wallet

- **Estimated Duration:** 1 month
- **FTE:**  2.5
- **Costs:** 40,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT 
| 0b. | Documentation | We will provide documentation that explains the implementation of the support for EOS-based transactions processed from the LocalScale SmartWallet. |
| 0c. | Article | We will publish an **article** that explains how the LocalScale SmartWallet supports EOS-based transactions and authorization.
| 1. | Authorization model changes | We will adjust our mobile app authozitaion to allow access from EOS accounts. This requires changes to our backend and APIs. |  
| 2. | Implementation of new auth model in app | We'll implment the new auth model in the app to allow app access with an EOS account. |  
| 3. | Support for mobile EOS-based POS transactions in SmartWallet | Allow users to conduct transactions on the SmartWallet POS using EOS accounts (Receive function with QR scanning and transaction processing). |  
| 3. | Support for mobile EOS-based Send transactions in SmartWallet | Allow users to send EOS-based tokens to other users  on the SmartWallet POS using EOS accounts (Send function with user search). | 
| 4. | Design, Architecture and Testing | The estimation for this milestone takes into account time spend on product design, product architecture, project management, testing and release management. |



### Milestone 4 Example — Implement compatibility with the Hypha Platform & Tools

- **Estimated Duration:** 1 month
- **FTE:**  3
- **Costs:** 45,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT 
| 0b. | Documentation | We will provide documentation that explains the implementation of the support for EOS-based transactions processed from the LocalScale SmartWallet. |
| 0c. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0d. | Article | We will publish a **articles** on social media, blog and website outlining the integration details between Hypha and LocalScale platforms, in particular in the way EOS-based account holders can freely navigate from one platform to the other in an integrated way.  
| 1. | Authorization compatibility model |  Will allow users to inter-operate between Hypha and LocalScale from an authorization standpoint. Users with EOS-based accounts will be able to navigate projects and marketplaces between the two systems seamlessly. 
| 2. | Added UI functionality | We will expand the user interface to provide extra integration layers allowing users to visualize the connections between particular Hypha DAOs and their respective LocalScale organisation or bioregion.  |  
| 3. | API integration | We will provide an extended set of APIs allowing the Hypha platform to remotely access information regarding particular users, organisations, farms, local businesses on LocalScale, in the way they can connect their DAO and access the different marketplaces and tools.  | 
| 4. | Design, Architecture and Testing | The estimation for this milestone takes into account time spend on product design, product architecture, project management, testing and release management. |


## Future Plans

- We would like to invite you to review the deck that we attached to the grant proposal, as it outlines our roadmap and future technical developments.
- In essence, our project is organically supported by the community of users we cater to. The participative ownership model we provide invites participants in acquiring equity through the esr-based LSCL token we expose to the community. 
- Moreover, as a network of networks, the project is already supported by multiple communities around the world (Seeds, Hypha, Gaia Union, Big Impact, The Blue Economy, The B-Corp network etc) which are using the platform as their operating system for the regenerative economy.
- Financially, the organisation will self-sustain itself as it scales. The revenue streams (outlined in our deck) will be based on token sales, transaction commissions, referral fees, rev share from partnerships, to name a few.


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

- As technology providers and engaged participants in the Telos network (their CTO Doug being on of our advisors), we are very familiar with the originating EOS network and its constituents.
- This application for an ENF Grant was suggested by our partner Hypha, which is one of the recipients of such grants. As our technology integration is getting deeper with Hypha, the need to mutually support the same blockchains is a natural evolution of the partnership and outline in the mutual MOU we signed in 2023.  
- Work already done: the platform is already launched and aims at orchestrating and rewarding local impact-positive initiatives to regenerate bioregional economies.
- The system already provides many key technology integrations (Telos, Stripe, Ecologi, Hypha, PaperKarma, Discord, etc) and modules which carry the particular objectives to sustain local economic development using regenerative local digital currencies.
- Our organisation also partners with research institutes such as Les Greniers d'Abondance, The Shift Project, ASU, in order to help raise awareness about systemic resilience for communities. The research we help publish is then used as a driver to the roadmap for the platform. See an example at https://localscale.org/research/en/intro_summary.jsp?uid=97p8290f3eea52d4c40cd4b904d594ad (section 3, pathway 4) and how it was instrumental in the development of our Seed Exchange Project (https://localscale.org/seeds-exchange.jsp).
- The Hypha organisation has already contributed to our project, in the form of a token grant. 
- The project has already raised a pre-seed round in the form of private funds raised from Silicon Valley tech executives.
