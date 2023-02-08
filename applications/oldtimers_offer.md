# EOS Network Foundation Grant Proposal

- **Project Name:** Oldtimers Offer
- **Team Name:** Oldtimers
- **EOS Payment Address:**  oldtimerseos
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 2

## Project Overview

Create a decentralized marketplace in a combination of the smart contract (created on EOS EVM) and React. The majority of data (vehicle ID, details of vehicles, available options for rent or buy, reviews score,...) will be recorded on blockchain (EOS EVM). Our primary work is to create Dapp (web 3.0) marketplace for classic vehicles. After that, developers can use that open-source code and easily create simular marketplaces (for real estate, sea vessels, bookstore,...). More precisely, it will be 2 open source codes. One for smart contract and another for React.

### Overview

- **Name:** Oldtimers Offer
- **Brief Description:** Creating a self-regulated marketplace for classic vehicles, was always our dream from the beginning of time involved in the blockchain industry. 
- **Relationship to Antelope:** Antelope and EOS EVM are closely connected blockchain networks (Silkworm). More users and developers on EOS EVM will be a benefit for the Antelope blockchain network. With our open-source codes, we will surely succeed in that.
- **Reason for Interest:** The Oldtimers team has been involved in blockchain development since 2017 and has expertise in the EVM area. These enhancements(open-source codes for smart contract and react) will increase the usability and popularity of the EOS EVM in terms of creating more marketplaces on blockchain and will include more and more startups.

### Project Details

- **A. Creating a Smart Contract for a marketplace (futures included rent, buy, and reviews):** The smart contract will be recording information as they enter into the application to ensure that the market is fully decentralized and controlled by users. Submitted info such as vehicle id and details (color, type of transmission, or available option for buy & rent, the price for the vehicle,..) will be recorded on the EOS EVM blockchain. That information will allow users to rent, and buy a vehicle and to give reviewed points to rented vehicles. Money from renting and buying will go automatically to users and one small portion (for the service fee) will be kept on a smart contract or will be sent to a treasury wallet. That would ensure a profitable business. Listing vehicles to the market is free, but the smart contract is created to have a fee for renting and buying process. This feature is controlled by the creator of the smart contract and the fee can be changed or removed (if the owner of the smart contract put 0 for fee services). The smart contract will establish several mapping to monitor:
- who rented the vehicle, 
- how much a vehicle is rented, 
- to keep and to change the owner of the vehicle(if somebody buys the vehicle), 
- reviewed points for the vehicle,... 
The smart contract will have unit tests. Unit tests will fully cover core functions to ensure the functionality and security of the smart contract. Once the smart contract reaches an acceptable level of confidence will be deployed on the test net. After that can start integration and connection with React.

- **B.Integration and customization token (ERC-20) in the marketplace smart contract:** Previus step is done almost 95%, and price is calculated with nativ token (EOS on EVM) for renting/buying and service fee. Our next step will be a feature for a token. The token (ERC-20 standard) feature will give option for creator of smart contract that can put custom token (ERC-20) for payments. 

- **C. Create react Dapp for the marketplace:** Ordinary users in the classic vehicle market are not so involved in the blockchain industry. Because of that, we have to make their experience in using Dapp as much as possible easier and to be simple using(doom - 3 clicks process) application. Multiple components for forms and responsive design will make that happen. To provide a better user experience, we brought in our team Dan B. (a very experienced react developer). Our React application will take data from EOS EVM (from the smart contract) to show users important/necessary data.

- **D. Integration and connection of the smart contract with created React Dapp:** To integrate the smart contract into the React application our developers should include in their work libraries such as Ethers.js, Web3.js, and Wagmi. Because of the situation that the application received plenty of data form the blockchain network (EOS EVM) we have to ensure good RPC communication between our React application and the smart contract created on EOS EVM. Once the Dapp reaches an acceptable level of confidence on the testnet and locally, will be deployed publicly with a smart contract on mainnet.

### Ecosystem Fit

- This project fits into the EOS EVM ecosystem
- Target Audience: EVM developers and worldwide users 
- The project improves the usability and popularity of the EOS EVM
- We are not aware of other projects similar to this in the EOS EVM ecosystem

## Team

### Team members

- **Lead:** Milan Bjegovic (CEO)
- John (want to stay anonymous) (COO)
- Marko Milutinovic (Blockchain Developer)
- Dan B. (nickname) (React Developer)

### Contact

- **Contact Name:** Milan Bjegovic
- **Contact Email:** office@oldtimersoffer.com
- **Website:** https://oldtimersoffer.com/

