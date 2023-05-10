# EOS Network Foundation Grant Proposal

-   **Project Name:** Moonboat NFT Marketplace
-   **Team Name:** Moonboat Team
-   **EOS Payment Address:** moonboatfund
-   **Level:** 2
-   **Pomelo Grant(s):** https://pomelo.io/grants/totoro
-   **Project is Open-Source:** Yes
-   **Project was part of Token sale:** No
-   **Repository where Project resides:** https://github.com/moonboatnft/

## Contact

- **Contact Name:** Hongshu
- **Contact Email:** mailto:team@moonboat.io
- **Website:** https://moonboat.io

## Project Overview

Moonboat(Moonboat NFT Marketplace) is a decentralized, open and extensible NFT Marketplace built on EVM and EOS, relying on the high performance, security and reliability of EOS, bringing rich digital collectibles to EOS and EVM eco-users. Through Moonboat users can easily and quickly create, trade and auction digital collectibles.

### Overview

- **Name:** Moonboat NFT Marketplace
- **Brief Description:** A decentralized, open and extensible NFT Marketplace built on EVM and EOS.
- **Relationship to EOS Network / Antelope:** The NFT marketplace applies EOS underlying and technology to provide EOS and EVM users with an NFT platform that integrates creation, trading, and auction, and the project code will be open source for contribution to EOSIO repository.
- **Reason for Interest:** NFTs are the future of digital asset ownership. NFT trading volume has grown from USD 82 million 2020 to USD 2.5 billion in 2021, and USD 55.5 billion in 2022. Already, we have seen mainstream artists launch NFT projects, major brands enter the space, and existing decentralized finance (DeFi) projects making NFTs a core part of their offering - and we’re just getting started. EOS has the edge in the NFT blockchain with powerful and fast data processing capabilities. However, this market is not fully exploited at the moment, both in EOS and EVM. With our team's rich project experience and strong technical capabilities, we will deepen the NFT marketplace on EOS, and make EOS as great as it is in the NFT market.

### Project Details

- The development of our project on EOS has been completed, and the development on EVM is early on its process, and will eventually sync the update to the EOS version.
- The frontend of our project is developed using Vue3+ant-design. Our goal is to use the same platform to connect the data of both chains, which will integrate eosjs and web3.js related code, and access different wallets to achieve this, such as Metamask, Anchor and Metahub.
- The backend of our project uses the eggjs framework to achieve rapid development. The backend mainly implements NFT data storage and management, and provides interfaces for the frontend to display, search and other operations.
- Contracts on EOS: We develop a complete onchain order system that keeps all orders on the chain, making transactions more decentralized and reliable.
- Contracts on EVM: We use the Seaport protocol which used by OpenSea. Compared with the Wyvern protocol, it is more friendly to developers and saves gas fees, and is also compatible with the Wyvern protocol, which is also convenient for further crosschain in the future.
- We customized an EOS NFT standard that combines the features of ERC721 and ERC777 and is specifically adapted to the EOS network.
- We setup an EOS node and enabled the state-history plugin, and we used Golang to develop an efficient EOS logging application that receives state-history binary data and quickly deserializes it and stores the data in a queue for the backend.
- We will use Gloang to develop a logging middleware for EVM that will use SyncProgress to synchronize EVM logs and store the data in a queue, and the business service will process the data through the consumer.
- In most cases, the number of NFTs will be very large, and we will have the relevant backend services to handle summarizing this data and save it into elasticsearch so that users can quickly retrieve NFT assets by tags and types.

### Ecosystem Fit

Q: Where and how does your project fit into the ecosystem?
A: Our project will be lanuched on EOS and EVM chains, and users can use the product through their PC or mobile wallets.

Q: Who is your target audience?
A:  EOS and EVM users, dapp and gamefi developers, artists, collectors.

Q: What need(s) does your project meet?
A: To provide a NFT platform for users to create, trade, and auction digital works to circulate on EOS and EVM.

