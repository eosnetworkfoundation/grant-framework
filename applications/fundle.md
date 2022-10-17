# EOS Network Foundation Grant Proposal

- **Project Name:** Fundle
- **Team Name:** Fundle
- **EOS Payment Address:** fundle.gm
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 3
- **Pomelo Grant(s):**  N/A 
- **Project is Open-Source:** Partly
- **Project was part of Token sale:** No
- **Repository where Project resides:** BitBucket private repository

## Contact

- **Contact Name:** Wiebe Hendriks
- **Contact Email:** wiebe.hendriks@wefundle.com
- **Website:** https://wefundle.com

## Project Overview

This grant will be used to build the token bonding curve mechanism, integrate with TrustEVM and launch the platform. 

#### Platform video 
This video will show how the application will look like and how Fundle works!

https://vimeo.com/759605041
### Overview

- **Name:** Fundle
- **Brief Description:** 

  Fundle is a platform where businesses can raise funds and build tokenized communities to increase customer engagement! We allow businesses to build stronger   long-term relationships, offer new customer experiences and gain more out of a community. Businesses can offer a broader set of rewards to its  most       loyal customers while gaining promotion and feedback from them. Each business has its own token to build a digital community and economy. Holders of       that token (members) can unlock specific rewards, experiences, interaction or involvement. The model allows the community to be rewarded for the value     they’re helping create in the business. Gaining more value from the community for both business and members is what Fundle stands for.

  For a detailed explanation please visit: https://wefundle.com/ and https://wefundle.com/about
  
- **Relationship to EOSIO:** We are planning to run the token bonding curve mechanism/AMM on TrustEVM and EOS!
- **Reason for Interest:** Blockchain allows us to revolutionize and strengthen the position of the community. We truly believe in the added value of EOS, we would like to utilize the benefits of high throughput and low transaction costs for our users. These aspects are crucial for the success of our platform. With the entrance of the ENF, we see that many good developments are going on, and therefore we have trust in EOS for the future!

### Project Details

Our team has an ambitious long-term commitment to make Fundle the most popular all-in-one platform for community building, managing, and crowdfunding. 

We see an interesting opportunity in the crowdfunding and community-building market. In these markets involvement and interaction are essential for success. With the entrance of web3, we can strengthen and improve these factors. 

21 million users, $6,8 billion dollars pledged, and 227,000 projects funded. These are Kickstarter's stats and represent only 21.21% of the crowdfunding market, this means a total of 100 million users. Over the last years this market has proven to be a successful formula for funding products. However, there is little involvement, interaction, and control for backers. Furthermore the success rate of crowdfunding can be improved by intensive community building and working together. 

For businesses, the top 3 benefits of an online community are customer loyalty, reduction in support costs and brand awareness. 70% of communities positively affect the brand and company culture. Companies with online communities are 60% more profitable than companies which do not focus on online communities.

An average member contributes $67 of worth yearly to the community. 33% of organizations with an online community have 10,000 or more members. In the coming years, the social business market will potentially grow with a CAGR of 30.8% to 7 trillion by 2030. Community building is becoming an increasingly important topic for businesses. 

Active participation, involvement, and engagement remains difficult for large businesses. 55% of community professionals find it difficult to consistently engage members when running online communities.  For small businesses building and managing communities remains challenging and a barrier.

These market trends and opportunities form the basis of the Fundle platform. We can revolutionize this landscape by combining the benefits of these markets and blockchain. The way of community building and fundraising needs to be redeveloped to let it reach its maximum potential. We believe that building long-term relationships, involvement and control is essential for this. Our community token model allows businesses to reward members and engage with them more closely than before. The funding mechanism will be democratic and based on voting to release the funds stepwise. We will move towards a heavily interactive environment based on open business participation. The community can help tackling issues and be paid out in tokens. 

