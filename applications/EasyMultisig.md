# EOS Network Foundation Grant Proposal

- **Project Name:** EasyMultisig
- **Team Name:** Esteban Saa
- **EOS Payment Address:** trustswap111
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** https://pomelo.io/grants/eosevmmultis
- Project is Open-Source: Yes
- Project was part of Token sale: No
- Repository where Project resides: https://github.com/evm20/easymultisig

## Contact

- **Contact Name:** Esteban Saa
- **Contact Email:** steban@gmail.com
- **Website:** https://www.easymultisig.com

## Project Overview

EasyMultisig is a multisignature wallet designed for EOSEVM. It provides a secure and user-friendly solution for managing and executing transactions with multiple signatures on the EOSEVM network.

### Overview

- **Name:** EasyMultisig
- **Brief Description:** Makes it easy to deploy and manage multisignature wallets on EOSEVM. 
- **Relationship to EOSIO:** Is basic infrastructure for EOSEVM
- **Reason for Interest:** Address the need for robust multisignature wallet functionality on the EOSEVM network. We recognize the importance of secure and efficient transaction management for users, especially in decentralized finance (DeFi) and other applications that require multiple signatures for secure operations.

### Project Details

EasyMultisig is a project that aims to provide a comprehensive solution for managing multisignature wallets on the EOSEVM network. We are focused on designing intuitive and user-friendly UI elements that will enable easy configuration and management of multisignature wallets. EasyMultisig utilizes modern web development technologies and integrates with the EOSEVM framework for seamless blockchain integration. We will provide comprehensive documentation that covers the core components, protocols, architecture, and deployment instructions for EasyMultisig. EasyMultisig is a fork of the first version of the Gnosis Mutisig wallet.  EasyMultisig does not aim to provide or implement functionalities unrelated to managing multisignature wallets on the EOSEVM network. Our primary focus is to deliver a reliable and user-friendly solution specifically for multisignature use cases. 

- An alpha version of the wallet is ready at: https://www.easymultisig.com/
- The code repository is located at: [https://github.com/stebansaa/multisig](https://github.com/evm20/easymultisig)
- We will refresh the UI and improve branding and styling. 
- The frontend is built with Angular / Bootstrap.
- The contracts are well known multisig contracts written in solidity. 
- Documentation and tutorials will be added to the site.
- The frontend deploys  multisig contracts, while  storing the information on local storage. The contracts are then verified on the EOSEVM explorer, so that their security can be independently verified. 
- Related information on Multisig wallets: https://www.bitpanda.com/academy/en/lessons/what-are-multi-signature-wallets-and-how-do-they-work/
- The wallet is not a replacement for Metamask, it makes use of Metamask to sign the transactions. 

### Ecosystem Fit

EasyMultisig fills the gap for a robust and user-friendly multisignature wallet solution on the EOSEVM network. It aligns with the ecosystem's goal of providing secure and efficient decentralized applications (dApps) and services.
Our primary target audience includes developers, and power users of dApps on the EOSEVM network. EasyMultisig enables these stakeholders to enhance the security and trustworthiness of their transactions by implementing multiple signatures.

EasyMultisig meets the need for secure and reliable multisig wallet functionality on the EOSEVM network. It enables users to mitigate risks associated with single-key transactions and enhances the overall security of blockchain operations.

Although there may be similar projects in the Ethereum ecosystem, EasyMultisig focuses on the EOSEVM network, which combines the strengths of Antelope and Ethereum. This integration with EOSEVM sets EasyMultisig apart from similar projects in the Ethereum ecosystem.

## Team

### Team members

- **Team Leader:** Esteban Saa

### Legal Structure
- **Registered Legal Entity:** Esteban Saa

### Team Experience
This is the second grand we apply to, the first one was TrustSwap, where we deployed an AMM to the 4 EOSEVM testnets, and final mainnet. The project is active at frogge.finance, it was utilized as a test bench on the last EOSEVM testnet. 

### Team Org Repos
- https://github.com/evm20


### Team Member Repos
- https://github.com/stebansaa


### Team LinkedIn Profiles
https://www.linkedin.com/in/esteban-s-988b6457/

## Development Status
- The current alpha version is available at: https://www.easymultisig.com


## Development Roadmap

### Overview
- **Total Estimated Duration:** 1 Month. 
- **Full-Time Equivalent (FTE):**  1 FTE)
- **Total Costs:** $8,195 USD

### Milestone 1 — complete deployment and code updates
- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** $8,195 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can deploy and interact with our multisignature wallet |

## Future Plans
- A security audit can be coordinated.
- If dem adecuade add support for other EVMs in the Antelope ecosystem.

## Additional Information
This is our second grant application.
The multisig contracts deployed code can be reviewed on the explorer, resulting in that their security is independent from the frontend. Also the contracts deployed can be interacted with by using the EOSEVM explorer.
