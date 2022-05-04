# EOS Network Foundation Grant Proposal

- **Project Name:** EOSIO Web Client SDK
- **Team Name:** Greymass Inc.
- **EOS Payment Address:** funds.gm
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3

## Project Overview

This grant proposal is a follow up to the [Wallet+ Blue Paper](https://medium.com/eos-network-foundation/wallet-blue-paper-a040a1865977) section titled: Software Development Kits (page 12).

The EOSIO Web Client SDK is an effort to create a complete framework upon which web applications can be built to utilize EOSIO-based blockchains. The suite of SDKs and tools within this framework will give applications access to native EOSIO data types, API access to read and write data, authentication with external users through their wallets, and the flexibility to adapt to the custom needs of each network and application. 

All of these tools will be written in TypeScript and work in all JavaScript contexts. The tools will be designed to accommodate developers from a wide range of skill sets and experiences. 

### Overview

- **Name:** EOSIO Web Client SDKs
- **Brief Description:** Create a new, free, open-source product suite consisting of SDKs and tools capable of meeting the
needs of developers building web-based applications on EOSIO platforms.
- **Relationship to EOSIO:** Client SDKs are the core component that allow any developer to build and integrate an application with the EOSIO technology stack. 
- **Reason for Interest:** The Greymass team has been focusing on the evolution of web client SDKs due with their work on web protocols and wallet/application integrations going back to 2018. The team has developed multiple core level SDKs (JS, swift) since genesis and have EOSIO knowledge they would like to apply to complete a full suite of products for all client developers to use.

### Project Details

This product suite will be made up of a number of individual layers designed to come together to provide a cohesive EOSIO experience for both users and developers. The suite will be made up of the following projects, from the easiest for developers to work with to the most complex that may be required for advanced projects:

- **A. EOSIO Starter Kit:** Developers will be able to use an EOSIO Starter Kit to quickly integrate web applications with the EOSIO blockchain. This kit will offer easy access to both the Client Library and Core Library, as well as a number of optional add-ons that are recommended for most developers to get started.
- **B. EOSIO Client Library:** The Client Library is the core component that developers will use to integrate EOSIO into their applications. It will handle the responsibilities of data access, wallet integration, user session management, transaction processing, and a base set of user interfaces for common needs. The focus is on a modular approach capable of meeting the needs of any EOSIO-based blockchain and its operations.

- Event system
    - Drives optional user interface layer
- User Interface Abstraction
    - Plugin architecture
        - Predefined user interface bundled into starter kits
    - Localization/i18n
    - Candidates/Features:
        - Sign in
        - Sign out
        - Sign transaction
        - Transaction status
        - Prompts (Yes/No, OK, etc)
        - Message (Success, error, warn, etc)
- Abstract API access
    - Data Retrieval
        - Easily load account, table, or other types of data
- Sessions
    - Embedded `transact` to create transaction based on the configuration of this session
    - Ability to communicate with the signer attached to the session
    - Associated account information and helpers to easily access more data
- Transactions
    - Instantiate `transactor` with pipeline configuration
        - Starter Kit can default to using common plugins (Fuel?)
        - Defaults to none
    - The `transact` method takes action/transaction data input and...
        - passes through `presign` pipeline
        - passes through `sign` pipeline
        - validates
        - broadcasts
        - passes through `postsign` pipeline
    - Event handlers and messaging
        - transaction lifecycle 
            - success
                - transaction validation monitoring (checks tx exists)
            - failure
                - fallback methods (retry strategies, prompting, etc)
    - Plugin architecture to allow custom logic
        - Input/Output of each plugin: ESR string
        - Plugin Functionality:
            - Performing API calls
            - Conditionally modifying action data
            - Validating transaction data
        - Uses:
            - Estimating 
            - Providing Resources
            - Validating Data
        - Candidates/Examples: 
            - Add Action (Generic)
            - Cosign (Resource Providers)
            - Estimate (Resource Providers)
            - Validate (Generic)
            - Multisig (Generic) - both on-chain and off-chain

- **C. EOSIO Client Library Plugins:** The Client Library supports the usage of plugins to allow additional functionality and design. Plugins will exist for different areas the library is responsible for including wallet communication protocols, transaction mutation based on predefined conditions, monitoring of transactions before and after submission, as well as validation logic. 
- **D. EOSIO Core Library Extensions:** Extensions to the core library are also at the disposal of application developers in order to meet the needs of specific applications and/or blockchains. These extensions offer additional data abstraction for non-core types, support for non-standard APIs, call pattern modifications for APIs, and in-code definitions of contract code. These extensions can be custom designed for specific applications when these advanced needs arise. 

[TODO - remove notes below]

- Type non-core primitives
    - Define commonly used data types
    - Bundle into Core Library extensions
    - Include most commonly used into Starter Kit
    - Candidates:
        - Account (eosio)
        - Fee (eosio.token)
        - NameBid (eosio)
        - NFT (AA, Simple, etc)
        - PowerUp (eosio)
        - RAM (eosio)
        - REX (eosio)
        - Stake (eosio)
        - Token (eosio.token)
- Create non-core APIClient extensions
    - Candidates: 
        - atomicassets
        - dfuse
        - hyperion
        - resource provider spec (Fuel)
        - v1 history spec

- **E. EOSIO Core Library:** At the heart of all of these other projects is the Core Library, which is responsible for primitive data types, standard API access, transaction serialization, and other cryptographic operations. These core components will be used throughout all of the other client libraries and surfaced to the developer as they are used. This core library can be used in other standalone projects to create alternative client libraries that offer similar functionality.

[TODO - remove notes below]

- Rebuild/Extend APIClient
    - Create `Struct.fetch()` patterns for quick API access
    - Plugin architecture for common/optional non-native API services
    - ability to instantiate APIClient with additional configured plugins
    - support for load balancing and failover (potentially through plugins?)

- **F. Brand/Website/Identity:** Branding exploration will be performed to create an recognizable identity for developers. This will include messaging and assets that will be used throughout the promotional and educational materials required for the adoption of the project. A website complete with marketing materials for developers, documentation, and guides will leverage this brand to help new developers get started creating applications on EOSIO.

- Branding
- Features / Explanation
- Documentation
- Education / Guides
- News / Updates

Identity, website, developer outreach, education

Audience: Application Developers

- **G. Specifications and Standards:** During the creation of this new software, the identification of processes and techniques that require standardization will be identified and defined. These standards will be provided in the documentation for use external of the SDKs themselves to create cohesive design patterns throughout the ecosystem.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?

This project fits into the EOSIO Core code.

- Who is your target audience?

Web application and web client SDK developers

- What need(s) does your project meet?

The project improves the ability for developers to create applications that integrate with EOSIO.

- Are there any other projects similar to yours in the EOSIO ecosystem?

Yes, for web clients both eosjs and ual are libraries created by Block.one.

- If so, how is your project different?

The original libraries developers have to work with today are limited in their design and do not allow modern EOSIO developers to leverage the technology within their applications properly. Examples of the struggles when using the existing SDKs include the ability to easily integrate wallets, multi-user session management, providing resources for the user, transaction fee models, proper error handling and correction, their non-modular code design, inexistent process hooks, lack of extensibility, lack of fault tolerance, and finally the lack of ongoing development and future maintenance.

## Team

### Team members

- Greymass
    - **Lead:** Aaron Cox
    - Scott Sallinen
    - Johan Nordberg
    - Daniel Fugere
    - Myles Snider
    - Maximilian Larsson
    - Fang Ji
    - Alberto Forni
    - Tony Licavoli
    - Jacob Davis

### Contact

- **Contact Name:** Aaron Cox
- **Contact Email:** aaron@greymass.com
- **Website:** https://greymass.com

### Legal Structure
- **Registered Legal Entity:** Greymass Inc.
- **Registered Address:** Suite 201 - 3053 Edgemont Blvd North Vancouver BC V7R 2N5

### Team Experience

Multiple members of the team have been working on client side development for blockchains since 2016. With our aligned interests in pushing this technology further, Greymass was formed in 2018 to push these technologies further and create the tools required for an excellent everyday user experience. The team has created multiple core level SDKs for EOSIO, created one of the most popular client applications (Anchor), and has prototyped solutions to the hurdles many users face everyday.  

### Team Org Repos

**Organization:**

https://github.com/greymass

**SDK Development:**

Core SDKs

- https://github.com/greymass/abi2core
- https://github.com/greymass/eosio-core
- https://github.com/greymass/eosio-abi2ts
- https://github.com/greymass/eosio-key-encryption
- https://github.com/greymass/eosio-resources
- https://github.com/greymass/eosio-webauthn
- https://github.com/greymass/eosio-signing-request
- https://github.com/greymass/eosio-signing-request-java
- https://github.com/greymass/go-eosio
- https://github.com/greymass/swift-eosio
- https://github.com/greymass/swift-eosio-key-encryption

Client SDKs

- https://github.com/greymass/anchor-link
- https://github.com/greymass/anchor-link-browser-transport
- https://github.com/greymass/anchor-link-console-transport
- https://github.com/greymass/anchor-link-session-manager
- https://github.com/greymass/buoy-client
- https://github.com/greymass/buoy-nodejs
- https://github.com/greymass/hyperbuoy
- https://github.com/greymass/keycert-js
- https://github.com/greymass/keycert-js-pdf

### Team Member Repos

- https://github.com/aaroncox
- https://github.com/ScottSallinen
- https://github.com/dafuga
- https://github.com/jnordberg

### Team LinkedIn Profiles

n/a 

## Development Status

The Greymass team for over 3 years has been researching and building the core EOSIO components required for a comprehensive framework of web client SDKs. Many of the components for this new project can lean heavily on this work as the ecosystem moves to create a new suite of official products that can ease adoption by EOSIO developers.

**Wallet+ Blue Paper**

Significant thought went into the direction of potential new SDKs during the creation of the [Wallet+ Blue Paper](https://medium.com/eos-network-foundation/wallet-blue-paper-a040a1865977) in late 2021. The first proposal within this paper focuses on the need for a solution like this and many other proposals would see benefit from the creation of new SDKs. 

**Web - Core Library**

During the creation of the EOSIO Signing Request libraries, the Greymass team encountered significant hurdles and impossible situations while trying to develop the codebase with eosjs. Due to this, the team started work on a fundamentally different set of SDKs with modularity and flexibility in mind to serve as a replacement.

These efforts led to the creation of the `@greymass/eosio` SDK to allow for more advanced usage of EOSIO technologies.

- https://github.com/greymass/eosio-core

This existing code with minimal modification can serve as the Core Library for the new suite of web SDKs. Further work will need to be done to create additional data types and functionality. We propose to build this entire new suite of products based upon this library and treating it the official low level web client SDK.

**Web - Core Library Extensions**

Functionality that is not required for all use cases but is still considered a "core component" is to be an optional extension of the core library. Greymass has created a number of extension-like packages available for use, including: 

- https://github.com/greymass/eosio-resources
- https://github.com/greymass/eosio-webauthn
- https://github.com/greymass/eosio-key-encryption

These packages can be optionally included for use within applications on an as-needed basis. 

**Web - Client Libraries**

Prior research has gone into both [protocol development](https://github.com/greymass/anchor-link/blob/master/protocol.md) as well as the creation of numerous SDKs:

- https://github.com/greymass/anchor-link
- https://github.com/greymass/anchor-link-browser-transport
- https://github.com/greymass/anchor-link-console-transport
- https://github.com/greymass/anchor-link-session-manager
- https://github.com/greymass/buoy-client
- https://github.com/greymass/buoy-nodejs
- https://github.com/greymass/hyperbuoy

The UI and UX focused elements of these libraries can be extracted and improved upon to serve as the basis of a new web client SDK. Greymass will deprecate and replace it's existing anchor-link series of libraries and implement this functionality as plugins for the new client library. Additional plugins will also be created to support non-Anchor related protocols

**EOSIO Signing Request (ESR)**

One of the core components Greymass started with the development of Anchor was the ESR protocol. This was to standardize data types while communicating EOSIO information between various applications. This standard represents a way to effectively encapsulate transaction data and metadata for transmission.

This protocol was developed into EEP-7 and published in early 2019, while undergoing 3 iterations:

- https://github.com/eosio-eps/EEPs/blob/master/EEPS/eep-7.md

Greymass then also developed the SDKs required to interact with this standard for web clients (JS) and mobile applications (Swift/Java):

- https://github.com/greymass/eosio-signing-request
- https://github.com/greymass/eosio-signing-request-java
- https://github.com/greymass/swift-eosio

The ESR protocol will be at the core of the new client libraries as the primary method to pass transaction data between the various components in the suite.

## Development Roadmap

### Overview

- **Total Estimated Duration:** 9 months
- **Full-Time Equivalent (FTE):**  Six (6)
- **Total Costs:** $1,085,000 USD

### Milestone X - Core SDKs

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Description |
| 0c. | Unit Tests | Description |
| 1. | Serializer | Description |  
| 2. | Crypto Primitives | Description |  
| 3. | EOSIO Primitives | Description |  
| 4. | API Client | Description |  

### Milestone X - Core SDK Extensions

Extensions are meant to include additional functionality in the core library that is not standard, not used by all applications, or support for features not available on all EOSIO chains. Each extension will be it's own self-contained package, having it's own templated documentation and published for developers to optionally include in their application for use.

Listed below are examples of various extensions we have identified as providing benefit.

**Note**: The extension candidates listed below are entered alphabetically and not ordered by priority. They are just candidates for potential extensions and the priority on which to build first will need to be discussed.

##### Templates

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | API Client Extension Template | Base template for the creation of new API interface extensions. |
| 2. | Type Extension Template | Base template for the creation of new data type extensions. |

##### API Client Extensions

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | AtomicAssets | Description | 
| 2. | dfuse | Description | 
| 3. | FIO | Description | 
| 4. | Firehose | Description | 
| 5. | History (v1 spec) | Description | 
| 6. | Hyperion | Description | 
| 7. | Resource Provider | Description | 
| 8. | Roborovski | Description | 
| 9. | State History | Description | 
| 10. | Trace API | Description | 

##### Types

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Account | Description |  
| 2. | AtomicAssets | Description |  
| 3. | Block Producer | Description |  
| 4. | NameBid | Description |  
| 5. | PowerUp | Description |  
| 6. | RAM | Description |  
| 7. | REX | Description |  
| 8. | SimpleAssets | Description |  
| 9. | Stake | Description |  
| 10. | Token | Description |  
| 11. | Transaction Fee | Description | 

### Milestone X - Web Client SDK

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Description |
| 0c. | Unit Tests | Description |
| 1. | API Client | Browser focused API Client extension that provides failover and other browser specific logic. |  
| 2. | Base UI | Default user interface for base interactions (login, logout, transact, etc). |  
| 3. | Localization | Multiple language support for user interface. |  
| 4. | Sessions | In-browser session management for accounts and connected signature providers. |  
| 5. | Transact | Customizable transaction pipeline for preparing, signing, broadcasting, and post-processing of transactions. |  
| 6. | UI Components | Reusable interface components (prompt OK, Yes/No, status message, etc). |  

### Milestone X - Web Client Plugins

**Note**: The web client candidates listed below are entered alphabetically and not ordered by priority. They are just candidates for potential plugins and the priority on which to build first will need to be discussed.

##### Templates

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Account Creation Template | Base template for the creation of account creation plugins. |
| 1. | Resource Provider Template | Base template for the creation of resource provider plugins. |
| 1. | Wallet Plugin Template | Base template for the creation of new wallet interface plugins. |

##### API Client Extensions

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1. | Greymass Fuel | Resource Provider Plugin | 
| 1. | Greymass Account Creation | Account Creation Plugin | 
| 1. | EOSIO Signing Request (Anchor) | Wallet Plugin | 
| 1. | Scatter Protocol | Wallet Plugin | 

### Milestone X - EOSIO Starter Kit

### Milestone X - Website

#### docs

[TODO - brainstorming still]

- core
    - native types, how to use, what functions they offer
    - api client core usage
- core extensions
    - create an extension for custom data types
    - distribution for use in other apps
- web client sdk
- web client plugins
- starter kit
    - functional app demos
    - integrating into your desired framework
    - boilerplates (react, vue, angular, svelte, etc)

#### brand

[TODO]

## Future Plans

Greymass intends to "[dogfood](https://en.wikipedia.org/wiki/Eating_your_own_dog_food)" these new SDKs in to all current and future projects as a means to ensure the product remains stable and useful. This includes:

- Leveraging SDKs within Unicove, our open-source web wallet interface for EOSIO.
- Ensuring Anchor compatibility as a transaction signer.
- Integration of Fuel to provide network resources.
- Offering account creation services for client applications.

The long term plans for Greymass include building a number of products and services that leverage EOSIO technologies in the future once the development environment is easy to use for both developers and users.

## Additional Information

**How did you hear about the Grants Program?** Directly from the ENF.

The Greymass team has been slowly working to achieve a series of modern SDKs for EOSIO since 2019 after struggling to build products within the EOSIO space. This work started with the EOSIO Signing Request library and specification for use within Anchor, which then spawned a number of other projects as listed throughout this proposal, culminating in the vision outlined within.

The work done to date on all of this software has been financed through block producer rewards, donations, and personal financing from members of the team. 

Greymass applied for grants directly from Block.one in 2019/2020 for this work, which was not accepted.