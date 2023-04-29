# EOS Network Foundation Grant Proposal

- **Project Name:** Neutroswap
- **Team Name:** Nava Labs
- **EOS Payment Address:** 0x7De5A1Aa67ec3f67C326689FD36abA20ba703E65
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/Nava-Labs/neutroswap_v3

## Contact

- **Contact Name:** Jonas Aditya Sunandar
- **Contact Email:** contact@neutroswap.io
- **Website:** https://neutroswap.io

## Project Overview

Neutroswap is an automated market-maker (AMM) on the EOS EVM blockchain that is community-driven and offers the lowe fees for swapping assets. It also has some of the most lucrative rewards for staking and yield farming in the entire EOS EVM ecosystem, making it an appealing choice for those looking to generate returns on their assets. 
Our team decides to focus more towards bringing liquidity to EOS EVM chain more. It will enable more users, projects and exposure due to increasing TVL in EOS EVM. 

### Overview

> Please provide the following:

- **Name:** Neutroswap
- **Brief Description:** Community-driven AMM & Launchpad on EOS EVM
- **Relationship to EOS Network / Antelope:** Our app brings liquidity to EOS EVM attracting more projects and users to use the chain.
- **Reason for Interest:** Capital efficiency, impermanent loss, mitigation, higher fee rewards, reduced slippage, improved price discovery.

### Project Details

We have launched Neutroswap V2 and we want to move on to V3 and make our position stronger in EOS EVM. Our V3 version will cover concentrated liquidity.

Concentrated liquidity is an innovative approach to liquidity provision that allows liquidity providers (LPs) to enhance their capital efficiency and minimize impermanent loss by focusing their liquidity within a particular price range. By enabling LPs to stake specific token pairs within a designated price range, this novel method leads to a more efficient allocation of resources compared to conventional liquidity provision techniques.

#### Benefits of Concentrated Liquidity

1. Capital efficiency: LPs allocate funds within a chosen price range, allowing for more effective use of capital.
2. Impermanent loss mitigation: Concentrating liquidity in a specific range helps reduce exposure to price fluctuations, mitigating impermanent loss.
3. Customized strategies: LPs can tailor their strategies based on risk tolerance, market outlook, and price predictions, by selecting any desired price range. The tighter the range, the more liquidity passes through the position, and the more the LP earns.
4. Higher fee rewards: LPs can potentially earn higher trading fee rewards proportional to their contribution within the active price range.
5. Reduced slippage: Traders benefit from deeper liquidity where it's needed the most, resulting in reduced slippage and better execution prices.
6. Improved price discovery: Concentrated liquidity can lead to more accurate price discovery, as liquidity is focused on price ranges with higher trading activity and demand.

#### V2 Pools vs Concentrated Liquidity
V2 pools employ the XYK model, which maintains a constant balance within a liquidity pool so that the total value of one token always equals the total value of the other token in the pool, regardless of their current price against each other. In V2 pools, liquidity is spread across all possible price ranges, making it difficult for LPs to decide where to allocate liquidity. In reality, the majority of their liquidity remains unused.

In contrast, concentrated liquidity allows LPs to focus their liquidity within a specific price range, resulting in better capital efficiency, reduced impermanent loss, and increased trading fee rewards. Moreover, concentrated liquidity enables LPs to create customized strategies by allocating their capital to preferred price intervals.

##### V2 Pools:
- Based on the XYK model
- Liquidity spread across all possible price ranges
- Difficult for LPs to decide where to allocate liquidity
- Higher slippage and lower trading fee rewards

##### Concentrated Liquidity Pools:
- Customizable price ranges
- More efficient use of capital
- Reduced impermanent loss and higher trading fee rewards
- Allows LPs to create tailored strategies

### Ecosystem Fit

- Where and how does your project fit into the ecosystem? Currently EOS EVM needs more TVL to get organic exposure. With our launched, you might have seen the significant growth in EOS EVM. We want to continue to grow on EOS EVM by providing more value using our V3 version.
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)? Farmers, DeFi users, crypto users in general, traders
- What need(s) does your project meet? Neutroswap V3 will have benefits: impermanent loss mitigation, increased flexibility, higher performance. Especially it can bring more TVL to EOS EVM.
- Are there any other projects similar to yours in the EOS Network / Antelope ecosystem?
  - If not, are there similar projects in related ecosystems? Noahswap, Frogge might release the same solutions in the future.

