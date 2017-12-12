# Limitations and Future Work

The design of WaMDaM and its quest towards generality have limitations in these two main areas which constitute opportunities for future work. 

## Limitation 1: Use cases
The identified six use cases are basic examples and do not necessarily cover the complexity of the domain of systems water management nor do they cover all the possibilities of how the community of users want to use data. The reviewed data systems and the key features are not necessarily comprehensive of the large inventory of existing systems and the complexity of their data. The used twelve data sources are example datasets and do not necessarily represent the diversity of used data in the field. The example controlled vocabulary are preliminary and need a robust method on how to define and expand them. 

Future work may test and improve WaMDaM abilities to work with a larger set of use cases, other models and their results, and data sources in other study areas. With a larger set of data, future work is needed to create a more robust method to define, relate, specify terms for water management data and expand the list of available vocabularies similar to the work on semantic annotation for hydrologic sciences by Piasecki and Beran (2009). This is especially needed for the “Instance Name” controlled term because of the large number of infrastructure instances that could reach thousands or even millions. So there is a need for a robust method to name and organize a potentially growing controlled instance names. The method could benefit from the USGS convention of naming their gage stations that include the institution, site code, name and nearby town or and state.

## Limitation 2: Software 
The designed tools to support loading data into WaMDaM database are basic and require further testing and improvement to be more user-friendly. SQLite database and the WaMDaM Wizard in a desktop setting allow one user at-a-time to store and access data. Future work may build a software ecosystem to allow multiple users to store, access, visualize, and share data using a suite of webservers and tools. Such ecosystem would need to define a standardized machine-readable data encoding method to exchange data over the web and between models. Building additional data importers into WaMDaM would speed data loading and validations in WaMDaM and thus enable larger data integration and discovery. Further participation by others will expand usefulness of a future WaMDaM data system.

## Limitation 3: Community/Users 

Throughout WaMDaM development, we presented and discussed WaMDaM goals, use cases, designs, and results in eight regional, national, and international conferences, workshops, and professional meetings. We solicited informal feedback at different stages of the development from collaborators at seven different universities. It is by no means a representative of the water resources community but provided us with important insights. Future improvements should involve a larger community with more formal structure like surveys to guide a more robust and generic information model. 

We introduce WaMDaM method as a beginning to solve the problem within the bounded limitations above. It will become more useful as users

* Build more software tools to automate loading data into WaMDaM
* Feed WaMDaM with more diverse datasets in other areas
* Accurately register the datasets native terms
* Share and publish their WaMDaM data with others.


Although the development of WaMDaM has focused on water management data, none of the information model concepts are necessarily exclusive to water management. In principal, WaMDaM could be used for other systems based data like for water, energy, and food nexus but that is yet to be tested and demonstrated with use cases. 

## Invitation
We invite the systems modeling and hydroinformatics community to experiment with and provide feedback on WaMDaM to improve it and work towards the goal of developing a standard as the basis for a software ecosystem to organize, visualize, publish, and discover systems water management data over the web. 



 