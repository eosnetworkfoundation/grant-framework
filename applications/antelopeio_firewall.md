# EOS Network Foundation Grant Proposal

- **Project Name:**  Antelope Firewall
- **Team Name:**  Animus Labs LTD (representing Boid.com)
- **EOS Payment Address:**  animus.inc
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):**  2

- **Project is Open-Source:**  Yes
- **Project was part of Token sale:**  No
- **Repository where Project resides:**  <https://github.com/animuslabs>

## Contact

- **Contact Name:**  John Heeter
- **Contact Email:**  john@boid.com
- **Website:**  <https://www.animus.is>

## Project Overview

This is a proposal to build a firewall/proxy that would be used in an Antelope node operator's infrastructure. The end goal is to lower the barrier to entry for infrastructure providers to offer highly reliable public endpoints. We are especially excited to make it easier for anyone to operate a reliable public Antelope node without a complex understanding of DevOps.

### Overview

- **Name:**  Antelope Node Firewall
- **Brief Description:**  Lower the barrier to entry for infrastructure providers to offer highly reliable public endpoints.
- **Relationship to EOSIO:**  It's a layer on top of existing AntelopeIO API nodes.
- **Reason for Interest:**  We want to solve common issues that API node operators have.

### Project Details

#### Problem
Antelope Leap nodes are easily abused without proper network infrastructure. When nodes are abused by bots and malicious attackers, they become unreliable or unusable for normal users and create considerable strain on infrastructure providers. Therefore today only a small subset of public EOS nodes are usable in production. Based on our custom eospowerup.io proxy that rotates between APIs provided by the top 50 BPs we found that less than 10 are reliable and usable for production applications.

#### Proposed Solution
We propose an application that would sit behind an existing firewall such as NGINX (or replace your firewall for more simple networks) and in front of a Nodeos API node. The application would monitor incoming transactions and queries to perform smart logic such as blocking, or prioritizing based on the node operator's preference. The purpose is to make running highly available RPC nodes more accessible to node operators and reduce the load on the Nodeos software. The advantage of this application vs a traditional firewall is that this application is aware of Antelope transaction and query structure and can apply complex filter logic that a traditional firewall isn’t designed for.

