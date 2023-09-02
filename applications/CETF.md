# EOS Network Foundation Grant Proposal

- **Project Name:** CETF - Crypto Exchange Traded Funds
- **Team Name:** CETF
- **EOS Payment Address:** cet.f
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1

## Project Overview

"New Proposal"

### Overview

- **Name:** CETF - Crypto Exchange Traded Funds
- **Brief Description:** There are thousands of crypto assets on the market, it requires a lot of research to know which assets to invest in. Most people do not know and don’t want to know anything about whitepapers, tokenomics, or on-chain analytics. Yet, they would like to invest in crypto. One of the solutions are ETFs/indices, we are building decentralized asset management protocol that enables to create and manage such ETFs. In other words, our protocol enables to put many tokens into one token. Through simplistic UX the token is available to be acquired by investors without prior exposure to crypto.
- **Relationship to EOSIO:** Our market research has shown that each chain has their own asset management protocol, our aim is provide a solution for EOSIO.
- **Reason for Interest:** We've have deep interest in finance and we've been building on EOSIO for more than two years. Fundamental interest is to maximize number of individuals who have financial freedom.
- **Pitch deck:** https://drive.google.com/file/d/1FldnAjAXED5Knl_Ud76PRCk8wx5UIjAW/view?usp=sharing
- **Helios interview:** https://youtu.be/JFsF0z1yz1Y



### Project Details

We created first ETF on EOSIO called EOSETF, it consists of 13 EOS mainnet tokens. We deployed the fund to the mainnet in 2021 Q3. UI can accessed via https://eosetf.io/, contracts deployed to https://bloks.io/account/cet.f. Currently there are more than 150 investors holding EOSETF, TVL has peaked over 35k USD. The price of the EOSETF has been pegged to the price of the underlying tokens it consists of, since some users have created arbitrage bots to capture price discrepancies, and others just perfrom the arbitrage manually. At current stage (Phase 1) EOSETF is a proof of concept/MVP. We saw enough traction to start building the Phase 2.

Phase 2 is being tested here: https://testing.eosetf.io/.

New features in Phase 2:

1. Automatic rebalancing

In current Phase 1 it is manual and laborious process to rebalance the fund. The new rebalancing function enables easily to include and exclude tokens from the fund. EOSETF (and the future funds) will have fund managers that through https://polling.eosetf.io/ (currently connected to the testing fund, which you can try to rebalance. Pick tokens you'd like to include or exclude, click VOTE and then REBALANCE). There is no limit as to how many fund managers can participate in the rebalancing. The votes of fund managers are summed together to produce the final allocation. We've on-boarded three individuals from EOS community who have the skill and are interested in managing the EOSETF. Based on the votes of fund managers the REBALANCING function automatically exectues the trades via https://defibox.io/.

2. CETF staking

In Phase 1 we issued our native token CETF to all the creators of EOSETF (no token sale). In Phase 2 the CETF token can be staked. Staking enables to recieve portion of the fees that the EOSETF generates. Each week, stakers are able to claim EOSETF fees generated during the previous week.

3. CETF mining

Extremely important component of a funtioning ETF is its liquidity. As such we've created CETF mining function to incentivize liquidity providers for EOSETF/EOS pair on Defibox (https://defibox.io/pool-market-details/1232). Each week, stakers of LP tokens will be able to claim CETF tokens.


  <br />
  <br />
Smart contracts of the above mentioned functions are 95% complete and currently in debugging phase. UI of the Phase 2 is 50% complete.

Your support would help us to finish the Phase 2 and deploy it to EOS, WAX and TELOS. Each chain requires configuration since the rebalancing function needs to be configured with a DEX. Our plan is to on-board fund managers and custodians for the fund on WAX and Telos. The fund on EOS is already under msig between 5 Eden members (Vladislav Hramtsov, Lennar Lehestik, Chaney Moore, Dan Singjoy, Bastiaan Moossdorff).