Q: Are there any other projects similar to yours in the EOSIO ecosystem?
A: There is AtomicHub in the EOS ecosystem, no similar project in the EVM at this time.

Q: If so, how is your project different?
A: As of now AtomicHub mainly serves WAX and does not have much transactions on EOS. AtomicHub's NFT standard is a private protocol, which is very unfriendly to developers, developers have no ownership of the NFT contract and must publish data to AtomicHub's protocol, lacking sufficient flexibility. In contrast, the Moonboat protocol is simple enough and Moonboat only makes the protocol, the developer has ownership of the NFT contract, and there is enough flexibility for development.
And in EVM, we will be the first marketplace. We will work with the EVM team to bring in game projects and guide them to create NFTs on Moonboat marketplace, bringing greater richness to the EVM ecosystem.

## Team

### Team members

- **Team Leader:** Hongshu, one of the most experienced blockchain developers
- Ryuuichi, Backend Developer
- Leek, Frontend Developer
- Oanhere, Frontend Developer
- Lita, UI Designer
- Lio, Operation Manager

### Legal Structure

- **Registered Legal Entity:** N/A
- **Registered Address:** N/A 
- **Note::** We have sent the information to grants@eosnetwork.com

### Team Experience

The core members of Moonboat Team are the first ecological participants of EOS, who experienced and witnessed the launch of EOS and are still deeply involved in the ecological construction.

Team members have participated in several medium to large scale EOS projects before and after, Some of the members are core developers of the original Newdex, involved in the core code development of Newdex, Newpool, Defixbox and other projects, team members developed the Totoro project for experimental purposes and have participated in Pomelo's grant at https://pomelo.io/grants/totoro  
The team members also participated in the initial development of the NFT Marketplace project Treasureland which became the largest NFT Marketplace on BSC in the early days.  
The team also has dedicated operations staff with rich experience in Defi and NFT project operations, operating the largest project with over 10,000 users.  

### Team Org Repos

- Moonboat, https://github.com/moonboatnft
- Totoro, https://github.com/totorofinance

### Team Member Repos

- Hongshu, https://github.com/hongshu7
- Ryuuichi, https://github.com/ryuuichi01
- Leek, https://github.com/carrotlsp
- Oanhere, https://github.com/oanhere

## Development Status

We have a fully functional decentralized NFT marketplace working on EOS, address: https://moonboat.io. The EVM version we have completed the initial architecture and is currently under development.

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:**6 weeks
- **Full-Time Equivalent (FTE):** 6 FTE
- **Total Costs:** 49,000 USD

### Milestone 1 — Minimum Viable Product Development

- **Estimated Duration:** 6 weeks
- **FTE:** 6
- **Costs:** 49,000 USD

| # | Deliverables | Details |
| --- | --- | --- |
| 0a. | License | MIT license |
| 0b. | Documentation | Provide and update documentation for this milestone, in the form of a guide and example in the repository, guidance on how to run the tests in the README file, and provide a more in-depth introduction in our articles. |
| 0c. | Testing Guidelines | The functionality for this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the README file. |
| 1. | Core Contract Development: 10,000 USD | We will develop smart contracts based on the Seaport protocol and modify them to fit our needs. |
| 2. | Contract Audit: 14,000 USD | We will conduct a security audit of the core code, and if any issues are found, we will make modifications and conduct a re-audit. |
| 3. | Contract Deployment | We will deploy contracts on both the EVM testnet and mainnet. |
| 4. | UI Design: 2,000 USD | The designer will complete the frontend UI design work based on the requirements document. |
| 5. | Logging Middleware: 3,000 USD | We will use Gloang to develop a logging middleware that will receive EVM logs and store them in a queue, which will be processed by a consumer for data processing. |
| 6. | Data Search System: 3,000 USD | We will analyze the data and store it in Elasticsearch in a classified manner for the system to perform various dimensional searches conveniently. |
| 7. | Market Management System: 3,000 USD | Develop a backend system for managing NFT-related collections and artworks to meet operational requirements. |
| 8. | API Interface: 3,000 USD | Connect the frontend and backend by developing corresponding data interfaces. |
| 9. | Frontend Development: 5,000 USD | Develop the frontend interface based on UI design, improve functions, and connect with wallets. |
| 10. | Servers: 6,000 USD | Four high-performance frontend and backend servers, and MySQL, Redis, Elasticsearch. |