### Legal Structure
- **Registered Legal Entity:** Oldtimers Offer
- **Registered Address:** Sestre Bakovic 11/2, 18000 Nis, Serbia

### Team Experience

The Oldtimers team has been involved in all development aspects of the Oldtimers Offer code base since 2019.  Since 2017, Milan (CEO) has been involved in multiple EVM projects. Here is the name of some projects: Greedy Goblins(NFT, DAO, and lottery using Chain Link VRF), BeTrust(Fantasy Sports Betting (covered with a smart contract on EVM)), GPB(NFT with Merkle Tree integration), Mighty (Learn & Earn blockchain platform). Multiple members of the Oldtimers team have worked for more than 7 years as front-end developers in the web 2.0 industry. John has more impressive blockchain experience than our CEO, but he wants to stay anonymous.  

### Team Org Repos

- https://github.com/oldtimers-eos
- https://github.com/oldtimers-eos/Oldtimers-Rent-Buy-Smart-Contract
- https://github.com/oldtimers-eos/Oldtimer-OLD-Token-EOS-EVM-testnet

### Team Member Repos
- https://github.com/oldtimers-offer


### Team LinkedIn Profiles

- https://www.linkedin.com/in/milanbjegovic/


## Development Status

- https://github.com/orgs/oldtimers-eos/projects/3/views/1


## Development Roadmap

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):**  3
- **Total Costs:** $30,000 USD

### Milestone 1 - Smart Contract (A & B from Project Details)

- **Estimated duration:** 8 weeks
- **FTE:**  2
- **Costs:** $10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Oldtimers team will provide documentation of the Smart Contract on Git, suitable for customization and deploying. |
| 0c. | Unit Tests | Core functions will be fully covered by unit tests to ensure functionality and robustness of smart contract. |
| 1. | Smart Contract for a market place | The smart contract will record a majority of data from the application to the blockchain (EOS EVM). The recorded data will enable users to rent/buy vehicles and give review points to rented vehicles. The smart contract will create a self-regulated marketplace as a revolutionary solution. It will be achieved with a feature: Only the vehicle owner (which was added to the market) can add and change the details of the vehicle. Except for simple details such as Exterior Color, Transmission, Miles,... the owner can set an option for rent or sell (maybe both solutions) and a price for that. Example: Only vehicles available for rent can be rented (secured with a smart contract). The time when a vehicle is rented, the owner can not put it available for rent (secured via smart contract) option and in that way we build trust and reputation among application users. Another revolutionary solution is the mapping of review points, without the possibility of manipulation. It will be achieved with the following feature: Review point to a vehicle can give only to users who rent that vehicle (mapping wallet address on the blockchain) and the smart contract is secured so that users can make it only one time (one more mapping on the blockchain). We map who buys the vehicle, in that way the new owner has the option to add details such as the rent/buy option. The previous owner is automatically removed for that privilege. When users pay for rent, the money goes automatically to the vehicle owner (a smart contract calculated the profit with a function and keeps the amount for a service fee). The same things happen when users buy a vehicle. |  
| 2. | Integration of ERC-20 token with the smart contract | The feature will give the option for the creator of a smart contract that can put a custom token (ERC-20) for payments. |  


### Milestone 2 - React (C & D from Project Details)

- **Estimated Duration:** 12 weeks
- **FTE:**  3
- **Costs:** $20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Oldtimers will provide documentation of the React application on Git, as well as documentation for connection with smart contracts. |
| 0c. | Unit Tests | Core functions will be fully covered by unit tests to ensure functionality and robustness. |
| 0d. | Integration Tests | Integration tests will be developed, including integration and connection with a smart contract. |
| 1. | Create react Dapp for the marketplace | Multiple components for forms and responsive design will make easy and simple using Dapp for marketplace. To achieved that goal, we brought in our team Dan B. (very experienced react developer, who already has enough experience with Ethers.js, Web3.js and Wagmi libraries). |  
| 2. | Integration and connection of the smart contract with created React Dapp | Our front-end developers should include in their work libraries such as Ethers.js, Web3.js, and Wagmi to accomplish this task. They have to ensure good RPC communication between our React application and the smart contract created on EOS EVM. |  

## Future Plans

- Oldtimers intend to build more Dapps on EOS EVM and to provide revolutionary solutions from web 2.0 to the web 3.0 industry. We hope that our majority support for that work will be [ENF](https://eosnetwork.com/).

## Additional Information

**How did you hear about the Grants Program?** We learned about the Grants Program from Twitter and also from a member of the EOS Network Foundation.