#### Application UI 
<img width="1296" alt="image" src="https://user-images.githubusercontent.com/54183058/191728363-99844410-721e-4e51-ae91-471825e49806.png">

#### Application architecture 
<img width="637" alt="image" src="https://user-images.githubusercontent.com/54183058/193469553-1f083355-a2b3-4512-90d7-9cd5f76e5330.png">

Framework used for application and API: Laravel (PHP). The blue parts are already finished, these parts won't be open source since it is custom made for the Fundle platform! This part has no value for the community to be open source. The token bonding curve mechanism will be open source and usable for the EOS community.

#### Token Bonding Curve mechanism
With this grant we will build the token bonding curve mechanism which will thereafter be used for the Fundle application. We will build further up on the Balancer protocol. The protocol will allow users to buy/sell tokens per community according to a token bonding curve mechanism. So each community has its own token which is created when business create their community on Fundle. The reserve token will be a stablecoin (e.g. USDC,USDT). Per community the stablecoin will be bonded to the community token. When users send the stablecoin, the community token will be mint according to the current price and supply and when users want to sell their tokens the tokens are burned according to the current price and supply. The price of a community token will be determined by the $community supply and the holding patterns of token holders.
 
<img width="1433" alt="image" src="https://user-images.githubusercontent.com/54183058/196049946-824c72bb-c950-401c-8e65-4ba71e8534c3.png">

The structure of the community tokens will be the following:
<img width="584" alt="image" src="https://user-images.githubusercontent.com/54183058/192855088-b0474ed6-9b17-43a9-9d1a-4c8bfc0a661a.png">

We want to use EOS (via Trust EVM) because of transaction speed, lower costs, integration with popular wallets (coinbase, metamask) and fiat gateways. Payment accessibility is of high importance for our platform.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?

  Our platform will run on the EOS blockchain, this brings lots of new users (also non/new crypto users) who will interact and get to know EOS. The contracts of Fundle will be deployed on TrustEVM. Fundle shows others what possibilities TrustEVM has and that it is possible to build these platforms on the EOS blockchain! We can be a perfect use case for TrustEVM. The purpose of Fundle is to have lots of interaction between members and the business. This will result in many transactions on the EOS Blockchain. 

- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?

  Our focus is on two types of businesses. Innovative and creative businesses with existing communities who like to have more interaction with their         fanbase to gain more (value) from their community or offer new customer experiences. Or startups who want to build, grow and manage their                 community/business. 

  On the other side we have members. They buy tokens because they want to become part of the digital community to enjoy the benefits. We are also           targetting on members who have never used blockchain before (therefore payment accesibility with fiat on   ramps is important for us). The system is       going to be easy understandable and customer friendly. In our future plans when people can work for communities we will also be targetting                 creatives/freelancers. So, it is a platform that is useful and interesting for a wide range of people.

- What need(s) does your project meet?

  #### For members:
  Current platforms lack real community involvement and interaction. Members cannot really be "part of" and there is little interaction. Furthermore, both business and members cannot always have fair benefits (social and/or economical).

  Therefore, Fundle offers:
  - Exclusive membership with access to special perks and experiences. Members are proud token holders of the community.
  - Involvement and interaction with the business. 
  - More members entering the community can lead to an increase in personal token value.
  - Creatives can work for the community in exchange for community tokens. For example, website or logo design, (social media) marketing, video or picture creation/editing, etc.
  - Democratic fundraising mechanism where members have control over the collected money. (Mechanism will be included in the future)

  #### For businesses:
  From business perspective, much more can be gained from a community (skills,       opinions, etc.). An involved and active community will result in loyal customers, a reduction in support costs and an increase in brand awareness and     trust. This will positively affect the profit and success of the business.

  Therefore, Fundle offers:
  - Stronger and intenser community building thanks to the community token model. 
    - Incentivize members to engage and promote the business more than ever because members have economic & social incentives to help the business              succeed. This makes it a very effective marketing tool.
    - Stimulates members to participate and think actively.
    - Offering new types of rewards (digital assets or experiences).
  - Access to the skills and opinions of a whole community to help grow and improve the business and product.
    - The system enables to unlock new forms of product creation and working, namely together with members.
  - Building of a digital economy. The market cap of the tokens gives a good representation of the value that the community is worth. Community will grow not only by its members but also in value.
  - Flexible funding with multiple funding rounds and direct access to part of the funds. (Mechanism will be included in the future)

