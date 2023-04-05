# EOS Network Foundation Grant Proposal

- **Project Name:** EOSFLow
- **Team Name:** justmert
- **EOS Payment Address:** justmertacc1
- **[Level](https://github.com/eosnetworkfoundation/grant-framework#grant-levels):** 1
- **Pomelo Grant(s):** N/A
- **Project is Open-Source:** Yes
- **Project was part of Token sale:** No
- **Repository where Project resides:** https://github.com/justmert/eco-flow-frontend

## Contact

- **Contact Name:** Mert Köklü
- **Contact Email:** kklumert@gmail.com
- **Website:** https://github.com/justmert


## Project Overview

### Overview

- **Name:** EOSFlow
- **Brief Description:** EOSFlow provides a comprehensive platform that delivers various insights and metrics to track the activities and development of the EOS ecosystem and its associated open-source projects.
- **Relationship to EOS Network / Antelope:** EOSFlow provides comprehensive analytics to help users stay informed about the ecosystem's activities and development.
- **Reason for Interest:** Opportunity to provide a unique solution to the challenge of staying informed about the activities and development of EOS ecosystem.



### Project Details

As the EOS protocol ecosystem continues to grow, it's becoming increasingly challenging to stay informed about the ecosystem's status and trends, as well as the activities of the many open-source projects being built on or integrated with the protocol. With data scattered across various platforms through Github to Twitter, gaining a comprehensive view of the ecosystem can be a daunting task.

EOSFlow offers a cutting-edge solution to this problem, providing a comprehensive platform that delivers various insights and metrics to track the activities and development of the EOS ecosystem. Through intuitive and interactive visualizations and charts, EOSFlow empowers users to gain a clear understanding of code contributions, community engagements, trend data, and many other critical metrics related to the EOS ecosystem.

By tracking various off-chain sources, EOSFlow is the go-to platform for gaining a comprehensive view of the EOS and becomes uniqueness in the space.

* MVP Website: <https://eosflow.netlify.app/>

**Technical Schema**
![eosflow_technical_scheme](https://user-images.githubusercontent.com/37740842/230173958-1a7d4b71-6975-4e0c-ac4b-045b1f1ed5bb.png)


**Mockups**

| Dashboard Page | Project List Page | Project Page |
| --- | --- | --- |
| ![Screenshot 2023-04-05 at 21-32-12 EosFlow](https://user-images.githubusercontent.com/37740842/230174049-466f4886-5206-4bdc-9524-4bcc2cc71ddc.png)| ![Screenshot 2023-04-05 at 21-33-11 Projects](https://user-images.githubusercontent.com/37740842/230174104-f49d55a2-c665-4325-bf9d-ffa68304e0ae.png)| ![Screenshot 2023-04-05 at 21-32-36 Project Page](https://user-images.githubusercontent.com/37740842/230174137-cb6c2c3f-f580-480b-bbe9-2243b5819dba.png)|


### Ecosystem Fit

* Comprehensive analytics platform: EOSFlow provides a comprehensive platform that delivers various insights and metrics to track the activities and development of the EOS ecosystem and its associated open-source projects.

* Consolidated data sources: By consolidating data sources and presenting key metrics and insights in an intuitive and interactive format, EOSFlow addresses the challenge of scattered data sources, making it easier for users to understand the ecosystem's status and trends.

* Helping to make informed decisions: By providing valuable insights and metrics, EOSFlow can help ecosystem users make more informed decisions about which projects to support and contribute to as well as identify promising projects and high-risk ones.

* Gap in the market: EOSFlow fills the gap in the market by being the only project that becomes go-to core off-chain analytics dashboard for the EOS ecosystem.

* Discovering the evolution of the ecosystem: EOSFlow provides historical data and visualizations of key metrics, enabling developers and ecosystem users to better understand the development trajectory of EOS and its projects. This feature helps users identify areas where protocol gains trends and track the ecosystem's progress over time.

* Integration with approved grants and hackathons: EOSFlow can be integrated with approved grants and hackathons to keep track of the activity and development of these projects within the EOS ecosystem. By tracking the progress and development of grant recipients and hackathon projects, EOSFlow can provide valuable data and visualizations, which can be used to evaluate the success of these programs and their impact on the ecosystem.

* Encourage Community Collaboration: EOSFlow provides a centralized location for viewing project activity and contributions, encouraging community collaboration and engagement. By enabling users to easily identify areas where they can contribute to projects, thus empowers the community to work together towards a common goal, further strengthening the EOS ecosystem.

**Target audience**

The target audience for EOSFlow includes developers, researchers, and enthusiasts who are interested in monitoring the development and activity of EOS network and its open-source projects. The platform's analytical tools and visualizations can provide valuable insights into the performance of various projects, making it useful for those who want to gain a better understanding of the progress of the network and the direction it's headed in.


## Team

### Team members

- **Team Leader:** Mert Köklü

### Legal Structure
- **Registered Legal Entity:** Individual
- **Registered Address:** N/A

### Team Experience

As an experienced Web3 developer, I have become a grantee for Web3 Foundation, AAVE, Lens and Filecoin ecosystems by developing innovative projects. As a certified NVIDIA instructor, AAVE Turkey Community Co-Manager and ambassador for organizations such as Microsoft and The Graph protocol, I have become a trusted voice within the communities and gained a deep understanding of their needs and requirements. 

Currently, I'm focused on developing open-source and user-friendly applications that bring value to the EOS ecosystem.

### Team Org Repos

- [Peer-CLI](https://github.com/justmert/peer-cli): Swiss Army Knife for the IPFS (Received grant from Filecoin)
- [AaveQL](https://www.aaveql.org/): Aave GraphQL Documentation (Received grant from Aave) 
- [Aave API Telegram Bot](https://github.com/justmert/Aave-API-Telegram-Bot): Aave API Telegram Bot (Received grant from Aave)
- [chainweb.py](https://github.com/justmert/chainweb.py): Kadena Chainweb Python Bindings

### Team Member Repos

- https://github.com/justmert

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/mertkoklu/

## Development Status

The project is currently in the MVP stage which demonstrates the project's core functionality.

* **MVP Website:** <https://eosflow.netlify.app/>

You can find the source code of the project on Github with the links below:

* Open-source Backend: <https://github.com/justmert/eco-pulse-backend>
* Open-source Frontend: <https://github.com/justmert/eco-pulse-frontend>


## Development Roadmap

### Milestone Summary

- **Total Estimated Duration:** 2 months 
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 10,000 USD

### Milestone 1 — Build

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 5,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | I will provide both **inline documentation** of the code and a basic **how-to page** that explains how the user can interact with the platform. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 1. |  Database | Set up a Firebase project and Firestore database to store chart data and project metadata. |
| 2. |  Backend | To integrate Github Data to the EOSFlow, develop a Python backend that uses both the Github Rest and GraphQL APIs to fetch latest data from the Github. |
| 3. |  Frontend | Build the Project Detail and Dashboard pages, including the following implementations: Commit History By Weeks, Code Frequency, Top Contributors, Issue Activity, Issue Count, Star Count, Pull Request Count, Recent Issues, Recent Commits, Pull Request Activity, Recent Stargazing Activity. |
| 4. |  Frontend | Develop a Project List page that lists all EOS ecosystem projects in order of their respective stargazing counts. |
| 5. |  Integration | Integrate Algolia to improve the search functionality of the platform. |
| 6. |  Integration | Integrate Typeform to allow ecosystem users to suggest new projects for the platform. |
| 7. |  Integration | Integrate Google Analytics to track user engagement and improve the platform accordingly. |
| 8. |  Backend | Set up a regular update schedule for the backend to keep the database up-to-date with the latest data. |


### Milestone 2 - Expand

- **Estimated Duration:** 1 month
- **FTE:**  1
- **Costs:** 5,000 USD

| ID | Deliverable | Specification |
| ----- | ----------- | ------------- |
| 1. |  Feature | Integrate Twitter data of EOS and its associated projects into the platform, including metrics such as the number of tweets posted per day or week, the number of likes, retweets, and replies received, and other relevant analytics. |
| 2. |  Feature | Develop categorization feature to classify projects based on various criteria within the EOSFlow, such as DeFi, DEX. The feature will make it easier for users to find projects that are of interest to them. |
| 3. |  Feature | Develop project health score feature that evaluates multiple metrics to provide users with an overview of a project's health. The score helps identify promising projects and high-risk ones. The resulting score, weighted by metric importance, will display on the project detail page. |
| 4. |  Feature | Develop an API for EOSFlow that provides developers with access to EOSFlow charts and metadata. The API will use RESTful architecture and documented using OpenAPI Specification. Using the API, developers can embed charts and data into their own applications. |
| 5. |  Feature | Up-to-date ecosystem project list on EOSFlow will be customized based on the protocol's preference. If the protocol wishes project list to be updated independently, a GitHub crawler will be implemented to automatically discover ecosystem projects and adds them to the EOSFlow. Alternatively, if the protocol has a project list available on a platform such as Notion, we will use the platform's respective API to access the list. In addition, if the protocol has a website that displays its ecosystem projects, such as an awesome list or other third-party application, we can parse the GitHub links and incorporate them into EOSFlow. We will collaborate with the protocol to determine the most effective approach and ensure the project list is kept up-to-date and accurate. |


## Future Plans

In the short term, we intend to use EOSFlow to provide a comprehensive and user-friendly platform for developers and ecosystem users to track and analyze projects in the EOS ecosystem. We will continuously enhance and update the platform to ensure that it is the go-to resource for up-to-date information on EOS projects. 

In the long term, our team's plan is to continue supporting and improving EOSFlow to meet the evolving needs of the EOS community. This includes incorporating additional metrics and data sources to provide more detailed insights into projects. Besides, if the platform is well-received by the community, and gains traction, we are going to open a Twitter account for EOSFlow to engage with the community and promote top open-source projects on the EOS ecosystem. 


## Additional Information

**How did you hear about the Grants Program?** EOS Network Foundation Website

If you have any questions or requests, please feel free to contact me. Thank you.

* Email: kklumert@gmail.com
* Telegram: @mertkklu
* Discord: MertK#2634
