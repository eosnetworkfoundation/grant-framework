# EOS Network Foundation Grant Proposal



- **Project Name:** DeRisk
- **Team Name:** Carmine Finance s.r.o.
- **EOS Payment Address:** 0xa4ad2Ee4f67C3C83a0081060b6AeA2c88dFc36f3
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** 
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/CarmineOptions/derisk-research/


## Contact

- **Contact Name:** Marek Hauzr
- **Contact Email:** marek@carmine.finance
- **Website:** https://derisk.carmine.finance



## Project Overview

DeRisk on EOS, a platform to monitor and forecast risk of acquiring under the water loans to protect lending protocols and users.

### Overview

- **Name:** DeRisk, a platform to monitor and forecast risk of acquiring under the water loans.
- **Brief Description:** DeRisk is an open-source, risk monitoring platform that serves as an “early warning” mechanism to detect risky situations (mainly loans going underwater). 
- **Relationship to EOS Network / Antelope:** Open (and open-sourced) platform showing the state of loans and lending protocols on EOS. Help with using the platform, marketing and also early warning to lending protocols and community about potential high risks.
- **Reason for Interest:** 
  - Allows lending protocols to put measures in place to protect themselves and THEIR USERS.
  - Allows for a more efficient capital allocation and more capital flowing instead of stuck in liquidity pools.
  - Having DeRisk in EOS will decrease the chances of acquiring bad dent in the whole ecosystem, which will be an incentive for projects to build in EOS. 


### Project Details

- Mock-ups/designs of any UI components
  - We are already running a (working) demo on StarkNet https://demo.derisk.carmine.finance. It will also include additional features that will be delivered during September.

