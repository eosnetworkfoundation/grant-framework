# EOS Network Foundation Grant Proposal

-   **Project Name:** EOSIO Web Client SDK
-   **Team Name:** Greymass Inc.
-   **EOS Payment Address:** funds.gm
-   **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3

## Project Overview

This grant proposal is a follow up to proposal 1 of the [Wallet+ Blue Paper](https://medium.com/eos-network-foundation/wallet-blue-paper-a040a1865977) titled: Software Development Kits (page 12).

The EOSIO Web Client SDK is an project that will create a complete framework upon which web applications can be built to utilize EOSIO-based blockchains. The suite of SDKs and tools within this framework will give applications access to native EOSIO data types, API access to read and write data, authentication with external users through their wallets, and the flexibility to adapt to the custom needs of each individual network and application.

All of these tools will be written in TypeScript and compile into any JavaScript context. The tools will be designed to accommodate developers from a wide range of skill sets and experiences.

### Overview

-   **Name:** EOSIO Web Client SDKs
-   **Brief Description:** Create a new, free, open-source product suite consisting of SDKs and tools capable of meeting the needs of developers building web-based applications on EOSIO platforms.
-   **Relationship to EOSIO:** Web Client SDKs allow any developer to build and integrate a web application with the EOSIO technology stack.
-   **Reason for Interest:** The Greymass team has been focusing on the evolution of EOSIO web client SDKs since 2018 in part due to their work on web protocols and wallet/application integrations. The team has developed multiple core level SDKs (including JS, swift) since genesis. This work has given the team deep EOSIO knowledge they would like to apply to complete a full suite of products for all client developers to use.

### Project Details

This product suite will be made up of a number of individual layers designed to come together in order to provide a cohesive EOSIO experience for both users and developers. The suite will be made up of the following projects, ordered from the easiest for developers to work with to the most complex that may be required for advanced projects:

-   **A. EOSIO Starter Kit:** Developers will be able to use an EOSIO Starter Kit to quickly create web applications that integrate with the EOSIO blockchain. These starter kits will offer easy access to both the Client Library and Core Library, as well as a number of optional add-ons that are recommended for most developers to get started.
-   **B. EOSIO Client Library:** The Client Library is the primary component that most developers will use to integrate EOSIO into their applications. It will handle the responsibilities of data access, wallet integration, user session management, transaction processing, and serve as a base user interfaces for common needs. The focus is on a modular approach capable of meeting the needs of any EOSIO-based blockchain and its operations.
-   **C. EOSIO Client Library Plugins:** The Client Library supports the usage of plugins to allow additional functionality and UI element design. Plugins will exist for different areas the library is responsible for including wallet communication protocols, transaction mutation based on predefined conditions, monitoring of transactions before and after submission, as well as validation logic.
-   **D. EOSIO Core Library:** At the heart of all of these other components is the Core Library, which is responsible for primitive data types, standard API access, transaction serialization, and other cryptographic operations. These core components will be used throughout all of the other client libraries and surfaced to the developer as they are used. This core library can be used in other standalone projects to create alternative client libraries that offer similar functionality.
-   **E. EOSIO Core Library Extensions:** Extensions to the core library are also at the disposal of application developers in order to meet the needs of specific applications and/or blockchains. These extensions offer additional data abstraction for non-core types, support for non-standard APIs, call pattern modifications for APIs, and in-code definitions of contract code. These extensions can be custom designed for specific applications when these advanced needs arise.
-   **F. Brand/Website/Identity:** Branding exploration will be performed to create an recognizable identity for developers in the EOSIO space. This will include messaging and assets that will be used throughout the promotional and educational materials required for the adoption of the technology. A website complete with marketing materials for developers, documentation, and guides will leverage this brand to help new developers get started creating applications on EOSIO.
-   **G. Specifications and Standards:** During the creation of this new software, the identification of processes and techniques that require standardization will be identified and defined. These standards will be provided in the documentation for use external of the SDKs themselves to create cohesive design patterns throughout the ecosystem.

### Ecosystem Fit

**Where and how does your project fit into the ecosystem?**

This project fits under the core codebase as an extension for web developers to use.

**Who is your target audience?**

Web application and web client SDK developers.

**What need(s) does your project meet?**

The project improves the ability for developers to create applications, services, and tools that integrate with EOSIO.

**Are there any other projects similar to yours in the EOSIO ecosystem?**

Yes, for web clients both eosjs and ual are libraries created by Block.one which perform a similar function. This suite of tools will serve as a modern replacement.

**If so, how is your project different?**

The original libraries (eosjs/ual) available to developers today are limited in their design and do not allow modern EOSIO development techniques to be utilized properly. Examples of the struggles when using the existing SDKs include:

-   The integration of wallets and external applications
-   Multi account and blockchain session management
-   Automated management of network resources
-   Implementing of alternative transaction processing models (tx fees)
-   Proper transaction error handling and guided correction
-   Extensibility of core functionality
-   Handling API communication and errors

The new SDKs this project defines starts from the ground up to rectify these problems and create a stable foundation for continued development into the future.

## Team

The team behind this proposal is Greymass, an organization built to facilitate the growth of distributed ledger technologies and the infrastructure powering them.

Additional contributions could potentially be sourced from other teams based on interested received.

### Team members

-   Greymass
    -   **Lead:** Aaron Cox
    -   Scott Sallinen
    -   Daniel Fugere
    -   Johan Nordberg
    -   Myles Snider
    -   Maximilian Larsson
    -   Fang Ji
    -   Alberto Forni
    -   Tony Licavoli
    -   Jacob Davis

### Contact

-   **Contact Name:** Aaron Cox
-   **Contact Email:** aaron@greymass.com
-   **Website:** https://greymass.com

### Legal Structure

-   **Registered Legal Entity:** Greymass Inc.
-   **Registered Legal Entity Type:** Canadian Federal Corporation
-   **Registered Address:** Suite 201 - 3053 Edgemont Blvd North Vancouver BC V7R 2N5 Canada

### Team Experience

Multiple members of the Greymass team have been working on client side development for blockchains since 2016. With our shared interest in this aspect of the technology, Greymass was formed in 2018 to push these technologies further and create the tools required for an excellent everyday user experience. The team has created multiple core level SDKs for EOSIO, created one of the most popular client applications (Anchor), and has prototyped solutions to the hurdles many users face everyday.

The Greymass team is responsible for the creation of the following products:

-   The EOSIO Authenticator, Anchor
-   The EOSIO Web Wallet, Unicove
-   The EOSIO Resource Provider, Fuel
-   The EOSIO Account Creation Service, Sextant
-   The EOSIO Account API, Lighthouse
-   The EOSIO History API, Roborovski

### Team Org Repos

**Organization:**

https://github.com/greymass

**SDK Development:**

Core SDKs and tools

-   https://github.com/greymass/abi2core
-   https://github.com/greymass/eosio-core
-   https://github.com/greymass/eosio-abi2ts
-   https://github.com/greymass/eosio-key-encryption
-   https://github.com/greymass/eosio-resources
-   https://github.com/greymass/eosio-webauthn
-   https://github.com/greymass/eosio-signing-request
-   https://github.com/greymass/eosio-signing-request-java
-   https://github.com/greymass/go-eosio
-   https://github.com/greymass/swift-eosio
-   https://github.com/greymass/swift-eosio-key-encryption

Client SDKs and tools

-   https://github.com/greymass/anchor-link
-   https://github.com/greymass/anchor-link-browser-transport
-   https://github.com/greymass/anchor-link-console-transport
-   https://github.com/greymass/anchor-link-session-manager
-   https://github.com/greymass/buoy-client
-   https://github.com/greymass/buoy-nodejs
-   https://github.com/greymass/hyperbuoy
-   https://github.com/greymass/keycert-js
-   https://github.com/greymass/keycert-js-pdf

### Team Member Repos

-   https://github.com/aaroncox
-   https://github.com/ScottSallinen
-   https://github.com/dafuga
-   https://github.com/jnordberg

### Team LinkedIn Profiles

n/a

## Development Status

Development has not yet begun. However, the Greymass team for nearly 4 years has been researching and building the core EOSIO components required for a comprehensive framework of web client SDKs. Many of the components for this new project can lean heavily on this work as the ecosystem moves to create a new suite of official products that can ease adoption by EOSIO developers.

All of the following components played a role in the lead up to the path forward with this proposal.

**Research - Wallet+ Blue Paper**

Significant research went into the direction of potential new SDKs during the creation of the [Wallet+ Blue Paper](https://medium.com/eos-network-foundation/wallet-blue-paper-a040a1865977) in late 2021 into early 2022. The first proposal within this paper focuses on the need for a solution like this and many other proposals would see benefit from the creation of new SDKs.

**Standard - EOSIO Signing Request (ESR)**

One of the core components Greymass started with the development of Anchor was the ESR protocol. This was to standardize data types while communicating EOSIO information between various applications. This standard represents a way to effectively encapsulate transaction data and metadata for transmission.

This protocol was developed into EEP-7 and published in early 2019, while undergoing 3 iterations:

-   https://github.com/eosio-eps/EEPs/blob/master/EEPS/eep-7.md

**Web SDK - EOSIO Signing Request (ESR)**

Greymass also developed the SDKs required to interact with this standard for web clients (JS) and mobile applications (Swift/Java):

-   https://github.com/greymass/eosio-signing-request
-   https://github.com/greymass/eosio-signing-request-java
-   https://github.com/greymass/swift-eosio

The ESR protocol will be at the core of the new client libraries as the primary method to pass transaction data between the various components in the suite.

**Web SDK - Core Library**

During the creation of the EOSIO Signing Request libraries, the Greymass team encountered significant hurdles and impossible situations while trying to develop the codebase with eosjs. Due to this, the team started work on a fundamentally different set of SDKs with modularity and flexibility in mind to serve as a replacement.

These efforts led to the creation of the `@greymass/eosio` SDK to allow for more advanced usage of EOSIO technologies.

-   https://github.com/greymass/eosio-core

This existing code with minimal modification can serve as the Core Library for the new suite of web SDKs. Further work will need to be done to create additional data types and functionality. Documentation and educational materials on this technology will need to be created. We propose to build this entire new suite of products based upon this library and treating it the official low level web client SDK.

**Web SDK - Core Library Extensions**

Functionality that is not required for all use cases but is still considered a "core component" is to be an optional extension of the core library. Greymass has created a number of extension-like packages available for use, including:

-   https://github.com/greymass/eosio-resources
-   https://github.com/greymass/eosio-webauthn
-   https://github.com/greymass/eosio-key-encryption

These packages can be optionally included for use within applications on an as-needed basis.

**Web SDK - Client Libraries**

Prior research has gone into both [protocol development](https://github.com/greymass/anchor-link/blob/master/protocol.md) as Anchor was built, as well as the creation of numerous SDKs:

-   https://github.com/greymass/anchor-link
-   https://github.com/greymass/anchor-link-browser-transport
-   https://github.com/greymass/anchor-link-console-transport
-   https://github.com/greymass/anchor-link-session-manager
-   https://github.com/greymass/buoy-client
-   https://github.com/greymass/buoy-nodejs
-   https://github.com/greymass/hyperbuoy

The UI and UX focused elements of these libraries can be extracted and improved upon to serve as the basis of a new web client SDK. Greymass will deprecate and replace it's existing anchor-link series of libraries and implement this functionality as plugins for the new client library. Additional plugins will also be created to support non-Anchor related protocols

## Development Roadmap

### Overview

-   **Total Estimated Duration:** 9 months
-   **Full-Time Equivalent (FTE):** Six (6)
-   **Total Costs:** $1,085,000 USD

**Note**: Some of the milestones can possibly overlap and be done in parallel.

### Milestone 1 - Core Library

-   Estimated duration: 2 months
-   FTE: 3
-   Costs: $125,000 USD

| Number | Deliverable       | Specification                                                                                        |
| -----: | ----------------- | ---------------------------------------------------------------------------------------------------- |
|    0a. | License           | BSD 3-Clause                                                                                         |
|    0b. | Documentation     | Creation of documentation for the core libraries and how to utilize all of its features.             |
|    0c. | Unit Tests        | In-depth automated tests to ensure compatibility and prevent breaking changes from being introduced. |
|     1. | Serializer        | A complete data serialization library compatible with the EOSIO native serializer.                   |
|     2. | Crypto Primitives | Creation and defining of crypto primitives utilized within EOSIO.                                    |
|     3. | EOSIO Primitives  | Inclusion of EOSIO primitives built on top of the crypto primitives that EOSIO requires to operate.  |
|     4. | API Client        | A customizable API Client interface to allow communication with the blockchain API servers.          |

### Milestone 2 - Core Library Extensions

-   Estimated duration: 1 month
-   FTE: 2
-   Costs: $92,500 USD

Each extension will be it's own self-contained package, having templated documentation and published for developers to optionally include in their project. This milestone is the creation of the **standards** and **templates**, alongside the development at least one plugin to serve as the reference implementation.

##### Templates

| Number | Deliverable                   | Specification                                                   |
| -----: | ----------------------------- | --------------------------------------------------------------- |
|     1. | API Client Extension Template | Base template for the creation of new API interface extensions. |
|     2. | Type Extension Template       | Base template for the creation of new data type extensions.     |

**Note**: The extension candidates listed below are entered alphabetically and not ordered by priority. They are just candidates for potential extensions and the priority on which to built as the initial prototype will need to be discussed by the project sponsors.

##### API Client Extensions

| Number | Deliverable       | Specification                                                                                           |
| -----: | ----------------- | ------------------------------------------------------------------------------------------------------- |
|     1. | AtomicAssets      | Predefined API endpoints for accessing AtomicAssets specific data.                                      |
|     2. | dfuse             | A streaming client capable of receiving data based on dfuse standards.                                  |
|     3. | FIO               | Predefined API endpoints for accessing FIO specific functionality.                                      |
|     4. | Firehose          | A streaming client capable of receiving data from the dfuse firehose.                                   |
|     5. | History (v1 spec) | Predefined API endpoints for accessing data from services following the v1 history standard.            |
|     6. | Hyperion          | Predefined API endpoints for accessing data from Hyperion API servers.                                  |
|     7. | Resource Provider | Predefined API endpoints to access data from Resource Providers following the standard API definitions. |
|     8. | Roborovski        | Predefined API endpoints for retrieving and working with Robo historical data.                          |
|     9. | State History     | A streaming client capable of subscribing to data streams from the State History plugin.                |
|    10. | Trace API         | Overloaded API calls capable of calling the Trace API endpoints.                                        |

##### Types

| Number | Deliverable     | Specification                                                                        |
| -----: | --------------- | ------------------------------------------------------------------------------------ |
|     1. | Account         | Typed data definitions for EOSIO accounts, extendable on a per-chain basis.          |
|     2. | AtomicAssets    | Data types defined for the AtomicAssets standard.                                    |
|     3. | Block Producer  | Typed data definitions for EOSIO blockchains to populate Block Producer information. |
|     4. | NameBid         | Typed data definitions for EOSIO blockchains that support the NameBid feature.       |
|     5. | PowerUp         | Typed data definitions for EOSIO blockchains that support the PowerUp feature.       |
|     6. | RAM             | Typed data definitions for EOSIO blockchains that support the native RAM model.      |
|     7. | REX             | Typed data definitions for EOSIO blockchains that support the REX feature.           |
|     8. | SimpleAssets    | Data types defined for the SimpleAssets standard.                                    |
|     9. | Stake           | Typed data definitions for EOSIO blockchains that support staked tokens.             |
|    10. | Token           | Typed data definitions for the eosio.token contract.                                 |
|    11. | Transaction Fee | Typed data definitions for the integration of transaction fees.                      |

### Milestone 3 - Web Client SDK

-   Estimated duration: 3 months
-   FTE: 5
-   Costs: $365,000 USD

| Number | Deliverable   | Specification                                                                                                |
| -----: | ------------- | ------------------------------------------------------------------------------------------------------------ |
|    0a. | License       | BSD 3-Clause                                                                                                 |
|    0b. | Documentation | Creation of documentation for the web client SDK and usage of plugins.                                       |
|    0c. | Unit Tests    | Automated tests for the web client SDK to ensure functionality and prevent breaking changes.                 |
|     1. | API Client    | Browser focused API Client extension that provides failover and other browser-specific logic.                |
|     2. | Base UI       | Default user interface for base interactions (login, logout, transact, etc).                                 |
|     3. | Localization  | Multiple language support for user interface.                                                                |
|     4. | Sessions      | In-browser session management for accounts and connected signature providers.                                |
|     5. | Transact      | Customizable transaction pipeline for preparing, signing, broadcasting, and post-processing of transactions. |
|     6. | UI Components | Reusable interface components (prompt OK, Yes/No, status message, etc).                                      |

### Milestone 4 - Web Client Plugins

-   Estimated duration: 2 months
-   FTE: 3
-   Costs: $150,000 USD

Each plugin will be it's own self-contained package, having templated documentation and published for developers to optionally include in their project. This milestone is the creation of the **standards** and **templates**, alongside the development at least one plugin to serve as the reference implementation.

##### Standards

| Number | Deliverable  | Specification                                                                                 |
| -----: | ------------ | --------------------------------------------------------------------------------------------- |
|     1. | Middleware   | Definition of how transaction middleware is defined and the pipeline the data flows through.  |
|     2. | Transport    | Definition of communication between applications and signers.                                 |
|     3. | Interactions | Definition of how interactive events can be surfaced from plugins through the user interface. |

##### Templates

| Number | Deliverable                | Specification                                                   |
| -----: | -------------------------- | --------------------------------------------------------------- |
|     1. | Middleware Template        | Base template for the creation of transaction middleware.       |
|     2. | Interactions Template      | Base template for the creation of user interaction libraries.   |
|     3. | Transport Template         | Base template for the creation of new communication transports. |
|     4. | Account Creation Template  | Base template for the creation of account creation plugins.     |
|     5. | Resource Provider Template | Base template for the creation of resource provider plugins.    |
|     6. | Wallet Plugin Template     | Base template for the creation of new wallet interface plugins. |

**Note**: The plugin candidates listed below are entered alphabetically and not ordered by priority. They are just candidates for potential plugins and the priority on which to built as the initial prototype will need to be discussed by the project sponsors.

##### Plugins

| Number | Deliverable                    | Specification            |
| -----: | ------------------------------ | ------------------------ |
|     1. | Greymass Fuel                  | Resource Provider Plugin |
|     2. | Greymass Account Creation      | Account Creation Plugin  |
|     3. | EOSIO Signing Request (Anchor) | Wallet Plugin            |
|     4. | Scatter Protocol               | Wallet Plugin            |
|     5. | WAX Cloud Wallet               | Wallet Plugin            |

### Milestone 5 - EOSIO Starter Kit

-   Estimated duration: 1 month
-   FTE: 2
-   Costs: $50,000 USD

| Number | Deliverable                              | Specification                                                                            |
| -----: | ---------------------------------------- | ---------------------------------------------------------------------------------------- |
|     1. | Basic Starter Kit                        | A beginner kit that includes the most commonly used components for all EOSIO networks.   |
|     2. | Basic Starter Kit - Documentation        | A guide on how to utilize the starter kit in an existing application.                    |
|     3. | Basic Starter Kit - Integration Examples | One or more example codebases that integrate the starter kit with common web frameworks. |

### Milestone 6 - Brand / Website / Documentation

-   Estimated duration: 4 months
-   FTE: 5
-   Costs: $305,000 USD

| Number | Deliverable                | Specification                                                                                                                                                                                                                                                |
| -----: | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|     1. | Brand                      | The branding for the product suite, including name, visual identity, domains and socials.                                                                                                                                                                    |
|     2. | Website                    | Primary developer focused marketing website to facilitate the onboarding of new developers into the ecosystem. Product landing pages describing features for each part of the product suite to help guide developers towards relevant educational materials. |
|     3. | Plugin / Extension Library | A searchable index of all the various packages that can be utilized with the product suite.                                                                                                                                                                  |
|     4. | Documentation              | Complete documentation of all products within the suite linked throughout the marketing portion of the website. API references, code/usage samples, and basic guides.                                                                                        |
|     5. | Developer Support          | Various funnels to push developers into community channels to get support while developing with the product suite.                                                                                                                                           |

## Future Plans

Greymass intends to "[dogfood](https://en.wikipedia.org/wiki/Eating_your_own_dog_food)" these new SDKs in to all current and future projects as a means to ensure the product remains stable and useful. This includes:

-   Leveraging SDKs within Unicove, our open-source web wallet interface for EOSIO.
-   Ensuring Anchor compatibility as a transaction signer.
-   Integration of Fuel to provide network resources.
-   Offering account creation services for client applications.

The long term plans for Greymass include building a number of products and services that leverage EOSIO technologies in the future once the development environment is easy to use for both developers and users.

It should be anticipated that future funding will be required to facilitate the creation of additional Web Client Plugins and Core Library Extensions.

## Additional Information

**How did you hear about the Grants Program?** Directly from the ENF.

The Greymass team has been slowly working to achieve a series of modern SDKs for EOSIO since 2019 after struggling to build products within the EOSIO space. This work started with the EOSIO Signing Request library and specification for use within Anchor, which then spawned a number of other projects as listed throughout this proposal, culminating in the vision outlined within.

The work done to date on all of this software has been financed through block producer rewards, donations, and personal financing from members of the team.

Greymass applied for grants directly from Block.one in 2019/2020 for this work, which was not accepted.
