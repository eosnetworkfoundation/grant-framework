# EOS Network Foundation Grant Proposal

- **Project Name:** EO2
- **Team Name:** EOTWO SAS
- **EOS Payment Address:** eotwodonacc
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):**  3
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** Yes
- **Repository where Project resides:** https://github.com/EO2-earth/EO2-app

## Contact

- **Contact Name:** Plinio HERRERA SCHUWIRTH
- **Contact Email:** p.herrera@eo2.earth
- **Website:** https://www.eo2.earth


## Project Overview

EO2's Mission is to contribute to a more inclusive, efficient, and reliable Carbon Market by providing all stakeholders with easier access to quality Carbon Credits. Our goal is achieved through the tokenization of regulated Carbon Credits and their (crypto-) representation into EO2 Digital Token, which reduces frictions and improves their usability and diffusion.
The core project function is represented in a smart contract that constitutes a two-way bridge between off-chain Carbon certificates and their in-chain Token representation. The smart contract is hosted on an EOSIO-based blockchain. To connect with the smart contract, users will interact with an app tailored according to the specific needs of each user class (Corporate or Individuals).
The user interface has been designed to facilitate the adoption from users with different levels of experience with technology and digital assets. Developing an intuitive user interface that simplifies the customer journey (registration, wallet, etc.) and the product cycle management (buy, sell, donate, etc.) was our goal to attract users with different levels of familiarity with technology and digital assets, and so promoting Carbon Markets inclusiveness.

The following video provides a simple overview of our project: https://www.youtube.com/watch?v=0yrKXtR34Do&t=3s 

### Overview

- **Name:** EO2, a Security Token that represents regulated Carbon Credit.
- **Brief Description:** EO2 aims to tokenize quality Carbon Credits and make them available to individuals and SMEs. 
- **Relationship to EOSIO:** EO2 Smart-contract is derived from the EOSIO Token Standard and it is hosted on EOSIO-Based Blockchain. The Smart-Contract is connected to our User Interface to facilitate the use for non-crypto users.
- **Reason for Interest:** At EO2, we believe that a transparent and efficient system of carbon offset is essential for transitioning to a zero-emission society. Our Mission is to make the regulated Carbon Market more inclusive and allow easy access to regulated Carbon Credits for individuals and SMEs. We want to provide an effective offset to clear the carbon footprint and a sustainable means to make a transaction and store value. 

### Project Details

The product consists of two applications focused on each user segment and/or the intended use of the Token: one for customers who will use EO2 Token as means of payment, for donations, and as a store of value; the second app is design to meet the needs of corporate users who will use the EO2 Token to pursue their sustainable agenda. Both applications will be declined in desktop and mobile version. 
- **Individual user Webapp:** ReactJS 18 UI Boilerplate and React CSS and material-UI for component designs. Account creation on EOSIO-based blockchain, Plug and play KYC and AML screening integration using a third-party provider (Likely to be Scorechain), backend using AWS and Sidebar Menu with Dashboard, Assets, Support, and buttons for each project-specific development. The webapp will include the integration of external authorization providers' such as ANCHOR and LEDGER.
- **Marketing:** consists of a three stage funnel that will help to the brand recognition and adoption:
	
	-**Captivating attention** through social networks, active participation in sustainability-related communities and providing incentives to individual users to join the EO2 community. As for corporate customers, specific marketing campaigns will leverage their needs aiming to develop more structured partnertship. The Greentech Alliance constitutes a preferential channel to create synergies and partnertship with relevant customers.
	
	-**Educating** non-crypto users and/or environmental sensitive people on the digital ecosystem, Carbon Markets and sustainability in general, highlighting the core values of EO2 and EOS network. Among the topics covered are: blockchain, digital assets, carbon markets, EO2 and EOSIO-based blockchain. The content will be delivered with videoclips, (co-produced or sponsored by ecosystem partners), social network posts, articles hosted on our own blog.  Incentives to engage and interact with the platform (e.g. in the form of rewards) will be in place.
	
	-**The conversion** will happen by leveraging the interest and engagement build in the previous phase and by making early adopters ambassadors of EO2.  

The B2B channel will be developed in a second stage following the prior engagement of indivuduals. 

- **PoC/MVP or other relevant prior work or research on the topic:**

