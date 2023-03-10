# EOS Network Foundation Grant Proposal
-   **Project Name:** Moonboat NFT Marketplace
-   **Team Name:** Moonboat Team
-   **EOS Payment Address:** moonboatfund
-   **Level:** 3
-   **Pomelo Grant(s):** N/A
-   **Project is Open-Source:** Yes
-   **Project was part of Token sale:** No
-   **Repository where Project resides:** https://github.com/moonboatnft/evm-contracts

## Contact

- **Contact Name:** Hongshu
- **Contact Email:** team@moonboat.io
- **Website:** https://moonboat.io

## Project Overview

Moonboat(Moonboat NFT Marketplace) is a decentralized, open and extensible NFT Marketplace built on EVM and EOS, relying on the high performance, security and reliability of EOS, bringing rich digital collectibles to EOS and EVM eco-users. Through Moonboat users can easily and quickly create, trade and auction digital collectibles.

### Overview

- **Name:** Moonboat NFT Marketplace
- **Brief Description:** a decentralized, open and extensible NFT Marketplace built on EVM and EOS.
- **Relationship to EOSIO:** The NFT marketplace applies EOS underlying and technology to provide EOS and EVM users with an NFT platform that integrates creation, trading, and auction, and the project code will be open source for contribution to EOSIO repository.
- **Reason for Interest:** NFTs are the future of digital asset ownership. NFT trading volume has grown from USD 82 million 2020 to USD 2.5 billion in 2021, and USD 55.5 billion in 2022. Already, we have seen mainstream artists launch NFT projects, major brands enter the space, and existing decentralized finance (DeFi) projects making NFTs a core part of their offering - and we’re just getting started. EOS has the edge in the NFT blockchain with powerful and fast data processing capabilities. However, this market is not fully exploited at the moment, both in EOS and EVM. With our team's rich project experience and strong technical capabilities, we will deepen the NFT marketplace on EOS, and make EOS as great as it is in the NFT market.

### Project Details

The development of our project on EOS has been completed, and the development on EVM is early on its process, and will eventually sync the update to the EOS version.
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

- **Team Leader:** Hongshu, One of the most experienced blockchain developers
- Ryuuichi, Backend developer
- Leek, Frontend developer
- Oanhere, Frontend developer
- Lita, UI designer

### Legal Structure
- **Registered Legal Entity:** We are in the initial process of registration
- **Registered Address:** N/A

### Team Experience

The core members of Moonboat Team are the first ecological participants of EOS, who experienced and witnessed the launch of EOS and are still deeply involved in the ecological construction.

Team members have participated in several medium to large scale EOS projects before and after, Some of the members are core developers of the original Newdex, involved in the core code development of Newdex, Newpool, Defixbox and other projects, team members developed the Totoro project for experimental purposes and have participated in Pomelo's grant at https://pomelo.io/grants/totoro
The team also participated in the initial development of the NFT Marketplace project treasureland on BSC, which became the largest NFT Marketplace on BSC in terms of trading volume in the early days.

### Team Org Repos

- Moonboat, https://github.com/moonboatnft
- Totoro, https://github.com/totorofinance

### Team Member Repos

- Hongshu, https://github.com/hongshu7
- Ryuuichi, https://github.com/ryuuichi01
- Leek, https://github.com/carrotlsp
- Oanhere, https://github.com/oanhere

## Development Status

We have a fully functional decentralized NFT marketplace working on EOS, address: https://moonboat.io
The EVM version we have completed the initial architecture and is currently under development.

## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 12 weeks
- **Full-Time Equivalent (FTE):** 6 FTE
- **Total Costs:** 190,000 USD

### Milestone 1 —  Requirements Analysis and UI design

- **Estimated duration:** 2 weeks
- **FTE:**  2
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT license |
| 0b. | Documentation | Provide project planning documents, Introduce users to our development system process. |
| 1. | Demand Analysis	| Unpacking requirements, developing business process diagrams, planning business modules, standardizing development documentation and testing processes, etc.|  
| 2. | UI design	| Designers complete frontend UI design work based on requirement documents.|  

