# EOS Network Foundation Grant Proposal

- **Project Name:** API Transaction Lifecycle
- **Team Name:** OCI, Object Computing, Inc.
- **EOS Payment Address:**  N/A
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3

## Project Overview

This project is in response to the API Blue Paper section titled: API Transaction Lifecycle.

### Overview

- **Name:** API Transaction Lifecycle
- **Brief Description:** The API Transaction Lifecycle project is designed to provide EOSIO users clear visibility into transaction status at each step in the process. Four key enhancements to the EOSIO API code are included in this project: a) Transaction Retry, b) Transaction Finality API, c) Transaction Resource Cost Estimation, d) Subjective Billing Improvements.
- **Relationship to EOSIO:** The core EOSIO APIs to be improved through this project are critical components of the EOSIO code that allows applications to interact with the blockchain.
- **Reason for Interest:** The OCI team has been involved in core EOSIO development since 2017 and has expertise in this area. These enhancements will increase the usability and functionality of the APIs.

### Project Details

- **A. Transaction Retry:** API nodes will monitor transactions as they enter the system and ensure they are resubmitted into the system if they are not processed in a configurable time period. This feature will establish a pool of known incoming transactions and monitor their inclusion into the blockchain. Once the system reaches an acceptable level of confidence that a transaction has been included in a block, the transaction can be pruned from the pool. If a transaction is identified as missing from the blockchain based on the given criteria, the Transaction Retry feature will attempt to resubmit the transaction to the network for inclusion in future blocks until the point at which the transaction expires.
- **B. Transaction Finality Status:** API nodes will monitor transactions as they enter the system and provide a new API method to report transaction status.
- **C. Transaction Resource Cost Estimation:** API nodes will provide an estimate of resources (central processing unit (CPU), random access memory (RAM), and internet bandwidth (NET)) to perform a transaction when a transaction is sent to a new compute_transaction endpoint. The transaction will be applied subjectively to the local chain to calculate resource costs like CPU and NET and determine the resulting deltas in RAM usage. The response will be returned to the client to inform them of the costs associated with the given transaction data.
- **D. Subjective Billing Improvements:** API nodes will provide an added leeway per account that allows a more permissive “subjective billing” rate (rate of utilization) in order to provide a better user experience while maintaining system integrity. The existing subjective CPU decay window will be made configurable from the existing hard-coded value of 24 hours to allow node operators to provide a more relaxed subjective CPU penalty to users. The existing `disable-subjective-account-billing` function will be expanded to also apply to the 3-strike rule, allowing block producers to prevent abnormal transaction loss for accounts expected to sometimes fail during production.

### Ecosystem Fit

- This project fits into the EOSIO Core code.
- Target Audience: EOSIO application and SDK developers
- The project improves the usability of the EOSIO APIs in multiple ways
- We are not aware of other projects similar to this in the EOSIO ecosystem

## Team

### Team members

- **Lead:** Brian Johnson
- Kevin Heifner
- Jonathan Giszczak
- Chris Gundlach
- Huang-Ming Huang
- Alice C. Dames (PM)
- John W. Schultz (DM)

### Contact

- **Contact Name:** Dan Fedj
- **Contact Email:** fedjd@objectcomputing.com
- **Website:** https://objectcomputing.com/

### Legal Structure
- **Registered Legal Entity:** Object Computing, Inc.
- **Registered Address:** 12140 Woodcrest, Executive Dr., Ste 300, St. Louis, MO 63141

### Team Experience

The OCI team has been involved in almost all development aspects of the EOSIO code base since 2017. Multiple members of the OCI team have worked on the EOSIO code base, and Brian Johnson and Kevin Heifner are top contributors to the EOSIO repo. 

### Team Org Repos

- https://github.com/objectcomputing/
- https://github.com/objectcomputing/OpenDDS
- https://github.com/micronaut-projects/micronaut-core
- https://github.com/grails/grails-core

### Team Member Repos
- https://github.com/brianjohnson5972
- https://github.com/heifner
- https://github.com/jgiszczak
- https://github.com/cj-oci
- https://github.com/huangminghuang

### Team LinkedIn Profiles

