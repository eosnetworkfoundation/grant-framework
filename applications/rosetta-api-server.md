# EOS Network Foundation Grant Proposal

- **Project Name:** Build Rosetta API service
- **Team Name:** Lowkey codes
- **EOS Payment Address:** delightlabs1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** No

## Contact

- **Contact Name:** Bryan RHEE
- **Contact Email:** contact@delightlabs.io
- **Website:** [https://delightlabs.io/](https://delightlabs.io/)

## Project Overview

### Overview

- **Name:** Build Rosetta API service
- **Brief Description:** Parsing actions and matching data in Rosetta API standard for other Antelope integration developers' convenience.
- **Relationship to EOSIO:** This integration would hugely help other engineers (especially in exchanges) to build dApps, and the Antelope ecosystem to be broaden
- **Reason for Interest:** We want to contribute to the infrastructure building field, and Rosetta API support is the best fit for us, full of backend developers

### Project Details

- Build a collector and parser for Antelope's transactions and store our dedicated RDB with keeping txs' history
  - Allow many APIs to support historical data lookup, which off-chain RDB processing is inevitable.
  - We can cover both gRPC and REST connection (prefer gRPC)
- Data source
  - Build from public snapshots of the data depot
  - Use the public endpoint of BPs'.
- Implement the Rosetta server following its API specification
  - Language: Golang on [`rosetta-sdk-go`](https://github.com/coinbase/rosetta-sdk-go)
- Maintain the infrastructure for operation. (Publicize our API server & endpoint)
- Documentation & developer support

Please check our similar works stated in `Additional information`.

### Ecosystem Fit

- Lowering the barrier to entry for developers
  - Who: Anyone who does not have to know the whole specification of Antelope
  - How: Provide the APIs they already know and have integrated before, eliminating the need to learn Antelope-specific API.
  - Where would be good: Exchange developer, Blockchain statistics application (CoinGecko, CMC, etc.), Multichain bridging project, etc.

## Team

### Team members

- **Team Leader:** Yeon HWANG
- Joon LEE
- Young LEE
- Derick MOON
- Sooyoung HA
- Bryan RHEE
- Joowon YUN
- Maro KIM

### Legal Structure

- **Registered Legal Entity:** Lowkey codes
- **Registered Address:** Hyecheon Bldg 1126-7 (11th flr), 354 Gangnam-daero, Gangnam, Seoul, SOUTH KOREA

### Team Experience

- Before blockchain, well experience in OS & emulator development (Tizen of Samsung)
- Much experience in validating Cosmos SDK-based projects & ETH layer 2 blockchains
- Experience in blockchain core development (connect between Tendermint & WASM execution engine)
- 1st dApp on Terra(now Terra classic): Terraswap - enough experience of WASM-based smart contract development & action processing
- Mainnet technical partner of Xpla (former C2X)
- EOSIO-based project-building experience (Polaris of Chain Partners, mentor & participant of EOSIO hackathon)

### Team Org Repos

[https://github.com/DELIGHT-LABS](https://github.com/DELIGHT-LABS)

- Terraswap
  - [Frontend](https://github.com/terraswap/terraswap-web-app)
  - [Offchain backend service](https://github.com/terraswap/terraswap-service)
  - [Contract - Terra classic](https://github.com/terraswap/classic-terraswap)
  - [Contract - Terra 2.0](https://github.com/terraswap/terraswap)
- XPLA chain
  - [Mainnet code](https://github.com/xpladev/xpla)
  - [Token migration frontend (Terra classic -> mainnet)](https://github.com/xpladev/token-migration-web-app)
  - [Token migration relayer (Terra classic -> mainnet)](https://github.com/xpladev/warp-relayer)
- Data API service
  - [Terraswap on Terra classic](https://github.com/DELIGHT-LABS/terraswap-graph)
  - [Unified service for Cosmos-SDK based chain](https://github.com/DELIGHT-LABS/cosmwasm-etl) (Private, in development, I'll add you if you need to check it)

### Team Member Repos

- Yeon HWANG: [https://github.com/caramis](https://github.com/caramis)
- Joon LEE: [https://github.com/jbamlee](https://github.com/jbamlee)
- Young LEE: [https://github.com/jhlee-young](https://github.com/jhlee-young)
- Sooyoung HA: [https://github.com/yoosah](https://github.com/yoosah)
- Bryan RHEE: [https://github.com/psy2848048](https://github.com/psy2848048)
- Joowon YUN: [https://github.com/JoowonYun](https://github.com/JoowonYun)
- Maro KIM: [https://github.com/honeymaro](https://github.com/honeymaro)

### Team LinkedIn Profiles (if available)

- Yeon HWANG: [https://www.linkedin.com/in/yeon-hwang/](https://www.linkedin.com/in/yeon-hwang/)
- Joon LEE: [https://www.linkedin.com/in/joonbum-lee-173354112/](https://www.linkedin.com/in/joonbum-lee-173354112/)
- Young LEE: [https://www.linkedin.com/in/jihyunglee/](https://www.linkedin.com/in/jihyunglee/)
- Derick MOON: [https://www.linkedin.com/in/sanghoon-moon-79b5a81b2/](https://www.linkedin.com/in/sanghoon-moon-79b5a81b2/)
- Sooyoung HA: [https://www.linkedin.com/in/sooyoung-ha-9a0195140/](https://www.linkedin.com/in/sooyoung-ha-9a0195140/)
- Bryan RHEE: [https://www.linkedin.com/in/psy2848048/](https://www.linkedin.com/in/psy2848048/)
- Joowon YUN: [https://www.linkedin.com/in/joowon-yun-520a1557/](https://www.linkedin.com/in/joowon-yun-520a1557/)
- Maro KIM: [https://www.linkedin.com/in/maro/](https://www.linkedin.com/in/maro/)

## Development Status

Not yet started before, but we have a similar experience, [Data API service](https://github.com/DELIGHT-LABS/cosmwasm-etl)

About our development ability, 7 developers (1 FE, 1 data, 5 BE & system) and 1 product designer are working at DELIGHT LABS. We have full experience in Cosmos SDK projects - both validation & dApp building. Especially, we validate 10+ projects, including Terra classic, Terra 2.0, ORBS, Xpla, Oasis protocol, Fetch.ai, Findora, Casperlabs, SSV, Rizon, Medibloc, and so on, and we build & operate 1st dApp and AMM DEX - Terraswap on both of Terra classic & 2.0.

As mentioned above, we have enough experience in the blockchain industry, and now we have started to expand our area to Antelope, which is our homeland. With not only our blockchain core experience but also enough knowledge in CS background, we will contribute to and build a strong basis on the Antelope ecosystem.

- Twitter: [https://twitter.com/delightlabs_io](https://twitter.com/delightlabs_io)

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 28 weeks development + 1-year support after deploy
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** USD 230K

### Milestone 1 - Spec survey & architecting

- **Estimated duration:** 8 weeks
- **FTE:** 1
- **Costs:** USD 25K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Although the actual code is not written in this stage, we will provide brief documentation in each expected module. Also, Brief README will be ready |
| 0c. | Testing Guide | Makefile script & Github action will be ready |
| 1 | Data provider meeting | Research how to import data from the data depot and decide how to import |
| 2 | Data demander meeting | Make meetings and gather their demands on API |

### Milestone 2 - Data API & Construction API

- **Estimated Duration:** 8 weeks
- **FTE:**  2
- **Costs:** USD 50K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** in README |
| 0c. | Testing Guide | Test will be available through Makefile. Target coverage: >= 70% |
| 0d. | Docker | Daemon service of Dockerfile |
| 1 | API service | Implement Data API & Construction API without off-chain data import<br/>- `/account/balance`, `/account/coin` (no support `"block_identifier"` optional parameter)<br/>- `/block`<br/>- `/construction/combine`, `/construction/hash`, `/construction/metadata`, `/construction/parse`, `/construction/payloads`, `/construction/preprocess`, `/construction/submit`<br/>- `/network/list`, `/network/options`, `/network/status`<br/> |

### Milestone 3 - Indexer API

- **Estimated duration:** 8 weeks
- **FTE:** 2
- **Costs:** USD 75K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** in README |
| 0c. | Testing Guide | Test will be available through Makefile. Target coverage: >= 70% |
| 0d. | Docker | Daemon service of Dockerfile |
| 1 | Mock service of the data provider | Get their data spec and make a mock service. It will be used for better testing & development |\
| 2 | Data subscribe module | Subscribe data from the data depot & reorganize into the dedicated RDB |
| 3 | API service | Apply aggregator for historical lookup support<br/>- `/account/balance`, `/account/coin` supporting `"block_identifier"` optional parameter<br/>- `/block/transaction`<br/>- `/events/blocks`<br/>- `/search/transactions` |

### Milestone 4 - Documentation & its development

- **Estimated duration:** 4 weeks
- **FTE:** 1
- **Costs:** USD 7.5K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | API specification will be written in both of self-serviced application and web application |
| 0c. | Testing Guide | Test will be available through Makefile. Target coverage: >= 70% |
| 0d. | Docker | Daemon service of Dockerfile |
| 1 | Document service | - Improved GitHub MD documentation<br/>- Document service page (one of Gitbook, Hugo, etc)<br/>- Swagger |

### Milestone 5 - Code Audit

- **Estimated duration:** 4 weeks
- **FTE:** 1
- **Costs:** USD 50K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | API specification will be written in both of self-serviced application and web application |
| 0c. | Testing Guide | Test will be available through Makefile. Target coverage: >= 70% |
| 0d. | Docker | Daemon service of Dockerfile |
| 1 | Audit report | Audit from reliable orgs. Get any `safe`-level remark<br/>The cost is estimated number and it will be revised if there is any change in actual cost. |

### Milestone 6 - Developer / exchange support

- **Estimated duration:** 1 year
- **FTE:** 1
- **Costs:** USD 22.5K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | API specification will be written in both of self-serviced application and web application |
| 0c. | Testing Guide | Test will be available through Makefile. Target coverage: >= 70% |
| 0d. | Docker | Daemon service of Dockerfile |
| 1 | Technical support | Bugfix, feature update, following up further Antelope version upgrade, answer to incoming questions |

## Future Plans

- Once the API server is deployed, we will operate with code upgrade for at least a year. Moreover, we will support bugfix for enough years.
- Currently, very few EOSIO-based tokens are listed on CEXes. But we hope many Antelope-based tokens would be listed as easily as ERC20. Native tokens as well as others would be supported equally on `/account/balance`.
- We will also influence our works and give much help to relayers from/to Antelope to check Tx state tracking.

## Additional Information

- Our similar reference - [Cosmwasm-ETL](https://github.com/DELIGHT-LABS/cosmwasm-etl) (private, in development)
  - For unifying data processing codes to cover all DELIGHT LABS' DEXes built on Cosmwasm-based projects
  - Collector: Tx stores on AWS S3
  - Parser: JSON tx parsing into DTO, and store into DB
  - Aggregator: process RDB for providing personal stats
  - Provide data service on Graphql
  - UI implementation: [Terraswap dashboard on Terra classic](https://app-classic.terraswap.io/)

**How did you hear about the Grants Program?** From one member of the committee and had a F2F meeting