Phase 3 though is where the real magic happens. Once the Phase 2 is polished and perfected, the idea is to scale it in such way that anybody could easily set up their own ETFs.

Our philosophy for building is simplicity, our target group are individuals without prior exposure to crypto.

ETFs could be the vehicle through which EOSIO chains can receive more liquidity. Through ETFs built on CETF, investors could get exposure to assets of different chains, assuming there are proper bridges. Our ETFs might be the only crypto related assets they should hold in order to get exposure to the whole industry.

Eventually in Phase 3 it would be possible to create a single token that encompasses all the financial asset classes. One token containing fully diversified portfolio, exposure that sophisticated investor could only dream of, yet available to anyone. Creation of all encompassing asset is one the holygrails of finance. Such asset could eventually be created on CETF protocol.



### Ecosystem Fit

<b> - Where and how does your project fit into the ecosystem? </b>

  Fits on every chain that runs on EOSIO and has a DEX.

<b>- Who is your target audience?</b>

 -  Phase 2

 1. Existing investors in the ecosystem.

 2. Investors without prior exposure to crypto.



 - Phase 3

 1. Fund managers.
 
 2. Investors without prior exposure to crypto.
 
 3. Existing investors in crypto.

<b>- Are there any other projects similar to yours in the EOSIO ecosystem?</b>

  No.

<b>- If not, are there similar projects in related ecosystems?</b>

  Yes, each major chain has their own asset management protocol. All of them listed in the attached pitch deck.

## Team

### Team members

- Names of team members:

  Vladislav Hramtsov

  Lennar Lehestik

### Contact

- **Contact Name:** Vladislav Hramtsov
- **Contact Email:** hramtsovvladislav@gmail.com

### Legal Structure

- **Registered Legal Entity:** Asynchronous OÜ (LLC)
- **Registered Address:** Estonia, Lääne-Viru maakond, Rakvere linn, Kungla tn 6-6, 44308
- https://ariregister.rik.ee/eng/company/16532294/Asynchronous-O%C3%9C?active_tab=register

### Team Experience

We both been deep into theoretical finance, primarily during our time in Stockholm School of Economics.

I (Vladislav) have previously worked in PwC tech/legal department. When Peter Keay 3 years ago released his first developer course, I quit PwC to focus fully on learning development on EOSIO. Since then, I kept learning and buidling. Lennar has been on this journey with me but on a part-time basis as in parallel he has been working with Lustre.AI.