- https://www.linkedin.com/in/brian-johnson-a7740612/
- https://www.linkedin.com/in/heifner/ 
- https://www.linkedin.com/in/jonathan-giszczak/ 
- https://www.linkedin.com/in/ciju-john-4271789/
- https://www.linkedin.com/in/clayton-calabrese-1175b6122/
- https://www.linkedin.com/in/christopher-gundlach-34250554/
- https://www.linkedin.com/in/huang-ming-huang-87670031/
- https://www.linkedin.com/in/alicedames/
- https://www.linkedin.com/in/john-w-schultz-78465b16/

## Development Status

- https://github.com/eosnetworkfoundation/mandel/tree/feature/oci_api_phase1
- [EOS API Blue Paper](https://medium.com/eos-network-foundation/api-blue-paper-e78c0be0d878)
- conversations related to this project with stakeholders from the EOS Network Foundation (Yves La Rose discussed).

## Development Roadmap

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):**  3 not including PM
- **Total Costs:** $380,000 USD

### Milestone 0 - Initiate Project

- **Estimated duration:** 1 week
- **FTE:**  2
- **Costs:** $50,000 USD

### Milestone 1 - Release Candidates: a) Transaction Retry, b) Transaction Finality Status

- **Estimated duration:** 12 weeks
- **FTE:**  2
- **Costs:** $150,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | OCI will provide documentation of the APIs in Markdown, as well as documentation suitable for release notes.  |
| 0c. | Unit Tests | Core functions will be fully covered by unit tests to ensure functionality and robustness. |
| 0d. | Integration Tests | Integration tests will be developed, including new and modified tests. |
| 1. | EOSIO API Transaction Retry | Nodes will monitor transactions as they are sent into the system and ensure they are resubmitted into the system if they are not processed in a configurable time period. This feature will establish a pool of known incoming transactions and monitor their inclusion into the blockchain. Once the system reaches an acceptable level of confidence that a transaction has been included in a block, the transaction can be pruned from the pool. If a transaction is identified as missing from the blockchain based on the given criteria, the system will attempt to resubmit the transaction to the network for inclusion in future blocks until the point at which the transaction expires. |  
| 2. | EOSIO API Transaction Finality Status | Nodes will monitor transactions as they are sent into the system and will provide a new API method to report transaction status. |  


### Milestone 2 - Release Candidates: c) Transaction Resource Estimation, d) Subjective Billing Improvements

- **Estimated Duration:** 8 weeks
- **FTE:**  2
- **Costs:** $100,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | OCI will provide documentation of the APIs in Markdown, as well as documentation suitable for release notes.  |
| 0c. | Unit Tests | Core functions will be fully covered by unit tests to ensure functionality and robustness. |
| 0d. | Integration Tests | Integration tests will be developed, including new and modified tests. |
| 1. | EOSIO Transaction Resource Cost Estimation | Nodes will provide an estimate of resources (central processing unit (CPU), random access memory (RAM), and internet bandwidth (NET)) to perform a transaction when a transaction is sent to compute_transaction. The transaction will be applied subjectively to the local chain to calculate resource costs like CPU and NET and determine the resulting deltas in RAM usage. The response will be returned to the client to inform them of the costs associated with the given transaction data. |  
| 2. | EOSIO Subjective Billing Improvements | Nodes will provide an added leeway per account that allows a more permissive “subjective billing” rate (rate of utilization) in order to provide a better user experience while maintaining system integrity. The existing subjective CPU decay window will be made configurable from the existing hard-coded value of 24 hours to allow node operators to provide a more relaxed subjective CPU penalty to their users. The existing `disable-subjective-account-billing` function will be expanded to also apply to the 3-strike rule, allowing block producers to prevent abnormal transaction loss for accounts expected to sometimes fail during production. |  

### Milestone 3 - Project Completion

- **Estimated Duration:** 1 week
- **FTE:**  2
- **Costs:** $80,000 USD



## Future Plans

- Only support for the API Transaction Lifecycle is included in this project; additional, separate support and enhancement projects as outlined in the ENF's blue papers are planned following completion of this one.
- OCI intends to bid on future ENF projects through the Grant Framework.


## Additional Information

**How did you hear about the Grants Program?** We learned about the Grants Program from a member of the EOS Network Foundation.

