# EOS Network Foundation Grant Proposal

- **Project Name:** EOS ID
- **Team Name:** Tonomy Foundation
- **EOS Payment Address:** tonomyaccou1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** <https://pomelo.io/grants/recovery>
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** <https://github.com/Tonomy-Foundation/Tonomy-ID/tree/development>

## Contact

- **Contact Name:** Jack Tanner
- **Contact Email:** jack+public@tonomy.foundation
- **Website:** <https://tonomy.foundation/>

## Project Overview

### Overview

- **Name:** EOS ID - A super easy-to-use non-custodial self-sovereign identity and EOS wallet for EOS users, designed for mainstream people.
- **Brief Description:** EOS ID is a crypto and SSI wallet on Android and iOS for the EOS blockchain network. It is fully white-labelled for the EOS Network. EOS ID ensures high security and convenience for users. It provides free accounts, eliminating the need to manage their private keys and allows rapid onboarding and usage of EOS web2 and web3 apps with password-less and form-less login.
- **Relationship to EOS Network / Antelope:** We will deliver a user application designed specifically for the EOS Network and its community. We will use a tech stack that is Antelope-native and can be used on any pure Antelope chain. We have plans to support other public and private Antelope networks and new markets.
- **Reason for Interest:** Our goal is to validate and monetise the Tonomy ID smart wallet solution. We believe that EOS is an ideal choice due to our ability to provide substantial assistance with current onboarding and usability challenges within the ecosystem.

### Project Details

#### EOS ID

Current solutions in the EOS market leave a large technical entry barrier for new users of EOS apps. It’s too difficult to create an account and then go on to manage it while using EOS applications. A clear indicator of this problem is that we already see several prominent EOS apps moving to no-custodial or bespoke self-managed web applications, as seen in the table below. Whether using Anchor/equivalent or bespoke solutions, user onboarding and retention is hurting in EOS. A trusted and user-friendly EOS wallet will boost application growth in the EOS ecosystem. Think of how well Metamask (which has a very difficult UX) provides an onboarding experience to all Ethereum networks by having a known, trusted wallet for all Ethereum apps.

Overview of several prominent applications used in EOS and their identity system
|            | Anchor | Google | Bespoke | Others                                              |
| ---------- | ------ | ------ | ------- | --------------------------------------------------- |
| Atomic     | ✔      |        |         | Scatter, Wombat                                     |
| Bullish    |        |        | ✔       |                                                     |
| Eden       | ✔      |        |         | Ledger                                              |
| Newdex     | ✔      |        |         | Scatter, Wombat, Metahub, Token pocket, Leaf wallet |
| Paycash    |        |        | ✔       |                                                     |
| Pomelo     |        | ✔      |         | Apple, Github, Weibo, (Anchor for tx only)          |
| Prospector |        | ✔      |         |                                                     |
| Upland     |        |        | ✔       |                                                     |
| Vigor      | ✔      |        |         | Scatter, Metamask                                   |

What if we could provide a single, fully open-source alternative that provides users with a better experience and security and makes EOS users really feel like they are part of the EOS community?

Our team is developing a user-friendly and secure EOS wallet. EOS ID allows users to sign into web applications and sign verifiable data and transactions.

EOS ID has advanced capabilities under the hood, hidden from its users, which makes it possible to build easy onboarding and application experiences. This includes a seamless single-sign-on process that utilises W3C Verifiable Credentials for identity data sharing.
To prevent Sybil attacks, we offer a light level of protection during login to Web2 and Web3 apps.
Free account creation is included, and we will improve upon existing Antelope open-source software modules like Warf, the Antelope SSI Toolkit, and Tonomy ID. This is only the beginning of a far-reaching project, with plans to support all major Antelope networks and add more features.

EOS ID is a well-researched concept that offers a unique solution to the problems associated with the self-sovereign identity (SSI) and profile avatar systems outlined in the Core+ and Wallet+ blue papers. Our SSI solution allows users to share W3C verifiable credentials, including personal information such as name, email, and residential address, during login. This process is GDPR compliant, privacy-preserving, and eliminates signup forms, providing a streamlined and secure user experience.

#### Tonomy ID

We have almost completed the (open source) MVP of Tonomy ID, a white-labelable SSI and transaction signing wallet built on Antelope. See the latest demo video here:

<https://www.youtube.com/watch?v=b81Ju7r7T1M>

