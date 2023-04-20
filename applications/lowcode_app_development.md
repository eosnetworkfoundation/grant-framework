# EOS Network Foundation Grant Proposal

- **Project Name:** Blockchain Low-Code App Development and Automation Platform
- **Team Name:** Ampnet IO Ltd.
- **EOS Payment Address:** ivankardum11
- **[Level]:** 2
- **Pomelo Grant(s):** https://pomelo.io/grants/lowcode
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/0xDev3/dev3-sdk, https://github.com/0xDev3/dev3-frontend, https://github.com/0xDev3/blockchain-api-service, https://github.com/0xDev3/solidity-commons


## Contact

- **Contact Name:** Ivan Kardum
- **Contact Email:** ivan@dev3.sh
- **Website:** https://dev3.sh/


## Project Overview

Blockchain low-code app development is the process of creating decentralized applications using a human-readable interface and pre-built components, instead of writing code manually. 

Workflows Templates are part of our Low-Code App solution, and this is our next step in development. 

By defining a series of steps through JSON objects, developers can create complex processes that include blockchain transactions and queries. This approach simplifies the development process, reduces the likelihood of errors, and makes it easier for non-technical users to create decentralized applications.


### Overview

- **Name:** Blockchain Low-Code App Development and Automation Platform
- **Brief Description:** Giving developers the open-source tool to build, automate, maintain & scale secure, user-friendly blockchain apps – from prototype to production.
- **Relationship to EOS Network / Antelope:** With our Platform, which is an open-source code, anyone from the EOS-EVM ecosystem can access it and thus there is no need to develop something from scratch so that the rest of the EOS community can use it to develop new and existing blockchain apps, as well as automate the blockchain process.
- **Reason for Interest:** We believe that with our toolkits we provide the possibility for blockchain and non-blockchain developers, and generally, the EOS community, to build on the EOS-EVM network more easily, and thus, through joint collaboration and open access, we increase the value of the EOS network.

### Project Details

**Build your blockchain app with no coding required**  
Users will be able to deploy and connect all the necessary smart contracts for the platform such as for real-world asset tokenization, decentralized finance, and NFTs, to blockchain and metaverse games - Dev3 covers all your needs. Users can use smart contracts for new blockchain apps or simply extend existing ones by adding blockchain functionality to their existing web and mobile apps.

**Automate repetitive blockchain processes** 
If users already have some blockchain transactions and are dealing with tedious tasks, they can simply use the workflow module to automate their repetitive processes.

**4 Key Elements of the Platform**
There are 4 key elements of the Low-code platform. The first 3 elements have been developed (there is still room for improvement), but the last element - **Workflow**, is the one that remains for development, and then we will have complete automation-ready, not only the development and automation of new blockchain apps and processes but also the automation of existing blockchain apps and process as integration with third parties.

With Dev3 Workflows – you can quickly and easily create templates for any process involving blockchain interactions.

Wireframe / mock-up: https://app.moqups.com/890kc7IXkE7viaoy5LVSW8MEOUjEtJ8n/view/page/a3afcac31

**Workflow Template Step (Proposed Format)**
Every workflow step is a JSON object, and the Workflow Template itself is an object containing an array of steps together with some other metadata.

{
	id: "927075e7-3ebb-4054-a31f-42860e5f7e6c"
	name: "test template",
  description: "this template calls approve and invest on the crowdfunding contract 0x123...abc",
	steps: [
		// ...array of steps definitions...
		// one concrete step
		{
			chain_id: "1",
			from: "", // if empty string sent, user can connect any wallet to process tx
			to: "0x456...def", // if empty string sent, user will provide this value
			value: "0", // if empty string sent, user will provide this value
			data: {
				function_name: "solidity_function_name", // or empty if not function call
				function_params: [ // or empty array if not fn call, or if fn accepts zero parameters
					{
						type: "address",
						value: ""     // value can be: 
													//    - empty (""): user will provide this value
													//    - hardcoded ("0x123...abc")
													//    - input from any step **before**:
													//        - example1: "steps[step_number].function_params[function_param_position]
													//    - output from any step **before**: 
													//        - example1: "steps[step_number].return_values[return_value_position]"
													//        - example2: "steps[step_number].events[event_signature][value_position]
													//        - example3: "steps[step_number].tx.hash"
													//        - example4: "steps[step_number].from"
													//        - example5: "steps[step_number].to"

		
					}, 
					// ... more function params
				],
			},
			output_params: [ "bool" ],
			readOnly: false // if true, this step is a transaction, if false - it's a query
		}
	]
}

The user defining the template steps is responsible for taking care that every referenced output exists in the steps before.

**An overview of the technology stack to be used:**
- Backend - Spring
- Frontend - React native


### Ecosystem Fit

- Where and how does your project fit into the ecosystem? 
It fits as a developer tooling for the EOS community. It is a non-excludable platform, which means users from the EOS ecosystem can easily kick-off building & automating blockchain applications easily and for free. Also, the platform is non-rival, which means that the use of the platform by one person does not prevent access to other people, nor does it reduce the availability to other users from the EOS ecosystem.

- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)? 
The target audience is those users (mainly developers) who want to build quickly blockchain (prototype) apps and automate the new and existing ones. Dev3 platform is the ideal developer tool for new Web3 projects and easily onboarding Web2 companies and users. 

- What need(s) does your project meet?
Using our Low-code App Development Platform, the EOS community will have the perfect tool for building, maintaining and scaling user-friendly blockchain apps in the best possible UX manner:
 a) Attract non-blockchain developers to easily build blockchain apps on the EOS-EVM network
 b) EOS Network will have a tool for rapid proof-of-concept development
 c) Access to hundreds of smart contracts in human-readable form for easier development
 d) Import *any* EVM smart contract address and we will convert it into a human-readable format
 e) Reduced x10 development costs and the learning curve for companies that want to break into the web3 space.

- Are there any other projects similar to yours in the EOS Network / Antelope ecosystem?
  - If so, how is your project different? - As far as we are aware, there is no similar project in the EOS Network ecosystem
  - If not, are there similar projects in related ecosystems? - Thirdweb


## Team

### Team members

- **Team Leader:** Filip Dujmusic
- Ivan Kardum
- Mislav Javor
- Domagoj Latecki
- Ivan Piton

### Legal Structure
- **Registered Legal Entity:** Ampnet IO Ltd.
- **Registered Address:** Ulica Vjekoslava Heinzela 62a, 10000 Zagreb, Croatia.

### Team Experience
Mislav Javor, CEO is a software developer & blockchain enthusiast. Organizer of the Zagreb Blockchain Development Meetup, actively promoting blockchain education with lectures at universities and in media. Mislav is the book author of A Developer's Guide to Ethereum.
Filip Dujmusic, CTO is a smart contract developer. Exploring the integration of Ethereum clients on mobile platforms and how to create a user-friendly approach. 
Domagoj Latecki - Backend developer includes developing scalable applications with an emphasis on clean architecture.
Ivan Kardum - Business developer, with experience in the fintech and blockchain field.