### Milestone 2 - Function Upgrade

- **Estimated Duration:** 12 weeks
- **FTE:** 12
- **Costs:** 100,000 USD (not included in this grant)

| No. | Deliverables | Details |
| --- | --- | --- |
| 1. | More Blockchain Networks | In addition to EOS and EVM networks, more blockchain networks can be supported, such as BSC and Polygon. This can expand the user base of the platform. |
| 2. | More Types of Digital Assets | Currently, the platform only supports NFTs, but other types of digital assets can be considered, such as FT (fungible token) and other types of digital securities. |
| 3. | Enhancement of Social Functions | In addition to trading and auction functions, social functions can be added, such as personal pages, community forums, and social sharing. This can increase user stickiness and the social effect of the platform. |
| 4. | Better User Experience | The platform's UI/UX can be optimized, with more features added such as search, filter, and sort functions, making it easier for users to find the digital assets they want. |
| 5. | Market Data Analysis and Reports | By collecting and analyzing transaction data, more market analysis and reports can be provided to users, such as NFT market trends, most popular digital assets, and average prices. This can help users make wiser investment decisions. |

### Milestone 3 - Platform Operation Numbers

- **Estimated Duration:** 24 weeks
- **FTE:** 24
- **Costs:** 60,000 USD (not included in this grant)

| No. | Deliverables | Details |
| --- | --- | --- |
| 1. | Increase in User Base | Monthly new users reach 1,000. |
| 2. | Cumulative Transaction Volume | Reaching 10,000 NFTs. |
| 3. | Monthly Active Users | Exceeding 5,000 users. |
| 4. | Popular Albums | Establishing partnerships with important artists, creators, and brands. |

## Market Operations

*   Community building: Building an active community is crucial, which can be achieved by constantly promoting the market, interacting and communicating with users, and organizing a series of events. The platform can interact with users through social media, Telegram, WeChat, and other social channels, allowing users to share and promote their NFT works, interact and communicate with other users, which can help increase user stickiness and retention rate.
    
*   Promotional activities: The platform can regularly hold promotional activities, such as raffles, competitions, NFT art exhibitions, and thematic lectures, to attract more users to join and use the platform. These activities can be organized in collaboration with the platform's partners, artists, NFT enthusiasts, and other relevant parties, thus increasing the platform's visibility and attractiveness.
    
*   Continuous technological upgrades: Technological upgrades and updates can help the platform maintain competitiveness and attractiveness. Moonboat platform can consider introducing new technologies, features, and services to meet the constantly changing market and user demands.
    
*   Security and guarantee: In blockchain transactions, security and guarantee are very important factors. Moonboat platform should take a series of security measures, such as strengthening user identity verification, multi-signature, smart contract auditing, and risk control, to ensure the safety of user assets and platform security stability.
    
*   Expanding partnerships: Moonboat platform can consider cooperating with other NFT platforms, digital currency exchanges, and relevant organizations to expand the platform's influence and user base. The platform can provide users with more choices and transaction channels, thus attracting more users and transaction volume.
    
*   Data analysis and marketing strategies: The platform can understand user needs and market trends through data analysis and market research, in order to formulate more targeted marketing strategies and business plans. The platform can use various marketing methods, such as SEO optimization, social media marketing, advertising, and content marketing, to improve brand awareness and user conversion rate.

# Chinese Translation 中文翻译

