# EOS Network Foundation Grant Proposal

- **Project Name:** Small Business Accounting & Web3
- **Team Name:** CosmicStep Software, Inc dba tipit.io
- **EOS Payment Address:** tipitmanager
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** Company/Large, 1. New Proposal
- **Pomelo Grant(s):** https://pomelo.io/grants/tipit1
- **Project is Open-Source:** Yes for the Framework
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/tipitio/sba-web3


## Contact

- **Contact Name:** Mark Stair
- **Contact Email:** marks@tipit.io
- **Website:** https://tipit.io  (Note this is the tipit social wallet website, a new website and/or company will be created for this grant.)


## Project Overview

This grant proposal stems from the EVMxIdeathon on 14 Nov 2022 with the winning submission for the Web3 category:  Small Business Accounting & Web3.

This grant provides funding for the development and release of the framework to sync EOS blockchain with QuickBooks Online.  Approval of this grant will give access to EOS blockchain to small businesses that are already using QuickBooks and be used standalone to capture blockchain information for accounting purposes.

### Overview

- **Name:** Small Business Accounting & Web3
- **Brief Description:** Create a framework and syncing solution between EOS blockchain and accounting solutions like QuickBooks and QuickBooks online.
- **Relationship to EOSIO:** Links Partner (customers, vendors, and employees) to their EOS accounts by syncing these from QuickBooks online (QBO).  This will allow the system to track payments sent and received on EOS blockchain into QBO for accounting purposes.
- **Reason for Interest:** Our sister company, High5Software, has been providing small business solutions that sync to QB for two decades and achieved the highest QB Gold Partner for syncing QB and SME: Service Management Enterprise.  Leveraging this expertise will allow us to build a sync platform between EOS blockchain and QBO to provide accurate accounting using the typical base currency of USD.  Using price oracles, accurate accounting can be captured into QBO for use for sales tax, income tax and other general accounting practices.  This solution will also give small businesses an inexpensive way to receive EOS payments on invoices as well as pay vendors and employees.

### Project Details

- **A. Framework:** Multi-tenant software framework to enable Web3, EOS modules that sync with QUickBooks Online (QBO) and capability to sync with QB and other accounting solutions.
- **B. Partner Accounts:** Configure EOS account for all the partners that work with EOS/Web3 including Customers, Vendors/Suppliers/Subcontractors, Employees and the comppany using the system
- **C. tipit Pay:** Secure online payment system that can allow EOS payments in addition to traditional Credit Card and ACH payments using various processors.  tipit Pay links are added to invoices and emails of invoices.  Example: https://pay.tipit.io/home?platform=tipitpayrequest&to=gilsertience&amount=1000&symbol=GIL&contract=gilsertience&memo=But%20why%20not%20tho&precision=4
- **D. Web3 Monitoring:** Monitor company and partner accounts for transactions that should be captured into the accounting system.  This includes payments received into specific EOS accounts, for example receiving Pomelo grant funds and getting invoice payments from customers and sending payments to vendors and employees.
- **E. QBO Sync:** Sync all transactions to and from EOS blockchain into QBO.
- **F. Pricing Oracle:** Capture token prices at the time of the transaction for accurate accounting into QBO.  For example, if 5 EOS is received from a Pomelo grant at multiple different times, the system will accurately price those transations into the base currency, typically USD.
- **G. Ideathon:** Small Business Accounting & Web3 won the Ideathon on 14 Nov 2022.  The presentation and description can be found here: https://devpost.com/software/small-business-accounting-web3

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?
Most teams within the EOS ecosystem are considered "small businesses" and can use this system to accurately handle their accounting for sales tax, income tax and other accounting purposes.

- Who is your target audience?
All small businesses and independant contractors that are working with EOS for receiving and sending payments.  Also targeted to companies using QBO.

- What need(s) does your project meet?
Accurate accounting solution using the most popular small biz accounting system, QuickBooks Online while utilizing EOS blockchain.

- Are there any other projects similar to yours in the EOSIO ecosystem?
There are no solutions known for EOS.  There are three solutions on the QBO marketplace that work with other blockchains but none that work with EOS or Antelope chains.
FIO blockchain has some related elements such as tracking partner accounts across other blockchains and an invoicing solution, however no QBO syncing is available as far as we know.  FIO could possibly be a partner of this solution to allow payment handling on other blockchains such as BTC and ETH however investigation is outside the scope of this grant.