__________________________________________________________________________________________________________________________________________________________

- Are there any other projects similar to yours in the EOSIO ecosystem?
  To the best of our knowledge there are no similar projects in the EOS or related ecosystems.

## Team
### Team members

- **Team Leader:** Wiebe Hendriks

- Niels Snakenborg
- Leo Frehe
- Gerton Knipping
- Rhett Oudkerk Pool
- Zaisan

### Legal Structure
- **Registered Legal Entity:** We are in the initial process of registration
- **Registered Address:** N/A

### Team Experience

**Wiebe Hendriks**

Role: CEO

An ambitious and enthusiastic person with an entrepreneurial and problem-solving mindset. Strong affinity with innovation and IT. Likes to go the extra mile. Background in Industrial Engineering and Management at Eindhoven University of Technology. Within Fundle focusing on general tasks (strategy, product design/functionalities), Software Development (front-end, blockchain), Marketing and Financial.

**Niels Snakenborg**

Role: Software Developer 

A senior software developer that loves to work with people, new technologies and innovations. Designed, build en deployed several solutions for big companies in the past 7 years and uses this experience for Fundle and as an iOS and web developer. I get energy from working with like minded people and I am responsible for the backend development.

**Leo Frehe**

Role: Business Advisor 

Over 20 years proven track record in senior/executive roles within both IT and business consultancy. From Professional- and Software Services to Manages Services and IP Solutions. Leading Sales and Delivery teams. With a passion for driving demonstrable results through leadership and teamwork. I have high energy and passion for business, business technology & innovation.

**Gerton Knipping**

Role: Marketing & Brand Advisor 

Founder of branding and positioning agencies with over 25 years of experience. Colleagues, clients and project teams consider me as a positive-critical person with a practical approach. I have always been a generalist with a sharp focus on details who was responsible for the clear translations from strategy to creation. Passion for solving problems; complex or simple, always with the highest attainable end result.

**Rhett Oudkerk Pool**

Role: Business/Web3 Advisor 

CEO and founder of Zaisan, Europechain and previously Kahuna. A passionate entrepreneur, business leader, consultant, public speaker, and investor in Cyber Security & Web3 Companies. Always left of the chasm. Helping innovative companies and entrepreneurs create next-generation business models utilizing blockchain technology, to be part of the Internet of Value. 

**Zaisan**

Role: Business and blockchain development support 

Zaisan has been around in EOSIO ecosystem for several years, formally known as Europechain BV. The company is founded by several European block producers, and is focusing on software projects and business consultancy. The company has previously taken the task of writing the EOSIO Core+ Blue Paper on request of ENF.


### Team Org Repos

- Our code is privately hosted in a BitBucket repository

### Team Member Repos

- https://github.com/WiebeHendriks
- https://github.com/Niels-Snakenborg

### Team LinkedIn Profiles

- https://www.linkedin.com/in/wiebe-hendriks/
- https://www.linkedin.com/in/niels-snakenborg-05a07661/
- https://www.linkedin.com/in/leo-frehe-9433811/
- https://www.linkedin.com/in/rhettoudkerkpool/

## Development Status
The platform is already far in development. The non-blockchain part is finished and tested right now with users on usability and bugs. This version shows exactly how the first phase of the platform will work and look like. The missing piece before we can go live is the token bonding curve mechanism.

#### Articles

Some relevant literature and articles about tokenized communities, community building and token bonding curves! 

**Community building importance for businesses**

