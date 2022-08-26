#

# **EOS Network Foundation Grant Proposal**

- **Project Name:** Verifiable Credentials for the Antelope SSI Toolkit
- **Team Name:** Tonomy Foundation
- **EOS Payment Address:** tonomyaccou1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 2
- **Pomelo Grant(s):** <https://pomelo.io/grants/recovery>
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** [https://github.com/Tonomy-Foundation/Antelope-SSI-Toolkit](https://github.com/Tonomy-Foundation/Antelope-SSI-Toolkit)

## **Contact**

- **Contact Name:** Jack Tanner
- **Contact Email:** jack@tonomy.foundation
- **Website:** [https://tonomy.foundation](https://tonomy.foundation/)

## **Project Overview**

### **Overview**

#### **Name**

Allow any Antelope account to issue, hold and verify Verifiable Credentials signed by its Antelope account key(s)

#### **Brief Description**

[Glossary of terms](https://tonomy-foundation.notion.site/de24bdb6655e4ca397028dbed217eedb?v=d4a1cf04d48c4337968c0d99fe0cc378)

The self-sovereign identity (SSI) toolkit allows software developers to use self-sovereign identity in their Antelope applications. This open-source typescript library can be used on public or private Antelope chains and is consumed by wallets and front-end clients to provide SSI functions with Antelope [DIDs](https://w3c.github.io/did-core/). The kit aims to have two main components:

1. Verifiable credentials - this allows any Antelope account to create, hold and verify [verifiable credentials](https://www.w3.org/TR/vc-data-model) (VC). This can be used with personal information, medical records, certificates or any other data. It can be used and verified with another account.
2. [DIDComm](https://identity.foundation/didcomm-messaging/spec/) - A standardised transport between any Antelope account and any other account, privately and securely.

**This grant proposal focuses on building the first component of the toolkit - verifiable credentials**. We will build the typescript library allowing application developers to use Verifiable Credentials on Antelope identities. DIDComm will be built later. The Verifiable Credentials library is currently the most important part of the Antelope SSI Toolkit.

This grant aims to fulfill the needs outlined in the SSI section of the CORE+ paper. It creates an alternative, privacy-preserving and internationally standardized approach to the &quot;Profile and avatar system&quot; set out in the Wallet+ paper.

For an introduction to SSI, check out [Core+ paper (section 8)](https://drive.google.com/file/d/1UVnGDzwp76YUoQnnFWgMDwEYTPmWw_fT/view) or the links in the [Awesome SSI](https://github.com/animo/awesome-self-sovereign-identity) resource list.

This is an _example_ showing how you can use this library to issue a Verifiable Credential signed by the &quot;active&quot; key of an Antelope account. The final implementation interface may differ, but will have the same functionality.

```js
const { JsSignatureProvider } = require('eosjs/dist/eosjs-jssig');  // development only
const { Credentials } = require('@Tonomy/Credentials');

const myId = "did:eosio:telos:mytelosaccount";
const universityId = "did:eosio:telos:exampleuniversity";
const universityVerificationMethod = "did:eosio:telos:exampleuniversity#active";

const credential = {
  "@context": [
    "https://www.w3.org/2018/credentials/v1",
    "https://www.w3.org/2018/credentials/examples/v1"
  ],
  id: myId,
  type: ["VerifiableCredential", "AlumniCredential"],
  issuer: universityId,
  issuanceDate: new Date("2010-01-01T19:23:24Z"),
  credentialSubject: {
    id: myId,
    alumniOf: "Example University"
  }
};

const universityActivePrivateKey = "5JReG19oN7f3R2XQt8Pb8qDYYHJsjoEnx8gcYcitLEK8RWrdqDt"
const credentials = new Credentials();
const signatureProvider = new JsSignatureProvider(universityActivePrivateKey);
const signedCredential = await credentials.issue(universityVerificationMethod, signatureProvider, credential);
console.log(signedCredential);
// credential {
//   ...
//   proof: {
//     type: "EcdsaSecp256k1VerificationKey2019";
//     created: "2010-01-01T19:23:24Z";
//     proofPurpose: "assertionProf";
//     verificationMethod: "did:eosio:telos:exampleuniversity#active";
//     jws: "ewogICJhbGciOiAiUlMyNTYiLAogICJraWQiOiAiMTMzNzQ3MTQxMjU1IiwKICAiaWF0IjogMCwKICAiaXNzIjogIkM9R0IsIEw9TG9uZG9uLCBPVT1OdWFwYXkgQVBJLCBPPU51YXBheSwgQ049eWJvcXlheTkycSIsCiAgImI2NCI6IGZhbHNlLAogICJjcml0IjogWwogICAgImlhdCIsCiAgICAiaXNzIiwKICAgICJiNjQiCiAgXQp9..d_cZ46lwNiaFHAu_saC-Zz4rSzNbevWirO94EmBlbOwkB1L78vGbAnNjUsmFSU7t_HhL-cyMiQUDyRWswsEnlDljJsRi8s8ft48ipy2SMuZrjPpyYYMgink8nZZK7l-eFJcTiS9ZWezAAXF_IJFXSTO5ax9z6xty3zTNPNMV9W7aH8fEAvbUIiueOhH5xNHcsuqlOGygKdFz2rbjTGffoE_6zS4Dry-uX5mts2duLorobUimGsdlUcSM6P6vZEtcXaJCdjrT9tuFMh4CkX9nqk19Bq2z3i-SX4JCPvhD2r3ghRmX0gG08UcvyFVbrnVZJnpl4MU8V4Nr3-2M5URZOg"
//   }

const verifiedCreedential = await credentials.verify(signedCredential);
console.log(verifiedCreedential);
//     verifiedCreedential true
```

See
[https://github.com/Tonomy-Foundation/Antelope-SSI-Toolkit](https://github.com/Tonomy-Foundation/Antelope-SSI-Toolkit)

#### **Relationship to Antelope**

This project leverages the Antelope accounts and the Antelope DID method to sign verifiable credentials. It is a core building block for identity applications on top of all Antelope blockchains, public and private. This software can be used by any Antelope application to send VCs privately among accounts on the same Antelope chain, and also between separate Antelope chains, and also to any other chain or non-chain with a DID method (see [list here](https://www.w3.org/TR/did-spec-registries/#did-methods)).

#### **Reason for Interest**

We believe that these components have a strategic technical value for the Antelope ecosystem and are sorely missing. This case is outlined in the Core+ paper.

To add to what is already written in Core+, SSI brings a number of strong advantages for apps built on Antelope:

1. Interoperability between chains and even to other blockchain systems that comply to the DID standard. This allows all kinds of data (identity, certificationf, medical and more) to be used across the internet in a highly reusable way, reducing data wastage, and ultimately reducing the burden of the user to input the same data into websites over and over.
2. The interoperability layer (DID) allows for standardized communication. This can be used for communications within and between dapps. It could also be leveraged as a standard inter-blockchain communication protocol.
3. SSI adoption has been encouraged and invested in heavily by enterprise companies like IBM and Microsoft as well as the EU, the US and Canada. They have funded or contributed strongly to the development of these technologies and thus likely adopters and evangelists of the technology. This gives validity to the technology and a trusted set of technologies to Antelope chains and applications. It also puts these large-scale enterprises in a strong position to adopt technology, which due to its interoperable nature can be leveraged by Antelope applications.
4. Standardised and well-adopted tooling to allow data standards and transfer across the Internet. Antelope apps can benefit a significant amount of existing SSI tooling that already exists. The DID standard has [moved to a W3C Recommendation](https://www.w3.org/2022/06/DIDRecommendationDecision.html) as of June 30 2022 indicating a serious move towards it becoming an approved Internet standard.
5. Taking identity and other credentials off the blockchain and allowing clients to share it directly is a much more scalable strategy. This allows applications and Antelope chains to scale better.
6. Verifiable Credentials are stored client-side and are privacy-preserving by default. This ensures data privacy legislation compliance out-of-the-box, this is utterly important for areas like the EU (GDPR), the USA with various state-based privacy laws like the New York Privacy Act or others. This is especially important for enterprise and government adoption.

### **Project Details**

#### Data models of the core functionality

DID data model: [https://w3c.github.io/did-core/](https://w3c.github.io/did-core/)

Verifiable Credentials data model: [https://www.w3.org/TR/vc-data-model/#core-data-model](https://www.w3.org/TR/vc-data-model/#core-data-model)

#### API specifications of the core functionality

Verifiable Credentials API: [https://github.com/Tonomy-Foundation/Antelope-SSI-Toolkit/blob/master/src/credentials.ts#L31](https://github.com/Tonomy-Foundation/Antelope-SSI-Toolkit/blob/master/src/credentials.ts#L31)

#### An overview of the technology stack to be used

We will create a typescript library that can be consumed in web apps, nodejs servers and React Native applications allowing them to create and verify VCs.

This typescript library will use the [EOSIO-DID resolver](https://github.com/Gimly-Blockchain/eosio-did-resolver) to fetch DID documents for Antelope accounts and use the cryptographic material (in JWK format) to verify the credential.

We will use an existing Verifiable Credential library to issue and verify the credential. To accomplish this we will need to create an implementation of the [Verifiable Conditions W3C library](https://github.com/w3c-ccg/verifiable-conditions), which is used in the Antelope DID to express the multiple keys in an account. This implementation will take the form of a software module that is imported into the VC library.

Several VC libraries exist, and we will choose the best library for the purpose of signing a VC with an Antelope account&#39;s key. Existing libraries include:

- [https://github.com/decentralized-identity/did-jwt-vc](https://github.com/decentralized-identity/did-jwt-vc)
- [https://github.com/rabobank-blockchain/vp-toolkit](https://github.com/rabobank-blockchain/vp-toolkit)
- [https://github.com/digitalbazaar/vc-js](https://github.com/digitalbazaar/vc-js)
- [https://github.com/Sphereon-Opensource/rn-vc-js](https://github.com/Sphereon-Opensource/rn-vc-js)
- [https://github.com/transmute-industries/verifiable-data](https://github.com/transmute-industries/verifiable-data)

#### PoC/MVP or other relevant prior work or research on the topic

Jack Tanner was the lead engineer for the EOSIO DID. He worked with the Decentralised Identity Foundation (DIF) and the W3C Credentialled Community Group (W3C CCG), creating the W3C Verifiable Conditions standard used in several blockchains including Antelope.

#### What your project is _not_ or will _not_ provide or implement

We will not implement a library for DIDComm or Verifiable Presentations, yet.

### **Ecosystem Fit**

#### Where and how does your project fit into the ecosystem?

The SSI toolkit is used by Antelope wallets and by dapps.

Wallets can store and share credentials related to user data (such as their identity, medical, certificates and more). These credentials can then be shared with dapps that can use them, and even create more credentials to be stored in the wallet. A few example use cases:

1. Store identity data, have this verified by a KYC-provider and then allow this to be reused for KYC in multiple dapps. VCs can be the foundation of a new decentralised KYC service.
2. Store your corona vaccination certificate on your phone&#39;s wallet. You can then share this directly with event owners, or transportation services to allow you entry to their event/vehicle. Unlike a traditional identity service, sharing a credential goes directly from your phone to their device and does not require a third party service to validate the data, significantly improving privacy and scalability.

Dapps do not need you to interact with a wallet to be able to use verifiable credentials. They can be used directly inside the app or directly with other applications. A few examples of use cases:

- A peer-to-peer marketplace where users can buy and sell second-hand cars. Each cars is a credential that is shared directly from the buyer to the seller for final verification before the sale is made.
- A logistics app, tracking shipping containers of bananas. A credential is created for the crate of bananas and signed as an event each time it is moved from a location. It is sent from the person who currently has custody of the container to the new custodian of the banana crate.

#### Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp&#39;s userbase, yourself)?

Our target audience is existing Antelope wallets, as well as Antelope dapps to use these wallets and use the VC libraries themselves.

Tonomy Foundation also plans to integrate this library into their identity wallet (see [overview here](https://github.com/Tonomy-Foundation/EOS-network-foundation-grant-framework/blob/main/applications/tonomy-cross-platform-wallet.md)), to be deployed on the public Antelope blockchains - Telos, EOS and/or WAX.

#### What need(s) does your project meet?

This project solves several issues currently encountered by decentralised applications on Antelope:

1. Identity and accountability
2. Privacy compliance
3. Interoperable data
4. Scaleability

**Identity and accountability** - There is currently a lack of identity solutions in Antelope. This refers to a solution in which information can be shared which identifies the user of an account. This lack of identity solutions leads to accountability problems. It can be seen on democratic apps like Eden, Pomelo and in marketplace scams like on Atomic Hub with NFT sales.

To be clear. The SSI toolkit does not provide a sybil attack prevention mechanism.

It provides a private, highly standardised and, with significant tooling, available way to privately and directly share personal information. This can then be used as part of a private identity and accountability solution.

**Privacy compliance** - Due to the lack of identity solutions mentioned above, several dapps such as Eden, Pomelo, Hypha and more put personal information on (or equivalent through hash anchoring to IPFS) the blockchain. This is the easiest solution they can find to solve accountability issues.

This is illegal in the Europe Union, Brazil, Canada, Chile, China, India, South Korea, several US states and more. Laws in these states have a provision allowing users to request their data to be deleted, a law called the &quot;[right to be forgotten](https://gdpr.eu/right-to-be-forgotten/)&quot; in the EU&#39;s GDPR. A citizen from any of these states could join one of these dapps, and then request that their personal information is removed from the dapp. The personal data is unable to be removed as it is recorded in the blockchain history and stored on every node that stores the history of the blockchain. This gives the citizen the right to sue any and all of these node operators on this network that retains a copy of the data.

SSI gives us a way to store personal data in a decentralised way (on the user&#39;s device), that does not compromise the privacy of the user and allows for accountability solutions to be built around it.

Credentials and other identity data are stored on the phone or connected device of the user. This sovereign data is then fully under their control, meaning they have consent by default over who they share that data with. This is not only a legal privacy compliance measure, but a way of providing a level of ethical control over user data.

**Interoperable data** - Verifiable credentials is a [W3C standardised data model](https://www.w3.org/TR/vc-data-model/). By creating this standard format, credential data can be verified in the same format around the world on all different types of devices, no matter what blockchain they are associated with.

The main standard which VCs rely on is the [decentralised identifier (DID)](https://w3c.github.io/did-core/). The DID standard has just been upgraded to a W3C Recommendation status on 30 June 2022 Signifying that the Standard has, after significant consensus between its members, being endorsed by the W3C. This has happened due to the large amount of adoption of DIDs and VCs. With this status, the [W3C expresses that relevant software](https://www.w3.org/standards/types#REC) &quot;should implement these specifications&quot;. Relevant software includes browsers and other identity management software.

In the coming few years, expect to see more and more adoption of VCs in identity solutions. Ensuring that Antelope is able to participate in this identity movement is critical to ensure it stays at pace with the latest identity technology.

Antelope Verifiable credentials start to align the Antelope ecosystems in these technologies so that it is ready for these enterprise and state-level systems to exist. These should be leveraged due to their interoperable data standards in Antelope applications.

To give an example of what this could mean, if Korea were to adopt SSI as their new digital identity system then a user of an EOS dapp will be able to use their SSI Korean digital passport to log in to their application in a private, anonymous and accountable way in the future. They could then use the same data again (without a fee) to log in to a Microsoft application and prove they are 17+ years old without revealing their date of birth.

**Scaleability** - Sharing credential data directly from one Antelope account to another, without a third party service to verify that data, requires less infrastructure and scales better. Several dapps use the blockchain or IPFS to store third-party data, or servers to store and validate such. With Verifiable Credentials, this data can be stored directly on the user&#39;s device and sent directly to other users when and only when it is needed, without creating the such infrastructure. This reduces the infrastructure burden on projects and Antelope chains and allows them to scale higher.

#### Are there any other projects similar to yours in the Antelope ecosystem?

There are no other projects that allow for Verifiable Credentials based on any Antelope account.

There are currently three DID methods. The EOSIO DID method is used because it remains fully Antelope-protocol compliant. That means that it can be used for any and all unmodified Antelope blockchains.

[https://github.com/Gimly-Blockchain/eosio-did-spec](https://github.com/Gimly-Blockchain/eosio-did-spec)

OmniOne (powered by Antelope) has created a DID method. It is unusable because it deviates from the DID-core standard, as well as relies on proprietary infrastructure, and therefore can only be used on the OmniOne blockchain accounts. Additionally, there is no open-source implementation and no usable DID resolver.

[https://omnione.net](https://omnione.net/)

[https://github.com/OmniOne-Blockchain/did\_method/blob/master/did\_method.md](https://github.com/OmniOne-Blockchain/did_method/blob/master/did_method.md)

Infra Blockchain (powered by Antelope) has created a DID method. It is DID-core standard compliant. This DID method makes a decision about the structure of an Antelope account as well as having an identifier that is specific to Infra Blockchain infrastructure. Because of this, it can only be used on Infra Blockchain accounts.

[https://infrablockchain.com](https://infrablockchain.com/)

[https://github.com/InfraBlockchain/infra-did-method-specs/blob/main/docs/Infra-DID-method-spec.md](https://github.com/InfraBlockchain/infra-did-method-specs/blob/main/docs/Infra-DID-method-spec.md)

## **Team**

### **Team members**

- Team Leader: Jack Tanner
- Chris Verhoef
- Mikhail Rusanov
- Carrie Ann Smith
- Mia Jacobson
- Suneet Bendre
- Rebal Alhaqash
- Stefan Selg

### **Legal Structure**

- **Registered Legal Entity:** [Tonomy Stichting](https://www.kvk.nl/orderstraat/product-kiezen/?kvknummer=86537288)
- **Registered Legal Country:** Netherlands
- **Registered Address:** Thorbecke Laan, Baarn, Utrecht 3741TR, Netherlands

### **Team Experience**

The following work was done by project lead Jack Tanner during his consulting and employment with [Gimly](https://www.gimly.io/). These experiences have led him to understand the identity landscape and create a design that will enable Antelope chains to deliver one of the most advanced and empowering identity solution for web3:

- Architecting and developing the entire [Myd](https://europechain.io/identity/myd-missing-piece-puzzle-ssi/) sovereign (not self-sovereign) identity solutions for Europechain. See [myd.online](https://myd.online/).
- Running the [EOSIO identity working group](https://www.gimly.io/eosio-identity) in which we researched and built the EOSIO DID in collaboration with the community and Block One.
- Writing the [EOSIO DID spec](https://github.com/Gimly-Blockchain/eosio-did-spec)
- Leading the development of the [EOSIO DID resolver](https://github.com/Gimly-Blockchain/eosio-did-resolver)
- Leading and writing the W3C standard [Verifiable Conditions](https://github.com/w3c-ccg/verifiable-conditions) to allow Antelope and other DID methods to suitably expose multi-key material and delegated authorizations in DID Documents. This was then incorporated in the Antelope DID.
- Researching recovery techniques, sovereign storage, locking protocols and more for the research deliverable for EU funded project [Gimly ID](https://www.gimly.io/gimly-id). This research survey existing technologies needed to build a fully self sovereign identity system.

Additionally, Jack has been independently involved in several relevant prior works:

- Co-writing the [EOSIO Privacy report](https://eos.io/news/blockchain-privacy/) in collaboration with the Suneet and the EOSIO community and Block One. He led the research into existing privacy architectures, very relevant for understanding and leading architecture of SSI applications.
- Leading the development of the [Civic Participation Tool](https://theblockstalk.medium.com/civic-participation-tool-upgrade-to-openstad-e7aed01c5271#c5a3) in which the team created a direct democracy tool on EOSIO with an SSI identity integration.
- Organising and running many [Antelope workshops](https://theblockstalk.medium.com/the-eosio-blockchain-developer-workshop-now-available-on-youtube-ddeba54f0d94) - in person and online - and writing education and practical Antelope material on [Medium](https://theblockstalk.medium.com/), [Github](https://github.com/theblockstalk) and [Twitter](https://twitter.com/theblockstalk).
- Jack has been technically involved in blockchain since 2016 learning from Matthew Di Ferrente and Nick Johnson (core Ethereum Foundation developers) as a developer, auditor, educator and technical influencer. He has worked on many blockchain protocols and dApp architectures.

Our co-founder and board member Chris Verhoef has experience as a director of research development at Farm Credibly, a community development manager at the New Fork, and Scrum Master for Tonomy. His natural ability to combine leadership and collaboration is an asset to all!

Our board member Mikhail Rusanov has experience as a deputy director of Public Relations in NGO Irma, CEO in Directional Drilling Services, and international engineering endeavors. Mikhail’s critical thinking, attention to detail, and commitment to providing high-quality results

Our director of technology Carrie Ann Smith has experience with the design, development, and deployment of many hardware and software projects. Some examples include humanitarian deployment of cellular-enabled power systems in Africa, leading projects for life-saving medical devices at Stryker, and many leadership positions. Her critical thinking, planning/organization, and desire to generate high-quality results are an advantage to the project!

Suneet Bendre is an experienced developer working in blockchain and self sovereign identity for the past three years. His experience includes:

- Development of the SSI framework and micro-services and microservics of [Gaia-X](https://gaia-x.eu/what-is-gaia-x), an EU federated data sharing and exchange platform.
- Contributing to the [EOSIO Privacy report](https://eos.io/news/blockchain-privacy/) with Jack Tanner.
- Technical consulting for the Indian government&#39;s blockchain incubation project [Apiary](https://apiary.stpi.in/) including market research, problem solvin and story telling.
- Other experience includes backend development with [Robustwealth](https://www.thewealthmosaic.com/vendors/robustwealth) wealth trading platform and [Mastercard](https://www.mastercard.com/).

Rebal Alhaqash is our full stack developer. With 2.5 years experience with React and React native, he leads the user facing side of the application. He has previously worked on the [Farm Credibility](https://farmcredibly.com/) project creating smart contracts in Solidity and connecting these to the front-end client. He has also worked with server side technologies in JavaScript and nestjs.

Stefan Selg & Mia Jacobson comprise our marketing and public relations team. They are both active in the community and are graduates of marketing, content, and growth programs. Their dedication and experience will certainly aid in our success!

### **Team Org Repos**

- [https://github.com/Tonomy-Foundation](https://github.com/Tonomy-Foundation)
- [https://github.com/Tonomy-Foundation/civic-participation](https://github.com/Tonomy-Foundation/civic-participation)

### **Team Member Repos**

- [https://github.com/theblockstalk](https://github.com/theblockstalk)
- [https://github.com/theblockstalk/eosio-contracts](https://github.com/theblockstalk/eosio-contracts)
- [https://github.com/theblockstalk/awesome-eosio](https://github.com/theblockstalk/awesome-eosio) (added several tools in some [PRs](https://github.com/DanailMinchev/awesome-eosio/pull/70))
- [https://github.com/theblockstalk/eosworkshop1](https://github.com/theblockstalk/eosworkshop1)
- [https://github.com/theblockstalk/eosio-sovereign-contract-poc](https://github.com/theblockstalk/eosio-sovereign-contract-poc)
- [https://github.com/theblockstalk/funnels](https://github.com/theblockstalk/funnels)
- [https://github.com/kamitor](https://github.com/kamitor)
- [https://github.com/carrie2240](https://github.com/carrie2240)
- [https://github.com/bendre](https://github.com/bendre)
- [https://github.com/Rebal67](https://github.com/Rebal67)

### **Team LinkedIn Profiles (if available)**

- [https://www.linkedin.com/in/jack-tanner/](https://www.linkedin.com/in/jack-tanner/)
- [https://www.linkedin.com/in/christiaanverhoef/](https://www.linkedin.com/in/christiaanverhoef/)
- [https://www.linkedin.com/in/rusanovmp/](https://www.linkedin.com/in/rusanovmp/)
- [https://www.linkedin.com/in/carrie-ann-smith-95240899/](https://www.linkedin.com/in/carrie-ann-smith-95240899/)
- [https://www.linkedin.com/in/mia-jacobson-012218139/](https://www.linkedin.com/in/mia-jacobson-012218139/)
- [https://www.linkedin.com/in/suneet-bendre/](https://www.linkedin.com/in/suneet-bendre/)
- [https://www.linkedin.com/in/rebal-alhaqash-683b0b174/](https://www.linkedin.com/in/rebal-alhaqash-683b0b174/)
- [https://www.linkedin.com/in/stefan-selg-b9347b1b5/](https://www.linkedin.com/in/stefan-selg-b9347b1b5/)

## **Development Status**

The work to bring SSI to Antelope as being ongoing for several years. Jack Tanner, as a contractor and then employee of Gimly has led the work to create and market the EOSIO DID. This has been a team effort with Caspar Roelofs, the director of Gimly.

Please see some publications here:

- [https://forums.eoscommunity.org/t/eosio-self-sovereign-identity/2194/7](https://forums.eoscommunity.org/t/eosio-self-sovereign-identity/2194/7)
- [https://forums.eoscommunity.org/t/eden-identity-data/3236](https://forums.eoscommunity.org/t/eden-identity-data/3236)
- [https://www.gimly.io/eosio-identity](https://www.gimly.io/eosio-identity)

This project is the next and most important step in this SSI journey for Antelope (Verifiable Credentials are the primary use case of SSI).

## **Development Roadmap**

### Overview

- **Total Estimated Duration:** 2 months
- **Full-Time Equivalent (FTE):** 0.8 FTE
- **Total Costs:** $36,000 USD (rounded down from $36,541 - see below)

We use our aligned consuling rate of €130 / hour. Our aligned consulting rate is used when the technology we build aligns with the Tonomy Foundation&#39;s vision (we use a rate of €200 when it doesn&#39;t). It reflects our at-cost rate which includes a buffer to cover risks and unknowns in operating costs. We are a non-for-profit foundation. If we make any profit it goes back into our operation budget which goes towards open-source societal technologies.

Calculation:

| 0.8 | FTE per month |
| --- | --- |
| 172 | Work hours per month |
| 2 | Months |
| € 130 / hour | Aligned consulting rate |
| € **35,776 EUR** | **Total cost** |
| **$ 36,541 USD** |

### Milestone 1 Verifiable Credential issue()

- **Estimated duration:** 1 month
- **FTE:** 0.8
- **Costs:** $18,000 USD

| **Number** | **Deliverable** | **Specification** |
| --- | --- | --- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both inline documentation of the code in Typescript types and TSDoc definition of the issue() function.The main README.md file will show an example flow. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the README.md, we will describe how to run these tests. |
| 1. | Environment setup | We will set up a developer environment which includes a running Antelope node that can be used during unit test execution. |
| 2. | Decision for Verifiable Credential library | We will evaluate the options available for use of an existing verifiable credentials library that can best support the Antelope protocol. This may happen during step 3 and 4. Results of this discussion will be published in a Github issue. |
| 3. | Implementation of W3C Vrifiable Condition | This will require us to create a plug-in to the verifiable credential library so that it can support the W3C verifiable conditions Standard as part of the Antelope DID - allowing the VC to be signed by any permission inside an Antelope account. |
| 4. | Implementation of issue() function | We will implement the issue() function that signs a VC with the chosen permission of the Antelope account. It can be signed by one key, several keys, or a delegated permission. |

### Milestone 2 Verifiable Credential verify()

- **Estimated Duration:** 1 month
- **FTE:** 0.8
- **Costs:** $18,000 USD

| **Number** | **Deliverable** | **Specification** |
| --- | --- | --- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both inline documentation of the code in Typescript types and TSDoc definition of the verify() function.The main README.md file will show an example flow. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the README.md, we will describe how to run these tests. |
| 0d. | npm | We will publish the resulting library to npmjs.com for ease of use by the community. This will show an example flow of how to use it. |
| 0e. | Article | We will publish an article what the library does, why and how to use it. |
| 1. | Implementation of verify() function | We will implement the verify() function that verifies that the signature of a VC is valid for the Antelope account and the chosen permission used to authorize it. |
| 2. | Documentation and publish | We will finalise the documentation and publish this to npmjs.com. We will then write our article and distribute this in relevant Antelope Telegram, Twitter and Discord channels and SSI channels (for the Verifiable Conditions). |

## **Future Plans**

We plan to promote this software library within the Antelope community. Furthermore, we expect wallet providers of public, and consultancy agencies working with Antelope in enterprise to be the first adopters of this software.

We also plan to promote this software library within the greater SSI community as it achieves something that no other DID method currently supports - multi-signature VCs. This will be due to our implementation of the W3C Verifiable Conditions standard. We will promote this within the [Decentralised Identity Foundation](https://identity.foundation/), [W3C CCG](https://w3c-ccg.github.io/) and other channels, specifically highlighting its benefits, which in turn highlights the benefits of the Antelope account structure.

The Tonomy Foundation is building support for credential sharing in its up and coming Tonomy ID product, outlined [here](https://github.com/Tonomy-Foundation/EOS-network-foundation-grant-framework/blob/main/applications/tonomy-cross-platform-wallet.md). This can be used on any existing Antelope blockchain. We will be using the SSI Toolkit library in this identity wallet.

We plan to finish the SSI toolkit&#39;s functionality and hope to receive funding via the ENF and/or pomelo grants. The upcoming features are:

1. Verifiable presentations - support for the W3C verifiable presentations standard used to send a VC to another account.
2. DIDComm - support for the W3C DIDComm standard which allows any DID-compatible accounts to send a message or stream to another.

## **Additional Information**

**How did you hear about the Grants Program?**

Twitter
