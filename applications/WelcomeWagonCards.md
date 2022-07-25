# EOS Network Foundation Grant Proposal

- **Project Name:** WelcomeWagon Cards
- **Team Name:** Agenix LLC
- **EOS Payment Address:** agenix.gm
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** List URL(s) to Pomelo grants for your team (or list N/A for non-applicable) https://pomelo.io/grants/edenelection
- **Project is Open-Source:** YES
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/ChuckMacDonald/welcomewagon

## Contact

- **Contact Name:** Chuck MacDonald
- **Contact Email:** chuck@agenix.io
- **Website:** welcomewagon.ai

## Project Overview

### Overview

- **Name:** Welcomewagon Claim Link Infrastructure and Card Production
- **Brief Description:** Services and API work to allow for bulk management of EOS account & NFT claim urls, physical print prototype, design templates. 
- **Relationship to EOSIO:** Welcomewagon.ai will be an onboarding & engagement service for all coalition chains, and our printed cards will be used worldwide to onboard real people.
- **Reason for Interest:** We want to make EOS easy and fun for everyone. With many more project ideas to come, we need onboarding and engagement solved first.

### Project Details

We have built a Proof-of-Concept https://github.com/ChuckMacDonald/welcomewagon/blob/main/6-Cards%20PoC%20%26%20Phone%20Mockup.jpg for a system that abbreviates 
long-form URLs for EOS account creation and for NFT claims into custom-domain-shortened URLs and simple QR codes. 
It will allow us to build using traditional infrastructure and user databases, yet link to EOS accounts, and reward them with NFTs for accomplishing simple tasks.
The first of these simple tasks is the use of a printed card to create a .gm EOS account, and the NFT reward for this task is claimed by using the link on the same card.

Using standard web tools such as URL shorteners, G-suite, & CRM in conjunction with the Greymass account creation process & atomicassets NFT gifts, we are able
to create a database of URLs (both in text and QR) from which we can create print material. At this point it is not automated, but we hope to minimize the manual 
process as much as possible thru this grant. 

Our goal with this grant is to build the back-end infrastructure that will enable us to scale up the production of our cards, and to better analyze how the cards are
used by the EOS community so that we can improve their design and distribution. 

This requires funding for subscriptions to several web services (eg. Bitly.com URL shortening service, Hubspot CRM, Make.com, G-Suite, Figma, Adobe, etc.), as well as
infrastructure for hosting. Depending on the scale at which we are able to produce the cards, we will quickly need to replace the subscription-based URL shortener
with our own solution. 

Production of the printed material requires research and experimentation with graphical layout software (and its integration with our database of URLs) to populate 
large quantities of business cards and posters. As batches of business cards are successfully printed, they need to be distributed to on-the-ground onboarding 
opportunities, such as blockchain conferences or to social movements like EOS Marketplace, and local meetups. In order to properly measure the effectiveness of this
method as an onboarding tool, we will have to collect and analyze every bit of data created. We are currently developing a list of potential test partners who could
take a set of cards and commit to their distribution. Part of this printing and distribution process will be the discovery of our gross costs, and an idea of the 
value of these cards to the market and the EOS Network. 

We also plan on creating testing cards that will have QR codes that would automatically recharge, allowing the bearer to repeatedly distribute new EOS accounts and NFTs.

This project is a component of the larger welcomewagon project, but is specifically focused on the production of claim links & the quick ramp-up of 
the QR card production, as well as the creation and upkeep of a database of shortened links that we can use for large-scale card production.

The most serious immediate envisioned limitation is that of Bitly.com, which for $200 per month can allow us to create approximately 1500 cards per month (3000 unique
links). They obviously offer packages for more links, but we know that we will need to set up our own in-house link shortening service in very short order. We plan
to evaluate this potenial transition in the future.

There are concerns with the security of 7-digit abreviated URLs against brute force attacks, but at this stage it is not an issue, because we are dealing with
extremely low-value claim links, and because we are still unknown. In the future though, especially with the permanent cards, or with cards that contain backed NFTs
(eg.'Claim this NFT backed by 10 EOS') the danger could be mitigated in several ways, such as SMS confirmation. 

- Mock-ups/designs of any UI components
- Data models of the core functionality
- API specifications of the core functionality
- An overview of the technology stack to be used
- Documentation of core components, protocols, architecture, etc. to be deployed
- PoC/MVP or other relevant prior work or research on the topic
- What your project is _not_ or will _not_ provide or implement
  - This is a place for you to manage expectations and to clarify any limitations that might not be obvious

### Ecosystem Fit

Welcomewagon.ai is 'the smart engagement solution for your web3 destination'.
Our mission is to make the EOS experience easy and fun for all users. By intentifying our users' profiles and offering them a journey tailored to their level of experience, 
we hope to quickly make an impact in the EOS and EOSIO ecosystems. We hope that by offering the simplest of interactions with our newly onboarded users, they will 
come back to welcomewagon to learn more about the network. Dapps and other destinations will want to partner with us to direct the new users their way. If this model is successful, 
networks will wish to partner with us to enhance their general ecosystem. 
We hope to very quickly have a large collection of concise e-learning materials, which will be free for anyone to view (only welcomewagon members will be rewarded with NFTs
for watching the material.)

