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
- **Brief Description:** Prior to building Rust Antelope CDT, we want to check the cost effective plan among the cases we thought.
- **Relationship to EOSIO:** More than C++, many developers using other languages could access & come into Antelope ecosystem and become to be an Antelope builder. We set the first target to Rust.
- **Reason for Interest:** We want to contribute in non-token area, like infrastructure. As our past experience of building on EOSIO, it run so fast but it seemed that few developers can understand and be a builder. C++ was essential language 10+ years ago, but the trend moves as time goes by. For making bigger builder pool, modern language support & language diversity are essential.

### Project Details

Prior to building Rust Antelope CDT, we want to check these 2 parts and expected direction to implement:

1. Sufficient compatibility between EOS VM and wasm binary from Wasmer-based compiler
    - Rust `antelope.cdt` API implementation
1. Lack of compatibility between EOS VM and wasm binary from Wasmer-based compiler exists
    - Devleoping compiler first -> Rust `antelope.cdt` API implementation
    - Or Wasmer VM integration on Antelope

As the following plan is quite different among each case, we decided to devide the research proposal.

### Ecosystem Fit

By this implementation, Antelope can broad to one more contract language, Rust. And this would be the basis to broad to more language ecosystem. As recently WASM can be made from Golang and Javascript, we look forward Antelope to cover more popular language users.

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

NOTE: There is no official general Rust LLVM. [This standardization project](https://rust-lang.github.io/compiler-team/working-groups/llvm/) is still in incubation status.

**Assumptions**: For cost-effective building, we want to build from the many works of Wasmer, although Antelope doesn't need to mount Wamser.

#### Cases

1. If `IR ≅ IR'` and `API ≅ API'`
    - We can directly start from Wasmer's implementation
      - Implement Antelope-specific data structure and API of `eosio.cdt` (Like table, vector, and etc)
1. Else if `IR ≅ IR'` and `API != API'`
    - Implement a compiler first, which works for adjusting WASM API interface from Wasmer spec to EOSVM spec
    - Aftern then, do (1)
1. Else (`IR != IR'` and `API != API'`)
    - Mounting Wasmer on Antelope would be the cheapest
    - Mounting Wasmer with the existing state DB compabilization, and do (1)
    - [Draft proposal of this case](https://github.com/DELIGHT-LABS/grant-framework/blob/docs/wasmer-integration/applications/wasmer-integration.md)

### Why Wasmer?

Performance is placed in the top tier. [benchmark 2021](https://00f.net/2021/02/22/webassembly-runtimes-benchmarks/) And it has the biggest ecosystem among WASM VM. This project supports many languages accordingly.

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 1 month
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 10,000 USD

### Milestone 1 — Research the difference between EOSVM and Wasmer

- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 10,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 1 | Research report | Will check and deliver its result of comparison language-LLVM compiling spec and WASM API spec of EOSVM and Wasmer<br/>A report and following proposal will be provided |

## Future Plans

Following proposal will be provided according to this research result.

## Additional Information

**How did you hear about the Grants Program?** Personal recommendation