We will be forking/modifying this to build EOS ID. The work to build Tonomy ID to date is not part of this grant funding, which we have bootstrapped. You can see more details further on in “Development Status”

#### Design Prototype

We have a mature design prototype for EOS ID.

See the link below for a design preview of some of the features.

<https://www.canva.com/design/DAFf5wI9P4Q/D5EhshbR3VsK2nEPr7necw/edit?utm_content=DAFf5wI9P4Q>

Full prototype viewing is available on request. Please email our team if interested.

#### EOS ID Features

- **Fast and secure data sharing and onboarding:** EOS ID allows dApps to onboard users easily with password-less login to apps with the option of multi-factor authentication. Additionally, dApps can request user information to be shared like the user's name, email or address, done with a form-less login. This means that users can log in to apps from a single account with password-less and form-less login, which enhances security and user experience. It’s similar to combining a password manager, form filler and Google single-sign-on with a sovereign design. This login process is GDPR compliant, password-less, privacy-preserving, and eliminates signup forms, providing a streamlined and secure user experience.
- **In-app transaction and verifiable data signing:** The EOS ID single-sign-on flow will allow Web2 and Web3 apps to manage fully non-custodial keys inside the client the user is in. This allows their unique ability to sign transactions and verifiable credentials directly within the client without having to make a request back to the wallet each time. This is a significant user experience improvement. DApps will also be able to send requests for transactions to be signed in the EOS ID wallet if extra security is needed.
- **Fully managed private keys:** All private keys in EOS ID are fully managed by the mobile application and never exposed to the user. For users, this eliminates the inconvenience and confusion created by importing or exporting private keys, as they are fully managed within the application. For integrators, knowing that users never manage keys gives them the guarantee that keys are fully sovereign and highly secure.
- **White-labelled EOS wallet:** EOS ID is a fully white-labelled crypto and SSI wallet that is branded and coloured to suit the styles and symbols of EOS. We give the EOS user their own wallet that is uniquely theirs and identifies with the colours and symbols of the EOS network.
Inbuilt free account service: Our solution includes a free account creation service that enables anyone to create an account on EOS super easily.
- **Light Sybil attack prevention:** To prevent Sybil attacks, we will implement a reCAPTCHA challenge during the account creation process. This can be used by Web3 apps like Pomelo or Hypa and other applications that require safeguards against accounts created by bots. We plan to mature the Sybil attack prevention mechanisms to be more secure and privacy-preserving.

#### Application Registry

We have designed and developed an application registry management system that allows integrators to register Web2 and Web3 apps that users can sign into with Tonomy ID. This feature will enable users to access a wider range of applications while simplifying the login process.

This is a no-code solution to allow application developers to integrate easily with Tonomy ID.

See the design preview here:

<https://www.canva.com/design/DAFf-JhyiPY/kAAUzPE4F3-pj6gW15CSOg/edit?utm_content=DAFf-JhyiPY>

#### Antelope protocol libraries

In addition to the core EOS ID solution, we are further developing several Antelope protocol libraries that will enhance the overall functionality of the platform. These include:

- Antelope SSI toolkit artefacts - allowing others to create and use verifiable credentials on any Antelope blockchain.
- Warf - a library being matured for use on any Antelope chain.
- Tonomy ID - EOS ID will be a white-labelled version of the open-source Tonomy ID, which can be deployed on any Antelope chain. EOS ID will be the first deployed identity solution on a public chain, and we plan to support other public chains in the future.
- A reference for how to use SSI - this will give other Antelope developers a reference for how to use DIDs and VCs in Antelope apps.

#### Architecture and technology stack

We will be building on top of the existing Tonomy ID architecture, which is open source. See the "Application Architecture" tab here:

<https://drive.google.com/file/d/1vEaKBllnh8_6XVVeMLzNi0DNT44QiMaI/view?usp=sharing>

The current SDK architecture can be explored in more detail here:

<https://github.com/Tonomy-Foundation/Tonomy-ID-SDK/tree/development/src/sdk>

### Ecosystem Fit

- **Where and how does your project fit into the ecosystem?**

EOS ID is a high usability and security wallet designed and branded specifically for the EOS Network. It can be used to login to EOS Web2 and Web3 apps, sign transactions on EOS dApps, sign verifiable private data and send peer-to-peer messages between EOS users.

- **Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**

Our direct target audience will be the EOS Network users, primarily EOS token holders and EOS builders. We will specifically cater to those using EOS ID to sign in and access EOS applications.