- **项目名称:** Moonboat NFT 交易市场
- **团队名称:** Moonboat 团队
- **支付地址:** moonboatfund
- **等级:** 2
- **Pomelo资助:** https://pomelo.io/grants/totoro
- **项目是否开源:** 是
- **项目是代币销售的一部分:** 否
- **项目开源库:** https://github.com/moonboatnft/

## 联系人

- **联系名称:** Hongshu
- **联系邮件:** team@moonboat.io
- **网站地址:** https://moonboat.io

## 项目概述

Moonboat(Moonboat NFT Marketplace)是一个去中心化、开放且可扩展的NFT交易平台，建立在EVM和EOS的技术基础上。我们对项目充满信心，致力于为EOS及EVM用户带来丰富的数字藏品，并提供方便快捷的创造、交易、拍卖功能。

### 概述

- **名称:** Moonboat NFT交易所
- **简介:** 一个建立在EVM和EOS技术基础上的去中心化、开放的、可扩展的NFT交易平台。
- **与EOSIO的关系:** Moonboat交易所应用EOS底层技术，为EOS和EVM用户提供一个集创造、交易、拍卖为一体的NFT平台，项目代码将开源，丰富EOSIO代码资源库。
- **感兴趣的原因:** NFT是数字资产所有权的未来，交易总量已迅速增长，EOS在NFT区块链中占据优势。但目前无论在EOS还是EVM，这个市场并未被充分发掘。Moonboat拥有丰富的项目经验和强大的技术能力，在EOS上深耕NFT市场，让EOS在NFT市场成为一股不可忽视的力量。

### 项目详细

- Moonboat前端使用Vue3和ant-design开发，目标是通过同一个平台打通两条链的数据，集成eosjs和web3.js相关代码，并接入不同的钱包，如Metamask、Anchor和Metahub等钱包。
- 后端采用eggjs框架快速开发，主要实现NFT数据的储存和管理，并为前端提供展示、搜索和其它操作的接口。
- EOS端的合约：开发完整的链上订单系统，将所有订单保存在链上，使得交易更加去中心化和可靠。
- EVM端的合约：采用Seaport协议，对开发者更友好，省gas费用，同时也兼容Wyvern协议，方便未来的跨链。
- 定制EOS的NFT标准，综合了ERC721和ERC777的特点，特别适配于EOS网络。
- 搭设EOS节点并开启state-history插件，使用Golang开发高效的EOS日志处理应用，接收state-history的二进制数据，反序列化并将其存入队列，供后端使用。
- 使用Golang开发EVM的日志中间件，使用SyncProgress同步EVM日志并将数据存储到队列，业务服务通过消费者处理这些数据。
- 由于NFT的数量可能非常庞大，相关的后台服务将归纳这些数据，并将其存入elasticsearch，这样用户可以通过标签和类型。
- 作为项目方，我们对Moonboat充满信心，致力于为用户提供优质的NFT交易平台。

### 生态系统适应性

Q: 您的项目在哪里以及如何融入生态系统?
A: 我们的项目会发布在EOS以及EVM链上，用户通过PC或者手机钱包即可使用产品。

Q: 谁是你的目标受众（链/dapp/钱包/UI 开发人员、设计师、你自己的用户群、一些 dapp 的用户群、你自己）？
A: EOS以及EVM用户、dapp及链游的开发者、艺术家、收藏家。
    
Q: 您的项目满足什么需求？
A: 为用户提供一个集创造、交易、拍卖为一体的NFT平台，让数字作品在EOS和EVM上流通起来。
    
Q: 在EOSIO生态系统中还有其他类似的项目吗？
A：在EOS生态中有AtomicHub，在EVM目前还没有。
    