In the meantime though, we want to focus on the production of our QR cards as we move into trade-show season, as colleges and universities resume, and as social movements like
Hu-Fi and Eden gain traction. The onboarding potential is massive, if these cards are put into the right hands. Distributors who order batches of the cards will be able to customize
them with their own NFT, and will be forever linked to the account that they helped to onboard. The sybil defence to this system is built in: We can offer free or subsidized accounts
because they only way they can be claimed is with a physical card, distributed by a real person. 

We are not aware of any other EOSIO project that is doing what we are building: Simple onboarding + incentivized e-learning. Several projects are doing one or the other.. 
Wombat wallet offers free accounts (via socials login) and then promotes specific dapps and destinations, but does not offer concerted e-learning. We know of no other product across 
EOSIO - or any other chain - that accomplishes what our business cards do. 

On other networks, these types of blockchain interactions are very difficult to find, if they exist at all. 
https://www.vechain.org/vechain-powers-canadian-company-micromations-saas-platform-truestoryteller-enabling-quick-onboarding-of-clients-to-blockchain/
VeChain has been using blockchain-linked QR codes for several years now, and it now has a nft marketplace... 

- Where and how does your project fit into the ecosystem?
- Who is your target audience (chain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
- What need(s) does your project meet?
- Are there any other projects similar to yours in the EOSIO ecosystem?
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?

## Team

### Team members

- **Team Leader:** Chuck MacDonald
- Name of team member Domenic Thomas
- Name of team member Joe Lagan
- Name of team member Rob Dewilder
- Name of team member Sean Anderson

### Legal Structure
- **Registered Legal Entity:** Agenix, LLC
- **Registered Address:** 701 Orley PL Bel Air, MD 21014 USA


### Team Org Repos

- https://github.com/ChuckMacDonald/welcomewagon

### Team Member Repos

- https://github.com/ChuckMacDonald
- https://tru.cool (Joe Lagan)

### Team LinkedIn Profiles (if available)

https://www.linkedin.com/in/robert-dewilder-6b83311/
https://www.linkedin.com/in/domenic-thomas-5403676/
https://www.linkedin.com/in/seanxanderson/

## Development Status

Beginning in the fall of 2021, I (Chuck) began experimenting with the Greymass account creation process, and became aware that the sharing of those urls could lead 
somewhere interesting for onboarding on EOS. After several conversations with Aaron Cox of Greymass, an experimental set of codes was given to me, and I began sharing
the codes with friends and family. The process was still rather rough, but I was able to help most people get thru it. This past spring, I began experimenting with 
QR codes in print, and found that results were far better when using an abreviated url. https://github.com/ChuckMacDonald/welcomewagon/blob/main/0-Account%20claim%20Component.png
I was able to produce a large handbill (1/2 a page) that contained several codes on it. https://github.com/ChuckMacDonald/welcomewagon/blob/main/1-Handbill%20Page%20Front%201.png
https://github.com/ChuckMacDonald/welcomewagon/blob/main/2-Handbill%20Page%20Reverse.png I gave a number of public and private talks on 'Real Life Implications of the 
Bitcoin Sector', featuring EOS and Eden. While a bit convoluted, the talks were successful in raising awareness, and they helped me to further hone my onboarding 
delivery. Around this time I was developing a friendship with Domenic Thomas of Agenix, and we decided to become partners in this venture. During my time in Eden I 
have seen the value of authentic relationships between real people when onboarding, and it led me to create a very simple physical product that could be shared between
individuals in person. This opens the door to 'Real Life' organizations bringing their entire membership list onto EOS if they have a compelling reason to do it. 
This will allow representatives at trade shows to hand out a real EOS account to someone they are speaking with, even handing them another card that contains a gift 
of an NFT backed by 1, 5, 10 or more EOS.https://github.com/ChuckMacDonald/welcomewagon/blob/main/3-Card%20PoC%20Front.png https://github.com/ChuckMacDonald/welcomewagon/blob/main/4-Card%20PoC%20Back1.png

We are now reaching out to organizations and networks who might like to partner with us to test these cards. We have looked into bulk printing options, various print 
formats and qualities, and even permanent etched steel cards, with QR links that would recharge automatically. 

We are building welcomewagon.ai on web2 standards, integrating with CRM (Hubspot), and limiting (at this time) blockchain integrations to claim links, so that we
can build our MVP as quickly and efficiently as possible. Above all, we want our product to be functional at each step of its development. The cards work today, 
although they are built using a method that is more far manual than we would like. 


## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 6 weeks
- **Full-Time Equivalent (FTE):** 2.5 FTE
- **Total Costs:** 10,000 USD

### Milestone 1 — Production of First Batch of Cards

- **Estimated duration:** 2 weeks
- **FTE:**  2.5
- **Costs:** 4,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Project Github will include a listing of all services used & a flow chart of the APIs used. There will also be a document at welcomewagon.ai/help walking users through the process. The process will be explained in general terms, because our implementation of it is dependant on subscriptions to several services, and custom integrations of those services. 
| 0c. | Testing Guide | We will provide a detailed step-by-step walkthrough of the process. Testing of the process will be the picking of a random card from thedelivery and scanning it with a phone, and the completion of the action.   
| 1.  | Delivered Product          | 200 unique business cards delivered (digitally) within 24 hours of the ENF providing a design or logo for the NFT with unique account claim and NFT claim links on each card. Printing and shipping may follow, at the ENF's option.  
| 2.  | Product Interface to EOSIO | Our cards are standalone URLs which trigger blockchain events - the creation of a new .gm EOS account, and the claiming of an NFT.  
| 3.  | Front-End / User Interface | The user interface is the printed card. The user may either scan the QR codes, or they can input the URLs manually. 


### Milestone 2 - Automatically Re-charging Cards

- **Estimated Duration:** 2 weeks
- **FTE:**  2
- **Costs:** 3,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation will include a listing of all services used & a flow chart of the APIs used. There will also be help at welcomewagon.ai for the process.
| 0c. | Testing Guide | We will provide a detailed step-by-step walkthrough of the process. The test will be to use a card and then use it again after its recharge period has elapsed. 
| 1. | Delivered Product | 10 digital business cards. The end result will be printable proofs of 10 unique cards sent to ENF for evaluation. 


### Milestone 3 - Templates and Enhanced Process Documentation

- **Estimated Duration:** 2 weeks
- **FTE:**  2
- **Costs:** 3,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | Documentation will include the use of our cards & the use of the design templates we will create. 
| 0c. | Testing Guide | We will provide a detailed step-by-step walkthrough of the process of using the printed cards
| 0e. | Article | We will publish an **article** that explains what we have accomplished through the grant, and show how our process can be used to share URLs and digital goods in creative ways.  
| 1. | Figma Template | We will publish a simple EOS-branded Figma template with components set up to receive the QR codes and URLs from a sheet. eg. "NFT and EOS account card Template"
| 2. | Google Sheets Template | We will publish a simple Google Sheets template which will pair with the Figma template to populate it.

## Future Plans

Once the cards can be produced in bulk, we will turn our attention to a process for ordering them on the welcomewagon.ai website. While we are building a solution for
ordering them, we plan to rely on direct sales contact with our customers.. 

Once the cards begin to achieve success in Real Life settings, we anticipate an overwhelming demand for them. When we have users coming to welcomewagon.ai because of the cards or
because of another referral in the EOS ecosystem, we will generate large quantities of valuable data on EOS users and their tendancies. This data will be valuable to 
dapps and other destinations. Through focused, short e-learning sessions, we will educate our users on the network and dapps, and our e-learning department will grow, 
as it takes on more clients that need material made for them. We are building this prototype on EOS, but will also onboard to EOS Coalition chains and engage using the
same mechanisms as on EOS (the Greymass account creation process, and NFTs). We will also be one of the first users for Greymass's process when it allows other custom
domains. We have 2-letter name-space domains on each network that we plan to use in that eventuality.

Apart from the potential for printed links, we will also offer our solution as a way to provide organizations with a bulk digital onboarding solution. eg. "This email
contains instructions for you to create your new EOS account and claim this community's membership NFT"

The future of blockchain interactions in print is very bright, especially when NFC chips and AR are added into the mix. We envision persistant signage at Points-of-sale,
NFC account faucets in public places, guerilla marketing such as stickers at drive-thru windows, and cards like ours passed out at mass gatherings of people - festivals,
concerts, sporting events, protests, etc. 


## Additional Information

**How did you hear about the Grants Program?**

We heard about the Grants Program thru regular EOS channels - Everything EOS, ENF press releases, etc. We have put in a lot of work on this project already, and
hope to receive remuneration for it in exchange for a well documented, accessible product. We are confident that our onboarding technique is something that all EOSIO
networks urgently require, and that these networks will see value in subsidizing its development, and we are also confident that by providing a method that all but 
eliminates sybil attack vectors, the networks will also subsidize the creation of the accounts. 

Much of the work for our first two deliverables has already been done. The design of the process, the layout of the cards, testing on users of various levels of technical
competence, etc, are an ongoing work in progress, but we feel confident that the cards are now useable - especially for the kind of person that one might find at a blockchain
conference or hackathon. The major work still outstanding is mostly technical - the API scripting and either web or in-house services to scale the operation up.

We have been in consultation with many specialists in the EOSIO community, especially Greymass and BountyBlok.
No other teams have contributed financially to this project. 

We are excited to offer our solution to the EOSIO community as it prepares for the rollout of its new branding.  