Indirectly, we will collaborate with dApp providers like Atomic, Pomelo, Upland, Newdex and others to integrate the login and other features of EOS ID into their applications. We also have connections with various dApps that will benefit greatly from using EOS ID as a login system for their apps. With EOS ID, we provide an innovative, user-friendly solution for logging into applications in the EOS ecosystem while addressing key issues in the self-sovereign identity space.

We directly meet the needs set out in the EOS Network Foundation’s blue papers:

- EOS ID proves a unique solution to the problems associated with the self-sovereign identity (SSI) and profile avatar systems outlined in the [Core+](https://eosnetwork.com/blog/core-blue-paper/) and [Wallet+](https://eosnetwork.com/blog/wallet-blue-paper/) blue papers.
- The Application registry provides an intuitive application management UI and addresses issues outlined in the [Wallet+](https://eosnetwork.com/blog/wallet-blue-paper/) blue paper regarding the application registry.

We plan to reach an even broader audience with the more generic Tonomy ID software, which uses Antelope as a decentralized public key store for the identity data of each user. Our adoption roadmap includes collaboration with existing relationships at Newcoin and Zaizaan, who are already interested in using our technologies. We will, in good time, aim to launch Tonomy ID on all major public Antelope networks like Telos, WAX and UX.

Our strategy involves showcasing the capabilities and advantages of EOS ID to communities focused on self-sovereign identity and verifiable credentials and exploring potential use cases. By doing so, we aim to expand our reach to new individuals and communities within the EOS/Antelope ecosystem.

- **What need(s) does your project meet?**

Primarily, we solve the problem of having a secure, non-custodial wallet for EOS that has a mainstream-ready user experience. Our solution enables faster onboarding to EOS apps and provides easy transaction signing within dApps, making it ideal for users and developers. Our goal is to offer a simple and streamlined user experience that meets the needs of dApps seeking an accessible onboarding process.

We solve problems regarding privacy and privacy compliance in existing apps that put personal information on the blockchain as a go-to solution for profile aviators (which does not comply with GDPR and most modern privacy regulations). Using verifiable data, dApps can securely create and authenticate private user data. This meets the needs of applications to be able to access user information and users to be able to control their personal data and privacy.

- **Are there any other projects similar to yours in the EOS Network / Antelope ecosystem?**

The Anchor wallet by Greymass is currently the standard go-to non-custodial wallet for EOS (and most Antelope chains).

Similar to Anchor, EOS ID is a transaction signing wallet, and we will provide documentation for developers to integrate EOS ID users to log in to their apps, sign transactions and share data.

There a several important differences between Anchor and EOS ID:

- **Open-source:** EOS ID mobile wallet is and always will be open source. Anchor desktop is open source, while Anchor mobile is not.
- **Features:** EOS ID provides additional features
  - Apps can (optionally) sign transactions directly in the client (without confirming it in the mobile wallet).
  - Apps can sign verifiable data with W3C Verifiable Credentials directly to the client.
  - Apps can sign and send peer-to-peer messages to other EOS users.
  - Form-less account signup: With EOS ID, users will be asked for their details like name, address and email once and then users will be able to share that with apps as they sign into them privately and with a click of a button making registration forms a thing of the past.
- **White-labelled:** EOS ID is branded for the EOS Network, featuring the distinct colour scheme, logo, and symbols of EOS as its primary theme and label. Anchor does not have the option to do this across its apps, because they are a multi-chain wallet.
- **Free account:** EOS ID comes out of the box with support for free EOS accounts indefinitely. Unlike Anchor or most other EOS wallets, which cost ~$1 per account. We expect to cover EOS account creation costs from BP vote rewards, which we expect to generate by making voting for Tonomy Foundation BP easy and accessible within EOS ID.
- **Sybil protection:** We will provide a light level of Sybil account protection within EOS ID. This will be in the form of reCAPTCHA protection when accounts are created. Apps will be able to request a verifiable credential that proves that the reCAPTCHA was completed. We can make this an on-chain badge in the future if demand exists.
- **No user key management:** Users of EOS ID never handle or even see any public/private keypairs used to authorise the account. This makes account management much simpler and more like a regular Web2 identity and is one of our primary ways of ensuring that it is ready for mainstream users.
- **Recovery:** EOS ID uses a user-created secure password as the primary way for users to log in and log out of their accounts This is a familiar mechanism, and users can recover their accounts from memory. As a backup, users can save their passwords in a secure key manager. Anchor requires the user to back up their private key (which is impossible to commit to memory) and provides features to make it easy, however, it can still be challenging to use, particularly for non-technical users. EOS ID plans to create user-friendly non-custodial recovery options such as social recovery, hardware keycard, or security question recovery in the future, all without requiring users to manage or even see their private keys.

Anchor is a more general-purpose wallet. It allows the user direct access to the private keys and allows their account permissions to have any structure. Additionally, it is a multi-chain wallet. This makes Greymass more adaptable to work in more ways than EOS ID for how people want to manage their accounts.

EOS ID is focused on making a highly usable wallet and makes several assumptions about permissions structure and key management to allow this to happen. We see EOS ID as a go-to solution for mainstream EOS people and Greymass as a solution for business accounts, higher-security and other specific account management needs of people and organisations. We don't see EOS ID as a replacement for Anchor, rather, we see it as coexisting alongside Anchor and delivering different options for different people

## Team

### Team members

- **Team Leader:** Name of team leader
- Name of team member 1
- Name of team member 2
- Name of team member 3, etc.

### Legal Structure

- **Registered Legal Entity:** Stichting Tonomy
- **Registered Address:** Thorbecke Laan, Baarn, Utrecht 3741TR, Netherlands

### Team Experience

> Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past. For research-related grants, references to past publications and projects in a related domain are helpful. If you applied for a Pomelo grant in the past, please be sure you listed them in the section above and mention them in detail in this section.

> If anyone on your team has applied for a grant at the EOS Network Foundation previously, please list the name of the project and legal entity here.

### Team Org Repos

- <https://github.com/<your_organization>>
- <https://github.com/<your_organization>/<project_1>>
- <https://github.com/<your_organization>/<project_2>>

> Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

### Team Member Repos

- <https://github.com/<team_member_1>>
- <https://github.com/<team_member_2>>

### Team LinkedIn Profiles (if available)

- <https://www.linkedin.com/in/<person_1>>
- <https://www.linkedin.com/in/<person_2>>

## Development Status

### Tonomy ID

Tonomy ID is the cross-platform mobile wallet (Android and iOS) for public and private Antelope blockchains.

The Tonomy Foundation is nearing the completion of the MVP of Tonomy ID, which we plan to use to develop EOS ID. The grant proposal would add the necessary modifications to Tonomy ID to ensure that we can launch on EOS meeting and exceeding all of the existing expectations of wallets, and go beyond to deliver a wallet experience that will amaze EOS users.

<https://github.com/Tonomy-Foundation/Tonomy-ID/tree/development>

Try out the login flow on the functional staging app (under active development - unstable and may have bugs) here:

- Demo video: <https://www.youtube.com/watch?v=b81Ju7r7T1M>
- Demo app: <https://demo.staging.tonomy.foundation>
- Tonomy ID: <https://play.google.com/store/apps/details?id=foundation.tonomy.projects.tonomyidstaging>
- Documentation: <https://docs.tonomy.foundation>

There has already been a large amount of work that has gone into Tonomy ID, including technical research, design usability testing and significant development. This work is provided for free outside of this grant; however, it still provides a significant amount of value to the proposal in this grant.

### Antelope SSI Toolkit

As part of a previous EOS Network Foundation grant, the Tonomy Foundation Delivered the Antelope SSI toolkit, allowing any account on Antelope blockchains to issue and verify W3C Verifiable Credentials.

- Blog: <https://blog.tonomy.foundation/issue-and-verifying-verifiable-credentials-with-an-antelope-account-d1b4e76bfba0>
- Codebase: <https://github.com/Tonomy-Foundation/Antelope-SSI-Toolkit>

Since delivering the toolkit, the Tonomy Foundation has distributed this within the Antelope and SSI communities. The Tonomy Foundation has further gone on to merge the major changes needed for the toolkit into the community-driven libraries maintained by the Decentralized Identity Foundation.

We plan to use these tools in EOS ID further to deliver form-less onboarding features.

## Development Roadmap

### Milestone Summary

We have developed a roadmap outlining the modifications necessary to integrate and launch Tonomy ID on EOS seamlessly. It focuses on the above-mentioned features and adds compatibility for existing expectations of EOS Wallets and integration with the EOS resource model and infrastructure.

After our experience with the Antelope SSI Toolkit, we have grouped similar tasks and fewer milestones with more work in each. We aim to minimise disruptions caused by focus switching for the reviewers of our milestones, which we understand are under significant demand now. This also makes payments more predictable for us.

- Total Estimated Duration: 4 months
- Full-Time Equivalent (FTE): 1.5 FTE
- Total Costs: 132,000 USD

We use our aligned consulting rate of EUR €130 / hour. Our aligned consulting rate is used when the technology we build aligns with the Tonomy Foundation's vision (we use a rate of €260 when it doesn't). It reflects our at-cost rate, which includes a buffer to cover risks and unknowns in operating costs. We are a non-profit foundation. If we make any profit, it goes back into our operating budget, which goes towards open-source societal technologies.

Calculation:

| Unit          | Description             |
| ------------- | ----------------------- |
| 1.5           | FTE per month           |
| 4             | Months                  |
| 155           | Work hours per month    |
| € 130 / hour  | Aligned consulting rate |
| € 120,900 EUR | Total cost              |
| $ 132,000 USD |

### Milestone 1 — Integration with EOS infrastructure

- **Estimated duration:** 2 month
- **FTE:**  1.5
- **Costs:** 66,000 USD

| ID  | Deliverable                                           | Specification                                                                                                                                                                                    |
| --- | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 0a. | License                                               | Apache 2.0                                                                                                                                                                                       |
| 0b. | Documentation                                         | Provide documentation on readthedocs.io or equivalent showing how apps can integrate and use EOS ID login and other features.                                                                    |
| 0c  | Testing Guide                                         | Unit and integration tests will be written to cover the integration with EOS Network and to show features are working.                                                                           |
| 0e. | Article                                               | We will publish an article announcing the launch of EOS ID on EOS.                                                                                                                               |
| 1.  | Integrate with EOS Network’s system contracts         | Create an environment for Tonomy ID that uses the EOS system contracts. Ensure Tonomy ID still runs by checking if all integration tests are passing and manual testing has no major bugs.       |
| 2.  | Integrate with the use EOS resource model             | Integrate the EOS resource model with CPU, NET and RAM with staking and Powerup. Ensure Tonomy ID still runs by checking integration tests are all passing and manual testing has no major bugs. |
| 3.  | EOS ID app branding                                   | Apply the EOS logo and symbols, colours and name to Tonomy ID.                                                                                                                                   |
| 4.  | Deploy to EOS testnet                                 | Deploy EOS ID to an EOS testnet. Test that it works.                                                                                                                                             |
| 5.  | Account creation service with Sybil attack prevention | Build a service that creates an EOS account with a reCAPTCHA challenge. Integration tests that show it working.                                                                                  |
| 6.  | Wallet transaction signing                            | Build the regular client-wallet request for a transaction to be signed inside of EOS ID. Write several integration tests that show the major success and failure cases.                          |
| 7.  | Deployment on EOS                                     | Deploy EOS ID on EOS. Test that it works.                                                                                                                                                        |
| 8.  | Integrators support                                   | Tech support for dapps that want to integrate with EOS ID.                                                                                                                                       |

Requirements for EOS ID at the end of this milestone:

- Functional requirements
  - EOS ID will have all the features of Tonomy ID
    - Users can create an account and log in to EOS ID with a username and password
    - Users can change their password
    - Users can Scan a QR code on an external application
    - Users can log in to an external web application with single-sign-on flow
    - Users can sign transactions and/or W3C verifiable credentials in external web applications (but not in the EOS ID mobile wallet)
  - Users will need to complete a reCAPTCHA challenge to create an account
  - Users can sign transactions in the EOS ID mobile wallet when requested by an external web application
  - See the design preview here (DRAFT): <https://www.canva.com/design/DAFf5wI9P4Q/D5EhshbR3VsK2nEPr7necw/edit?utm_content=DAFf5wI9P4Q>
- Non-functional requirements
  - EOS ID will be branded to the colour and symbols of the EOS network
  - EOS ID will be deployed on the EOS network, with no major bugs

### Milestone 2 - Form-less login with personal information

- **Estimated Duration:** 1 month
- **FTE:**  1.5
- **Costs:** 33,000 USD

| ID  | Deliverable                                         | Specification                                                                                                                                                                                                                                |
| --- | --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0a. | License                                             | Apache 2.0                                                                                                                                                                                                                                   |
| 0b. | Documentation                                       | Provide documentation on readthedocs.io or equivalent showing how apps can integrate and use EOS ID login and other features.                                                                                                                |
| 0c  | Testing Guide                                       | Unit and integration tests will be written to show features are working.                                                                                                                                                                     |
| 0e. | Article                                             | We will publish an article announcing the launch of EOS ID’s new features on EOS.                                                                                                                                                            |
| 1.  | Design and usability testing  (partially completed) | Create a full design prototype in Figma. Run usability testing with several members from the EOS community. Document the results of the testing and update the designs. Figma files are private, and the testing results can be made public. |
| 2.  | Development of the form-less login                  | Development of the feature in EOS ID to allow login to apps with personal data shared in consent screens.                                                                                                                                    |
| 3.  | Deployment on EOS                                   | Deployment on an EOS testnet, testing and then deployment on the EOS Network.                                                                                                                                                                |
| 4.  | Integrators support                                 | Tech support for dapps that want to integrate with EOS ID.                                                                                                                                                                                   |

New requirements for EOS ID at the end of this milestone

- Functional requirements
  - Users can enter their personal information and upload a profile picture to EOS ID
  - Users can share their personal information with external applications when requested
  - See the design preview here (DRAFT): <https://www.canva.com/design/DAFf5wI9P4Q/D5EhshbR3VsK2nEPr7necw/edit?utm_content=DAFf5wI9P4Q>

### Milestone 3 - App Manager

- **Estimated Duration:** 1 month
- **FTE:**  1.5
- **Costs:** 33,000 USD

| ID  | Deliverable                                        | Specification                                                                                                                                                                                                                            |
| --- | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0a. | License                                            | Apache 2.0                                                                                                                                                                                                                               |
| 0b. | Documentation                                      | Provide documentation on readthedocs.io or equivalent showing how apps can integrate and use EOS App Manager.                                                                                                                            |
| 0c  | Testing Guide                                      | Unit and integration tests will be written to show features are working.                                                                                                                                                                 |
| 0e. | Article                                            | We will publish an article announcing the launch of EOS App Manager on EOS.                                                                                                                                                              |
| 1.  | Design and usability testing (partially completed) | Create a full design prototype in Figma. Run usability testing with several members from the EOS community. Document the results of the testing and update the designs. Figma files are private, and testing results can be made public. |
| 2.  | Development of the App Manager

(mostly completed) | Development of the App Manager allowing dApp developers to easily manage their apps for EOS ID logins.                                                                                                                                   |
| 3.  | Deployment on EOS                                  | Deployment on an EOS testnet, testing and then deployment on the EOS Network.                                                                                                                                                            |
| 4.  | Integrators support                                | Tech support for dApps that want to integrate with EOS ID.                                                                                                                                                                               |

New requirements for EOS ID at the end of this milestone

- Functional requirements
  - Users can see an overview of the EOS Apps that they are currently managing
  - Users can register a new EOS App which can be used in the EOS ID single-sign-on flow
  - Users can update the information of an EOS App
  - Users can delete an EOS App
  - See the design preview here (DRAFT): <https://www.canva.com/design/DAFf-JhyiPY/kAAUzPE4F3-pj6gW15CSOg/edit?utm_content=DAFf-JhyiPY>

## Future Plans

We would like to support the following features on EOS ID in the future:

- **Increased Sybil attack prevention:** we would like to support the need for Sybil attack prevention in many popular EOS apps like Pomelo or Atomic. Several strategies exist, and we do not think any strategy is strong enough, but we would like to support several options that dApps can choose. Integrating <https://port.link> directly in the app or using a social graph would be examples of this.
- **Sovereign recovery:** Allow users to recover their accounts if they forget their passwords. We have several mechanisms planned, such as social recovery, hardware wallet recovery or security questions that are mainstream-friendly and non-custodial.
- **Email notifications:** Allow the user to get notifications on specific transactions and actions on EOS.
- **Multi-factor authentication:** Allows users to sign requests with additional factors of authentication using an on-phone PIN or biometric authentication
- **Multi-language:** The app aims to be inclusive and accessible by offering multiple language options in future releases, though for the first release, only English will be available.
- **Sovereign storage:** Allow dApps to store data in a secure storage vault encrypted client-side by a Tonomy ID key. This would allow users a private data storage module allowing dapps to offload important user data without storing it themselves. This needs to be combined with a well-implemented recovery solution to be viable.

As mentioned, we plan to launch on other Antelope chains like Telos, WAX or UX network.

## Additional Information

**How did you hear about the Grants Program?** Twitter