Q: 如果是这样，您的项目有何不同？
A: 目前来看AtomicHub主要是服务于WAX，在EOS上并没有太大的交易量，AtomicHub的NFT标准是私有协议，对于开发者非常不友好，开发者对NFT的合约没有拥有权，必须将数据发布到AtomicHub的协议中，缺少足够的灵活性。而Moonboat协议足够简单，并且Moonboat只制定协议，开发者对合约有所有权，对开发有足够的灵活性。
而在EVM，我们将会是第一个Marketplace，我们将会与EVM团队合作，引入游戏项目方并将NFT上线到Moonboat，为EVM生态带来更大的丰富性。

## 团队

### 团队成员

- **负责人:** Hongshu, 最有经验的区块块开发者之一
- Ryuuichi, 后端开发
- Leek, 前端开发
- Oanhere, 前端开发
- Lita, UI设计师
- Lio, 运营经理

**法律结构**

-   **注册法律实体：** N/A 
-   **注册地址：** N/A
-   **备注：** 我们已信息发送到grants@eosnetwork.com

### 团队经验

Moonboat团队的核心成员是EOS的第一批生态参与者，他们经历并见证了EOS的上线，目前仍在深度参与生态建设。
团队成员前后参与了多个大中型的EOS项目，部分成员是原Newdex的核心开发人员，参与了Newdex、Newpool、Defixbox等项目的核心代码开发、团队成员以试验目的开发了Totoro项目并参与过Pomelo的grant，地址为：https://pomelo.io/grants/totoro
团队人员还参与BSC上NFT Marketplace项目Treasureland的初始开发，并在初期成为BSC上最大的NFT Marketplace。 
同时团队还有专门的运营人员，有丰富的Defi及NFT项目运营经验，运营的最大项目用户数超过10000人。

### 团队组织 Repos

- Moonboat, https://github.com/moonboatnft
- Totoro, https://github.com/totorofinance

### 团队成员 Repos

- Hongshu, https://github.com/hongshu7
- Ryuuichi, https://github.com/ryuuichi01
- Leek, https://github.com/carrotlsp
- Oanhere, https://github.com/oanhere

## 开发状态

我们有一个功能齐全的去中心化NFT市场部署在EOS上，地址是：https://moonboat.io
EVM版本我们已经完成了初始架构，目前正在开发中。

## 开发路线图

### 里程碑总结

- **总共周期:** 6 周
- **全职当量 (FTE):** 6 FTE
- **总计花费:** 49,000 USD

### 里程碑1 — 最简化可实行产品开发

- **预估周期:** 6 周
- **FTE:**  6
- **花费:** 49,000 USD

| 序号 | 可交付成果 | 明细 |
| -----: | ----------- | ------------- |
| 0a. | 许可 | MIT license |
| 0b. | 文档 | 为这一里程碑提供并更新文件，其形式为指导文件和仓库中的示例，在自述文件中提供指导，并在我们的文章中提供更深入的介绍。 |
| 0c. | 测试指导 | 这个里程碑的功能可以通过运行我们提供的单元测试来测试，在自述文件中提供了如何运行这些测试的指导。 |
| 1. | 核心合约开发: 10,000 USD| 我们将在Seaport协议的基础上开发智能合约，并修改以适配我们的需求。  |  
| 2. | 合约审计: 14,000 USD| 我们将对核心代码进行安全审计，如果存在问题将进行修改并重新审计。 |  
| 3. | 部署合约 | 我们将在EVM测试网以及主网上分别部署合约。 |  
| 4. | UI设计: 2,000 USD	| 设计师根据需求文件完成前端UI设计工作。 | 
| 5. | 日志中间件: 3,000 USD | 我们将使用Gloang开发一个日志中间件来接收EVM日志，并将日志存储在一个队列中，业务服务将通过消费者处理数据。 |  
| 6. | 数据搜索系统: 3,000 USD | 我们将数据进行后台分析并归类存储到elasticsearch中，方便系统进行各种维度的检索。 |  
| 7. | 市场管理系统: 3,000 USD | 开发一个后台系统，用于管理与NFT相关的收藏品、艺术品，并满足运营要求。 |  
| 8. | API接口: 3,000 USD | 对接前端，开发相应的数据接口，以连接前端和后端。 |  
| 9. | 前端开发: 5,000 USD | 通过UI设计来开发前台界面，完善功能，并对接钱包。 |  
| 10. | 服务器: 6,000 USD | 4台高性能前端后端服务器，以及Mysql，Redis，ElasticSearch。 |

