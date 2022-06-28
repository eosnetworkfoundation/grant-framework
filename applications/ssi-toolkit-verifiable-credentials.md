# EOS Network Foundation Grant Proposal

- **Project Name:** Verifiable Credentials for the EOSIO SSI Toolkit
- **Team Name:** Tonomy Foundation
- **EOS Payment Address:** tonomyaccou1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/Tonomy-Foundation/EOSIO-SSI-Toolkit

## Contact

- **Contact Name:** Jack Tanner
- **Contact Email:** jack@tonomy.foundation
- **Website:** https://tonomy.foundation

## Overview

- **Name:** Allow any EOSIO account to issue, hold and verify Verifiable Credentials signed by their EOSIO account key(s)
- **Brief Description:**
The SSI kit allows software developers to use self-sovereign identity in their EOSIO applications. This open-source typescript library can be used on public or private EOSIO chains and is consumed by wallets and front-end clients to provide SSI functions with EOSIO DIDs. The kit aims to have two main components:
  - Verifiable credentials - this allows any EOSIO account to create, hold and verifiable credentials and send them in a verifiable presentation. This can be used with personal information, medical records, certificates or any other data. It can be used and verified with another account.
  - DIDComm - A standardised transport between any EOSIO account to any other account, privately and securely.

**This grant proposal focuses on building the first component of the toolkit - verifiable credentials.** We will build the typescript library allowing application developers to use Verifiable Credentials on EOSIO identities. DIDComm will be built later.

This grant aims to fill the needs set out in the SSI section of the [CORE+](https://drive.google.com/file/d/1UVnGDzwp76YUoQnnFWgMDwEYTPmWw_fT/view) paper. It creates an alternative, privacy-preserving and internationally standardized approach to the “Profile and avatar system” set out in the [Wallet+](https://drive.google.com/file/d/18_aLgCo6uAJN1-ZT1mtUs59SxwffhShm/view) paper.

For an introduction to SSI check out:
https://github.com/animo/awesome-self-sovereign-identity

See README.md in the repository for an example usage:
https://github.com/Tonomy-Foundation/EOSIO-SSI-Toolkit