### Milestone 2 — Smart Contracts

- **Estimated Duration:** 2 weeks
- **FTE:**  2
- **Costs:** 50,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT license |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles. |
| 0c. | Testing Guide | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file. |
| 1. | Core Contracts | We will develop smart contracts based on the Seaport protocol, modified to suit our needs |  
| 2. | Depoly Contracts | We will depoly contracts on EVM Testnet and Mainnet |  

### Milestone 3 — Frontend Interface and Backend Services

- **Estimated Duration:** 4 weeks
- **FTE:**  4
- **Costs:** 80,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT license |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles. |
| 0c. | Testing Guide | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file. |
| 1. | Logging middleware | We will use Gloang to develop a logging middleware to receive EVM logs and store the logs in a queue, and the business service will process the data through the consumer |  
| 2. | Search system | We analyze and categorize the data in the background and store it in elasticsearch, so that the system can provide various dimensional searches |  
| 3. | Marketplace management system | Develop a backend system for managing NFT-related collections, artworks, and meeting operational requirements |  
| 4. | API Interface | Docking frontend, developing corresponding data interface, connecting frontend and backend |  
| 5. | Frontend development | Develop frontend interface based on UI design, improve features, and dock wallets |  

### Milestone 4 — In-depth testing

- **Estimated Duration:** 2 weeks
- **FTE:**  2
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT license |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles. |
| 0c. | Testing Guide | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file. |
| 1. | In-depth test	 | Automated unit tests with 100% coverage and multiple rounds of functional testing are completed internally to ensure functionality and robustness. |  

### Milestone 5 — Documentation and System launch

- **Estimated Duration:** 2 weeks
- **FTE:**  2
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT license |
| 0b. | Documentation | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles. |
| 0c. | Testing Guide | The functions of this milestone can be tested by running the unit tests we provide, and guidance on how to run these tests is provided in the Readme file. |
| 1. | Development Documentation | Establish a perfect development documentation system to meet and support the quick access of developers. |  
| 2. | Support Documentation | Publish support system and provide detailed support and help documentation for users. |  
| 3. | System launch | After sufficient testing and complete documentation, the system will be officially launched. |  

## Future Plans

- Provide more tools to support game projects and art creators.
- We will build Moonboat DAO, realize community management, and promote the implementation of decentralized operation and R&D of Moonboat.

## Additional Information

**How did you hear about the Grants Program?** 
We hear about the grants program by following ENF’s Twitter and telegram channels.

---

# Chinese Translation 中文翻译

- **项目名称:** Moonboat NFT 交易市场
- **团队名称:** Moonboat 团队
- **支付地址:** moonboatfund
- **等级:** 3
- **Pomelo资助:** 无
- **项目是否开源:** 是
- **项目是代币销售的一部分:** 否
- **项目开源库:** https://github.com/moonboatnft/evm-contracts

## 联系人

- **联系名称:** Hongshu
- **联系邮件:** team@moonboat.io
- **网站地址:** https://moonboat.io

## 项目概述

Moonboat(Moonboat NFT Marketplace)是一个去中心化的、开放的、可扩展的NFT交易平台，建立在EVM和EOS的基础上，依靠EOS的高性能、安全性和可靠性，将丰富的数字藏品带给EOS及EVM生态用户，通过Moonboat用户可以方便快捷的创造、交易、拍卖数字藏品。

### 概述