The MVP is already completed. If not published yet by the time of the review of this application, you can request access to p.herrera@eo2.earth. Access to the MVP code will remain restricted and be shown upon request.

- **What EO2 is not or will not provide or implement:**

  EO2 will provide a boilerplate with basic and adaptable capabilities of its User Interface (Desktop and mobile), Smart Contract, and an Admin dashboard to evaluate the APP interaction. Those sections in the menu will be available for the user to be modified for their project. What will not be shared with the community are the functionalities specific to the business logic behind EO2. 
  
  EO2 can provide advice on using the boilerplate based on goodwill only. EO2 is not committed to providing support of any type in the development beyond the documentation of each component.


### Ecosystem Fit

- **Where and how does your project fit into the ecosystem?**

EO2’s target are users who are not yet familiar with crypto and digital assets in general, so customers of EO2 will translate into additional users of the EOSIO Ecosystem. Also, EO2 is building its identity around the authentic promotion of sustainability and the choise of EOSIO plays a relevant role in this strategy. The EOS ecosystem as a whole can benefit from this association between its technology and sustainability. 

- **Who is your target audience (chain/dapp/wallet/UI developers, designers, your user base, some dapp's userbase, yourself)?**

Apps developed by EO2 that are meant to be open-source are aimed at Dapp/UI Developers.

Our target audience is composed by:
-	Individuals that wants to either store the value of their savings or voluntarily clear their carbon footprint.
-	Companies looking for a more straightforward solution to fulfill their environmental goals without the intrinsic risk of greenwashing present in voluntary carbon markets. 
-	Investors looking for new cryptocurrencies to invest their money or to balance their investment portfolio.
-	Companies covered by the EU ETS that would benefit from an alternative to make their banked allowances more liquid, thus allocating extra resources to finance new technology and speed up their transition to Net-Zero.

- **What need(s) does your project meet?**

Our project is looking to make EUAs trading more accessible, easier to manage, and more inclusive.

As most regulated carbon markets, the EU compliance Carbon Market is substantially a closed system. Barriers to access the market, allow only covered enterprises (those required by the law to comply with it) and intermediaries to currently trade, invest and offset their emissions with EU Emission Allowances. Due to this friction, all stakeholders different from the above (i.e. SMEs and individuals) need to buy unregulated carbon certificates from the voluntary carbon market, proving to be prompt to greenwash. 

By enabling stakeholders to access the regulated carbon market, our project proposes a more solid and reliable alternative to those currently purchasing carbon certificates in the voluntary carbon market. To SMEs and individuals, the tokenization of Emission Allowances represents an easy and frictionless access to the regulated carbon market. 

Each Token is backed by an Emission Allowance, which provides value stability over time. EO2 will be the custodian of the Emission Allowances, and Token holders will be able to redeem the Token and be assigned with the underlying Allowances.   Each Token can be undefinetely transacted among users and companies, but once donated (I.e. from an individual to a company) , Tokens can only be “burned”. When Tokens are burned, the underlying Emission Allowances are surrendered off-chain before the European Commission registry. In addition, EO2 will make public the list of surrendered Emission Allowances in order to disclose to what extent companies and individuals are effectively contributing to the fight against climate change.

- **Are there any other projects similar to yours in the EOSIO ecosystem? If not, are there similar projects in related ecosystems? **

To the best of our knowledge, there are no direct competitors proposing the same or comparable offer, either inside or outside the EOS ecosystem. Nevertheless, There are some projects offering tokenized voluntary carbon markets certificates outside the EOS ecosystem.. Although we cannot assess the quality of their underlying carbon credits, it is worth noting that in general voluntary carbon markets are prompt to greenwashing and due to lack of regulations or common standard, it is challenging to make an informed decision when purchasing voluntary carbon credits, regardless of their digital support. By way of example,there are green projects which claim to protect trees that were never in danger of being cut, thus making the green certificates arising from said projects not valuable from a environment-protection point of view.  
As opposed to the voluntary carbon certificates, the European Commission is the guarantor of Emission Allowances and supervises the market stability over time. 

## Team

The team behind the project comes from diverse backgrounds. Besides IT expertise, the team members' experience includes Tax & Legal, Accounting, , Business Administration, Marketing & Communication, Corporate Finance, Sustainable Markets, and Strategy. 

### Team members

- **Team Leader:** Plinio Herrera Schuwirth 
-  Marco Bassan Guerrieri
- **IT Team Members:**
- Miguel Angel Lopez (project manager, full-stack developer)
- Nesrine Mrabet (full-stack developer)
- Jose Tomas Schuwirth (full-stack developer)
- Juan Schuwirth (full-stack developer)
- **Communications Team Members:**
- Catalina Ruiz Cristi
- Damien Guiral


### Legal Structure
- **Registered Legal Entity:** EOTWO SAS (French Societe par action simplifiee)
- **Registered Address:** 250 Avenue des Mouettes, 06700, Saint Laurent du Var, France.

### Team Experience

The team has more than 20 years of collective experience in software development plus 10 years in IT project management. Some of the project that the team has worked on include integration of payment system in the Chilean tax offices, programming microcontrolers for IoT solutions and, participating in blockchain bounties.


### Team Org Repos

https://github.com/EO2-earth


### Team Member Repos

-	https://github.com/mi-lopez
-	https://github.com/nmrabet
-	https://github.com/jtschuwirth
-	https://github.com/jeschuwirth

### Team LinkedIn Profiles (if available)

-	www.linkedin.com/miguel-angel-l%C3%B3pez-78639944/
-	www.linkedin.com/nmrabet
-	www.linkedin.com/in/pliniohs
-	www.linkedin.com/in/marco-bassan-guerrieri-b7aa176a/


## Development Status

**IT Development Status:**

The smart contract has been written with C++ language  using the EOS SDK and is currently running on TLOS Testnet.
The web application is hosted on AWS. Additionally, we have a NodeJS service running to get requests from the web application. That requests are made by API calls using REST protocols. 
All our source code is hosted on Github in a private account connected with AWS to do the deploys on the server machine.
We use git-flow architecture to work on our repositories.We have already developed a MVP with the primary business functions for our project and can be shown upon request. We are planning to launch the prototype publicly to test its functionalities in a live environment.

**Off-chain Development Status:**

-	Recognition of the innovative nature of EO2 by the French Interdepartmental Regional Body for the Economy, Employment, Labor and Solidarity (DRIEETS d'Île-de-France ).
-	Accepted as a member of the Greentech Alliance, A hub of 1500+ companies and 12.000 followers committed to fighting climate change using innovative technologies. (www.greentech.earth) 
-	Social network presence on Facebook, Instagram, Youtube, and Linkedin. Looking to expand to Medium and Discord. 
-	Webpage (www.EO2.earth & www.EO2.app)
-	Obtained a registry number to trade carbon allowances in the EU ETS.
-	Partnership with EDHEC Business School, Ranked #7 worldwide for its MBA (The economist 2021). The provide MBA students to help EO2 in its sustainability challenges as external consultants as part of their curriculum.
-	Grew a network of 500+ sustainability professionals on social networks


## Development Roadmap


### Overview

- **Total Estimated Duration:** 4 months 
- **Full-Time Equivalent (FTE):** Eight (8)
- **Total Costs:** 122,000 USD
	- **IT Development:** 50,000 USD
	- **Marketing-related expenses:** 52,000 USD
	- **Compliance & legal costs:** 15,000 USD
	- **Petty cash and eventualities:** 5,000 USD

**Note:** Some of the milestones can possibly overlap and be done in parallel.
### Milestone 1 Users web-app boilerplate
- **Estimated duration:** 2 month
- **FTE:**  4
- **Costs:** 25,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | BSD 3-Clause |
| 0b. | Documentation | Creation of documentation for the web app and basic usage |
| 0c. | Testing Guide | End to end tests using third-party software providers such as  https://ghostinspector.com/ |
| 0d. | Video | Provide an introductory video on how to build and set up the boilerplate |
| 1.  |	Multipage UI| Webapp with multiple pages and essential interaction (login, logout, send, receive, create an account) and multiple modals with QR generator for accounts to be easily scanned and imported with ANCHOR. |
| 2.  | Language | Multi-language support for the UI |

### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1
- **Costs:** 4,000 USD

...


## Future Plans

> Please include here

- how you intend to use, enhance, promote and support your project in the short term, and
- the team's long-term plans and intentions in relation to it.


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website / Medium / Twitter / Element / Announcement by another team / personal recommendation / etc.

> Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
