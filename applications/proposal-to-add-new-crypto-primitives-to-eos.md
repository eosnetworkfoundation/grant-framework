# EOS Network Foundation Grant Proposal

- **Project Name:** Proposal to Add New Crypto Primitives to EOS
- **Team Name:** ZeroPass
- **Payment Address:** zeropassxxxx
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3


## Project Overview


### Overview
We are proposing to add different signature verification algorithms for EOS. There are different ways to achieve this, but back and forth with different core developers lands us on trying to implement them as SDK library for smart contracts, with probably OC compilation flag needed for more complex ECC math.
Please provide the following:

**Why those specific signature verification algorithms?** 
These algorithms are among others included in eMRTD standard, which means they can be used in biometric passports and increasingly more in local ID documents (biometric). The specific algorithms are needed to onboard the massive Public Key Infrastructure (PKI) provided by countries to an EOS blockchain. ECC Brainpool standard curves is Grmany pushed crypto, for certificates of all sorts. The P-384 elliptic curve is recommended by NIST, and RSASSA-PSS is fixing and replacing all RSA RSA-PKCS#1 v1.5 certificates in newer deployments.  Our solution Port is at the moment designed to run off-chain on a central server, having these cryptographic primitives and algorithms will allow us to move the solution to fully on-chain.



### Project Details

