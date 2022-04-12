# EOS Network Foundation Grant Proposal

- **Project Name:** EOSIO Web Client SDK
- **Team Name:** Greymass Inc.
- **EOS Payment Address:** funds.gm
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3

## Project Overview

This grant proposal is a follow up to the [Wallet+ Blue Paper](https://medium.com/eos-network-foundation/wallet-blue-paper-a040a1865977) section titled: Software Development Kits (page 12).

As the proposal describes, the first steps towards creating a more robust client SDK ecosystem is the development of the core protocols and techniques, as well as the creation of new SDKs targetting web clients to begin with. Additional SDK frameworks can be developed for non-web clients based off the learnings of development in the web client SDKs.

### Overview

- **Name:** EOSIO Web Client SDKs
- **Brief Description:** Create a new, free, open-source product suite consisting of SDKs and tools capable of meeting the
needs of developers building web-based applications on EOSIO platforms.
- **Relationship to EOSIO:** Client SDKs are the core components that allow any developer to build and integrate an application with the EOSIO technology stack. 
- **Reason for Interest:** The Greymass team has been interested in the evolution of web client SDKs due to their work with web protocols and integrations going back into 2018. The team has developed multiple core level SDKs (JS, swift) since gemesos and have EOSIO knowledge they would like to apply to complete a full suite of products for all client developers to use.

### Project Details

This product suite will be made up of a number of individual layers designed to come together to provide a cohesive EOSIO experience for both users and developers. The suite will be made up of the following projects, from the easiest for developers to work with to the most complex that may be required for advanced projects:

- **A. EOSIO Starter Kit:** Developers will be able to use an EOSIO Starter Kit to quickly integrate web applications with the EOSIO blockchain. This kit will offer easy access to both the Client Library and Core Library, as well as a number of optional add-ons that are recommended for most developers to get started.
- **B. Client Library:** The Client Library is the core component that developers will use to integrate EOSIO into their applications. It will handle the responsibilities of data access, wallet integration, user session management, transaction processing, and a base set of user interfaces for common needs. The focus is on a modular approach capable of meeting the needs of any EOSIO-based blockchain and its operations.
- **C. Client Library Plugins:** The Client Library supports the usage of plugins to allow additional functionality and design. Plugins will exist for different areas the library is responsible for including wallet communication protocols, transaction mutation based on predefined conditions, monitoring of transactions before and after submission, as well as validation logic. 
- **D. Core Library Extensions:** Extensions to the core library are also at the disposal of application developers in order to meet the needs of specific applications and/or blockchains. These extensions offer additional data abstraction for non-core types, support for non-standard APIs, call pattern modifications for APIs, and in-code definitions of contract code. These extensions can be custom designed for specific applications when these advanced needs arise. 
- **E. Core Library:** At the heart of all of these other projects is the Core Library, which is responsible for primative data types, standard API access, transaction serialization, and other cryptographic operations. These core components will be used throughout all of the other client libraries and surfaced to the developer as they are used. This core library can be used in other standalone projects to create alternative client libraries that offer similar functionality.
- **F. Brand/Website/Identity:** Branding exploration will be performed to create an recognizable identity for developers. This will include messaging and assets that will be used throughout the promotional and educational materials required for the adoption of the project. A website complete with marketing materials for developers, documentation, and guides will leverage this brand to help new developers get started creating applications on EOSIO.
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

The original libraries developers have to work with today are limited in their design and do not allow modern EOSIO developers to leverage the technology within their applications properly. Examples of the struggles when using the existing SDKs include the ability to easily integrate wallets, multiuser session management, providing resources for the user, transaction fee models, proper error handling and correction, their non-modular code design, inexistent process hooks, lack of extensability, lack of fault tolerance, and finally the lack of ongoing development and future maintenence.

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

The Greymass team has for over 3 years been building the core EOSIO components required for a framework of modern web client SDKs. Many of the components for this new project can lean heavily on our previous work as we work to create the new suite of products to ease development for EOSIO developers.

**Wallet+ Blue Paper**

[TODO] - Link to blue paper and explain.

**Web - Core Library**

During the creation of the EOSIO Signing Request libraries, the Greymass team encountered significant hurdles and impossible situations while trying to develop the codebase with eosjs. Due to this, the team started work on a fundamentally different set of SDKs with modularity and flexibility in mind to serve as a replacement.

These efforts led to the creation of the `@greymass/eosio` SDK to allow for more advanced usage of EOSIO technologies.

- https://github.com/greymass/eosio-core

This existing code with minimal modification can serve as the Core Library for the new suite of web SDKs. Further work will need to be done to create additional data types and functionality.

**Web - Core Library Extensions**

[TODO]

- https://github.com/greymass/eosio-resources
- https://github.com/greymass/eosio-webauthn
- https://github.com/greymass/eosio-key-encryption

**Web - Client Libraries**

[TODO]

Protocol: https://github.com/greymass/anchor-link/blob/master/protocol.md

- https://github.com/greymass/anchor-link
- https://github.com/greymass/anchor-link-browser-transport
- https://github.com/greymass/anchor-link-console-transport
- https://github.com/greymass/anchor-link-session-manager
- https://github.com/greymass/buoy-client
- https://github.com/greymass/buoy-nodejs
- https://github.com/greymass/hyperbuoy

**EOSIO Signing Request (ESR)**

One of the core components Greymass started with the development of Anchor was the ESR protocol. This was to standardize data types while communicating EOSIO information between various applications. This standard represents a way to effectively encapsulate transasction data and metadata for transmission.

This protocol was developed into EEP-7 and published in early 2019, while undergoing 3 iterations:

- https://github.com/eosio-eps/EEPs/blob/master/EEPS/eep-7.md

Greymass then also developed the SDKs required to interact with this standard for web clients (JS) and mobile applications (Swift/Java):

- https://github.com/greymass/eosio-signing-request
- https://github.com/greymass/eosio-signing-request-java
- https://github.com/greymass/swift-eosio

The ESR protocol will be at the core of the new client libraries as the primary method to pass transaction data between the various components in the suite.

## Development Roadmap

[TODO]

## Future Plans

[TODO]

> Please include here

- how you intend to use, enhance, promote and support your project in the short term, and
- the team's long-term plans and intentions in relation to it.

## Additional Information

[TODO]

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

> Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
