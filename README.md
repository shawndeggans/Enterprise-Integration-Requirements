# Enterprise-Integration-Requirements
The Enterprise Integration Requirements is a set of documents and tools to help an integration team consider, plan, and execute a medium to large scale integration project. 

## Higher-level Integration Goal
*Overall Goal of the Integration*

State the goal of the overall integration using your favorite user story format.

Example: To achieve the business goal of seamlessly moving geological survey data from the Azure Data Lake to Salesforce, the exploration team needs an integration between the two systems with guaranteed delivery of event data in the form of JSON. Additionally, the mobile development team needs a REST API that provides access to the exploration team's geological summary report. 

*Enterprise Architecture Decision for Integration*

State the defense for architectural choices.

Example: Because of its built in connectors and ease-of-use, the Integration Team has selected Mulesoft as the primary technology to help deliver data from the Azure Data Lake to Salesforce. Mulesoft will provide REST API in the form of a process layer and an experience layer for the mobile development team. The integration team will also make use of Azure Data Factory to transform and extract geological survey data, and the integration team will build microservices to fascilitate data enrichment for the experience layer. 

*High-level Business Requirements*

Gather basic business requirements in the form of Assert must, shall, will, will not.

Integration shall align geological survey data to the correct salesforce account of the geologist.