We implemented a [EOSIO Cryptography Kits](https://github.com/ZeroPass/eosio.ck) the fastest RSA implmenetation for EOSIO. It can ran RSA4096 verificaitons on the mainnet today. We also have a working [PoC Port smart contract](https://github.com/ZeroPass/eosio-port). The smart contract can already do passive and active passport attestation for passports based on RSA PKCS 1.5 PKI. 

The project itself is best described by deliverables, so to avoid repeating we will try to manage expectations by disclosing shortcomings of the presented use case of full-on Passport identity on EOS blockchain, that we come around to while deploying the server version. Some (rare) countries' old passports don’t have ANY passport cloning prevention mechanism (e.g.: older US passports before next geneartion passport - NGP). For those old passports we will have to use oracle, not full on-chain verification. That being said, this kind of verification can be flagged as lower-level confidence. All newer passports have some sort of protection against passport cloning, but some countries don't implement Active Authentication AA - they can’t sign and directly prove to the public that the passport isn’t cloned. This passports can only prove to an oracle (server) that the passport wasn't cloned using Diffie-Hellman based chip authentication protocol. In this case, the passport can be fully verified on-chain (trust chain), but passport genuineness has to be verified by the oracle. The verification can still be fully automated, but it does require some trust in the oracle's claims that it had verified the authenticity of the passport. The oracle passport verification will require some decent amount of crypto work. This proposal alone won’t be able to deliver everything to full completion, but it does solve 70% of the problems we have to make the Port solution come to life fully on blockchain.


### Ecosystem Fit

Port can be used as a better version of (anonymous) identity on the blockchain. It's open-source and open-access nature allows any dapp to plug into it, and profit from the infrastructure it provides. It fixes the issue with DIDs, where self-sovereign identity in the practice always gets implemented as one KYC provider signing the attestations. Here the passport proves authenticity itself, cutting the middle man and cutting friction associated with it. I.e.: removing the costs and needed trust (don't be evil, versus can't be evil). Adding different signature verification algorithms can serve as crypto primitive for EOSIO, and upon which our contract can be built on. To expand the use-cases we are mainly focusing on: making the Port a native way for EOS to solve Sybil protection, Identity, and multiple levels of verifications.

Right now, there are projects such as Pomelo and EOS Support integrating Port to help prevent Sybil attacks for their platforms (we would like to move it fully on-chain later). These signature verification algorithms will also benefit Randall Roland’s (CEO EOS Support) proposal that seeks to improve the user onboarding process of the EdenOS software. If successful, it might be the basis for the identity of the future Eden version. The development would allow users to skip video calls for Sybil check and switch to a more asynchronous election. Group calls could be postponed to a better time for everyone in the group, or could even become optional if the groups can achieve consensus on Telegram chats. Our team has also been contacted by different NFT projects looking to do wide NFT drops, without the claimed abuse they detect right now. There are nice humanitarian applications, for instance, somebody can start an easy project to provide UBI-style donations to people with Ukrainian passports.

## Team

### Team members

- Luka Percic
- Crt Vavros
- Nejc Skerjanc

### Contact

- **Contact Name:** Luka Percic
- **Contact Email:** zeropass@pm.me
- **Website:** [zeropass.io](https://zeropass.io/)

### Legal Structure
- **Registered Legal Entity:** ZP Aplikacije d.o.o.
- **Registered Address:** Tublje pri Komnu 5, Dutovlje, Slovenia

### Team Experience

ZeroPass is a team of 3 from Slovenia (EU) with product/developers/cryptography skills.
Our most notable accomplishments in EOS community are:

- High severity [bug discovery in EOSIO node](https://b1.com/press/eosio-ram-resource-exploit-patch/) and disclosed through B1 hacker one bounty.
- EOS smart contract for BPs rotation.
- EOS smart contract for RAM resource market (RAM token).
- Providing bug fixes and patches for EOSIO CDT and EOSIO node software.
- 3rd place with [ROW project](https://github.com/ZeroPass/row.contract) at B1 hackathon / Google Cloud Platform, for proving WebAuthn to be fully done on-chain.
- [eosio.ck](https://github.com/ZeroPass/eosio.ck) - RSA & SHA-3 cryptography library for EOSIO smart contract.

### Team Code Repos

- https://github.com/ZeroPass
- https://github.com/ZeroPass/eosio.ck
- https://github.com/ZeroPass/eosio-port

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
- https://github.com/ZeroPass/eosio.ck


We also built and deployed port itself (server solution) that acts as our beta version for what we are trying to move on chain. In addition, we already experimented and built Port PoC smart contract for passport attestation on-chain (RSA PKCS 1.5 PKI only). 
- https://github.com/ZeroPass/eosio-port

We can also attach research from our documentation (which is not completly up to date). It is presented in the [In-depth section](https://github.com/ZeroPass/Port-documentation-and-tools#in-depth).

## Development Roadmap

- **Total Estimated Duration:** 5,5-7 months
- **Full-Time Equivalent (FTE):**  16,5-21 FTE months
- **Total Costs:** $120.000

### Milestone 1 - Opensource RSA

- **Estimated duration:** 0 month
- **FTE:** 0
- **Costs:** 20.000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation and step by step guide already provided in [README.md](https://github.com/ZeroPass/eosio.ck/blob/master/README.md).  | 
| 0c. | Testing Guide | [In the guide](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#algorithm-testing=), we are describing how to run those tests. |
| 0d. | Running it | We deployed on the [Jungle 3 and CryptoKylin testnets](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#testnet=). |
| 1. | EOSIO SDK library | Open-sourcing RSA PKCS v1.5 signature verification algorithm and the Keccak hash algorithms: SHA3-256, SHA3-512, SHAKE-128 and SHAKE-256 found in the [EOSIO Cryptography Kits](https://github.com/ZeroPass/eosio.ck) |

We built, optimized, tested and deployed on the testnet to make it the fastest wasm RSA implementation in eosio. For example, it can verify RSA 4096 bit keys consistently under 10ms (3ms on average, much faster for the more standard  RSA 2048 bit).

We want to charge 20k$ to open source it (MIT license). That will also allow us to commit to work on the next items, even when delivery itself isn’t guaranteed because of unknown unknowns and EOSVM  limits that might turn multiple taken approaches into a no-go.  

### Milestone 2 - RSASSA-PSS

- **Estimated duration:** 1 month
- **FTE:** 3 FTE months
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation and step by step guide will be updated in [README.md](https://github.com/ZeroPass/eosio.ck/blob/master/README.md).  | 
| 0c. | Testing Guide | [In the guide](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#algorithm-testing=), we will describe how to run those tests. |
| 0d. | Running it | We will deploy on the [Jungle 3 and CryptoKylin testnets](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#testnet=), or provide Docker if OC flag (Optimized Compilation) will be required for it to run. |
| 1. | EOSIO SDK library | RSASSA-PSS signature verification algorithm. It is a probabilistic and provably secure RSA signature scheme as opposed to RSA PKCS v1.5. |

All updated cryptosystems are switching to RSASSA-PSS.

### Milestone 3 - EC math primitives

- **Estimated duration:** 2.5-3.5 month
- **FTE:** 7.5-10.5 FTE months
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation and step by step guide will be updated in [README.md](https://github.com/ZeroPass/eosio.ck/blob/master/README.md).  | 
| 0c. | Testing Guide | [In the guide](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#algorithm-testing=), we will describe how to run those tests. |
| 0d. | Running it | We will deploy on the [Jungle 3 and CryptoKylin testnets](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#testnet=), or provide Docker if OC flag (Optimized Compilation) will be required for it to run. |
| 1. | EOSIO SDK library | General-purpose math primitives (i.e. addition, multiplication, inverse etc…)  for elliptic curve arithmetics over an arbitrary finite field. |

This will allow defining higher-level cryptography EC algorithms (e.g. ECDSA verification algo) on custom elliptic curves in smart contract. **The primitives will be built on top of the existing secure and audited EC cryptography library.**

### Milestone 4 - ECDSA

- **Estimated duration:** 1-3 months
- **FTE:** 3-9 FTE months
- **Costs:** 40,000 USD (10,000 USD per signature algorithm)

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation and step by step guide will be updated in [README.md](https://github.com/ZeroPass/eosio.ck/blob/master/README.md).  | 
| 0c. | Testing Guide | [In the guide](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#algorithm-testing=), we will describe how to run those tests. |
| 0d. | Running it | We will deploy on the [Jungle 3 and CryptoKylin testnets](https://github.com/ZeroPass/eosio.ck/blob/master/README.md#testnet=), or provide Docker if OC flag (Optimized Compilation) will be required for it to run. |
| 1. | EOSIO SDK library | To implement different ECDSA signature verification algorithms for other ECC curves, we will write example implementation for **P-384** which will include adding **sha-384** |
| 2. | EOSIO SDK library | Example implementation for **BrainpoolP256r1** |
| 3. | EOSIO SDK library | Example implementation for **BrainpoolP384r1** |
| 4. | EOSIO SDK library | Example implementation for **BrainpoolP512r1** |

### Milestone 5 - A cryptographic system contract

- **Estimated duration:** 1 month
- **FTE:** 3 FTE months
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation and step by step guide will be provioded in contract repository readme | 
| 0c. | Testing Guide | We will write instructions how to run tests in the guide posted in contract repository readme |
| 0d. | Running it | We will deploy on the Jungle 3 and CryptoKylin testnets, or provide Docker image if running eos node in OC mode (Optimized Compilation) will be required. |
| 0e. |	Article | 	We will publish an article that explains why adding these signature algortims makes EOS much more ready to onboard goverment supported projects. We would also present why doing the same on other blockchain platforms without hard fork is close to impossible curtesy of EOSVM speed and Optimized Compilation.|
| 1. | EOSIO Smart Contract | A cryptographic smart contract meant to be deployed by BPs, and used by many dapp developers |

Milestones 1,2,3 and 4 will be part of the crypto SDK library which anyone can use in their smart contracts. We expect that running node in OC mode will be required for some cases (we'll try to omit it), this would make it necessary for the BPs to deploy it using eosio privileged permissions. We can't expect every developer to have access to BP's contract deployment and as such, it should be deployed in a form of system contract. The contract contains all described cryptographic primitives and verification actions, and allows other contracts to pass their data for verification to it. This way only one contract needs to be maintained by the BPs, and the whole proposal can become a crypto primitive for other dapps to utilize. 


## Future Plans

**Pending additional research;**
We might be able to also implement ECC curve alt_bn128 curve which is widely available on other major blockchain platforms like EVM and Polkadot. We will feel more comfortable promising delivery after at least ECC general implementation is done.

We are planning to rebuild [Port](https://port.link/) on-chain, and this proposal provides the crypto primitives needed to begin the process.
Our RSA PKCS 1.5 implementation is also already used in our another project: [ROW](https://row.link/), which hopefully will one day become a full-fledged webauthn signer.
In the more distant future we are also planning to build dapp on top these projects, using both on-chain Port and ROW projects as building blocks.

## Additional Information

**How did you hear about the Grants Program?** 
Telegram

We also invite all to donate on Pomelo for our current [implementation of Port](https://pomelo.io/grants/ygc2lp2oe), and try increasing your Pomelo [Trust Bonus](https://pomelo.io/profile?tab=trust).
