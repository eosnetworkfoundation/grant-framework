# EOS Network Foundation Grant Proposal

- **Project Name:** Go Antelope SDK (`go-antelope-sdk`)
- **Team Name:** Junhang LEE
- **EOS Payment Address:** haydinrvgage
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/psy2848048/go-antelope-sdk

## Contact

- **Contact Name:** Junhang LEE
- **Contact Email:** psy2848048@gmail.com
- **Website:** https://github.com/psy2848048

## Project Overview

### Overview

- **Name:** Go Antelope SDK
- **Brief Description:** A Golang library that provides easy interacts with Antelope blockchain
- **Relationship to EOSIO:** Peronal cotributor. Previous a mentor of EOS hackathon & a builder on EOSIO
- **Reason for Interest:** I've seen Antelope SDK is written in some launguage but net yet in Golang

### Project Details

Not only in blockchain core but also in backend services Golang is now broadly used. The language is specialized in parallelism by a special feature, Goroutine, which is more improved implementation than general Coroutine. As there is noy yet SDK written in Golang, I would like to propose this contribution as following steps:

1. REST API wrapping: Everything are executable by REST API (except signing). For fast deliver, try to wrap all APIs first and deploy.
1. Some API can be replaced into local processing. (e.g. `abi_json_to_bin`) Make it working in local.
1. List trust BPs from their public information and developer in case of BP API node is temporarily unavailable.
1. Build a documentation application code with self-deploying guide
1. Give access to the community and support for library users & SDK contributors.

As this is a personal contribution, I set the goal of this contribution as the fastest deploy with minimum implementation. I believe the power of Antelope community and our community can maintain this SDK better than what I do if it needs to be improved.

### Ecosystem Fit

The diversity of lauguage is very important. According that, the more language in the ecosystem has, it is better. Like Python, Golang is not really hard to learn but has strong features. Therefore, the size of Golang ecosystem goes bigger as time goes by. For making bigger Antelope, Antelope needs to cover Golang.

## Team

### Team members

- **Team Leader:** Junhang LEE

### Legal Structure

- **Registered Legal Entity:** Junhang LEE
- **Registered Address:** Sannaemaeul 8th 805-903, 28 Chungam-ro, Paju, Gyeonggi-do, SOUTH KOREA

### Team Experience

- Mentor of EOSIO hackathon (Sydney)
- Both of blockchain core & dApp development experience

### Team Org Repos

- [Repo](https://github.com/psy2848048)
- [Example repos for my EOSIO lecture](https://github.com/psy2848048/deveos)

### Team Member Repos

- [Repo](https://github.com/psy2848048)

### Team LinkedIn Profiles (if available)

[Profile](https://www.linkedin.com/in/psy2848048/)

## Development Status

[Working repo](https://github.com/psy2848048/go-antelope-sdk) (private, org will be moved once the wrapping is finished)

In the past, I worked a [draft Python library](https://github.com/psy2848048/pyeosio) for my EOSIO lecture. It only wraps API without internal sign feature. (In that time, local wallet API server is available and anyone can make sign from there.)

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 4 weeks
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 10,000 USD

### Milestone 1 - Write SDk code matching with API

- **Estimated duration:** 3 weeks
- **FTE:**  1
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Inline comment inside the module, and brief README |
| 0c. | Testing Guide | Available in Makefile script & Github action. Coverage >= 70% |
| 1. | SDK code | Ready-to-use state from other Golang projects. Cover all APIs listed on [Chain API](https://developers.eos.io/manuals/eos/latest/nodeos/plugins/chain_api_plugin/api-reference/index), [Producer API](https://developers.eos.io/manuals/eos/latest/nodeos/plugins/producer_api_plugin/api-reference/index), [Net API](https://developers.eos.io/manuals/eos/latest/nodeos/plugins/net_api_plugin/api-reference/index), [DB size API](https://developers.eos.io/manuals/eos/latest/nodeos/plugins/db_size_api_plugin/api-reference/index), and [Trace API](https://developers.eos.io/manuals/eos/latest/nodeos/plugins/trace_api_plugin/api-reference/index) |

### Milestone 2 - Self-serviced doc application

- **Estimated Duration:** 1 week
- **FTE:**  1
- **Costs:** 2,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Inline comment inside the module, and brief README |
| 0c. | Testing Guide | Available in Makefile script & Github action. Coverage >= 70% |
| 1. | Self-serviced doc application | Write self-serviced documentation MD codes (in Gitbook, Hugo, and etc) |

## Future Plans

Once it is finished, I'm expected to be transferred the ownership of the repository to Antelope org. And it will be opened & used to any other Golang-based projects. I'm also going to use this work to any other Golang-based works on Antelope, and maintain this repository for a while. But I'm looking forward this library to improving itself from any member of Antelope ecosystem.

## Additional Information

**How did you hear about the Grants Program?** From members of the committee