## Team

### Team members

- **Team Leader:** Jonas Aditya Sunandar
- Wilsen Tiomajaya
- Erwin Phanglius
- Akramurridjal Rahman
- Ryan Tjin
- Kevin
- William Wijaya

### Legal Structure
- **Registered Legal Entity:** PT Nava Labs
- **Registered Address:** Foresta Fiore B3 No 10 BSD, Tangerang Selatan, Indonesia

### Team Experience
- EMURGO/Cardano
- Good Games Guild
- Whitehackers
- Metaversepad
- Arbipad
- HARA token
- Asosiasi Blockchain Indonesia
- Coinvestasi

### Team Org Repos

- https://github.com/Nava-Labs
- https://github.com/Nava-Labs/neutroswap-contract

### Team Member Repos

- https://github.com/xerod
- https://github.com/jonassunandar
- https://github.com/erwinphanglius
- https://github.com/RyanTjhin

### Team LinkedIn Profiles (if available)
- https://www.linkedin.com/in/jonas-sunandar-83307b164/
- https://www.linkedin.com/in/wilsen-t-110533113/
- https://www.linkedin.com/in/akramurridjal/
- https://www.linkedin.com/in/erwin-phanglius-a22a121a6/
- https://www.linkedin.com/in/ryan-tjhin-90b16521b/
- https://www.linkedin.com/in/william-wijaya-792075199/

## Development Status
We are in the researching and looking for partners phase to help us build the solution. We haven't decided the UI/UX, but it will be quite similar to Uniswap V3

References: 
- https://blog.uniswap.org/uniswap-v3

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

> :zap: If any of your deliverables is based on someone else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Milestone Summary

> Note: the numbers in the three lines below are examples.  Please replace with your own calculations!  Then delete this instruction line.
> You **must** keep these three Milestone Summary lines below for your grant to be approved.  The Total Cost should add up to the costs
> of all of your Milestones.  Please **DO NOT** remove the three lines below.  If you do, your grant will be rejected or delayed while you fix it.
- **Total Estimated Duration:** 2 months 
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 12,000 USD

> Please note that this application is automatically parsed.<br/>
> For the above fields, please only put the answer on that line.  If you want to add more information, please put it below these instructions.<br/>
> Please remember to delete all lines that start with `>` as they are just instructions and not needed in the application submission.<br/>
> 
> Notes on above fields:
> - Total Estimated Duration: Duration of the whole project (example: 2 months or 7 weeks)
> - Full-Time Equivalent (FTE): This is the average number of full-time employees working on the project throughout its duration (see [Wikipedia](https://en.wikipedia.org/wiki/Full-time_equivalent), example: 2 FTE or possibly 2.5 FTE as it is an average)
> - Total Costs: This should be the requested amount in USD for the whole project (example 12,000 USD). Note that the acceptance criteria and additional benefits vary depending on the [level](../README.md#grant-levels) of funding requested. This and the costs for each milestone need to be provided in USD; if the grant is paid out in EOS, the amount will be calculated according to the exchange rate at the time of payment.

### Milestone 1 Example — Implement EOS Application

- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 8,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT / Apache 2.0 / GPLv3 / Unlicense |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our EOS nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)
| 1. | Application interface to Antelope | We will create an integration layer ... (Please list the functionality that will be implemented for the first milestone) |  
| 2. | Front-End / User Interface | We will create a UI that connects to ... |  
| 3. | Caching layer | We will create a caching layer ... |  
| 4. | API interface to our app | We will create an API that ... |  



### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  2
- **Costs:** 4,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT / Apache 2.0 / GPLv3 / Unlicense |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our EOS nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)
| 1. | Performance Enhancements | We will create performance enhancements to ... (Please list the functionality that will be implemented for the first milestone) |  
| 2. | Added UI functionality | We will add UI functionality to... |  
| 3. | Add 3rd Party API integration | We will add 3rd party integration to ... |  


... Add more milestones as above as needed ...


## Future Plans

> Please include here:

- how you intend to use, enhance, promote and support your project in the short term, and
- the team's long-term plans and intentions in relation to it.


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

> Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
