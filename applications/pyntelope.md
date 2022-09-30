
# EOS Network Foundation Grant Proposal

- **Project Name:** Pyntelope (formerly eospyo)
- **Team Name:** Detroit Ledger Technologies (DLT)
- **EOS Payment Address:** detroitfunds
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels)**: 3
- **Pomelo Grant(s):** [https://pomelo.io/grants/eospyo](https://pomelo.io/grants/eospyo), [https://pomelo.io/grants/nodesuiteimp](https://pomelo.io/grants/nodesuiteimp), [https://pomelo.io/grants/smartcontract](https://pomelo.io/grants/smartcontract)
- **Project is Open-Source**: Yes
- **Project was part of Token sale**: No
- **Repository where Project resides**: [https://github.com/FACINGS/eospyo/tree/main/eospyo](https://github.com/FACINGS/eospyo/tree/main/eospyo)

## Contact

- **Contact Name:** Adam Zientarski
- **Contact Email:** adam@detroitledger.tech
- **Website:** [https://detroitledger.tech/](https://detroitledger.tech/)

## Project Overview

Pyntelope aims to be the most comprehensive, feature-rich, and usable Python blockchain library for Antelope. We believe this will enable significantly faster and easier development of all blockchain applications that require significant backend integration. The speed of the Antelope chains will enable the large-scale adoption of blockchain-backed apps at a fast pace, especially for gaming. Combining the ubiquity of Python with a library interface that enables and encourages rapid development against existing smart contracts is an obvious path to more Antelope developers and thus more apps and more users for Antelope chains.

### Overview

- **Name:** Pyntelope (Pronounced: pin-te-lope)
- **Brief Description:** A Python library that provides easy signing and interface with Antelope blockchains and smart contracts.
- **Relationship to EOSIO:** Detroit Ledger Technologies has been a block producer candidate on the EOS Main chain since its launch date (June 2018) and contributed to the launch of sister chains Telos, WAX & others.
- **Reason for Interest:** The lack of development on EOS for Python and growing gamification resources makes Pyntelope a necessity going forward. Our team and experience combined with the need for an open-source fully featured Python library, that is friendlier to use, makes for a perfect fit.


### Project Details

**Mock-ups/designs of any UI components**

As this is a developer's library in Python most of the functionality is spelled out in the API Specifications section, but for creating libraries dynamically from abi files the interface will be as such.

	pyntelope make-from-abi -destination ./token/eosio.token.abi

Additionally, there’s a tutorial available on medium. [https://detroitledgertech.medium.com/eospyo-tutorial-ff63a0f759ee](https://detroitledgertech.medium.com/eospyo-tutorial-ff63a0f759ee)

We will create appropriate tutorials for each milestone. This will enable us to step immediately into outreach and evangelizing as we reach each milestone.

**Data models of the core functionality**

![Data models](https://drive.google.com/uc?export=view&id=18b86HnaB7CdzSb3veVCaA3KNp3JwxB3V "Data models")
    
**API specifications of the core functionality**

The Following is a list of the class names as named inside the existing library.


- **Action**

	For specifying the smart contract, action, data, and authorization details for a call.


- **Authorization**

	For specifying the account name and permission types to be used.


- **Transaction**

	For specifying which actions should be included in a given transaction.


- **Predefined Network Connections**

	Pyntelope out of the box includes the following named network connections, pointing to the associated URLs. In milestone 2 they will be made configurable via YAML file.


	WaxTestnet:[ https://testnet.waxsweden.org/](https://testnet.waxsweden.org/)

	WaxMainnet:[ https://facings.waxpub.net](https://facings.waxpub.net/)

	EosMainnet:[ https://api.eossweden.org](https://api.eossweden.org/)

	KylinTestnet:[ https://kylin.eossweden.org](https://kylin.eossweden.org/)

	Jungle3Testnet:[ https://jungle3.eossweden.org](https://jungle3.eossweden.org/)

	TelosMainnet:[ https://telos.caleos.io/](https://telos.caleos.io/)

	TelosTestnet:[ https://testnet.telos.caleos.io](https://testnet.telos.caleos.io/)

	ProtonMainnet:[ https://proton.cryptolions.io](https://proton.cryptolions.io/)

	ProtonTestnet:[ https://testnet.protonchain.com](https://testnet.protonchain.com/)

	UosMainnet:[ https://uos.eosusa.news](https://uos.eosusa.news/)

	FioMainnet:[ https://fio.cryptolions.io](https://fio.cryptolions.io/)

	Local:[ http://127.0.0.1:8888](http://127.0.0.1:8888/)


- **Data Classes**

	Pyntelope uses unique named data classes for serialization to the Antelope native types these types include the following and will include additional types in future Antelope update:

	- **UnixTimeStamp**
	Standard epoch

	- **String**
	This works for all single byte UTF8 Characters currently

	- **Asset**
	Serializes an amount (can be a float value) and currency name together. Uses Symbol type to serialize precision and name of the currency, uses Uint64 type to serialize amount. Amount and name are separated by one space. Example: 50.100000 WAX

	- **Symbol**
	Serializes a precision and currency name together. Precision is used to indicate how many decimals there are in an Asset. Type, amount, precision, and name are separated by a comma. Example: 1,WAX

	- **Bytes** 
	Basic bytes value, used mainly for serialization internally. Example: b’\x00'

	- **Array**
	An Array of other types. Value has parameters type_ and values: type_ must be defined as eospyo type, and values is a list of those types. Example parameters: type_ = eospyo.types.Name, values = [“name1”, “name2”]

	- **Name**
	EOSIO Account name. Read for exact conventions [here](https://developers.eos.io/manuals/eosio.cdt/v1.8/best-practices/naming-conventions)

	- **Int8**
	Integer between -128 and 128

	- **Uint8**
	Unsigned integer between 0 and 256

	- **Uint16**
	Unsigned integer between 0 and 65536 (2¹⁶)

	- **Uint32**
	Unsigned integer between 0 and 4294967296 (2³²)

	- **Uint64**
	Unsigned integer between 0 and 18446744073709551616 (2⁶⁴) This one is most commonly used in contracts since it has the largest range

	- **Varuint32**
	Variable Length Unsigned Integer. This provides more efficient serialization of 32-bit unsigned int

**An overview of the technology stack to be used**

This project will be entirely in Python 3.8+. Tests and other development tools require docker and leap binaries.

**Documentation of core components, protocols, architecture, etc. to be deployed**

We have several pieces of documentation available, including:

- Readme in the repository to help people get started with using the project: [https://github.com/FACINGS/eospyo#readme](https://github.com/FACINGS/eospyo#readme)
- Article going over more in-depth usage and detail:  
[https://detroitledgertech.medium.com/eospyo-tutorial-ff63a0f759ee](https://detroitledgertech.medium.com/eospyo-tutorial-ff63a0f759ee)
- Different transaction examples for commonly used actions: 
[https://github.com/FACINGS/eospyo/tree/main/examples](https://github.com/FACINGS/eospyo/tree/main/examples)

**PoC/MVP or other relevant prior work or research on the topic**

This project has already been started and is in use for both DLT and FACINGS and is available for the general public on GitHub as linked in the overview section.

**What your project is _not_ or will _not_ provide or implement**

As this project is being proposed in multiple stages, various features will not be available until the appropriate stage has been completed. Additionally, this library will not support physical ledgers, although if there is interest after we have completed this proposal we would be happy to investigate and apply for future funding.


### Ecosystem Fit
**Where and how does your project fit into the ecosystem?**

Pyntelope aims to provide the fastest integration between off-chain resources and Antelope chains. Allowing automated signing of blockchain actions common to the development of games and other mixed applications. Current Python libraries are unmaintained or do not include pytest modules or full transaction deserialization. Additionally, we wish to provide tools that allow developers to point Pyntelope tools at existing smart contracts and receive back a complete and ready to use library to allow Python developers to be Python developers without having to be smart contract engineers.

**Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?**

Our target audience includes developers of any Python application, whether it's a website server, game developer, QA engineers, and data analysts. We believe that with an extension of features as described in this document that many dapp developers will find and use this library and draw them into the Antelope ecosystem with its ease and speed of development.

DLT and FACINGS, Inc. are already using Pyntelope in projects built in pairing with Onboard Games (NFTDraft and Pinmaster). FACINGS, Inc. is using Pyntelope in its reservation and redemption flow for off-chain payment (credit cards mostly).

**What need(s) does your project meet?**

Currently, Python developers wishing to create mixed paradigm applications are using tools, specifically, Antelope, that require them to already be very comfortable and familiar with blockchain technology and these tools do not provide significant or easy automated testing solutions nor easy access to response data for making additional off-chain decisions. Pyntelope aims to provide easier automated test writing and execution, more efficient parsing of response, and most importantly the ability to interface with smart contracts without having to understand natively all of the strict typing inherent to Antelope. Pyntelope also provides simple and easy to understand libraries unique to a given smart contract for the most rapid release cycles.

**Are there any other projects similar to yours in the EOSIO ecosystem?**

We’re aware of the following projects. Our analysis is inline.

[pyeoskit](https://github.com/learnforpractice/pyeoskit)
- They have a great project. It used to be heavily based on UUOSKit.

[UUOSKit](https://github.com/uuosio/UUOSKit/):
- It uses libuuoskit binaries using cython.
- Lacks the ability to use an external wallet (or file on disk). This creates a global state issue and makes it impossible to use on read-only file systems.
- Also, since it contains Cython elements, it may be hard to port it to some systems and prepare all dependencies.

[eospy](https://github.com/eosnewyork/eospy):
- Their project is similar to ours. However, it seems that development has recently slowed.

[µEOSIO](https://github.com/EOSArgentina/ueosio):
- This is what Pyntelope is based on.
- Pyntelope is very different, more pythonic. And internally, states are immutable and thus less bug-prone, especially for parallelizing via async or queue processing.
- Pyntelope is far more comprehensive with faster development speed and support for wider use cases.


## Team

### Team members
 
- **Team Leader**: Karyne Mayer, VP of Engineering
- Bruno Souza, Senior Engineer
- Faisal Bagalegel, Junior Engineer
- Jonas Brunetto, Part-time Senior Engineer
- Charlie Dumont, Educational Program Director

### Legal Structure
- **Registered Legal Entity:** EOS Detroit, Inc. d/b/a Detroit Ledger Technologies
- **Registered Address:** 1570 Woodward Ave., Floor 3, Detroit, MI 48226

### Team Experience
Detroit Ledger Technologies (formerly EOS DETROIT), is a pioneering block producer for Antelope networks founded in March 2018 to participate in the launch of EOS. Outside of block production, the company focuses on Web3 product design and implementation. Members of the Detroit Ledger Technologies team helped build governance products like the WAX Office of Inspector General (OIG), WAX Labs, and Telos RFP; and NFT-powered products such as Topps GPK Bernventures, Pinmaster, and NFTdraft, in partnership with DLT’s first incubated startup, FACINGS. The team also supports and maintains open source tools such as NodeSuite, Smart Contract Migration Tool, and the previous phases of development of Pyntelope (formally eospyo).

The engineers tasked to participate in the project have 30 years of combined experience and have worked on projects for a variety of companies such as HP, Coca-Cola, and more.

### Team Org Repos

- [https://github.com/eosdetroit](https://github.com/eosdetroit)
- [https://github.com/eosdetroit/nodesuite](https://github.com/eosdetroit/nodesuite)
- [https://github.com/eosdetroit/smart-contracts-migration](https://github.com/eosdetroit/smart-contracts-migration)
- [https://github.com/eosdetroit/govboard](https://github.com/eosdetroit/govboard)
- [https://github.com/FACINGS/eospyo](https://github.com/FACINGS/eospyo)

 

### Team Member Repos

- Karyne Mayer: [https://github.com/karynemayer](https://github.com/karynemayer)
- Bruno Souza: [https://github.com/brnosouza](https://github.com/brnosouza)
- Faisal Bagalegel: [https://github.com/Fossilia](https://github.com/Fossilia)
- Jonas Brunetto: [https://github.com/jmbrunetto](https://github.com/jmbrunetto)
- Charlie Dumont: N/A

 
### Team LinkedIn Profiles (if available)

- Karyne Mayer: [https://www.linkedin.com/in/karyne-mayer/?originalSubdomain=br](https://www.linkedin.com/in/karyne-mayer/)
- Bruno Souza: [https://www.linkedin.com/in/bruno-cunha-de-souza/](https://www.linkedin.com/in/bruno-cunha-de-souza/)
- Faisal Bagalegel: [https://www.linkedin.com/in/faisal-bagalagel-6a14b8190/](https://www.linkedin.com/in/faisal-bagalagel-6a14b8190/)
- Jonas Brunetto: [https://www.linkedin.com/in/jonasbrunetto/](https://www.linkedin.com/in/jonasbrunetto/)
- Charlie Dumont: [https://www.linkedin.com/in/c-dumont-0922a8181/](https://www.linkedin.com/in/c-dumont-0922a8181/)


## Development Status

This project is already in use and has been through several iterations of Pomelo grants. We have finished the last round of funded promises for the Pomelo grant. This includes an already published tutorial, an improved CI/CD pipeline for maintenance, along with the ability to deploy new smart contracts to the chain.


## Development Roadmap 


### Milestone Summary

- **Total Estimated Duration:** 14 weeks development, 8 weeks evangelization

- **Full-Time Equivalent:** (FTE): 3

- **Total Costs:** $170,000

  
### Milestone 1 — Pytest 

- **Estimated duration:** 4 weeks
- **FTE:** 3
- **Costs:** 40,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT License |
| 0b. | Documentation | We will provide and update documentation for each milestone in the form of example files in the repository, usage in the Readme file, and more in-depth usage in our article. |
| 0c. | Testing Guide | All our functionality can be tested by running the pytest unit tests we provide. A guide on how to run these tests is provided in the Readme file |
| 0d. | Docker | We use docker to start up a container that runs a local nodeos instance with specific users and contracts deployed for developer testing. This along with the Poetry dependency manager ensures developers have the same environment when working with Pyntelope. 
| 1. | Pytest plugin overview | We will create a pytest plugin to make it easier to develop Pyntelope unit tests with mocked blockchain responses because blockchain calls are error prone due to network and blockchain eventual consistency. This feature would allow developers to replicate these errors to be sure application code is prepared to handle these errors. This is a good design pattern for developing robust backend systems.
| 2. | Pytest plugin applications / rationale | The pytest plugin will allow developers to work without relying on the current blockchain state, as if the blockchain is performing irregulating at a given crunch time, development can be significantly hindered as it is challenging to handle possible blockchain responses. A pytest plugin also has the benefit of automatically testing a project against blockchain responses whenever a change is made (if a project is set up with pipelines), supporting our point that this will lead to robust backend systems. All these tests will be able to run offline, this allows for testing regardless of the blockchain state and the user's network state. 
| 3. | Planned decorators / mockers |• **Chain_mock_transaction_timeout:** Mocks a transaction running longer than allowable block time. <br> • **Chain_mock_network_timeout:** Convenient syntactic sugar wrapping the existing pytest timeout library. <br> • **Chain_mock_insufficent_ram:** Mocks chain response of an action that requires more RAM than is available to the authorizing account. <br> • **Chain_mock_insufficent_cpu:** Mocks chain response of an action that requires more CPU than is available/staked to the authorizing account. <br> • **Chain_mock_insufficent_net:** Mocks chain response of an action that requires more net resource than is available/staked to the authorizing account. <br> • **Chain_mock_invalid_authorization:** Mocks chain response to an action with improper validation. <br> • **Chain_mock_rows:** Mocks chain response for a smart contract table query.|



### Milestone 2 — General improvements

- **Estimated duration:** 2 weeks
- **FTE:** 3
- **Costs:** 20,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT License |
| 0b. | Documentation | We will provide and update documentation for each milestone in the form of example files in the repository, usage in the Readme file, and more in-depth usage in our article. |
| 0c. | Testing Guide | All our functionality can be tested by running the pytest unit tests we provide. A guide on how to run these tests is provided in the Readme file |
| 0d. | Docker | We use docker to start up a container that runs a local nodeos instance with specific users and contracts deployed for developer testing. This along with the Poetry dependency manager ensures developers have the same environment when working with Pyntelope. 
| 1. | Native Async calls | Because Antelope calls rely on the blockchain they can cause io binding which is unacceptable for many use cases as such we will provide native async calls in the library. <br> Additional methods and classes added here would be an async version of the Transaction method named “send” called “async_send”.
| 2. | Full UTF-8 support for multibyte characters | Currently only single-byte UTF-8 characters are supported, we would like to address this by allowing multi-byte UTF-8 characters by altering the current string serialization implementation. 
| 3. | Configurable network endpoints via YAML files |We have provided some safe defaults for network endpoints, however not all users will want to use those for various reasons and we would like to move the URL configuration for networks to YAML files to make easier changes.
| 4. | Implement missing types |Pyntelope has most types defined for serialization but there are a few we are missing, and we plan to implement the rest of them including float32, float64, float128, checksum160, checksum256, and checksum512 types.|



### Milestone 3 — ABI introspection

- **Estimated duration:** 8 weeks
- **FTE:** 3
- **Costs:** 80,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT License |
| 0b. | Documentation | We will provide and update documentation for each milestone in the form of example files in the repository, usage in the Readme file, and more in-depth usage in our article. |
| 0c. | Testing Guide | All our functionality can be tested by running the pytest unit tests we provide. A guide on how to run these tests is provided in the Readme file |
| 0d. | Docker | We use docker to start up a container that runs a local nodeos instance with specific users and contracts deployed for developer testing. This along with the Poetry dependency manager ensures developers have the same environment when working with Pyntelope. 
| 1. | Abi introspection overview | As ABIs provide a full summary of the available behaviors in an Antelope smart contract they are the most immediate and complete source of information regarding the interface to said contracts. In order to provide more rapid development, this tool would allow developers to call an action using an ABI as an argument  (URL or local file)  and be provided with a specific library containing the appropriate classes and methods to be able to interact with this contract directly without having to build this interface themselves.
| 2. | Abi introspection application/ rational | This would allow both simple contracts and very complex contracts to be readily available for complete interface to Python developers allowing them to treat the blockchain as any other abstracted data and processing source. This is similar to how ORM abstracts away the complexity of database queries and allows developers to stay in the mindset of development. We wish to take this model to the next level and save developers the effort of building these abstractions thus further enhancing the speed of development. 
| 3. | Contract Interfacing Example |Example for interfacing the basic eosio.token contract: <br> The interface for creating the unique libraries will look as follows: <br> **pyntelope make-from-abi -destination ./token/eosio.token.abi** <br> This command will create a file called eosio_token.py that includes a function that returns the following instantiation arguments: <br> **auth:** a Pyntelope auth object <br> **net:** a Pyntelope net object
| 4. | Methods from the above example |The example above will provide the following methods with additional fields as named wherein each argument will be a matched pydantic type that will verify that the received argument matches the data type that will be serialized automatically in the interface. <br> **open** <br> • owner <br> • symbol <br> • ram_payer <br> **issue** <br> • to <br> • quantity <br> • memo <br> **retire** <br> • quantity <br> • memo <br> **transfer** <br> • to <br> • from <br> • quantity <br> • memo <br> **close** <br> • owner <br> • symbol <br> **create** <br> • issuer <br> • maximum_supply |



### Milestone 4 – Promotion & Developer Evangelization

- **Estimated duration:** 8 weeks
- **FTE:** 2
- **Costs:** 30,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT License |
| 0b. | Documentation | We will provide and update documentation for each milestone in the form of example files in the repository, usage in the Readme file, and more in-depth usage in our article. |
| 0c. | Testing Guide | All our functionality can be tested by running the pytest unit tests we provide. A guide on how to run these tests is provided in the Readme file |
| 0d. | Docker | We use docker to start up a container that runs a local nodeos instance with specific users and contracts deployed for developer testing. This along with the Poetry dependency manager ensures developers have the same environment when working with Pyntelope. 
| 0e. | Article | We have provided an article detailing the functionality of the project https://detroitledgertech.medium.com/eospyo-tutorial-ff63a0f759ee and plan to publish more articles in the future as needed.
| 1. | Overview | The DLT team is capable of developing Pyntelope into a quality, go-to library for building projects on Antelope-powered networks. But libraries are only valuable if developers actually use them. In order to spread the word and introduce developers to the Pyntelope library, DLT will deploy a multifaceted strategy.
| 2. | Language accessibility  | DLT plans to make the library accessible in multiple languages. The languages DLT wants to target are Chinese, Korean, Spanish, and Portuguese. By providing robust documentation in additional languages, Pyntelope will have a larger pool of potential users. The funding requested for this milestone will provide translations and translation updates for 1 year.
| 3. | workshops  | The DLT team will perform a number of in-person and online workshops to give developers a crash course on how they can use Pyntelope to begin creating blockchain-enabled applications on Antelope networks. <br> At the local level, Educational Program Director. Charlie Dumont, and one of the library architects, Faisal Bagalegel, will host workshops with our local blockchain meetups, Detroit Blockchainers and Michigan Bitcoiners, and Python-focused meetups such as Python Ann Arbor. <br> The various other team members will also help participate in teaching virtual versions of the workshop targeted toward the Antelope community. <br> DLT will instruct 6 workshops during the duration of the milestone.|



## Future Plans

As previously mentioned we would be interested in providing integration with physical ledgers for additional security for various use cases, this will be done by creating a Pyntelope plugin that can be integrated into existing physical ledgers. The integration will require a great deal of research, if there is a desire for this feature we will do this research and submit a new milestone. Apart from physical ledger support, we also intend to provide additional language translations for the docs, review merge requests, and continue to ship out minor features and fixes as both DLT and FACINGS rely on Pyntelope for various projects, so we have a strong incentive to keep supporting the project as much as possible.

  
## Additional Information

**How did you hear about the Grants Program?** In general, we heard about the program from following the ENF’s announcements on Twitter and various other channels. Also, DLT’s spinout company, FACINGS, Inc. had previously submitted and been approved for a grant.
