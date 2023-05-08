# EOS Network Foundation Grant Proposal

- **Project Name:** EOS sw/eden public history API
- **Team Name:** sw/eden
- **EOS Payment Address:** eosswedenswe
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):** https://pomelo.io/grants/fullhistory
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** -

## Contact
- **Contact Name:** Vahid Toosi
- **Contact Email:** vahid@playparkx.com
- **Website:** https://eossweden.org

## Project Overview
This proposal is for providing and maintaining Public and Freely Availabile Non Filtered Full history Hyperion API. With the reduction in BP placement and thereby income, we have been operating this infrastructure at a loss for the last 18 months.

We have been supporting EOS since it's infancy, and wish to continue to do so, even with the changed economic situation. However, **we need support to continue to operate at this scale.**

### Overview
- **Name:**
sw/eden
- **Brief Description:**
Operating public EOS Full-history hyperion API
- **Relationship to EOS Network / Antelope:**
Publicly accessible Full history is essential to keep the transparency and accessability of any public blockchain. This information is required for Tax Purposes, as well as providing full transaction traceability for any Block explorer, user and DAPP that might require that information.
- **Reason for Interest:**
We have been supporting EOS since the first public testnet, and has been providing an Available Full History API since Mainnet launched

![](https://eossweden.org/wp-content/uploads/2023/04/eos-hyperion.png)

### Project Details
With rising cost of running the hyperion service, due to rising energi costs, rents and inflation, in combination with the weak market, we have run this service with an increasing loss since end of 2021. We don't see a possibility to keep the hyperion service up running without funding from the EOS Network Foundation.

This proposal is for covering the cost of running and maintaining the EOS hyperion. Milestones are divided in historical, present and future.

Currently our Elasticsearch cluster for our EOS Full History is using 40.7TB of disk. Including replicas of the data for redundancy. We store more recent data in fast and high performant drives, while older data is moved to normal Datacenter SSD drives, The oldest data is then moved to Enterprise HDD drives, as it is requested less frequently. The Elasticscluster drives are also
RAID 1, so we are **using more than 80TB of disk** space atm.

Our EOS Elasticsearch and Hyperion cluster is using 5 dedicated servers, plus 4 additional machines that operate Nodeos instances for the API cluster. On top of that we also have 3 dedicated servers in hetzner for backup nodes, load balancing and caching.

We also have dedicated server to store backups of snapshots, blocklogs and other backups that can be required for the operation.

Our tech team is 4 people, to ensure we have 24/7 availability, 2 are working fulltime on our API infrastructure, Maintaining, Improving and optimizing the systems, softwares and hardware. The remaining two are part of the rotating standby schedule, as well as focusing on other tasks in our operation.

We estimate that the API Infrastructure requires an average of 1.5 fulltime employees at this stage, to cover the 24/7 availability.

### Ecosystem Fit
**Where and how does your project fit into the ecosystem?**
It is an essential tool for anyone that has intentions to Use EOS, or build any DAPP on EOS.
**Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**
The target audience is all of the above, anyone that would require account or contract history. The main users seem to be DAPP operators and users with coding knowledge.
**What need(s) does your project meet?**
Accessability of EOS Transaction and action History
**Are there any other projects similar to yours in the EOS Network / Antelope ecosystem?**
We are the only team providing Hyperion Full History.
One other team is providing Full History Dfuse, which is another solution.
**If so, how is your project different?**
We provide **unfiltered** Full History to allow accurate query of the entire EOS History.

#### Data on our API infrastructure
According to eosnations validator, we are the only available hyperion (Last checked 2023-04-19).

How our Hyperion metrics compares to other History options is hard to say. This type of data is hard to compare and verify against any known metric.
In an attempt to present verifiable data, we can compare all valid requests passing through our Push API (status_code 20'x').

We are then able to compare those requests with EOS onchain transactions so far in 2023. In an attempt to present recent and verifyable data that provides us with some type of indication on activity and demand on our API endpoints. Now, PUSH API and History is not the same thing, but the data shows that our endpoint is actively used. The data is until 2023-04-19.

**Push API - Endpoint to push transactions onchain**
| Month | 20x requests | compared to onchain trx |
| ----- | ----------- | ------ |
| 2023-01 | 11,767,248 | 26.24% |
| 2023-02 | 10,833,664 | 26.02% |
| 2023-03 | 12,872,418 | 31.19% |
| 2023-04 | 7,660,719 | 36.96% |

**EOS Transactions** - onchain metrics
| Month | Transactions | Actions | Active Accounts |
| ----- | ----------- | ----------- | ----------- |
| 2023-01 | 44,844,302 | 100,884,790 | 599,428 |
| 2023-02 | 41,629,907 | 94,559,996 | 1,155,722 |
| 2023-03 | 41,273,376 | 94,343,573 | 227,499 |
| 2023-04 | 20,729,170 | 52,247,815 | 154,541 |


## Team
### Team members
- **Team Leader:** Eric
- Anders
- Joakim
- Henrik
- Vahid

### Legal Structure
- **Registered Legal Entity:**  PlayPark AB
- **Registered Address:** Verdandigatan 5, 114 24 Stockholm, Sweden

### Team Experience
We have been operating and pioneering the EOSIO/Antelope infrastructure ecosystem since the day we joined. From creating the first public EOS testnet, to creating the first live Block on EOS, and providing Full-History API service since day one for EOS and surrounding testnets.
<br>
![](https://media.tenor.com/mJ5dB2u5UrEAAAAC/is-experts.gif)

### Team Org Repos
- https://github.com/eosswedenorg
- https://github.com/eosswedenorg-go/
- https://github.com/eosswedenorg/antelope-api-healthcheck
- https://github.com/eosswedenorg/apt

### Team Member Repos
- https://github.com/xebb82
- https://github.com/pnx
- https://github.com/coachbjork

### Team LinkedIn Profiles (if available)
- https://www.linkedin.com/in/vahidtoosi/
- https://www.linkedin.com/in/ericbjork/
- https://www.linkedin.com/in/anyobservation/

## Development Status
Public API: https://api.eossweden.org
Documentation: https://api.eossweden.org/v2/docs

- links to improvement proposals or [RFPs](https://github.com/eosnetworkfoundation/grant-framework/tree/main/docs/rfps) (requests for proposal),

## Development Roadmap
### Milestone Summary
- **Total Estimated Duration:** 9 months
- **Full-Time Equivalent (FTE):** 1.5 FTE
- **Total Costs:** 135,000 USD
<br>
![](https://media.tenor.com/yuqvJfyDjisAAAAC/boat.gif)
<br>
The graph below is representing our Monhtly income from operating on EOS compared to the costs for running our Infrastructure for the Full History API for the last 18 months.
Since the end of 2021, we have been operating at a loss. This also covers the expenses for running the BP node, snapshot service and APT packages.

The USD value is calculated on the EOS closing price on the claimed Block and vote rewards.

Net Loss past 18 months: **$287,132**
<br>
![](https://eossweden.org/wp-content/uploads/2023/04/eos_hyperion_net.png)


### Milestone 1  — Running hyperion Q2 of 2023
- **Estimated Duration:** 3 month
- **FTE:**  1.5 *(24/7 availability)*
- **Costs:** Requested 45,000 USD *(Actual cost 60,000 USD)*

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT / Apache 2.0 / GPLv3 / Unlicense |
| 0b. | Documentation | N/A
| 0c. | Testing Guide | N/A
| 0e. | Article | N/A
| 1. | Hyperion | Full History unfiltered Hyperion API Endpoint |
| 1b. | Software Maintenance | Maintaining the software required to operate the Hyperion API cluster |
| 1c. | Hardware Maintenance | Maintaining phyiscal servers, including identifying potential issues, replacing parts |
| 1d. | 24/7 availability | We require at minimum one team member to be available at all times. |


### Milestone 2  — Running hyperion Q3 of 2023
- **Estimated Duration:** 3 month
- **FTE:**  1.5 *(24/7 availability)*
- **Costs:** Requested 45,000 USD *(Actual cost 60,000 USD)*

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT / Apache 2.0 / GPLv3 / Unlicense |
| 0b. | Documentation | N/A
| 0c. | Testing Guide | N/A
| 0e. | Article | N/A
| 1. | Hyperion | Full History unfiltered Hyperion API Endpoint |
| 1b. | Software Maintenance | Maintaining the software required to operate the Hyperion API cluster |
| 1c. | Hardware Maintenance | Maintaining phyiscal servers, including identifying potential issues, replacing parts |
| 1d. | 24/7 availability | We require at minimum one team member to be available at all times. |


### Milestone 3  — Running hyperion Q4 of 2023
- **Estimated Duration:** 3 month
- **FTE:**  1.5 *(24/7 availability)*
- **Costs:** Requested 45,000 USD *(Actual cost 60,000 USD)*

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT / Apache 2.0 / GPLv3 / Unlicense |
| 0b. | Documentation | N/A
| 0c. | Testing Guide | N/A
| 0e. | Article | N/A
| 1. | Hyperion | Full History unfiltered Hyperion API Endpoint |
| 1b. | Software Maintenance | Maintaining the software required to operate the Hyperion API cluster |
| 1c. | Hardware Maintenance | Maintaining phyiscal servers, including identifying potential issues, replacing parts |
| 1d. | 24/7 availability | We require at minimum one team member to be available at all times. |


## Future Plans
We are emotionally invested in the Antelope ecosystem, and are doing our best to keep supporting the users and projects on the platforms.

We hope to see a long-term sustainable model where EOS and the sister chains are successfull and can bring a strong connected ecosystem to fruition. Which we hope to be a significant contributor for, by providing tools and data to quickly and easy access information and get started on their projects.

![](https://media.tenor.com/FJxFggDhlWcAAAAC/party-happy.gif)

## Additional Information
**How did you hear about the Grants Program?**
Been following the development and work of ENF.

#### Github Repo
- https://github.com/eosswedenorg
- https://github.com/eosswedenorg-go
#### API docs
- https://api.eossweden.org/v2/docs
#### Nodeos Snapshots and Block log backups:
- https://snapshots.eossweden.org
#### EOSIO/Antelope Apt Repo
- https://eosswedenorg.github.io/apt/
#### HAProxy Antelope Health Check
- https://github.com/eosswedenorg/antelope-api-healthcheck
#### Bootable USB with EOSIO/Antelope tools
- https://github.com/eosswedenorg/eosio-livecd
#### EOSIO/Antelope vanity keygen
- https://github.com/eosswedenorg/eosio-keygen
#### Website
- https://eossweden.org
#### Antelope/EOSIO videos and content
- https://youtube.com/anyobservation
- https://academy.anyo.io/blog
