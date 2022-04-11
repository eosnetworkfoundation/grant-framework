# EOS Network Foundation Grant Proposal

- **Project Name:** API Transaction Lifecycle
- **Team Name:** OCI, Object Computing, Inc.
- **Payment Address:**  N/A
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3

## Project Overview

This project is is in response to the API Blue Paper section titled: API Transaction Lifecycle.

### Overview

Please provide the following:

- Name: API Transaction Lifecycle
- Brief Description: The API Transaction Lifecycle project consists of four main enhancements to the EOSIO API code: a) Transaction Retry, b) Transaction Finality API, c) Transaction Resource Cost Estimation, d) Subjective Billing Improvements.
- Relationship to EOSIO: The API Transaction Lifecycle project contains four main improvements to the EOSIO core APIs. The APIs are a critical component of the EOSIO code that allow applications to interact with the blockchain.
- Reason for Interest: The OCI team is interested in this project as it has been involved in the EOSIO core work since 2017 and has expertise in this area. These enhancements will increase the usability and functionality of the APIs.

### Project Details

We expect the teams to already have a solid idea about your project's expected final state. Therefore, we ask the teams to submit (where relevant):

- A. Transaction Retry. Nodes will monitor transactions as they are sent into the system and ensure they are resubmitted into the system if they are not processed in a configurable timeperiod. This feature will establish a pool of known incoming transactions and monitor their inclusion into the blockchain. Once the system reaches an acceptable level of confidence that a transaction has been included in a block, the transaction can be pruned from the pool. If a transaction is identified as missing from the blockchain based on the given criteria, it will attempt to resubmit the transaction to the network for inclusion in future blocks until the point it expires.
- B. Transaction Finality Status. Nodes will monitor transactions as they are sent into the system and will provide a new API method to report transaction status.
- C. Transaction Resource Cost Estimation. Nodes will provide an estimate of resources (central processing unit (CPU), random access memory (RAM), and internet bandwidth (NET)) to perform a transaction when a transaction is sent to send_transaction with read_only flag set true.  The transaction will be applied subjectively to the local chain to calculate subjective resource costs like CPU and NET and also determine the resulting deltas in RAM usage. The response will be returned to the client to inform them of the costs associated with the given transaction data.
- D. Subjective Billing Improvements. Nodes will provide an added leeway per account to allow a more permissive “subjective billing” rate (rate of utilization) to provide a better user experience while maintaining system integrity.

### Ecosystem Fit

Help us locate your project in the EOSIO landscape and what problems it tries to solve by answering each of these questions:

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
- Huang-Ming  Huang
- Alice C. Dames (PM)
- John W. Schultz

### Contact

- **Contact Name:** Alice C. Dames
- **Contact Email:** damesa@objectcomputing.com
- **Website:** https://objectcomputing.com/

### Legal Structure
- **Registered Legal Entity:** Object Computing, Inc.
- **Registered Address:** 12140 Woodcrest, Executive Dr., Ste 300, St. Louis, MO 63141

### Team Experience

Multiple members of the OCI team have worked on the EOSIO code base.  Kevin Heifner is one of the top contributors in the EOSIO repo and has worked as a contractor for block.one since 2019.  The OCI team has been involved in almost all development aspects of the EOSIO code base.

### Team Code Repos

- https://github.com/objectcomputing/
- https://github.com/objectcomputing/OpenDDS

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/brianjohnson5972
- https://github.com/heifner
- https://github.com/jgiszczak
- https://github.com/cj-oci

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

If you've already started implementing your project or it is part of a larger repository, please provide a link and a description of the code here. In any case, please provide some documentation on the research and other work you have conducted before applying. This could be:

- [EOS API Blue Paper](https://medium.com/eos-network-foundation/api-blue-paper-e78c0be0d878)
- references to conversations you might have had related to this project with anyone from the EOS Network Foundation (Yves La Rose discussed).

## Development Roadmap

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):**  three (3) not including PM
- **Total Costs:** $380,000 USD

### Milestone 0 - Initiate Project

- **Estimated duration:** 1 week
- **FTE:**  2
- **Costs:** $50,000 USD

### Milestone 1 - Release Candidates: a) Transaction Retry, b) Transaction Finality Status

- **Estimated duration:** 5 weeks
- **FTE:**  2
- **Costs:** $150,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide documentation of the APIs in Markdown as well as documentation suitable for release notes  |
| 0c. | Unit Tests | Core functions will be fully covered by unit tests to ensure functionality and robustness. |
| 0d. | Integration Tests | Integration tests will be developed including new and modified tests |
| 1. | EOSIO API Transaction Retry | Nodes will monitor transactions as they are sent into the system and ensure they are resubmitted into the system if they are not processed in a configurable timeperiod. This feature will establish a pool of known incoming transactions and monitor their inclusion into the blockchain. Once the system reaches an acceptable level of confidence that a transaction has been included in a block, the transaction can be pruned from the pool. If a transaction is identified as missing from the blockchain based on the given criteria, it will attempt to resubmit the transaction to the network for inclusion in future blocks until the point it expires. |  
| 2. | EOSIO API Transaction Finality Status | Nodes will monitor transactions as they are sent into
the system and will provide a new API method to report transaction status. |  


### Milestone 2 - Release Candidates: c) Transaction Resource Estimation, d) Subjective Billing Improvements

- **Estimated Duration:** 5 weeks
- **FTE:**  1
- **Costs:** $100,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide documentation of the APIs in Markdown as well as documentation suitable for release notes  |
| 0c. | Unit Tests | Core functions will be fully covered by unit tests to ensure functionality and robustness. |
| 0d. | Integration Tests | Integration tests will be developed including new and modified tests |
| 1. | EOSIO Transaction Resource Cost Estimation | Nodes will provide an estimate of resources (central processing unit (CPU), random access memory (RAM), and internet bandwidth (NET)) to perform a transaction when a transaction is sent to send_transaction with read_only flag set true.  The transaction will be applied subjectively to the local chain to calculate subjective resource costs like CPU and NET and also determine the resulting deltas in RAM usage. The response will be returned to the client to inform them of the costs associated with the given transaction data. |  
| 2. | EOSIO Subjective Billing Improvements | Nodes will provide an added leeway per account to allow a more permissive “subjective billing” rate (rate of utilization) to provide a better user experience while maintaining system integrity. |  

### Milestone 3 - Project Completion

- **Estimated Duration:** 1 week
- **FTE:**  1
- **Costs:** $80,000 USD

## Future Plans

Please include here

- Support for the API TRansaction Lifecycle is not included in this project.  Additional support or enhancements would be a separate project
- OCI intends to bid on future ENF projects through the Grant Framework.


## Additional Information

**How did you hear about the Grants Program?** Was told by a member of the EOS Network Foundation.