- https://peerboard.com/resources/online-community-statistics#engagement
- https://tribe.so/blog/30-online-community-stats-you-must-know-in-2019/
- https://www.linkedin.com/pulse/online-community-statistics-50-stats-know-2021-peerboard/

**Tokenized Communities**

- https://www.thetilt.com/revenue/community-tokens-business-model
- https://coinvise.substack.com/p/crowdfunding-projects-through-social?s=r

**Token bonding curves**

- https://medium.com/linum-labs/intro-to-bonding-curves-and-shapes-bf326bc4e11a
- https://billyrennekamp.medium.com/converting-between-bancor-and-bonding-curve-price-formulas-9c11309062f5
- https://yos.io/2018/11/10/bonding-curves/
- https://www.linumlabs.com/articles/bonding-curves-the-what-why-and-shapes-behind-it
- https://medium.com/molecule-blog/token-bonding-curve-design-parameters-95d365cbec4f
- https://tokeneconomy.co/dynamic-token-bonding-curves-41d36e43befa


## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 12 months 
- **Full-Time Equivalent (FTE):** 2-4 FTE
- **Total Costs:** 200,000 USD

The plan is to use this grant to finish the platform (blockchain + security), create brand awareness, build the team, launch the platform and further develop/improve features.  

### Milestone 1 - Balancer protocol customization and integration with application via TrustEVM

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | Smart Contracts | The Balancer protocol will be forked and the contracts will be customized for the Fundle platform. This part of the application will be open source. |
| 0b. | Documentation | We will provide **inline documentation** of the code. |
| 0c. | Testing | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests for the customized contracts. |
| 1. | TrustEVM application integration | We will integrate Trust EVM with our Laravel application with the following web3 php client: https://github.com/web3p/web3.php. |  
| 2. | Payment integration | Users can join communities bij sending USDC/USDT. They have 2 options to pay: connect their own wallet (Metamask, wallet connect, coinbase wallet etc.) or with fiat gateways (for ex. Moonpay, mercuryo). This part covers steps for the necessary payment architecture of the system including deployment on TrustEVM.  |
| 3. | Application security audit | The application will be audited on security vulnerabilities. |

- **Estimated Duration:** 2-4 months
- **FTE:**  3-4
- **Costs:** 120,000 USD

### Milestone 2 - Marketing/Sales & Application development
We made a plan with our marketing advisor about the go to market strategy! This includes total costs for the promotion of the platform and hiring of working students as (digital) marketer/communication and business developer/sales. 

With this team we can create brand awareness. We will create a network of publicity around the Fundle platform which ensures that lots of different people will get to know Fundle. The plan is to finetune the product first in the Netherlands. After that we will move with our promotion to Germany, United Kingdom and France since these countries have the highest transaction value in Europe for crowdfunding. The big market (and most potential customers) are based in the United States. When the product has been finetuned we want to move our marketing strategy there.    

The focus will be on:
- Businesses with an established existing community. Their problem is that active and intensive participation, involvement and engagement remains difficult. Therefore they want to have more interaction to gain more (value) out of their community or offer new customer experiences. These are often innovative companies who did for example a NFT launch already. 

- New businesses/startups. They experience that building, growing and managing communities is challenging and forms a barrier. A characteristic of them can be that they did a crowdfunding and are familiar with the added value of community building. 

On the application side we will improve our features so that users can have more interaction (so more transactions on the EOS Blockchain) and better experiences. See "Future Plans" for the plans we have! 

- **Estimated Duration:** 12 months
- **FTE:**  2-4
- **Costs:** 80,000 USD


## Future Plans

We see many expansion options for the Fundle platform and we will stay commited to it. We really believe in full tokenization and digital economies. In the coming years we will slowly move towards the adoption of digital economies. The roadmap can be found at:  https://wefundle.com/roadmap

## Additional Information

**How did you hear about the Grants Program?** Recommendation from Zaisan