## Team
CosmicStep Software, Inc includes High5Software.com and tipit.io.  High5Software provides service management software solution that syncs with QB and provides small business training and support.  tipit.io is a social wallet that works with Antelop chains to provide tipping accross social platforms such as Discord, Telegram, Twitter, Twitch, Github, and at tipit.io

### Team members

- **Team Leader:** Mark Stair
- John (Gilser) Campbell
- Mark Olson
- David Grabowski
- David Hernandez
- Tony Van Natter

### Legal Structure
- **Registered Legal Entity:** CosmicStep Software, Inc (Note that a new legal entity may be created)
- **Registered Address:** 6700 NE 181st St, Unit 82525, Kenmore, WA 98028 USA

### Team Experience

**High5Software** The High5Software group has 40 years of experience providing software solutions for service management and syncing with QuickBooks, QBO, and QuickBooks Time (tsheets) as well as syncing to other platforms like ServiceNow and other accounting systems.  High5 was one of the first service management solutions to sync with QB over 20 years ago with ABC's of Service Management previously called QBSM: QuickBooks Service Management, however that name was not allowed by Intuit.  Later we built a more extensive sync with our SME: Service Management Enterprise solution that handles time tracking, invoicing, payments, purchase orders, inventory management, subcontractor management and much more.  The High5 QB sync is best in class and achieved QB Gold Partner status while they had that program.  High5 SME was featured on QB marketplace so we have gone through certification of the sync.  Intuit now focuses the marketplace around QBO so this solution would initially sync with QBO.

**tipit.io** tipit provides a social wallet that handles tipping and campaigns across social platforms.  tipit supports over 80 Antelope tokens on EOS, Telos, and Wax on social platforms such as Telegram, Discord, Twitter, Twitch, Github and tipit.io website.  The team also has experience working with the DAPP network.

### Team Org Repos

- https://github.com/tipitio
- https://github.com/tipitio/sba-web3
- https://github.com/tipitio/tipit-resources
- https://github.com/tipitio/Contracts


### Team Member Repos

- https://github.com/orgs/tipitio/people/MarkStair
- https://github.com/orgs/tipitio/people/Gilser

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/markstair/

## Development Status

- tipit pay mockup has been built to allow a simple URL to be added to an invoice or email so customers can pay.  The solution support traditional credit card and ach payments from OpenEdge/PayPros, PayPal and others.  Adding additional payment providers is relatively easy.  We have built a mockup to pay in EOS using Anchor ESR: EOS/Electronic Signing Request so that invoice payments go into the correct account.  Example: https://pay.tipit.io/home?platform=tipitpayrequest&to=gilsertience&amount=1000&symbol=GIL&contract=gilsertience&memo=But%20why%20not%20tho&precision=4

- EOS Ideathon presentation is available at https://devpost.com/software/small-business-accounting-web3

## Development Roadmap

### Milestone Summary

-   **Total Estimated Duration:** 9 months
-   **Full-Time Equivalent (FTE):** Four (4)
-   **Total Costs:** $550,450 USD

### Milestone 1 - Framework

-   Estimated duration: 3 months
-   FTE: 3
-   Costs: $180,750 USD

| Number | Deliverable       | Specification                                                                                        |
| -----: | ----------------- | ---------------------------------------------------------------------------------------------------- |
|    0a. | License           | Determine best license                                                                               |
|    0b. | Documentation     | Creation of documentation for the framework and how include applications                             |
|    0c. | Testing Guide     | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
|     1. | Framework API     | Framework API for application extensions.                  |
|     2. | Multi-tenant DB   | Creation and definition of the multi-tenant database handling Partners and transaction recording     |
|     3. | Single Sign On    | Single sign-on that works with Intuit QuickBooks Online oAuth 2.0  |

### Milestone 2 - Partner Accounts

-   Estimated duration: 2 months
-   FTE: 3
-   Costs: $120,500 USD

| Number | Deliverable       | Specification                                                                                        |
| -----: | ----------------- | ---------------------------------------------------------------------------------------------------- |
|     1. | Partner Accounts  | Configure EOS account information for Partners including customers, vendors and employees            |
|     2. | Sync QBO          | Sync partner accounts with QuickBooks Online customers, vendors, and employees including method for duplicating partners that are in multiple categories  |
|     4. | Partner UI        | User interface to configure EOS accounts for partners                                                |

### Milestone 3 - Account Monitoring

-   Estimated duration: 1 month
-   FTE: 2
-   Costs: $40,200 USD