**Projects**:
Lucrifi - [https://github.com/AMPnet/lucrifi](https://github.com/AMPnet/lucrifi)
Chainlink - [https://github.com/0xDev3/dev3-chainlink-sdk](https://github.com/0xDev3/dev3-chainlink-sdk)

### Team Org Repos

- https://github.com/0xdev3

### Team Member Repos

- https://github.com/0xmislav
- https://github.com/filipdujmusic
- https://github.com/domagojlatecki
- https://github.com/ivankardum1

### Team LinkedIn Profiles (if available)

https://www.linkedin.com/in/mislavjavor/
https://www.linkedin.com/in/filipduj/
https://www.linkedin.com/in/ivan-kardum/
https://www.linkedin.com/in/domagoj-latecki/
https://www.linkedin.com/in/ivanpiton/

## Development Status

[https://github.com/0xDev3/](https://github.com/0xDev3/)

In a short, these are the key elements of the Blockchain Low-code App Development and Automation Platform:

1. **Dashboard - Intuitive Smart Contract Management** *(Already developed)*

Dev3 dashboard makes handling smart contracts a breeze.
- Easily handle EVM multi-chain deployments, smart contract versioning and get an auto-generated admin panel for every connected smart contract.
- Enables non-developers to build web3 business logic and deploy smart contracts
- Enables effortless automation of common Web3/Blockchain tasks
- Deploy or connect any EVM deployed smart contract address, and Dev3 will decompile it into a human-readable interface!

2. **SDK & API - Connecting Web2 with Web3** *(Already developed)*

Dev3 SDK & API enable organizations to:

- Keep using their existing tech stack, tools and processes while simultaneously adding blockchain features to their products
- Use traditional web, mobile & backend developers to build Web3 applications
- Write automation scripts for blockchain actions

3. **Execution Environment** *(Already developed)*

Ensure that all blockchain transactions and communications between your app & end users are secure and effortless.

Developers building on Dev3 and users creating process automation can rely on our class-leading transaction execution UX! Simply by opening a web link, the user is transported into Dev3 Execution Environment! There, Dev3 will detect the smart contract and provide the user with a simple to understand description of what the transaction is about to do! All the user needs to do is wait for the callback API/SDK event!

4. **Workflows** *(The support we need!)*

With Workflows, users will be able to automate blockchain actions and easily integrate third-party plugins. 

This is the last, and perhaps the most important element of the Platform **for which we ask for your support**, which fully enables workflow automation and combining "workflow items" from many categories, such as:

- Wallet Authorizations - Authenticate users through cryptographic message signing with Web3 wallets or through custodial wallets
- Deploy and Connect Smart Contracts and Execute Transactions - Add any number of contract deployments and transaction requests into a single, end-to-end business process
- KYC & AML Verification - Stay compliant by easily creating a user registration with KYC & AML verification
- Custodial Wallets - Initializing custodial wallets before entering a flow - ensuring anyone can participate
- Fiat On-Ramp & Off-Ramp - an integrated service that allows users to “Top-Up” their wallets with credit cards
- Digital Signing - Enable your users to digitally sign legal documents as needed
- Multisig - requires more than one private key to sign and authorize a crypto transaction.


## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 21 weeks 
- **Full-Time Equivalent (FTE):** 2 FTE
- **Total Costs:** 44,800 USD

**Note**: Some of the milestones will overlap and run in parallel.

### Milestone 1 — Proof of Concept & Idea Validation (Frontend Only)

- **Estimated duration:** 6 weeks
- **FTE:**  1
- **Costs:** 9,600 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both documentation of the code and a basic tutorial that explains how a user can spin up a local Workflow application. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile that can be used to spin up a local Workflow application. |
| 1. | Front-End / User Interface | A minimal frontend will be developed to showcase the idea of how the product might work.
Features:
PoC will contain the following 5 features:
1. create a template by uploading the JSON file in the proposed format
2. create a template by pasting the JSON content directly into the app
3. validate the template and upload it to IPFS to get a shareable link
4. share a link to a template
5. process the shared template steps by opening the link and connecting MetaMask |   

**Deliverable:** This application will be hosted on its own domain and will be used to test and validate the idea of templates and workflows. This will enable anyone to easily define their workflows and share them with anyone by simply sending the link.


### Milestone 2 — Workflows v1.0 (backend)

- **Estimated Duration:** 8 weeks
- **FTE:**  1
- **Costs:** 12,800 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both documentation of the code and a tutorial that explains how a user can spin up a local Workflow application (backend). |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile that can be used to spin up a local Workflow backend and local Workflow frontend containers. |
| 1. | Workflows Backend Service | Deliverable description: Workflows Backend Service is a REST API service exposing the APIs to enable the following:
→ project management (create a new project which is going to contain templates)
→ workflow templates (create, query, get all)
→ workflow templates - generate a permalink (when opened, a new instance of the template is created)
→ workflow instances (create, update the state, query state, get all with status)
→ multichain support (support for different EVM chains)

Backend will be implemented in the spring framework and will be packed inside the docker container. |  

MVP-Workshop scheme - https://drive.google.com/file/d/1-gAqa2k9R2svckSUElMQ_74CcTg9f6Mb/view?usp=sharing
*workflows.io is an imaginary domain used as an example here. We will come up with another name for this product.


### Milestone 3 — Workflows v1.0 (frontend)

- **Estimated Duration:** 14 weeks
- **FTE:**  1
- **Costs:** 22,400 USD

Workflows v1.0  frontend contains two parts:
1. Dashboard for creating templates and instances (frontend)
2. Execution Environment for processing workflow instances (frontend)

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both documentation of the code and a tutorial that explains how a user can spin up a local Workflow application (frontend). |
| 0c. | Testing Guide | Testing of the Workflows application will be mostly covered on the backend side. For the frontend testing, the regular QA human tests will be carried out. |
| 0d. | Docker | We will provide a Dockerfile that can be used to spin up a local Workflow backend and local Workflow frontend containers. |
| 1. | Workflows Frontend application | Web application built with React Native, contains two modules: Dashboard & Execution Environment. | 
| 2. | Workflows Frontend Dashboard | Design the Workflow Dashboard
→ Create a new project
→ Create a new template by defining steps
→ Show existing templates
→ Copy a permalink to an existing template
→ Show a list of created workflows instances with their execution statuses (i.e. 5/7 steps completed) | 
| 3. | Workflows Frontend Execution environment | → Design the Execution Environment
→ Process workflow instance by allowing users to connect wallet (Metamask) and execute actions step by step | 

**Platform access**
[https://app.dev3.sh/home](https://app.dev3.sh/home)


## Future Plans
After the MVP has been developed and released, the feedback of the community will be heard and taken into account. We might develop this product further in different directions:

- Implement **if/then conditionals** as the workflow step (to go more into the low/no code app builder direction)
- Implement third-party services as the workflow step, such as **KYC**, **gas auto-funding, on-ramp & off-ramp**
- Implement a **typescript SDK** to pack the exec environment into a frontend widget which is going to be used natively inside other frontend applications to make the flow processing even more user-friendly
- Remove the backend part completely and replace it with some form of **decentralized file storage** used to store the states of created workflow instances.
- Integrate other wallet providers.

**Supported use cases**
Workflows Templates structured as proposed in this document allow for various use cases such as:
- **approve + function_call** flow and other popular flows are easily converted to this model
- ************************multichain************************ transactions (execute step1 on one chain, step2 on another chain, and so on)
- **deployment scripts** - deploying a set of contracts and connecting them to each other
- any other **predefined series of steps**
- **basic frontend builder** for any contract call or more complex flow. Dev doesn’t have to handle transaction states and wait for one transaction to be mined to start another one. They simply have to describe the process and let the workflows guide the user.


## Additional Information
We heard about the Grants program at a conference from the EOS Network Foundation team in Amsterdam, and later we went to learn more about grants on the EOS Network Foundation website.
