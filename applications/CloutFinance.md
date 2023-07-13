# EOS Network Foundation Grant Proposal

- **Project Name:** Clout Finance
- **Team Name:** Clout Finance Team
- **EOS Payment Address:** 0x67185e72313A83Fb3e41Dc48E64f6Bb507dCe930
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 2
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/CloutFinance

## Contact

- **Contact Name:** Alex
- **Contact Email:** cloutfinance2023@gmail.com
- **Website:** https://theclout.finance


## Project Overview

Clout Finance is a decentralized spot and perpetual exchange that supports low swap fees and zero price impact trades. Trading is supported by a unique multi-asset pool that earns liquidity providers fees from market making, swap fees and leverage trading.

The Fees earned from the DEX, will be distributed to the Stakers, Liquidity provider and buy-back to deepen the liquidity



### Overview

- **Name:** Clout Finance, a Perpetual Decentralized Exchange
- **Brief Description:** Clout Finance is a decentralised spot and perpetual exchnage that will allow the users to take long and short call of assets like BTC, ETH, EOS, and more.
- **Relationship to EOS Network / Antelope:** Clout Finance Brings the Perpetuals to the EOS ecosystem allowing users to take long and short position directly from their metamask
- **Reason for Interest:** EOS EVM is a growing Ecosystem and Clout wants to be the part of the adaptation from the very start, the fast transactions that can be performed on EOS EVM is also one reason we are excited to build the application on EOS

### Project Details

**Clout Finance** offers following features: 
- Decentralised spot and Perpetual exchange allowing users to take short and long position directly from their non-custodial wallets
- Add Liquidity to the platform by minting CLP tokens in exchange of supported basket assets like ETH, BTC, EOS, USDT and more
- Remove Liquidity and get your assets back by burning the CLP 
- Staking the CLOUT and CLP tokens for rewards

***Fees Distribution***

   **60%** fees for CLP Stakers
    **30%** fees for CLOUT & esCLOUT Stakers
    **5%** fees for the dev team
    **5%** fees for  buyback and CLOUT-EOS LP

***CLP, platform's liquidity provider token***

CLP consists of an index of assets used for swaps and leverage trading. It can be minted using any index asset and burnt to redeem any index asset. The price for minting and redemption is calculated based on (the total worth of assets in the index including profits and losses of open positions) / (CLP supply).

Holders of the CLP token earn Escrowed CLOUT rewards and 60% of platform fees distributed in EOS.

***Rewards***

CLOUT Rewards provide benefits for long-term users of the protocol, these rewards come in the form of Escrowed CLOUT and Multiplier Points.

A summary of rewards and mechanics:

   **CLOUT**: earns **EOS / WETH**, **esCLOUT**, and **Multiplier Points** when staked
    **esCLOUT**: earns **EOS / WETH**, **esCLOUT**, and **Multiplier Points** when staked
    **Multiplier Points**: **boost EOS / WETH APRs** when staked
     **CLP**: earns **EOS / WETH**, **esCLOUT**, automatically staked on mint


### Ecosystem Fit

- Where and how does your project fit into the ecosystem? 

	Currently there is no Perpetual DEX on EOS EVM, that's where we come in, we can bring in new liquidity(TVL) and asset exposure with the CLP index token offerings and with our exciting fee distribution, we can attract new users.
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)? 

	Chains: By adding support of the respective native asset in our liquidity token CLP we would attarct users from ETH, BTC, MATIC, AVAX
	Dapps: By collaboration of major DEXes in the EOS ecosystem we leverage the existing dapp community of EOS
	Wallet: By collaboration with wallets like OKX, Bitkeep and more, we get exposure from their community
	
- What need(s) does your project meet? 

	Decentralised Perpetual trading is today’s need in any and every ecosystem, users must be able to take long and short positions without compromising their control of the asset
- Are there any other projects similar to yours in the EOS Network / Antelope ecosystem? 

	At the moment, we don't see any other project in the ecosystem and yes there are similar projects in related ecosystem 

## Team

### Team members

- **Team Leader:** Alex
- More details sent by mail to [grants@eosnetwork.com](mailto:grants@eosnetwork.com)

### Legal Structure
- **Registered Legal Entity:** Sent by mail to [grants@eosnetwork.com](mailto:grants@eosnetwork.com)
- **Registered Address:** Sent by mail to [grants@eosnetwork.com](mailto:grants@eosnetwork.com)

### Team Experience

