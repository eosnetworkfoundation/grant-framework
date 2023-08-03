# EOS Network Foundation Grant Proposal

- **Project Name:**  Antelope IBC NPM Library
- **Team Name:**  Animus Labs LTD (representing Boid.com)
- **EOS Payment Address:**  animus.inc
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):**  2
- **Pomelo Grant(s):** <https://pomelo.io/grants/eosioibc>
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:**  <https://github.com/animuslabs>

## Contact

- **Contact Name:**  John Heeter
- **Contact Email:**  <john@boid.com>
- **Website:**  <https://www.animus.is>

## Project Overview
We're creating an NPM library for Antelope IBC written in Typescript. It will feature a user-friendly API, strong type safety, high performance, and comprehensive documentation.

### Overview

- **Name:**  IBC TypeScript Library
- **Brief Description:**  We are building a Typescript NPM package for Antelope IBC which will be usable by developers on the client or server.
- **Relationship to Antelope:**  Builds on the Antelope IBC system contracts and proof server.
- **Reason for Interest:**  We had a huge issue with implementing the JavaScript code. We see the potential to reduce friction for other teams to implement IBC in their own applications.

### Project Details
The primary objective of this proposal is to perform a comprehensive rewrite of the existing JavaScript codebase that underpins the Cryptomechanics-developed Antelope Inter-Blockchain Communication (IBC) system. Our focus is to enhance the developer experience and simplify the process of building complex applications that utilize IBC. This library, which can be employed in both frontend and backend development and will use the WharfKit SDK. Currently we are working on an IBC application funded by Pomelo and we want to leverage the work we have done for this project into the development of the Antelope IBC SDK which could easily be adopted by other projects.

### Ecosystem Fit
An effective IBC SDK is crucial for the creation of many advanced applications such as marketplaces that allow users to trade items across multiple chains, moving tokens, NFTs, governance actions, and even scaling solutions. We expect this SDK will lead to an increase in product and feature concepts that leverage such capabilities. The only existing solution similar to this SDK is the existing example javascript code provided by the UX team which is not usable in modern web frameworks or on backend servers without extensive modifications.

## Team
### Team members

- **Team Leader:**  John Heeter - Founder @ Boid.com
- John Heeter - Technical Lead / Development
- Seth Choscilowicz - Development / DevOps

### Legal Structure

- **Registered Legal Entity:**  Animus Labs LTD
- **Registered Address:**  Hunkins Waterfront Plaza, Main Street, Charlestown, Nevis

### Team Experience

John Heeter - 8 years of developement experience (5 years blockchain experience eosio) / full stack dev; technical artist 3 years; technical director 3 years
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

## Development Status
Our current progress learning and working with IBC primitives can be seen in the AntelopeX repo: <https://github.com/animuslabs/antelopex-worker/blob/main/src/lib/ibcHelpers.ts>

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 3 FTE
- **Total Costs:** 30,000 USD

### Milestone 1 — Building of the NPM package

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 10,000 USD

We will implement basic IBC functionality into a usable Typescript library.
#### Some functions which will be usable

- Get transaction details from a history solution and format it for proof generation.
- Submit transaction details to a proof generation server.
- Format the response from a proof server into a usable transaction format to be submitted to the blockchain.
- Monitor the steps above and provide useful error handling.

### Milestone 2 — Implementation of the NPM package in our own application

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 10,000 USD

The typescript library will be implemented into one or more of our existing projects (such as AntelopeX or Boid) and any missing features will be implemented and bugs eliminated. Additionally we will add helper functions for common IBC use cases such as token transfers.
### Milestone 3 — Documentation, tests and external integration

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 10,000 USD

We will write comprehensive documentation of the library as well as code comments and basic tests. We will reach out to other projects and help them to implement the library into their codebase when possible. We may make tweaks to the functionality based on feedback from external projects.

## Future Plans

We will be using the IBC library in our own applications and will provide basic support for external projects to integrate the library. We will monitor feedback from external projects to iterate on the library and keep it updated as IBC evolves.

## Additional Information

**How did you hear about the Grants Program?**  Twitter

So far, we have been implementing the project with our own funds, we do not want to go beyond the Antelope environment with the idea. We submit the application for funding only to the EOS Network Foundation. Currently we have implemented some of the functionality in our AntelopeX codebase as mentioned above.
