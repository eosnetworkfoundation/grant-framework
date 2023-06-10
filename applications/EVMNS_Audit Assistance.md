
# EOS Network Foundation Grant Proposal
-   **Project Name:** Security Audit Assistance for EVMNS
-   **Team Name:** EVMNS Labs
-   **EOS Payment Address:** evmnsdomains
-   **Level:** 2
-   **Pomelo Grant(s):** https://pomelo.io/grants/evmns
-   **Project is Open-Source:** Yes
-   **Project was part of Token sale:** No
-   **Repository where Project resides:** https://github.com/evmns/EVMNS

# Contact
- **Contact Name:** Harry Davis
- **Contact Email:** evmns_manager@outlook.com
- **Website:** https://evmns.space/

# Project Overview
**EVMNS (EOS EVM Name Service) is a distributed, open and extensible multi-chain DID domain naming system built on EOS EVM,** relying on the high performance, security and reliability of EOS to better and seamlessly connect people, information, assets, dApps, etc. in the WEB3 world.<br/><br/>
EVMNS domains use the ERC721 protocol standard with .evm as the domain suffix, such as abc.evm, 123.evm, jack.evm, etc., to map human-readable and easy-to-remember names with all kinds of content at the same time, including but not limited to EVM addresses, EOS addresses, other cryptocurrency addresses, content hashes, URLs, and metadata.<br/><br/>
### Overview
- **Name:** EVMNS (EOS EVM Name Service)<br/>
- **Brief Description:** A distributed, open and extensible multi-chain DID domain naming system built on EOS EVM.<br/>
- **Relationship to EOSIO:** EVMNS's multi-chain layout will bring more new users to EOS EVM, because it helps users of other chains to know and understand EOS EVM, and to enjoy the unique advantages of EOS EVM (industry-leading transaction speeds, high TPS and low transaction cost), and help EOS EVM to expand its positive influence in the WEB3 world.<br/>
- **Reason for Interest:** WEB3 trend is developing rapidly, a set of DID domain naming system with perfect function, multi-chain layout and good user experience is the "identity infrastructure" of WEB3 application, and it can be confirmed that DID is like an avatar, which is the basic and essential element and the identity of WEB3 world.<br/><br/>

# Application Description
The development work for EVMNS has been mostly completed, and We are currently conducting in-depth internal testing and debugging. We believe that the service will be officially launched shortly, and we are excited to share EVMNS with the community.<br/><br/>
Before the official release, we need to conduct a comprehensive security audit of the smart contract to ensure that there are no security issues. **However, due to the greater complexity and larger code volume of the smart contract than our team had anticipated, the corresponding security audit costs have exceeded our budget by a significant amount, making it an enormous burden for us, even to the point of being unbearable.**<br/><br/>
Therefore, we sincerely request assistance from the EOS Network Foundation to help us complete this important security audit work.<br/><br/>
More details are as follows:<br/><br/>
1. Overview of Smart Contract Functions<br/>
**Domain Registration:** Users can register unique domain names on EVMNS.<br/>
**Domain Management:** Users can manage their registered domain names, such as changing the profile of the domain, changing the resolver, or modifying the TLS certificate.<br/>
**Domain Transfer:** Users can transfer their registered domain names to others.<br/>
**Resolver Registration:** Users can select a resolver to resolve the domain name, and different resolvers support different domain name functions.<br/>
**Domain Resolution:** Users/third-party dApps can query the profile content of EVMNS domain names, such as whether an EVMNS domain name is associated with an EOS EVM address.<br/>

2. Total lines of code in smart contract: about **9300 lines.**<br/>

3. Smart Contract Code repository: https://github.com/evmns/evmns-contracts<br/>

4. **If not audited, potential security risks may include, but are not limited to:** Mass registration of domain names, even those that are not yet open for registration; Control of domain name permissions, which may result in inability to manage or transfer domains; Domain name hijacking, which may result in inability to resolve to the correct wallet address, affecting users' transfer and payment activities.<br/>

5. EOS Network Foundation funding proposal for EVMNS: https://github.com/eosnetworkfoundation/grant-framework/pull/106<br/>
   
# Team
### Team members
- **Team Leader: Harry Davis**<br/>
- Allen Harris<br/>
- Frank Lee <br/>
### Legal Structure
- **Registered Legal Entity:** Jump Dream PTE. LTD.<br/>
- **Registered Address:** 5001 Beach Road#07-37, Golden Mile Complex, Singapore 199588<br/>
### Team Experience
The core members of EVMNS Labs are the first ecological participants of EOS, who experienced and witnessed the launch of EOS and are still deeply involved in the ecological construction.<br/><br/>
Team members have participated in several medium to large scale EOS projects before and after, and also developed ENS (Ethereum Name Service) related domain Exchange, domain bulk registry protocol, etc. We are not only EOS loyalists, but also ENS heavy players, with good understanding of DID domain naming system.<br/>
### Team Member Repos
- Allen Harris, https://github.com/sutaiyi
- Frank Lee, https://github.com/chenminmin4

# Development Roadmap
### Milestone Summary
- **Total Estimated Duration:** 4 weeks
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 30,000 USD

### Milestone 1 - Security audit completed
- **Estimated duration:** 4 weeks
- **FTE:** 2
- **Costs:** 30,000 USD

| ID  | Deliverable  |Specification|
| ------------ | ------------ | ------------ |
| 0a.   |License   | MIT License  |
| 0b.  | Documentation  | Provide and update documentation for this milestone in the form of instruction files and examples in the repository, provide guidance in the Readme file, and more in-depth guidance in our articles.  |
| 0c.  | Testing Guide  | We will clearly state the audit report verification method provided by the security audit company to facilitate the verification of the authenticity of the audit report.  |
| 1  | Audit Report  | After the security company completes the smart contract audit, a comprehensive audit report will be issued.  |<br/><br/>

# Additional Information
### How did you hear about the Grants Program? 
We learned of the program by following announcements on ENF’s Twitter and other channels.<br/>
