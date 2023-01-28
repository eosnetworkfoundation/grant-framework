# EOS Network Foundation Grant Proposal

- **Project Name:** QRY - Distributed API Ecosystem
- **Team Name:** EOS Rio
- **EOS Payment Address:** eosriobrazil
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** https://pomelo.io/grants/hyperion
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/eosrio/qry

## Contact

- **Contact Name:** Thiago Canellas
- **Contact Email:** canellas@eosrio.io
- **Website:** https://eosrio.io

## Project Overview

The present proposal addresses the issue of unreliable API infrastructure, pointed out in the [API+ Blue Paper](https://bit.ly/api-plus-english). The solution considers the Proposal 5: Distributed APIs (page 40) for the creation of a decentralized ecosystem of operators to provide RPC and History endpoints to the community.

### Overview

- **Name:** QRY - Distributed API Ecosystem
- **Brief Description:** QRY will abstract complexity and create a reliable alternative for developers accessing EOS APIs (RPC and history). QRY will leverage an already existing community of operators to provide high reliability and performance API services (RPC, EVM RPC, History, and others).
- **Relationship to EOSIO:** APIs are a fundamental piece of infrastructure for developers using the network. Increasing the reliability and abstracting complexity will reduce the barriers and costs to develop on EOS making it more attractive to developers.
- **Reason for Interest:** The teams involved in the project have been working on EOSIO since before mainnet launch, and have extensive experience operating free API infrastructure for EOS. EOS Rio is the creator and maintainer of Hyperion, one of the most used History API solutions in the ecosystem.

### Project Details

Developers working on decentralized applications must access state and historical information on the Blockchain, as well as push transactions to the network. The current options for developers on EOS to interact with the chain are:
1. To run their own nodes and infrastructure connecting to the blockchain, which has a significant operational cost, especially for historical information;
2. Use unreliable but free community maintained endpoints;
3. Or pay steep prices for privately managed instances or services with SLA.

QRY will offer an SDK for dApp developers to simply call queries from inside their JavaScript code, while the SDK handles endpoint selection and fallback by tapping into the existing decentralized network of operators, coordinated through QRY. 

The QRY Operator Client will allow independent infrastructure teams to publish relevant availability and performance data. It will also check client signatures and write usage information on the blockchain. Reference implementations will be built for Hyperion and nodeos native APIs (via HAProxy plugin), but QRY will also allow and incentivize support for other Transports (i.e. dfuse, robo, chronicle, etc) to connect to the network.

With that, QRY will offer a simple way for developers to interact with the blockchain, removing an important initial barrier for developers and a common bottleneck for decentralized applications.

**DELIVERABLES**

- **MVP:** An initial implementation that will allow developers to start using and providing feedback on the project. Includes a partial implementation of the QRY Operator Client for Hyperion, that connects to a centralized information hub (QRY Hub). It also includes the initial implementation of the SDK as a microservice for handling endpoint selection for current Hyperion/Chain API users.
- **JavaScript SDK:** The SDK will enable developers to make query calls from inside JavaScript/Typescript code with automatic endpoint selection by consulting publicly available as well as locally collected data.
- **Web interface:** Website that will allow users to create an account, register a public API key and check their current usage.
- **QRY Engine:** A smart contract platform that will allow the coordination and incentivization of infrastructure operators. This contract will allow users to register API keys and eventually pay for premium services, while providers use it for key validation and quota usage publishing.
- **Operator Client:** This client will be able to read a query request signature in order to validate the public key on the contract, as well as to check the available limit. Then it will write a new usage on the period to control the user's limits. The Client will also transmit relevant availability and performance information to a community hub. Hyperion will serve as a reference implementation for other transports. A plugin will be written for HAProxy allowing operators to use it for nodeos native APIs and other RPC nodes, such as EOS EVM. 

### Ecosystem Fit

- **Where and how does your project fit into the ecosystem?**


 QRY fits the ecosystem by making it easier for developers to create and maintain applications on EOS, tapping into an ecosystem of free APIs already offered by seasoned teams. In the future, we also expect to help independent teams operating fundamental infrastructure to generate additional revenue making the network more robust.

- **Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**

 We target developers that want to have better experience and reliability when interacting with the EOS blockchain. Independent infrastructure operators are also a core target as those teams will actually deliver the service.

- **What need(s) does your project meet?**

 API endpoint availability and reliability.

- **Are there any other projects similar to yours in the EOSIO ecosystem?**
   - **If so, how is your project different?**
   - **If not, are there similar projects in related ecosystems?**

 Similar projects to this are The Graph and SubQuery but they don't support Antelope chains.

## Team

### Team members

The team involved in this project is mainly EOS Rio but also includes EOSphere to write documentation and Sw/eden to work on the HAProxy plugin. Other teams operating Hyperion instances are committed to operate infrastructure once the project launches.

- **Team Leader:** Igor Lins e Silva (EOS Rio)
- Dominique Deschatre (EOS Rio)
- Thiago Canellas (EOS Rio)
- João Barbosa (EOS Rio)
- Jailon Aguiar (EOS Rio)
- Ross Dold (EOSphere)
- Eric Bjork (Sw/eden)
- Anders Bjork (Sw/eden)
- Henrik Hautakoski (Sw/eden)

### Legal Structure
- **Registered Legal Entity:** EOS Rio Infraestrutura de Redes Ltda
- **Registered Address:** Rua Lauro Muller 116, sala 3706 - Rio de Janeiro/Brazil - ZIP: 22290-160

### Team Experience

EOS Rio launched one of the first EOS wallets weeks after the Mainnet launch. SimplEOS had more than 178.000 downloads. The team is also responsible for developing and maintaining Hyperion History API, one of the main History solutions in the ecosystem, that is open source and operated by teams around the world. EOS Rio is also among the top performing BPs on networks in which it is elected, constantly contributing to evolving hardware and operational practices.

Sw/eden is a team which has been a staple in the EOSIO community since before EOS Mainnet launched. They have been an active node operator for EOS and other Antelope based blockchains since then. Focusing on providing high quality and reliable API services, Peering Nodes and Producer node, as well as building tools surrounding the backend infrastructure. On top of that they are keen on educating and informing the community through articles, videos and courses.

EOSphere is an Australian based blockchain infrastructure and services company. They have been keenly involved with the EOS Block Producer community since before mainnet launch in 2018. EOSphere launched the first EOS Voter Portal early in 2018 and went on to found EOSphere /dev a purely EOSIO focused development company in 2019. Other than providing rock solid infrastructure and services for the EOS Mainnet and greater Antelope networks, of late they are known for their user-friendly Antelope focused technical documentation and HeadsUp - Antelope Monitoring and Alerts Platform.

### Team Org Repos

- https://github.com/eosrio
- https://github.com/eosrio/hyperion-history-api
- https://github.com/eosphere
- https://github.com/eosphere/HeadsUp-Monitoring-Alerts
- https://github.com/eosswedenorg

### Team Member Repos

- https://github.com/igorls
- https://github.com/domiscd
- https://github.com/tccanellas
- https://github.com/joaoocb
- https://github.com/mrlon01
- https://github.com/Rossco99
- https://github.com/xebb82
- https://github.com/coachbjork
- https://github.com/pnx

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/igorls/
- https://www.linkedin.com/in/dominique-deschatre/
- https://www.linkedin.com/in/thiagocanellas/
- https://www.linkedin.com/in/jo%C3%A3o-ot%C3%A1vio-barbosa/
- https://www.linkedin.com/in/jailon-aguiar-b9465124/
- https://www.linkedin.com/in/ross-dold-b75b2b7/
- https://www.linkedin.com/in/ericbjork/
- https://www.linkedin.com/in/anyobservation/
- https://www.linkedin.com/in/henrik-hautakoski

## Development Status

A MVP with simplified architecture and limited features is already being developed with an initially limited scope of allowing Hyperion to send information to a centralized Hub. This also includes part of the SDK that will use this information to automate endpoint selection on the user/developer side.

Hyperion recent versions already include a Health API that checks its own infrastructure and also Leap/Nodeos. https://github.com/eosrio/hyperion-history-api/blob/main/api/routes/v2/health/health.ts

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 35 weeks
- **Full-Time Equivalent (FTE):** 3.30 FTE
- **Total Costs:** 378,630 USD

**Note:** We understand this is an Antelope project that will benefit all chains as it can be used by developers and operators of any chain. That is why we are submitting this project to both EOS Network Foundation and WAX Labs, with a cost division of 70/30 respectively. All values presented here already reflect this cost division. The project will be delivered in any case, even if one of the grants is not approved, as other internal resources from the teams are being allocated and other sources of funding are being sought, but delivery dates may be impacted, and deployment priority will be given to participating chains.

### Milestone 1 — MVP

- **Estimated duration:** 9 weeks
- **FTE:**  2.8
- **Costs:** 85,050 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License  | MIT |
| 0b. | Documentation  | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how operators can turn on the feature and how to connect to Hyperion Hub. |
| 0c. | Testing Guide        | Unit tests covering the core functionalities and a detailed guide on runnning the tests. |
| 0e. | Article              | We will publish at least one **article** and participate in AMAs and other channels to explain the MVP and the future developments to collect feedback from developers. Our target audience will be blockchain engineers and entrepreneurs especially on the Antelope Ecosystem. We will mention the ENF support whenever possible. |
| 1. | Operator Client v0| Hyperion feature to communicate data availability, latency and performance indicators. |
| 2. | QRY Hub              | Receive and aggregate endpoint information. |
| 3. | SDK    | Use locally collected and QRY Hub data to handle endpoint selection. |



### Milestone 2 — SDK 

- **Estimated Duration:** 6 weeks
- **FTE:**  3.10
- **Costs:** 61,740 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how to use the SDK and the Data Client.  |
| 0c. | Testing Guide | Unit tests covering the core functionalities and a detailed guide on runnning the tests. |
| 0d. | Docker | A docker image will be provided allowing for easy deployment of the SDK Connector Microservice.    |
| 0e. | Article | We will publish at least one **article** and participate in AMAs and other channels to promote and explain the SDK. Our target audience will be blockchain engineers and entrepreneurs especially on the Antelope Ecosystem. We will mention the ENF support whenever possible. |
| 1. | Interface Specification | Define how developers will be able to call queries from inside JavaScript/TypeScript.  |
| 2. | Implementation and testing | Deliver a npm package that can be installed by any developer. |
| 3. | Connector Microservice| Create a microservice for endpoint selection and request signing. |
| 4. | Documentation and examples | Documentation will be essential for this delivery |


### Milestone 3 — Web Interface

- **Estimated Duration:** 4 weeks
- **FTE:**  3.5
- **Costs:** 39,200 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will focus on intuitive flows and timely explanations on tooltips. |
| 0c. | Testing Guide |  Unit tests covering the core functionalities and a detailed guide on runnning the tests. |
| 0d. | Docker | A docker image will be provided allowing for easy deployment of local and web interfaces.|
| 0e. | Article | We will publish at least one **article** and participate in AMAs and other channels to promote the Web Interface. Our target audience will be blockchain engineers and entrepreneurs especially on the Antelope Ecosystem. We will mention the ENF support whenever possible. |
| 1. | UX/UI | A clean and intuitive design allowing developers to easily use the tools to access blockchain information. |
| 2. | Backend/API Layer | A backend will manage not only login information from users, but also the connection with the blockchain to register subscription information and allow users to manage subscriptions.  |
| 3. | Frontend | Implementing the interface and connecting to the backend |



### Milestone 4 — Operator Client

- **Estimated Duration:** 8 weeks
- **FTE:**  3.8
- **Costs:** 101,920 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how operators will enable it. |
| 0c. | Testing Guide | Unit tests covering the core functionalities and a detailed guide on runnning the tests. |
| 0e. | Article | We will publish at least one **article** and participate in AMAs focused on infrastructure operators. Our target audience will be blockchain operators on the Antelope Ecosystem. We will mention the ENF support whenever possible. |
| 1. | Key validation module | We will create a module to validate client signature and verify subscription status and usage. |
| 2. | Healthcheck and internal information | Improving upon Hyperion Healthcheck as a reference implementation |
| 3. | Blockchain writing | Operator Client will be responsible for periodically updating clients' usage information.  |
| 4. | HAproxy Plugin | Create a plugin for HAproxy allowing operators to use their current proxy architecture to fulfill QRY requirements for RPC endpoints |



### Milestone 2 — QRY Engine

- **Estimated Duration:** 8 weeks
- **FTE:**  3.4
- **Costs:** 90,720 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide **inline documentation** of the code that explains the contract and components interaction. |
| 0c. | Testing Guide |  Unit tests covering the core functionalities and a formal contract review by a recognized auditing provider. |
| 0e. | Article | We will publish at least one **article** and participate in AMAs and other channels to explain smart contracts and the project as a whole. Our target audience will be blockchain engineers and entrepreneurs especially on the Antelope Ecosystem. We will mention the ENF support whenever possible. |
| 1. | Ricardian Contracts | Contract specification with intent of code for each call.  |
| 2. | Registering actors | Create all the functions for registering actors in the contract.  |
| 3. |  Subscription | Create functions related to creating and managing subscriptions, including usage updates and evaluation |


## Future Plans

QRY's objective is to create a self-sustaining infrastructure ecosystem that will allow operators to coordinate in serving developers. The plan involves a utility token that will be used to access premium tiers of services through paid subscriptions. Token issuance is being designed to be aligned with network growth from the beginning. 

We believe such a project can directly contribute to making the EOS network more robust by creating additional revenue streams that will grow the resources of teams directly involved in the network operation and development.

QRY will be a multi-transport ecosystem and as soon as the reference implementation with Hyperion is stable we will expand to other types of providers and APIs.


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

We have been in close contact with ENF since the beginning and participated in the API+ working group.
