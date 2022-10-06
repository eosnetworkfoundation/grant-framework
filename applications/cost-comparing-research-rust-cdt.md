# EOS Network Foundation Grant Proposal

- **Project Name:** Research for building Rust Antelope CDT
- **Team Name:** Lowkey codes
- **EOS Payment Address:** delightlabs1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** N/A

## Contact

- **Contact Name:** Bryan RHEE
- **Contact Email:** contact@delightlabs.io
- **Website:** [https://delightlabs.io/](https://delightlabs.io/)

## Project Overview

### Overview

- **Name:** Research for building Rust Antelope CDT
- **Brief Description:** Checking the most cost-effective plan among the cases we thought of is mandatory for building Rust Antelope CDT.
- **Relationship to EOSIO:** Many developers using other languages besides C++ will be able to join the Antelope ecosystem and become its builders. We set the first target to Rust.
- **Reason for Interest:** Lack of language support despite the extremely fast processing speed leaves something to be desired, and we anticipate that modern language support & language diversity help improve this point and expand builder pool. Additionally, in terms of our interests, we would like to contribute to technology-focused areas.


### Project Details

The project will investigate the following two parts in order to verify the suitable direction to implement:

1. Sufficient compatibility between EOS VM and wasm binary from [Wasmer](https://github.com/wasmerio/wasmer)-based compiler
    - Rust `antelope.cdt` API implementation
1. Lack of compatibility between EOS VM and wasm binary from [Wasmer](https://github.com/wasmerio/wasmer)-based compiler exists
    - Developing compiler first -> Rust `antelope.cdt` API implementation
    - Or Wasmer VM integration on Antelope

This research has been written as a separated proposal since the follow-up plan will be quite different by the result.

### Ecosystem Fit

This implementation allows Antelope to extend one more contract language, Rust, and this would be the cornerstone of the multiple language support in the Antelope ecosystem. As WASM can be built with Golang and Javascript recently, we look forward Antelope to embracing more other languages' users.

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

### Description of the expected scenarios

```plain
┌──────────────┐             ┌──────────────┐            ┌─────────────────┐
│              │  eosio-llvm │              │            │      API        │
│   EOSIO C++  │  ───────►   │      IR      │   ───────► │    EOSVM IR     │
│              │             │              │            │ Interface set   │
└──────────────┘             └──────────────┘            └─────────────────┘

┌──────────────┐  Wasmer's   ┌──────────────┐            ┌─────────────────┐
│              │ rust-llvm   │              │            │      API'       │
│ Wasmer Rust  │  ───────►   │     IR'      │   ───────► │   Wasmer IR     │
│              │             │              │            │ Interface set   │
└──────────────┘             └──────────────┘            └─────────────────┘
```

NOTE: There is no official general Rust LLVM. This standardization project is still in incubation status.

Assumptions: For cost-effective building, we want to build from the many works of Wasmer, although Antelope doesn't need to mount Wamser.

#### Cases

1. If `IR ≅ IR'` and `API ≅ API'`
    - We can directly start from Wasmer's implementation
        - Implement Antelope-specific data structure and API of `eosio.cdt` (Like table, vector, etc.)
1. Else if `IR ≅ IR'` and `API != API'`
    - Implement a compiler, which works for adjusting WASM API interface from Wasmer spec to EOSVM spec
    - After then, start (1)
1. Else (`IR != IR'` and `API != API'`)
    - Mount Wasmer on Antelope would be the cheapest
    - Mount Wasmer, make compatible with the existing state DB, and work on (1)
    - [Draft proposal of this case](https://github.com/DELIGHT-LABS/grant-framework/blob/docs/wasmer-integration/applications/wasmer-integration.md)

### Why Wasmer?

Performance of Wasmer is placed in the top tier. See [benchmark 2021](https://00f.net/2021/02/22/webassembly-runtimes-benchmarks/). Also, it has the biggest ecosystem among WASM VM and supports many languages accordingly.

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 1 month
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 10,000 USD

### Milestone 1 — Research the difference between EOSVM and Wasmer

- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 10,000 USD

| ID  | Deliverable     | Specification                                                                                                            |
|-----|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| 0a. | License         | MIT                                                                                                                      |
| 1   | Research report | Comparison of language-LLVM compilation spec and WASM API spec of EOSVM and Wasmer<br/>A report and a follow-up proposal |

## Future Plans

There will be a follow-up proposal for supporting Rust CDT according to this research result.

## Additional Information

**How did you hear about the Grants Program?** Personal recommendation