### 里程碑2 — 功能升级

- **预估周期:** 12 周
- **FTE:**  12
- **花费:** 100,000 USD (不在此次grant内)

| 序号 | 可交付成果 | 明细 |
| -----: | ----------- | ------------- |
| 1. | 更多区块链网络 | 除了EOS和EVM网络之外，可以考虑支持更多的区块链网络，例如BSC、Polygon等。这样可以扩大平台的用户群体。 |  
| 2. | 更多的数字资产类型 | 目前平台仅支持NFT，但是可以考虑增加其他类型的数字资产，例如FT（fungible token）和其他类型的数字证券。 |  
| 3. | 社交功能的增强 | 除了交易和拍卖功能之外，可以增加社交功能，例如个人主页、社区论坛、社交分享等。这可以提高用户粘性和平台的社交效应。 |  
| 4. | 更好的用户体验 | 可以优化平台的UI/UX，增加更多的功能，例如搜索、筛选、排序等，使用户可以更方便地找到他们想要的数字资产。 |  
| 5. | 市场数据分析和报告 | 过收集和分析交易数据，可以为用户提供更多的市场分析和报告，例如NFT市场趋势、最受欢迎的数字资产、平均价格等。这可以帮助用户做出更明智的投资决策。 |  

### 里程碑3 — 平台运营数

- **预估周期:** 24 周
- **FTE:**  24
- **花费:** 60,000 USD (不在此次grant内)

| 序号 | 可交付成果 | 明细 |
| -----: | ----------- | ------------- |
| 1. | 用户新增量 | 月新增量达到1,000人。 |  
| 2. | 累计交易量 | 达到10,000枚NFT。 |  
| 3. | 月活跃用户数 | 突破5,000人。 |  
| 4. | 热门专辑 | 与重要艺术家、创作者和品牌建立合作关系。 | 


## 市场运营

- 社区建设：建立一个活跃的社区是至关重要的，这可以通过不断地进行市场推广、与用户进行互动和交流以及举办一系列活动来实现。平台可以通过社交媒体、电报、微信和其他社交渠道来与用户互动，让用户分享和推广自己的NFT作品，与其他用户互动和交流，这可以帮助平台增加用户粘性和留存率。

- 推广活动：平台可以定期举办推广活动，例如抽奖、比赛、NFT艺术品展览和专题讲座等，以吸引更多的用户加入并使用平台。这些活动可以与平台的合作伙伴、艺术家、NFT爱好者和其他相关方合作举办，从而增加平台的知名度和吸引力。

- 持续的技术升级：平台的技术升级和更新可以帮助平台保持竞争力和吸引力。Moonboat平台可以考虑引入新的技术、功能和服务，以满足不断变化的市场需求和用户需求。

- 安全和保障：在区块链交易中，安全和保障是非常重要的因素。Moonboat平台应该采取一系列的安全措施，如加强用户身份验证、多重签名、智能合约审计和风险控制等，以保障用户的资产安全和平台的安全稳定。

- 拓展合作伙伴：Moonboat平台可以考虑与其他NFT平台、数字货币交易所和相关机构进行合作，以拓展平台的影响力和用户基础。平台可以为用户提供更多的选择和交易渠道，从而吸引更多的用户和交易量。

- 数据分析和营销策略：平台可以通过数据分析和市场调查来了解用户需求和市场趋势，以制定更有针对性的营销策略和业务方案。平台可以采用各种营销手段，如SEO优化、社交媒体营销、广告投放和内容营销等，以提高品牌知名度和用户转化率。
