# EOS Network Foundation Grant Proposal

- **Project Name:** Chronicle

- **Team Name:** Zaisan BV

- **EOS Payment Address:** zaisanfinanc

- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 2

- **Pomelo Grant(s):** https://pomelo.io/grants/accounting

- **Project was part of Token sale:** No

- **Repository where Project resides:** https://github.com/EOSChronicleProject/eos-chronicle


## Contact

- **Contact Name:** Daniel Liven

- **Contact Email:** daniel@zaisan.io

- **Website:** https://zaisan.io/about/


## Project Overview

[Chronicle](https://github.com/EOSChronicleProject/eos-chronicle) is a
software package designed for processing the EOSIO state history. It
connects to a state history EOSIO node and exports the historical data
in a JSON object stream to its consumer. The software has been in use
in many different projects on public and private EOSIO blockchains.

The development has started after a crowdfunding round on EOS in
Autumn 2018. 15 different teams, among which were EOS block producers,
wallets, and software companies, have collected an equivalent of about
USD 30,000 into a multisig EOS account. By the time the first release
was ready for shipment, the EOS amount was equivalent to approximately
USD 15,000. Later on, several public grants on Telos, and a few
commercial projects, have supported further development.

The ["accounting" Pomelo grant](https://pomelo.io/grants/accounting)
has partially contributed to Chronicle software support and
development, although most of its funds went into hosting expenses.

This grant application will add a number of demanded features and
secure the future of Chronicle.

The original author of the software, working under the "cc32d9"
pseudonym, is part of Zaisan as a senior consultant.


### Overview

- **Name:** Chronicle development.

- **Brief Description:** New features and software maintenance of Chronicle software.

- **Relationship to EOSIO:** Chronicle is one of the popular readers for EOSIO state history data.

- **Reason for Interest:** cc32d9 is the original author and active supporter of the software.


### Project Details

The project will deliver a few long-waited enhancements, and a number
of new features.

Software maintenance tasks:

- Update Chronicle to work with latest releases of dependency
  libraries (Boost.org and EOSIO/Mandel libraries).

- Build scripts for Ubuntu binary packages; publish the binary packages.

- Update the Chronicle Tutorial to reflect new changes.

- Software support and maintenance during 2022.

New features:

- JavaScript NPM for Chronicle consumer: redesign the asynchronous mode.

- Research and look for alternative ways to store Chronicle data (currently EOSIO chainbase is in use).


### Ecosystem Fit

Chronicle has been an integral part of EOSIO software ecosystem for
about 3.5 years. It is the tool that allows application developers to
receive real-time updates from the blockchain, and maintain the
history of their transactions.

There are several other software solutions for reading the state
history. But they are either too specific for a particular task, or
not fast enough for bulk processing. Chronicle offers a universal
solution, and it is currently the fastest way to decode the state
history.

## Team

### Team members

- **Team Leader:** CTO of EOS Amsterdam and Senior Consultant at
    Zaisan.io, working under "cc32d9" pseudonym.

- Daniel Liven, managing the legal and financial aspects.

### Legal Structure
- **Registered Legal Entity:** Zaisan BV
- **Registered Address:** Keizersgracht 391A, 1016 EJ, Amsterdam, The Netherlands

### Team Experience

Zaisan has been around in EOSIO ecosystem for several years, formally
known as Europechain BV. The company is founded by several European
block producers, and is focusing on software projects and business
consultancy.

The company has previously taken the task of writing the EOSIO Core+
Blue Paper on request of ENF. 

### Team Org Repos

- https://github.com/Europechain
- https://github.com/eos-amsterdam-rnd

### Team Member Repos

- https://github.com/cc32d9

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/dliven/

## Development Status

- [Initial proposal and crowdfunding proceedings](https://github.com/cc32d9/eos-work-proposals/tree/master/001_EOS_Chronicle)
- [Main project repository](https://github.com/EOSChronicleProject/eos-chronicle)
- [Chronicle tutorial](https://github.com/EOSChronicleProject/chronicle-tutorial)
- [JavaScript NPM for Chronicle consumers](https://github.com/EOSChronicleProject/chronicle-consumer-npm)
- Blog publications: [fundraising](https://cc32d9.medium.com/fundraising-for-chronicle-and-history-indexer-26e0a06c2d1d), [overview of history solutions](https://cc32d9.medium.com/history-and-notifications-in-eosio-blockchain-8255194af93)

## Development Roadmap

### Overview

- **Total Estimated Duration:**  4 months
- **Full-Time Equivalent (FTE):**  0.25
- **Total Costs:** USD 20,000

### Milestone 1 — Chronicle software update

- **Estimated duration:** 2 months
- **FTE:**  0.25
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | Updated Chronicle README and the Tutorial to reflect all the recent changes |
| 0c. | Testing Guide | Tests scripts and guides will be part of documentation |
| 1. | Update dependencies | Update Chronicle to work with latest releases of dependency libraries (Boost.org and EOSIO/Mandel libraries).|  
| 2. | Ubuntu packages | Crate package build scripts; publish the packages for public download |   
| 3. | JavaScript NPM | Redesign the asynchronous mode to avoid memory overflow |  
| 4. | Third party contributions | Integrate, test and document third-party contributions, such as Docker and Kubernetes images |


### Milestone 2 — Research

- **Estimated duration:** 2 month
- **FTE:**  0.25
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1 | Alternative DB backend | Current Chronicle uses EOSIO Chainbase for its data. An alternative, more lightweight and less demanding, backend needs to be researched, and possibly taken for the next release. |


### Milestone 3 — Support and maintenance

- **Estimated duration:** 18 months
- **FTE:**  0.01
- **Costs:** 4,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1 | Software support | Processing bug reports and third-party contributions, updating the documentation, publishing new releases |




## Future Plans

The Chronicle software is versatile and modular, and easy to integrate
in other solutions. Probably a future history solution for EOSIO
blockchains will use Chronicle as an integral part. Also there is a
market demand for various streaming and notification services, and
Chronicle would easily fit for such services.

## Additional Information

**How did you hear about the Grants Program?** Twitter and Discord