- **名称:** Moonboat NFT交易所
- **简介:** 一个建立在EVM和EOS技术基础上的去中心化的、开放的、可扩展的NFT交易平台。
- **与EOSIO的关系:** NFT交易所应用了EOS底层及技术，为EOS及EVM用户提供一个集创造、交易、拍卖为一体的NFT平台，项目代码将开源，这将丰富EOSIO代码资源库。
- **感兴趣的原因:** NFT是数字资产所有权的未来。NFT交易总量已经从2020年上半年的8200万美元上涨到2021的176亿美元，2022年更是达到555亿美元。并且我们仅仅发掘了NFT市场表面的一部分。现在，我们看到主流艺术家启动NFT项目，大品牌进入这个领域，现有的Defi项目将NFT作为他们产品的核心部分，而我们才刚刚开始。EOS在NFT区块链中占据优势，拥有强大和快速的数据处理能力。但目前无论在EOS还是EVM，这个市场并没被充分发挥，我们凭借我们团队丰富的项目经验和强大的技术能力，将在EOS上深耕NFT市场，让EOS在NFT市场成为一股不忽视的力量。

### 项目详细

- 我们的项目前端使用Vue3+ant-design开发，我们的目标是使用同一个平台打通两条链的数据，这将集成eosjs和web3.js相关代码，并接入不同的钱包来实现，如Metamask、Anchor以及Metahub等钱包
- 后端采用eggjs框架实现快速的开发，后端主要实现NFT的数据储存和管理，并为前端提供展示、搜索和其它操作的接口。
- EOS端的合约：我们开发一个完整的链上订单系统，将所有订单都保存在链上，使得交易更加去中化以及更加的可靠。
- EVM端的合约：我们交采用的是Seaport协议，这也是OpenSea采用的协议，相比Wyvern协议，它对开发者更友好，还更省gas费用，同时也能兼容Wyvern协议，也方便未来的进一步跨链。
- 我们定制了一个EOS的NFT标准，综合了ERC721和ERC777的特点，特别适配于EOS网络。
- 我们搭设了一台EOS节点并开启了state-history插件，同时我们使用Golang开发一个高效的EOS的日志处理应用，用于接收state-history的二进制数据并快速的将它反序列化并数据存入队列以代后端使用。
- 我们将会使用Gloang开发一个EVM的日志中间件，它将使用SyncProgress来同步EVM日志并将数据存储到队列，业务服务通过消费者去处理这些数据。
- 大部分情况下，NFT的数量会非常庞大，我们会有相关的后台服务去处理归纳这些数据，并将它存入到elasticsearch，这样用户就可以通过标签和类型快速的检索NFT资产了。

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

**法律结构**

-   **注册法律实体：** 我们正在进行初步的注册程序
-   **注册地址：** N/A

### 团队经验

Moonboat团队的核心成员是EOS的第一批生态参与者，他们经历并见证了EOS的上线，目前仍在深度参与生态建设。
团队成员前后参与了多个大中型的EOS项目，部分成员是原Newdex的核心开发人员，参与了Newdex、Newpool、Defixbox等项目的核心代码开发、团队成员以试验目的开发了Totoro项目并参与过Pomelo的grant，地址为：https://pomelo.io/grants/totoro
团队人员还参与BSC上NFT Marketplace项目Treasureland的初始开发，并在初期成为BSC上最在的NFT Marketplace。

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

- **总共周期:** 12 周
- **全职当量 (FTE):** 6 FTE
- **总计花费:** 190,000 USD

### 里程碑1 — 需求分析和UI设计

- **预估周期:** 2 周
- **FTE:**  2
- **花费:** 20,000 USD

| 序号 | 可交付成果 | 明细 |
| -----: | ----------- | ------------- |
| 0a. | 许可 | MIT license |
| 0b. | 文档 | 提供项目规划文件，向用户介绍我们的开发系统流程。 |
| 1. | 需求分析	| 解读需求，制定业务流程图，规划业务模块，规范开发文档和测试流程等。 |  
| 2. | UI设计	| 设计师根据需求文件完成前端UI设计工作。 |  

### 里程碑2 — 智能合约

- **预估周期:** 2 周
- **FTE:**  2
- **花费:** 50,000 USD

