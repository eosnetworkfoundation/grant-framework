# EOS Network Foundation Grant Proposal

- **Project Name:** Build Rosetta API service
- **Team Name:** DELIGHT LABS
- **EOS Payment Address:** TBF
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** 0

## Contact

- **Contact Name:** Bryan RHEE
- **Contact Email:** contact@delightlabs.io
- **Website:** [https://delightlabs.io/](https://delightlabs.io/)

## Project Overview

### Overview

- **Name:** Build Rosetta API service
- **Brief Description:** Parsing actions, matching data in Rosetta API standard, and make other Antelope integration developer be comfortable
- **Relationship to EOSIO:**  This integration would hugely help of other developers (especially in exchanges) to integrate with, and wish to make broaden EOSIO ecosystem
- **Reason for Interest:** We want to contribute in non-token area, like infrastructure. Among items, this item would fit us, which is full of backend developers

### Project Details

- Build collector, parser on EOSIO's txs and store our dedicated RDB with keeping txs' history
  - Many API support historical data lookup, then offchain RDB processing is inevitable.
  - Please check our similar work. (Stated in Additional information)
  - We can cover both available in gRPC or REST connection (prefer gRPC)
- Data source
  - Build from public snapshots of the data depot
  - Use public endpoint of BPs'
- Implement Rosetta server following its API specification
  - Language: Golang on [`rosetta-sdk-go`](https://github.com/coinbase/rosetta-sdk-go)
- Maintain the infrastructure for operation. (Publicize our API server & endpoint)
- Documentation & developer support

### Ecosystem Fit

- Make lower barrier to developers
  - Who: Who don't have to know the knowledge of Antelope but needs some information of the Antelope (e.g. )
  - How: Provide the APIs which they already know and have integrated before. Don't have to learn Antelope-specific API.
  - Where would be good: Exchange developer, Blockchain statistics application (CoinGecko, CMC, etc), Multichain bridging project, etc

## Team

### Team members

- **Team Leader:** Yeon HWANG

### Legal Structure

- **Registered Legal Entity:** Organized as a limited company. Fully supports social security & taxation service
- **Registered Address:** Hyecheon Bldg 1126-7 (11th flr), 354 Gangnam-daero, Gangnam, Seoul, SOUTH KOREA

### Team Experience

- Before blockchain, well experience in OS & emulator development (Tizen)
- Much experience in validating Cosmos SDK based projects & ETH layer 2 blockchains
- Experience in blockchain core development (connect between Tendermint & WASM execution engine)
- 1st dApp on Terra(now Terra classic): Terraswap - enough experience of WASM-based smart contract development & action processing
- Mainnet technical partner of Xpla (former C2X)
- EOSIO based project building experience (Polaris of Chain Partners, mentor & participant of EOSIO hackathon)

### Team Org Repos

[https://github.com/DELIGHT-LABS](https://github.com/DELIGHT-LABS)

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

7 developers (1 FE, 1 data, 5 BE & system) and 1 product designer are working in DELIGHT LABS. We had full experience in Cosmos SDK projects - both of validation & dApp building. Especially, we validate 10+ projects including Terra classic, Terra 2.0, ORBS, Xpla, Oasis protocol, Fetch.ai, Findora, Casperlabs, SSV, Rizon, Medibloc, and so on, and we build & operate 1st dApp and AMM DEX - Terraswap on both of Terra classic & 2.0.

As like mentioned above, our team has enough experience in blochchain industry, and now we start to expand our area to Antelope(and come back to our homeland). With not only our blockchain core experience but also enough knowledge in CS background, we will contribute and build strong basis on Antelope ecosystem.

- Twitter: [https://twitter.com/delightlabs_io](https://twitter.com/delightlabs_io)

## Development Roadmap

### Overview

- **Total Estimated Duration:** 28 weeks development + 1 year support after deploy

### Milestone 1 - Spec survey & architecting

#### Action items

- Make meetings and gather their demands on API
- Research how to import data from the data depot and decide how to import
- List expected unit tests
- Integrate Github action & Makefile

#### Expected outcome

- Module-level documentation inside the code repo & README outline
  - Including comments above the expected methods
  - Including data importing plan
- Github action config in the code repo
- Meeting notes if there is any talk from demanding sides
- Makefile script

- **Estimated duration:** 8 weeks
- **FTE:** 1
- **Costs:** USD 25K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License |  MIT  |
| 0b. | Documentation | Module level documentation & README outline |
| 0c. | CI test | No working unit test but make the code be ready on Makefile & Github action |

### Milestone 2 - Data API & Construction API

#### Action items

- Implement Data API & Construction API without off-chain data import
  - `/account/balance`, `/account/coin` (no support `"block_identifier"` optional parameter)
  - `/block`
  - `/construction/combine`, `/construction/hash`, `/construction/metadata`, `/construction/parse`, `/construction/payloads`, `/construction/preprocess`, `/construction/submit`
  - `/network/list`, `/network/options`, `/network/status`
  - All unit tests covering the above
- HTTPS wrapped API server with daemon service or docker

#### Expected outcome

- Buildable code & building Makefile script
- Callable HTTPS API server attached one of Antelope-based blockchain
- Codecov badge with >= 70%

- **Estimated duration:** 8 weeks
- **FTE:** 2
- **Costs:** USD 50K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License |  MIT  |
| 0b. | API server | HTTPS wrapped API server. The endpoints stated above should work |
| 0c. | Code | Ready-to-build state |
| 0d. | CI test | Unit test coverage >= 70% |

### Milestone 3 - Indexer API

#### Action items

- Subscribe data from the data depot & reorganize in the dedicated RDB
- Apply aggregator for historical lookup support
  - `/account/balance`, `/account/coin` supporting `"block_identifier"` optional parameter
  - `/block/transaction`
  - `/events/blocks`
  - `/search/transactions`
  - All unit tests covering the above

#### Expected outcome

- Including the items on Milestone 2
- Internal RDB
- Schema create SQL

- **Estimated duration:** 8 weeks
- **FTE:** 2
- **Costs:** USD 75K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License |  MIT  |
| 0b. | API server | HTTPS wrapped API server. Historical lookup is also supported |
| 0c. | Code | Ready-to-build state |
| 0d. | CI test | Unit test coverage >= 70% |

### Milestone 4 - Documentation & its development

#### Action items

- Detailing MD documentation and improving its quality
- Doc service (Hugo, Gitbook, etc) & Swagger
  - JSON RPC schema of each endpoint
  - Build instruction
- Add some CLI interfaces if needed or any demand comes

#### Expected outcome

- Improved Github MD documentation
- Document service page
- Swagger

- **Estimated duration:** 4 weeks
- **FTE:** 1
- **Costs:** USD 7.5K

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License |  MIT  |
| 0b. | Docs service | Docs web application which is accesible at like rosetta-docs.antelope.delightlabs.io |
| 0c. | Swagger | Ready-to-build state |

### Milestone 5 - Code audit & Developer / exchange support

#### Action items

- Execute code audit
  - Bid more than 2 reliable orgs
- Continuous developer & exchange support
- Keep operating API server
  - With data processor to RDB
  - Communicating one of Antelope-based blockchain

#### Expected outcome

- Audit report
- Continuous developer & exchange support
- Running API server communicating one of Antelope-based blockchain

- **Estimated duration:** 1 year
- **FTE:** 1
- **Costs:** USD 22.5K + Audit cost (expected around USD 50K)

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | API server | HTTPS wrapped API server. Historical lookup is also supported |
| 0c. | Audit report | Audit from reliable orgs. Get a `safe` remark |

## Future Plans

- Once the API server is deployed, we will operate at least a year with code upgrade. Moreover, we will support bugfix with enough years.
- Currently, very few EOSIO-based tokens are listed on CEXes. But we wish that many Antelope-based tokens would be easily listed, easy like ERC20. Not only network token like EOS, but also other tokens would be supported equally on `/account/balance`.
- We will also influence our works and give many helps to relayers from/to Antelope to check Tx state tracking.

## Additional Information

- Our similar reference - [Cosmwasm-ETL](https://github.com/DELIGHT-LABS/cosmwasm-etl) (private, now in development)
  - For unifying data processing codes to cover all DELIGH LABS' DEXes built on Cosmwasm-based projects
  - Collector: Tx stores on AWS S3
  - Parser: JSON tx parsing into DTO, and store into DB
  - Aggregator: process RDB for providing personal stats
  - Provide data service on Graphql
  - UI implementation: [Terraswap dashboard on Terra classic](https://app-classic.terraswap.io/)

**How did you hear about the Grants Program?** From one member of the committee, and had a F2F meeting