![AntelopeIO_Firewall_Diagram](https://ipfs.animus.is/ipfs/QmZ3qEwAGuaboNYAypJdXtcGnofQX4yPrYhVStQnX5u8Vh?filename=diagram-antelope-firewall.jpg)

The initial version of the application would be written in Rust and could be easily scaled across multiple cores and operated with high uptime. The application could run on the same VM as Leap but for optimal flexibility could be hosted on a dedicated VM that scales independently.

#### **Features**

- **Dynamic Blacklisting**  Accounts, IPs, keys, and even specific contracts and actions can be blacklisted, throttled, and subjectively billed based on granular configuration. For example: the node operator may opt to only process one transfer action per account per second. For accounts that use inline actions or advanced techniques to subvert the firewall filtering, subjective CPU billing based on recent transaction history can effectively prevent abuse. All this logic can be easily configured by the node operator and dynamically automated based on metrics such as node CPU/RAM threshold logic. A side effect of this is that application specific nodes could provide fast and reliable operation for a limited subset of actions related to their application while throttling or deprioritizing other traffic.

- **Transaction Handling**  The Firewall can read incoming transaction data parameters and make subjective judgements based on the contents of the transaction. For example, you could block or subjectively bill any “transfer” action with a “from” data parameter that contains a blacklisted account. You could subjectively throttle transactions from accounts with a low balance, statistical analysis can grade accounts based on various metrics to give the account a “score” which helps the system understand if an account is a normal user or an automated bot and apply specialized rules accordingly.

- **Query Handling**  Repetitive requests for information can be automatically cached, throttled or blocked based on granular configuration and automatic statistics. This is especially useful to combat arbitrage bots which DDOS infrastructure.

- **Detailed Statistics**  Currently node operators have limited insight into what exactly is creating load for their Leap instances because general purpose firewalls don’t understand Antelope transaction/query structure. Our application can export detailed statistics in a format ingestible by Prometheus for visualization.

- **Granular routing**  The application could route queries and transactions to specific Leap instances such as an instance that is only responsible for push transactions that pertain to a specific contract. History queries could be routed to dedicated Hyperion nodes.

- **Automated Deployment**  Scripts for deployment via Docker, Ansible, or bare metal will be provided, Anyone could launch a highly available and production ready Leap instance from scratch in less than 30 minutes with minimal configuration and maintenance.

#### **Future additions**
Once the base level application has reached a production ready state and iterated based on node operator feedback there are additional developments that could improve the application.

- **Monetization**  Node operators who offer public APIs often do so as a free service that operates at a loss. This makes it difficult for operators to sustain the hardware and manpower required for high-availability RPC nodes. A monetization feature could be added to the firewall that would allow users to pay to have their contract actions whitelisted for less rate-limiting. For example, an application developer may pay a node operator a subscription fee to whitelist their contract operations in order to ensure a smooth experience for their users. Monetization can be totally automated with a smart contract and basic logic integrated into the firewall.

#### **Feedback from node operators**

- **EOSN**  Sounds very useful if it could replace NGINX/HAProxy. Consider building in Golang instead of Typescript. Increased performance and improved interoperability with Dfuse/Firehose such as reading Firehose blocks to reply to get_block requests without blocks.log.

- **GenerEOS**  I read your proposal and think it would be a useful product that would help many node operators.

- **EOSphere**  Love the idea .. like a patroneos 2.0, It really helped us at one point ,Would be great to have it again.

- **EOSUSA**  Should replace NGINX/HAProxy: If it's doing routing based on role, u dont wanna have more proxies scattered behind them, it should manage the routing and balancing

### Ecosystem Fit

Antelope Firewall can be an integral part of EOSIO/AntelopeIO ecosystem as an application firewall.

Node operators in the EOSIO/AntelopeIO ecosystem can create a better user experience for normal users and applications that rely on public infrastructure.

Reducing the load on the Nodeos application will reduce infrastructure costs and improve RPC api reliability for common users.

Additionally, this application would make it easy for application developers to host public nodes which throttle transactions and queries unrelated to their core application.

#### Existing solutions
Running a reliable Leap RPC on EOS and other high-traffic Antelope chains requires advanced DevOps skills. Node operators are required to maintain a considerably complex network infrastructure to support such a service. Typically this involves multiple layers of specialized Leap Nodes that act as filters for transaction propagation.

Existing EVM solutions:

- <https://github.com/ethereum-optimism/optimism/tree/develop/proxyd>
- <https://github.com/emeraldpay/dshackle>

## Team

### Team members

- **Team Leader:**  John Heeter - Founder @ Boid.com
- Jowita Choscilowicz - Project Manager
- John Heeter - Technical Lead / Development
- Seth Choscilowicz - Development / DevOps

### Legal Structure

- **Registered Legal Entity:**  Animus Labs LTD
- **Registered Address:**  Hunkins Waterfront Plaza, Main Street, Charlestown, Nevis

### Team Experience

John Heeter - 8 years of developement experience (5 years blockchain experience eosio) / full stack dev; technical artist 3 years; technical director 3 years
Jowita Choscilowicz - director 10 years / project manager 4 years / systems engineer 3 years
Seth Choscilowicz - blockchain dev ops 4 years eosio / systems engineer 14 years

### Team Org Repos

- <https://github.com/boid-com>
- <https://github.com/animuslabs>

### Team Member Repos

- <https://github.com/jdheeter>
- <https://github.com/mchosc>

### Team LinkedIn Profiles

- <https://www.linkedin.com/in/johnheeter>
- <https://www.linkedin.com/in/mchosc>
- <https://www.linkedin.com/in/jchoscilowicz>

## Development Status

The Antelope Firewall project is in the phase of architecture analysis and design. The project has not begun development yet.

We have collected our current experience from various organizations for which we have worked and from different clients for whom we have implemented projects. Experiences and conclusions from work in WEB2 environments are reflected in WEB3 ecosystems and in our opinion it is worth using these experiences and ideas that have been verified by the WEB2 market.

We created the concept of an application firewall for EOS and collected feedback from public node operators to illustrate the problem:

1. **EOS USA**

- EOS:
api: 1.5mil/hr
hyp: 200/hr about 50/50% api response 200/500
failures ~100% failed push trx (500)

- WAX:
api: 150K/hr
hyp: 205K/hr 5%
failures (push trx) but it´s heavily rate limited, response 50x abusers

- Proton:
api: 1.4mil/hr
hyp: 1500/hr about 50/50% api response 200/500
failures ~100% failed push trx (500)

- 1mil/hr blocked non-routable by proxy (no valid host headers for nodes)
- 117K/hr blocked at firewall for known abusive IP ranges

2. **EOS Nation**
20% failure rate, relying on Fail2Ban to prevent most bad queries/trx from reaching nodes, estimated 10x failure rate without Fail2Ban.

3. **Greymass**
50-100 failed transactions per second reach Leap instances, multitudes more are caught by firewalls/rate limiters.

4. **Boid BP**
Global API stats on EOS / Telos Mainnet / Telos Testnet / Hyperion / Hyperion Testnet about 1 mln per hour with spikes of 6k per second with automatic block of miners on EOS Mainnet 15% failure rate

5. **GenerEOS**
We use a combination of things in terms of firewall including nginx rate limits, Fail2ban, and for some chains also caching. I know that our APIs and p2p still get hammered and often are not usable.

6. **EOSphere**
On EOS we have a 43% transaction failure rate. We successfully process 300k EOS Transactions / hour. We fail 230k EOS Transactions / hour. Most of the failures are push transactions. 13.1Mil Successful EOS Actions / Transactions per day. Our WAX infra is over 30Mil Successful Actions / Transactions per day.

7. **EOS Amsterdam**
Approximately 90%+ transactions that make it through our existing rate-limiting solutions result in failures. Currently using: <https://gist.github.com/cc32d9/2466e15c14882b2d696415f6c2777954>

The application firewall turns out to be a natural element that should be an integral part of the EOSIO system.

## Development Roadmap

### Overview

- **Total estimated duration:**  6 months
- **Full-Time Equivalent (FTE):**  2-2.5
- **Total Costs:**  50,000 USD

### Milestone 1 — Create Antelope Firewall Prototype

- **Estimated duration:** 5 weeks
- **FTE:**  2.5
- **Costs:**  10,000 USD

| ID  | Deliverable   | Specification                                                                                                                                                                                                                                                                                                                         |
| --- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0a. | License       | MIT                                                                                                                                                                                                                                                                                                                                   |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how to configure and run, including technical draft: short document will act as an overview of the technical implementation details as part of the development planning stage. Will guide code structure and development milestones. |
| 0c. | Deployment    | We will provide a Prototype with a limited basic functionalities implemented. For example the firewall will be able to route queries to nodes and return responses with basic blacklisting functionality.                                                                                                                             |

### Milestone 2 — Implement Antelope Firewall MVP version

- **Estimated Duration:** 10 weeks
- **FTE:**  2
- **Costs:**  17,000 USD

| ID  | Deliverable           | Specification                                                                                                                                                                                                 |
| --- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0a. | License               | MIT                                                                                                                                                                                                           |
| 0b. | Documentation         | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how to configure and run Alpha and Beta version (MVP).                                                       |
| 0c. | Deployment Alpha      | We will provide a Alpha version with a major features implemented in a basic way. We will begin running on our own nodes. Our goal is to implement blacklisting, round-robin routing and special rules-based transaction handling logic.                                                                                     |
| 0d. | Deployment Beta (MVP) | We will provide a Beta version (MVP) with all features implemented in a basic way. The app should be ready to distribute to external infra providers for feedback and testing of the HTTP RPC functionality. This release will include improvements of functionality implemented in the Alpha. Additionally this release will include statistics and monitoring endpoints for prometheus. Additionally this release will include contract and account prioritization functionality, for example queries for certain contract tables could be rate-limited at a different rate. |

### Milestone 3 — Implement Antelope Firewall 1.0 version

- **Estimated Duration:** 14 weeks
- **FTE:**  2
- **Costs:**  23,000 USD

| ID  | Deliverable   | Specification                                                                                                                                                                                                                                                                                                                          |
| --- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0a. | License       | MIT                                                                                                                                                                                                                                                                                                                                    |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how to configure and run Antelope Firewall 1.0 version, which covers all of the application functionality and configuration. Also we will create deployment scripts for various platforms to simplify the process of getting started. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests.                                                                                                                                                                                      |
| 0d. | Deployment    | We will provide an Antelope Firewall 1.0 version - production ready solution, based on feedback from infra providers and issues discovered during beta testing. The focus of this release is improving features from the Beta and we may add additional configuration or functionality based on beta testing feedback from infra providers.                                                                                                                                         |
| 0e. | Article       | We will publish an **article** that explains what are the features of the product, how does it work and what was achieved as part of the grant.                                                                                                                                                                                        |

## Future Plans

The Antelope Firewall will be useful for EOS node operators, ensuring a high level of security.

We plan to offer a solution to active block producers, in the first place to everyone we've talked to so far: EOS USA, EOS Nation, Greymass, Boid BP, GenerEOS, EOSphere, EOS Amsterdam. We assume that we will reach 30 block producers within the first 3 months from the release of version 1.0. The next step in the coming months will be reaching out to other EOS block producers.

At the same time is important for us to collect feedback from the users of the tool by sending them a survey regarding the functionalities in 1.0 version. On this basis, we want to develop the application and prepare a set of new functionalities in 2.0. version. The new features will address the node operators needs.

In the long term, we plan to promote the Antelope Firewall in the dApps Providers target group in EOSIO ecosystems.

## Additional Information

**How did you hear about the Grants Program?**  Twitter

So far, we have been implementing the project with our own funds, we do not want to go beyond the EOSIO environment with the idea. We submit the application for funding only to the EOS Network Foundation.
