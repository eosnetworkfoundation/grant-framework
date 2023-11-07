# EOS Cryptography Proposal 2 b

- **Project Name:** EOS Cryptography Proposal 2 b
- **Team Name:** ZeroPass
- **EOS Payment Address:** portxxxxxxxx
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s)**  
https://pomelo.io/grants/ygc2lp2oe  
https://pomelo.io/grants/bot4eden
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/ZeroPass/ack


## Contact

- **Contact Name:** Luka Percic
- **Contact Email:** zeropass@pm.me
- **Website:** [port.link](https://port.link/)

## Project Overview


### Overview
We are exploring ways to introduce new signature verification algorithms to EOS smart contracts, including RSA and algorithms based on elliptic curves. There are various approaches to achieve this, and our research of various libraries in the [eos-cryptography-proposal](https://github.com/lukapercic/grant-framework/blob/main/applications/eos-cryptography-proposal.md) led us to implement some of the algorithms in our own ACK cryptographic library.  
Currently, signature verification using EC P-256 takes approximately ~7 ms in optimized compilation (OC). For Brainpool curves, we anticipate the verification time to exceed 10 ms, particularly for the 512-bit curve(s). Through the optimizations proposed in this grant, we aim to extract more performance and significantly reduce the verification times. Additionally, we are proposing implementation of ECDSA key recovery algorithm, new elliptic curves, and the SHA-384 hashing algorithm into the ACK library, making them available for EOS smart contracts.

### Project Details

We have implemented [Antelope Cryptography Kits](https://github.com/ZeroPass/ack), a cryptographic library for the Antelope blockchain. This library supports basic elliptic curve mathematical operations, certain modular arithmetics, EC signature verification algorithms (P-256 and secp256k1), and the fastest RSA signature verification implementation for EOSIO. It can perform RSA-4096 verifications on the mainnet today. Furthermore, we have a working [PoC Port smart contract](https://github.com/ZeroPass/eosio-port). The smart contract can already do passive and active attestation of biometric passports which uses RSA PKCS 1.5 signature scheme. 

This proposal aims to optimize the current EC implementation in the ACK library and accelerate EC-based signature verification algorithms. Specifically, we intend to introduce another coordinate system, such as the Jacobian system or the mixed Jacobian/Chudnovsky coordinate system, with the goal of reducing the number of required EC division operations. This enhancement is expected to significantly boost performance.

Furthermore, we are proposing the implementation of an ECDSA key recovery algorithm, which would reduce the need for the full public key during verification. Instead for example, a key hash could be utilized to verify the EC signature.

Moreover, this proposal also aims to introduce widely used elliptic curves and the SHA-384 hashing algorithm (commonly used with some EC, such as P-384).

### Ecosystem Fit

Port can be used as a better version of (anonymous) identity on the blockchain. Its open-source and open-access nature allows any dapp to plug into it, and profit from the infrastructure it provides. It fixes the issue with DIDs, where self-sovereign identity in the practice always gets implemented as one KYC provider signing the attestations. Here the passport proves authenticity itself, cutting the middle man and cutting friction associated with it. I.e.: removing the costs and needed trust (don't be evil, versus can't be evil). Adding different signature verification algorithms can serve as crypto primitive for Antelope, and upon which our contract can be built on. To expand the use cases we are mainly focusing on making the Port a native way for EOS to solve Sybil protection, Identity, and multiple levels of verifications.

Right now, there are projects such as Pomelo and EOS Support integrating Port to help prevent Sybil attacks for their platforms (we would like to move it fully on-chain later). These signature verification algorithms will also benefit Randall Roland’s (CEO EOS Support) proposal that seeks to improve the user onboarding process of the RespectOS software. If successful, it might be the basis (or part of) the identity of the future EOS-based DAOs.  We have been contacted by different NFT projects looking to do wide NFT drops, without the claimed abuse they detect right now. There are nice humanitarian applications, for instance, somebody can start an easy project to provide UBI-style donations to people with passports and IDs from affected countries. We are also defining a new concept of Escape Tokens, that allows governance and distribution tokens to escape the main liquidity pair, and when thriving, its value overflow to Port identities in (UBI style). 

In short; it is a real ID/Sybil building block that will enable many projects to plug and play. 

## Team

### Team members

- Luka Percic
- Crt Vavros
- Nejc Skerjanc

### Legal Structure
- **Registered Legal Entity:** Žerjal IT, d.o.o.
- **Registered Address:** Brje pri Komnu 40, 6223 Komen, Slovenia

### Team Experience

ZeroPass is a team of 3 from Slovenia (EU) with product/developers/cryptography skills.
Our most notable accomplishments in EOS community are:

- High severity [bug discovery in EOSIO node](https://b1.com/press/eosio-ram-resource-exploit-patch/) and disclosed through B1 hacker one bounty.
- EOS smart contract for BPs rotation.
- EOS smart contract for RAM resource market (RAM token).
- Providing bug fixes and patches for EOSIO CDT and EOSIO node software.
- 3rd place with [ROW project](https://github.com/ZeroPass/row.contract) at B1 hackathon / Google Cloud Platform, for proving WebAuthn to be fully done on-chain.
- [ack](https://github.com/ZeroPass/ack) - ECC primitives and ECDSA verification algorithms, RSA & Keccak hash algorithms cryptography library for Antelope smart contract.

### Team Code Repos
- https://github.com/ZeroPass
- https://github.com/ZeroPass/ack

 ### Team Members GitHub Accounts
- https://github.com/smlu
- https://github.com/nejc-skerjanc
- https://github.com/lukapercic

### Team LinkedIn Profiles
- https://www.linkedin.com/in/nejcskerjanc/
- https://www.linkedin.com/in/crt-vavros/
- https://www.linkedin.com/in/lukapercic/

## Development Status

**RSA PoC**
We painstakingly built, optimized, tested and deployed on the testnet to make it the fastest wasm RSA implementation in eosio. For example, it can verify RSA 4096 bit keys consistently under 10ms (3ms on average, much faster for the more standard  RSA 2048 bit).
- https://github.com/ZeroPass/ack


Our team built and deployed Port itself (server solution) which acts as our beta version for what we are trying to move on the chain. In addition, we already experimented and built Port PoC smart contract for passport attestation on-chain (RSA PKCS 1.5 PKI only). 

## Development Roadmap

- **Total Estimated Duration:** 19 weeks
- **Full-Time Equivalent (FTE):**  57 FTE weeks
- **Total Costs:** $87,000

### Milestone 1 - Optimization
- **Estimated duration:** 12 weeks
- **FTE:** 36 FTE weeks
- **Costs:** $55,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation and step-by-step guide will be updated in [README.md](https://github.com/ZeroPass/ack/blob/master/README.md).  | 
| 0c. | Testing Guide | [In the guide](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#algorithm-testing=), we will describe how to run those tests. |
| 0d. | Running it | We will re-deploy on the [Jungle 4](https://github.com/ZeroPass/ack/blob/master/README.md#testnet).|
| 1. | Antelope SDK library | Optimized EC arithmetic by using another coordinate system, such as the Jacobian coordinate system or the mixed Jacobian/Chudnovsky system.
| 2. | Antelope SDK library | Sha-384 |

Preliminary tests of using Jacobian coordinate system suggest a ~2-fold increase in speed using such a system.

### Milestone 2 - Adding Curves
- **Estimated duration:** 7 weeks
- **FTE:** 21 FTE weeks
- **Costs:** $32,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation and step-by-step guide will be updated in [README.md](https://github.com/ZeroPass/ack/blob/master/README.md).  | 
| 0c. | Testing Guide | [In the guide](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#algorithm-testing=), we will describe how to run those tests. |
| 0d. | Running it | We will re-deploy on the [Jungle 4](https://github.com/ZeroPass/ack/blob/master/README.md#testnet). |
| 1. | Antelope SDK library | Implementation of P-384, P-512 NIST curves |
| 2. | Antelope SDK library | Implementation of brainpoolP256r1, brainpoolP320r1, brainpoolP384r1, brainpoolP512r1 Brainpool curves |
| 3. | Antelope SDK library | Implementing ECDSA key recovery from signature |



## Future Plans
**Expected Part 3 of the proposal**  
- Implementation of EdDSA,
- Writing a "system" contract so any outside contracts can consume it. That way BPs can deploy it on eosio.* account to enable Optimized Compilation (OC) in the EOS public chain. 

**Pending additional research;**  
Possibility of implementation for ECC curve alt_bn128 curve which is widely available on other major blockchain platforms like EVM and Polkadot.

We are planning to rebuild [Port](https://port.link/) on-chain and this proposal provides the crypto primitives needed to begin the process.
Our RSA PKCS 1.5 implementation is also already used in another project: [ROW](https://row.link/), which hopefully will one day become a full-fledged WebAuthn signer.
In the more distant future, we are also planning to build a dapp on top of these projects, using both on-chain Port and ROW projects as building blocks.

## Additional Information

**How did you hear about the Grants Program?** 
Telegram

We also invite all to donate on Pomelo for our current [implementation of Port](https://pomelo.io/grants/ygc2lp2oe) and try increasing your Pomelo [Trust Bonus](https://pomelo.io/profile?tab=trust).