- Data models of the core functionality
  - Data collection through an indexer
  - Data standardization through a custom (per protocol) micro service
  - Data are stored in PostgreSQL and awailable through an open API
  - Data are visualized through StreamLit app (https://demo.derisk.carmine.finance), but this will be done through standard React FE.
  - In terms of core functionality:
    - We will integrate all lending protocols. 
    - Combine available liquidity on AMMs.
    - Provide comparison of the available liquidity and the required liquidity for liquidations.
    - Basic comparison of loans between lending protocols
    - Standardization of health factor - making it comparable between protocols
    - Basic comparison of lending protocols
    - Suggestions on insurance - based on the “free version” data.
    - Data standardization, so that it is easier to onboard liquidators for the entire chain, not just a single protocol.
    - We will run the app for at least following 12 months.

- API specifications of the core functionality
  - Will be delivered as part of the open source project.

- An overview of the technology stack to be used
  - Python, Streamlit, PostgreSQL, React

- Documentation of core components, protocols, architecture, etc. to be deployed
  - Will be delivered as part of the open source project.
  
- PoC/MVP or other relevant prior work or research on the topic
  - Already open sourced and being built on StarkNet. Will be finished by the end of September.
  -   https://demo.derisk.carmine.finance
  -   https://github.com/CarmineOptions/derisk-research/


- What your project is _not_ or will _not_ provide or implement
  - We can't guarantee we will be able to integrate new lending protocols or AMMs down the line, from this grant.
  - We will not simulate the complex behavior of the FULL ecosystem, we will do the lending section.



### Ecosystem Fit


- Where and how does your project fit into the ecosystem?
  - Protocols and users will receive an early warning system and understand the risks of acquiring the under the water loans. They will also benefit by being able to build insurance on top of it, list more tokens as collateral, etc

- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
  - Lending protocols and their stakers.

- What need(s) does your project meet?
  - High level - better DeFi utilization and broadening the spectrum of things available in DeFi in EOS.

- Are there any other projects similar to yours in the EOS Network / Antelope ecosystem?
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?
  - Not as far as I know. There are few that do similar "stuff" to us (not necessarily in EOS), but they do not provide continuous monitoring and their results are generally not public.

## Team

### Team members

- **Team Leader:** Marek Hauzr
- Lukas
- Ondrej
- Andrej
- David
- Guillermo

### Legal Structure
- **Registered Legal Entity:** Carmine Finance s.r.o.
- **Registered Address:** Sokolovská 428/130, Karlín, 186 00 Praha, Czech Republic

### Team Experience

We come from combination of Finance, HFT, AI/ML, MEV. Most things we did in the past were custom builds and were not open sourced. As a team we are working not only on the DeRisk, but we have already build Carmine Options AMM (https://app.carmine.finance).


### Team Org Repos

These are the ones of interest.
- https://github.com/CarmineOptions/
- https://github.com/CarmineOptions/derisk-research/


### Team Member Repos

- https://github.com/lukaspetrasek
- https://github.com/MarekHauzr
- https://github.com/DaveVodrazka
- https://github.com/Chepelau
- https://github.com/tensojka

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/marek-hauzr-8016077b/

## Development Status

- https://derisk.carmine.finance
- https://demo.derisk.carmine.finance


## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 12 months 
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 36,000 USD


### Milestone 1 - Infrastructure

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 6,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can set up the infrastructure. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains what was done/achieved as part of the grant.
| 1. | Database | PostgreSQL database to collect all the data, including the data structures |
| 2. | Data processing | Container feeding the database with non-standardized data |
| 3. | API | API to access the database by public |  


### Milestone 2 - Data standardization

- **Estimated duration:** 2 months
- **FTE:**  2
- **Costs:** 20,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can standardize the data and run the code. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains what was done/achieved as part of the grant.
| 1. | Data processing | Module standardizing the loan data and pushing them to database. The timeline of this milestone is mainly dependent on this task/feature. |
| 2. | Data processing | Module standardizing AMM data (available liquidity). |


### Milestone 3 - FrontEnd and data preparation for visualization 

- **Estimated duration:** 1.5 months
- **FTE:**  1
- **Costs:** 7,500 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can run the FE. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article** that explains what was done/achieved as part of the grant.
| 1. | FrontEnd | FrontEnd built in Streamlit for easy adjustments by any "data" developer (BI/AI/data/... engineers). |
| 2. | Risk module | Module comparing available liquidity and required liquidity by future liquidations. |
| 3. | Risk module | Module preparing basic comparison of loans between lending protocols. |
| 4. | Risk module | Module preparing casic comparison of lending protocols. |
| 5. | Risk module | Standardization of health factor to allow for smooth comparison of loans. |
| 6. | Risk module | Early warning module highlighting problematic loans and problematic areas for given protocols and entire chain. Including suggesting what to hedge or insurace and how it could be done. |


### Milestone 4 - Running everything for 12 months 

- **Estimated duration:** 12 months
- **FTE:**  0.1
- **Costs:** 2,500 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide documentation on everything is running. |
| 0c. | Testing Guide | We will provide guide, that will describe step by step process to running everything from setting VM to deploying containers. |
| 0d. | Docker | Non-applicable - images are prepared in previous milestones |
| 0e. | Article | We will publish an **article** that explains what was done/achieved as part of the grant.
| 1. | Continuous support | Running all of the above modules/containers for 12 months. |
| 2. | Continuous support | Since we are unable to foresee what will happen, we CAN'T guarantee that updates to protocols will fit into the budget. Same for new protocols. We will likely ask for additional (small) grants |



## Future Plans

- how you intend to use, enhance, promote and support your project in the short term, and

In the short term, we will promote with our community and we would like to do that also with partnership with EOS and EOS's lending protocols. Part of this would be sharing information about the risks (education).


- the team's long-term plans and intentions in relation to it.

In the future, based on the DeRisk monitoring we would like to bring Carmine Options AMM and provide insurance against the under the water loans. Effect of this is not only higher security for protocols and users, but much easier listing of altcoins in lending protocols on EOS, lower cost of capital in terms of lowering the sizes of security pools and more. Once this will be set up, we would have a path to bring other insurance/hedge products like hedging against impermanent loss, insurance against price drops,...


## Additional Information

**How did you hear about the Grants Program?** personal recommendation

We would like to provide DeRisk to all of DeFi world, since we believe DeFi will take over traditional finance. Implication of this is that when we develop new and better features, it will be easy to deploy them on DeRisk-EOS, thanks to the data standardization.

We want to make this project sustainable and open sourced. The sustainability means that down the line (after this project is conluded), we would like to convince EOS lending protocols to finance it. To provide them so much value, that they would be happy to finance it directly.

Lastly, I would like to mention, that it would be amazing if we could chat about the functionality and features of DeRisk. Since we could adjust (add) some other features that we are thinking of. We already tried contacting few "EOS representatives" on telegram, but not successfully.
