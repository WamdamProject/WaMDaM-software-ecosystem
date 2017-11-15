# Welcome to the WaMDaM Organization
This is a meta-repository to help navigate the many repositories under the [WaMDaMProject GitHub Organization](https://github.com/WamdamProject).

WaMDaM is both an information model and a couple of supporting software ecosystem. WaMDaM tools are designed to organize, identify, and compare systems water management data in a single database. 

Think of WaMDaM as a repository of water management data (purple cylinder) and a translator between numerous data sources on the left and different models on the right. WaM-DaM translates two aspects of the data: the syntax (i.e., structure) and semantics (terminology). WaMDaM intends to speed the time to find, organize, and synthesize data from different data sources, and prepare data for modeling.
![](/files/WaMDaM_workflow.jpg)


## Getting started: Work with WaMDaM application use cases (Reproduce reported results)

1.	Download the SQLite file with loaded data for the twelve US and Bear River Watershed datasets 
2.	Download the WaMDaM Wizard 
3.	Download the Mozilla Firefox SQLite Manager Add-on to interact with the SQLite database and query WaMDaM tables    
4.	If you’re familiar with Python, you may use of adapt Python scripts to visualize results


## Getting started: Use WaMDaM for your own data. How Can I use WaMDaM?   
1.	Get your data files 
    Understand their concepts in the WaMDaM framework
2.	Download the Excel workbook templates
    Prepare your data and fit it into WaMDaM workbooks.  Optionally register your data with select controlled vocabulary to help you relate and search synonymous terms across datasets.  
3.	Download the WaMDaM Wizard 
    Use the Wizard to load the data files into a WaMDaM SQLite database on your machine (no server needed)  
4.	Download the Firefox SQLite Manager
    Use or adapt SQL queries on GitHub and execute them in SQLite Manager 
    If you’re familiar with Python, you may use of adapt Python scripts to visualize results   

   

### What can you do with WaMDaM not possible before? Why WaMDaM?
WaMDaM is an effort to standardize how we organize water management data which supports eight features altogether that partially exist in prior methods to enable users to: 
1. Support different water resources systems components that are used in water management models like hydrology, infrastructure, and demand sites as reusable modules or sets of systems components.   
2. Represent connectivity and interactions between components in space through networks of nodes and links as used in systems modeling. 
3. Support scenarios that track topologic changes in networks, metadata and data values. 
4. Support multiple data types that are used in systems modeling like time series and multidimensional arrays.  
5. Uses consistent contextual metadata to unambiguously interpret data values.
6. Uses controlled vocabulary to relate inconsistent terms across data sources and models.  
7. Enables conditional data queries to access and compare subsets of data and metadata 
8. Developed in an open-source software environment.  



### WaMDaM Schemas and Information Model documentation  
* View primary [documentation](https://github.com/WamdamProject/WaMDaM_Information_Model) for the WaMDaM Information Model* 

* Support for multiple RDBMS: MS SQL Server, MySQL, PostgreSQL, and SQLite
* [https://github.com/WamdamProject/WaMDaM_Information_Model](https://github.com/WamdamProject/WaMDaM_Information_Model) 


### WaMDaM Application and use cases  
Demonstrate how WaMDaM enables systematic data query and comparisons across multiple different models and datasets.
[https://github.com/WamdamProject/WaMDaM_UseCases](https://github.com/WamdamProject/WaMDaM_UseCases
) 


### WaMDaM Wizard  
A Python-based Graphical User Interface to validate and load water management data mainly from an Excel Template into a SQLite WaMDaM compliant database.  
* [WaMDaM Wizard](https://github.com/WamdamProject/WaMDaM_Wizard) 
By using the Wizard, users are not expected to understand the underlying WaMDaM database of schema. Users just need to understand how to fit their data into these concepts: ObjectType, Attribute, Instance, Network, and Scenario. 

### WaMDaM Controlled vocabulary  
A Python/Django-based web application for managing the WaMDaM controlled vocabularies
* Online submittal and moderation of new terms and changes to existing terms
* Views of all existing vocabularies and terms
* Application deployed at [vocabulary.wamdam.org](http://vocabulary.wamdam.org)
* [https://github.com/WamdamProject/WaMDaM_ControlledVocabularies]()


### WaMDaM Publications and Presentations  
List of all the presentations and publications on WaMDaM products since inspection 
[https://github.com/WamdamProject/WaMDaM_Publications](https://github.com/WamdamProject/WaMDaM_Publications)


## Do you have feedback on WaMDaM? Tell us what interest you 
[Quick survey](https://goo.gl/forms/SQROuovc2Cs4bmZB3)


### Licensing  
WaMDaM and materials in this GitHub repository are disturbed under a BSD 3-Clause [LICENSE](/LICENSE). 
For alternative licensing arrangements, contact Adel M. Abdallah or David E. Rosenberg directly.    
  

### Sponsors and Credit 
WaMDaM and related software development have been developed under funding from several different sources. It was primarily supported by the National Science Foundation <a href="http://www.nsf.gov/awardsearch/showAward?AWD_ID=1135482" target="_blank">CI-Water Project</a> and later from the <a href="https://www.nsf.gov/awardsearch/showAward?AWD_ID=1208732" target="_blank">iUtah Project</a>. 
Any opinions, findings, and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the National Science Foundation.    

WaMDaM has been developed at and also additionally funded by the Utah Water Research Lab at Utah State University, Logan Utah during the period of August, 2012-2017. Thanks to Dr. Steven Burian at the University of Utah, Salt Lake City Utah for hosting Adel Abdallah as a visiting scholar 2014-2017.

David Tarboton, Josué Medellín-Azuara, and Stephen Knox provided thoughtful feedback and comments on earlier designs and manuscript drafts. We thank our collaborators and our research group for their feedback. 