| Number | Deliverable       | Specification                                                                                        |
| -----: | ----------------- | ---------------------------------------------------------------------------------------------------- |
|     1. | Monitor Partner EOS Accounts| Monitor Partner EOS accounts for relevant receive and send transactions on blockchain      |
|     2. | Non-Partner & Spam          | Document method to handle small (spam) transactions from non-partners                      |

### Milestone 4 - Pricing Oracle

-   Estimated duration: 1 month
-   FTE: 2
-   Costs: $40,200 USD

| Number | Deliverable       | Specification                                                                                        |
| -----: | ----------------- | ---------------------------------------------------------------------------------------------------- |
|     1. | Find Reliable Price Oracle | Investigate pricing oracles for EOS/USD and USDT (on EOS) to get accurate, real time pricing to base currency, USD     |
|     2. | Pricing Oracle           | Implement pricing oracle reading at time of partner account transactions                      |

### Milestone 5 - tipit Pay with EOS and USDT on EOS

-   Estimated duration: 2 months
-   FTE: 2
-   Costs: $80,400 USD

| Number | Deliverable       | Specification                                                                                        |
| -----: | ----------------- | ---------------------------------------------------------------------------------------------------- |
|     1. | ESR for EOS Invoice Payment | Create ESR for invoice payment requests that work with Anchor Wallet                       |
|     2. | QR Code EOS Payment         | Create QR code representing the ESR payment request                                        |
|     3. | Accept and Track EOS Payment| Track successful EOS payment and record against accounting record, i.e. invoice            |
|     4. | Price Oracle                | Utilize pricing oracle to determine & record price in EOS and USDT on EOS for the invoice  |
|     5. | Sync QBO                    | Sync payment against Invoice in QBO                                                        |

### Milestone 6 - tipit Pay with Credit Card and ACH

-   Estimated duration: 1 month
-   FTE: 2
-   Costs: $48,200 USD:  $40,200 USD development plus $8000 for payment processor setup and monthly fees

| Number | Deliverable       | Specification                                                                                        |
| -----: | ----------------- | ---------------------------------------------------------------------------------------------------- |
|     1. | Provide CC & ACH payments | Allow partners to pay in traditional Credit Card and ACH payments                            |
|     2. | Show Fees and Benefits    | Show fees of Credit Card, ACH and EOS payments along with EOS benefits of returns and instant transfer in 0.5 seconds (2 min confirmed)  |
|     3. | Partner Pays              | Provide option for the customer to pay transaction fees to encourage EOS usage               |

### Milestone 7 - QBO Marketplace Submission

-   Estimated duration: 2 months
-   FTE: 1
-   Costs: $40,200 USD

| Number | Deliverable       | Specification                                                                                        |
| -----: | ----------------- | ---------------------------------------------------------------------------------------------------- |
|     1. | QBO marketplace requirements | Implement all QBO marketplace requirements as described at https://developer.intuit.com/app/developer/qbo/docs/develop |
|     2. | Publish           | Submit application for QBO publishing |
|     3. | List              | List app on the QuickBooks App store if publishing approved by Intuit. Highlight EOS in listing.     |


## Future Plans

Note that all these ideas are large projects in themselves.  Other developer companies can create these applications to use in the Framework.
- QuickBooks sync:  Provide sync to QB desktop if requested by customers as some companies prefer QB over QBO
- EOS Books: Simple standalone accounting solution that doesn't need QBO or QB
- POS Point of Sale system to allow EOS based payments.
- KeyFA: Improved 2FA using keys in EOS wallet
- Time Tracking: EOS based time tracking with payment upon time approval
- Item NFTs:  New standard for physical items and equipment extending Atomic Assets and/or SimpleAssets but for business item handling
- Item Delivery Escrow:  Smart contract and system that can hold payment in "escrow" until items are received, then automatically release payment to supplier.  Also can handle payments to delivery companies.
- Sales Tax System: Decentralized sales tax handling system


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website and Twitter plus recommendation to apply for grant from Ideathon coordinator.

- tipit pay for Credit Card and ACH has already been implemented with several real payments made by customers using OpenEdge payment processor and PayPal.  Simple ESR payment request mockup has been coded enough to prove the concept but not completed or tested yet
- This idea is completely separate from tipit social wallet since that was focused on end users within social platforms while this project is for businesses.
- Will submit a pomelo grant for this idea as well in Season 4.  
- Will apply for grants on Telos, WAX, FIO, and others if they want the solution on those chains.