| 序号 | 可交付成果 | 明细 |
| -----: | ----------- | ------------- |
| 0a. | 许可 | MIT license |
| 0b. | 文档 | 为这一里程碑提供并更新文件，其形式为指导文件和仓库中的示例，在自述文件中提供指导，并在我们的文章中提供更深入的介绍。 |
| 0c. | 测试指导 | 这个里程碑的功能可以通过运行我们提供的单元测试来测试，在自述文件中提供了如何运行这些测试的指导。 |
| 1. | 核心合约开发 | 我们将在Seaport协议的基础上开发智能合约，并修改以适配我们的需求。  |  
| 2. | 部署合约 | 我们将在EVM测试网以及主网上分别部署合约。 |  

### 里程碑3 — 前端界面和后端服务

- **预估周期:** 4 周
- **FTE:**  4
- **花费:** 80,000 USD

| 序号 | 可交付成果 | 明细 |
| -----: | ----------- | ------------- |
| 0a. | 许可 | MIT license |
| 0b. | 文档 | 为这一里程碑提供并更新文件，其形式为指导文件和仓库中的示例，在自述文件中提供指导，并在我们的文章中提供更深入的介绍。 |
| 0c. | 测试指导 | 这个里程碑的功能检查可以通过运行我们提供的单元测试来完成，关于如何运行这些测试的指导在自述文件中提供。 |
| 1. | 日志中间件 | 我们将使用Gloang开发一个日志中间件来接收EVM日志，并将日志存储在一个队列中，业务服务将通过消费者处理数据。 |  
| 2. | 数据搜索系统 | 我们将数据进行后台分析并归类存储到elasticsearch中，方便系统进行各种维度的检索。 |  
| 3. | 市场管理系统 | 开发一个后台系统，用于管理与NFT相关的收藏品、艺术品，并满足运营要求。 |  
| 4. | API接口 | 对接前端，开发相应的数据接口，以连接前端和后端。 |  
| 5. | 前端开发 | 通过UI设计来开发前台界面，完善功能，并对接钱包。 |  

### 里程碑4 — 深度测试

- **预估周期:** 2 周
- **FTE:**  2
- **花费:** 20,000 USD

| 序号 | 可交付成果 | 明细 |
| -----: | ----------- | ------------- |
| 0a. | 许可 | MIT license |
| 0b. | 文档 | 为这一里程碑提供并更新文件，其形式为指导文件和仓库中的示例，在自述文件中提供指导，并在我们的文章中提供更深入的介绍。 |
| 0c. | 测试引导 | 这个里程碑的功能检查可以通过运行我们提供的单元测试来完成，关于如何运行这些测试的指导在自述文件中提供。 |
| 1. | 深度测试	 | 内部完成覆盖率为100%的自动化单元测试和多轮功能测试，以确保功能和稳健性。 |  

### 里程碑5 — 文档编写和系统上线

- **预估周期:** 2 周
- **FTE:**  2
- **花费:** 20,000 USD

| 序号 | 可交付成果 | 明细 |
| -----: | ----------- | ------------- |
| 0a. | 许可 | MIT license |
| 0b. | 文档 | 为这一里程碑提供并更新文件，其形式为指导文件和仓库中的示例，在自述文件中提供指导，并在我们的文章中提供更深入的介绍。 |
| 0c. | 测试引导 | 这个里程碑的功能检查可以通过运行我们提供的单元测试来完成，关于如何运行这些测试的指导在自述文件中提供。 |
| 1. | 开发文档 | 建立完善的开发文档系统，满足开发人员快速访问并提供相应支持。 |  
| 2. | 支持文档 | 发布帮助系统，为用户提供详细的支持和帮助文档。 |  
| 3. | 系统上线 | 经过充分的测试和准备好完备的文档后，系统将正式上线。 |  

## 功能计划

- 为游戏项目和艺术创作者提供更多的工具支持。
- 我们将建立Moonboat DAO，实现社区管理，推动Moonboat DAO实施去中心化运营和研发。

## 附加信息

**你是如何听到资助计划的?** 
我们是通过关注ENF的推特和电报渠道来了解项目的资助。