- [Swapped Finance](https://www.swapped.finance/)
- [Swapsicle](https://www.swapsicle.io/)
- [HokkFi](https://www.hokkfi.com/#/swap)

### Team Org Repos

N/A


### Team Member Repos

N/A

### Team LinkedIn Profiles (if available)

N/A

## Development Status

We have completed the Documentation outlining our plans. However, we are currently engaged in ongoing research and fine-tuning our implementation approach. The development of the UI/UX design is also in progress.

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 8.5 weeks 
- **Full-Time Equivalent (FTE):** 6 FTE
- **Total Costs:** 46,500 USD



### Milestone 0 — Requirement Analysis and Project Discovery

- **Estimated duration:** 1 Weeks
- **FTE:**  2
- **Costs:** 5,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | Social Outreach | Social Media campaigns to be planned with videos and infographics to be prepared |
| 0b. | Quests | To get the quick attention from web3 Community from other ecosystem, quests will be launched which will giveaway from CLOUT and USDT tokens |
| 0c. | Moderators | Getting moderators to engage and handle the community meanwhile of development |



### Milestone 1 — Smart Contracts

- **Estimated Duration:** 2 weeks
- **FTE:**  3
- **Costs:** 15,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | Vault Contract | Completion of Vault and underlying contracts  will enable the multi-asset basket liquidity for Clout Finance |
| 0b. | Router Contract | Completion of Router Contract and underlying contracts will enable the spot swapping|
| 0c. | PositionRouter contract | Completion of PositionRouter Contract and underlying contracts will enable the long and short order requests|
| 0d. | OrderBook Contract | Completion of OrderBook and underlying contracts enables the increase and decrease on created short and long positions  |
| 0e. | Reader Contract | Completion of Reader contract which will enable read-only data from the deployed contracts
| 0f. | OrderBookReader Contract | Completion of OrderBookReader contract and underlying contracts will enable read-only data from the deployed contracts
| 0g. | StakedCLP | A representative token, provided when CLP is staked |  
| 0h. | ClpManager | Completion of ClpManager contract and underlying contracts maintains and provides the price of CLP index  |  
| 0i. | RewardRouter | Completion of RewardRouter contract and underlying contracts manages the rewards distribution |  

### Milestone 2 — Smart Contracts Deployment Scripts

- **Estimated Duration:** 1 week
- **FTE:**  1
- **Costs:** 2000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | Testnet Script | Completion of the testnet deployment script allows us to seemlessly deploy the contracts on testnet |
| 0b. | Mainnet Script | Completion of the mainnet deployment script allows us to seemlessly deploy the contracts on mainnet |



### Milestone 3 — Subgraphs and Frontend changes

- **Estimated Duration:** 2 weeks
- **FTE:**  1
- **Costs:** 12500 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | theGraph self deployment | Preparing the server to start the theGraph indexer |
| 0b. | Trades Subgraph | subgraphs to fetch the trades of the Clout Finance  |
| 0c. | Stats Subgraph | subgraphs to fetch the stats of the Clout Finance  |
| 0d. | Referral and rewards Subgraph | subgraphs to fetch the referrals and rewards of the Clout Finance  |
| 0e. | Frontend changes | Fetching data from subgraph to frontend, updating other important changes on the frontend  |
| 0f. | Smart contract integrations | improvements in the integration of the smart contracts  |

### Milestone 4 — Liquidators and Order Keepers

- **Estimated Duration:** 1.5 week
- **FTE:**  2
- **Costs:** 7000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | Liquidators Bot | Completion of the Liquidation bot will liquidate the positions |
| 0b. | Order Keeper Bot | Completion of the order keeper bot will maintain and implements the increase or decrease position request to the orderbook |
| 0c. | Price Keepers Bot | A fail-safe bot that updates the 2nd price feed which is a aggregate of all CEX prices, to make sure there is no difference between oracle price and Exchange price |

### Milestone 5 — Mainnet launch & marketing

- **Estimated Duration:** 1 week
- **FTE:**  2
- **Costs:** 5000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | Mainnet deployment | Deployment on the EOS EVM mainnet |
| 0b. | Article | We will publish an informative threads on twitter, explaining the concept and how they will be utilized within our project.  |
| 0c. | Quest Campaigns | Campaigns launched on web3 project discovery platforms to gain exposure |


## Future Plans

- Include the Forex and equity market in the Perpetuals, so that users can take long and short positions on the Equity and Forex market as well


## Additional Information

**How did you hear about the Grants Program?** Twitter