CETF is our second project on EOSIO. More than two years ago we released the first version of Consortium (https://app.consortium.vote/). Consortium is an on-chain polling dApp, that enables communities to use their tokens to vote in polls. On EOS mainnet, around 10 000 votes have been cast by more than 1500 accounts. More recent feature of Consortium has been a claiming tool (https://app.consortium.vote/claim). Created specifically for Eden members, tool enables to claim various tokens of EOS mainnet. More than 40% of all Eden members have claimed tokens via the tool.

Next iteration of Consortium is deployed to WAX (https://wax.consortium.vote/). Next month the plan is to launch it. This version of Consortium has tokenomics system inspired by protocol owned liquidity model. Initially it will serve Alien Worlds' communities. (https://github.com/n0umen0n/ConsortiumWAX)

We have used tech from LiquidApps, dFuse, we went quite deep with Anchor (triying to build an app with react-native).

Recently we completed the Helios's incubator.

In Pomelo seoason 1 and 2 CETF got more than 6o contributions.

In the first Eden election Lennar was elected as a delegate, primarily pitching CETF.

### CETF Repos

Smart contracts

- https://github.com/n0umen0n/sceosetf

Front-end

- https://github.com/lennarlehestik/eosetfv2

### Team Member Repos

Vladislav

- https://github.com/n0umen0n

Lennar

- https://github.com/lennarlehestik

## Development Status

- Phase 1 - complete
- Phase 2 - 85% complete
- Phase 3 - ideation (some % complete as a lot of code will be used from Phase 2)

## Development Roadmap

Grant would cover following parts of our project:
1. finalizing development of Phase 2.
2. deployment of Phase 2 to EOS / TELOS / WAX. 
3. on-boarding custodians and fund managers.

Ideally, we'd like to request some funds for audit of our contracts but that is an additional 10k-15k USD (Sentnl's price tag). 

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** Requested amount for the project is 10 000 USD. 

### Milestone 1  — finalize UI and smart contracts of Phase 2

- **Estimated duration:** 1 month
- **FTE:** 1
- **Costs:** 3000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Front-end and smart contract repos will contain documentation on how to set up a fund.  |
| 0c. | Unit Tests | Core functions (rebalancing, creation and redemption of the fund) will be covered by unit tests to ensure functionality and robustness. |
| 1. | UI | 19 fixes/additions in the to do list. | 
| 2. | Smart contracts | 2.1 Consultation with a developer (implementing fixes in case they are objective). 2.2 Configuration of the contracts for deployment.

### Milestone 2 — Phase 2 deployment to EOS mainnet

- **Estimated Duration:** 2 weeks
- **FTE:** 1
- **Costs:** 2,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Front-end and smart contract repos will contain documentation on how to set up a fund.  |
| 0c. | Unit Tests | Core functions (rebalancing, creation and redemption of the fund) will be covered by unit tests to ensure functionality and robustness. |
| 1. | Msig to deploy contracts. Configuration to reflect the current tokens in the fund. Msig to update contracts. Msigs to deploy the configurations.|
| 2. | Conducting first fund rebalancing by current custodians. |
| 3. | Giving the rights to rebalance to the fund managers. |


### Milestone 3 — Kick-off of CETF 2.0

- **Estimated Duration:** 3 weeks
- **FTE:** 1
- **Costs:** 5000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation will be updated with all the relevant changes.  |
| 0c. | Unit Tests | Tests will be provided for the new features |
| 0d. | Rationale behind changing the milestones | After deployment of the fund on EOS we decided that we need to further improve CETF before deploying it to WAX (previously Milestone 3) and TELOS (previously Milestone 4). Improvements need to be made in areas of on-boarding, UX (simplification of the UI), tokenomics and governance. Such improvements would enable us to abstract away the blockchain and attract investors outside of EOS eco-system. Our plan is to raise seed round, potentially from EOS Labs. 5k that is yet to be received from this grant would serve as a kick-off and enable us to start with the changes in the contracts and design of the new UI. New Milestone 3 will consist of three deliverables.|
| 1. | Addition of Performance fee (smart contracts).| Currently the fund on EOS has only management fee. It is a very small percentage charged when user initially invests. Low fee is attractive for the investors in the fund but resuls in very low profits for the protocol. Performance fee is crucial because it will ensure high profit margin for the CETF protocol. Potential profits will incentivize developers and external investors to contribute to the protocol.|
| 2. | Complete refactoring of the smart contracts (+audit with chatGPT) |
| 3. | New UI/UX design in Figma |

## Future Plans

<b>Roadmap</b>

1. Seed round.
2. Fractal/DAO launch. 
3. Upgrade to CETF 2.0 (complete refactoring of smart contracts, new UI/UX progressive web-app, performance fee integration, referral system, on-boarding for investors outside EOS eco-system)
4. Smart contract audit
5. Milestone 1 - Campaign to reach 1m in AUM in one fund.
6. Series A
7. Platform for custom fund creation
8. Milestone 2 - Campaign to reach 50m AUM across all funds.


- Our estimation is that 95% of tokens in our fund will be ETH, Ethereum based tokens and BTC. Hence our bet is on EOS having reliable bridge. Initial lack of liquidity would not be even a problem, as the demand for our fund could provide incentives to bring more liquidity to EOS.



## Additional Information

**How did you hear about the Grants Program?** Zack's tweet.
