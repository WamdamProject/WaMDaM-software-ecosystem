# Welcome to the WaMDaM Organization
This is a meta-repository to help users navigate the many repositories under the [WaMDaMProject GitHub Organization](https://github.com/WamdamProject).

The repo also hosts the [MKDocs design files][1] and their output HTML pages [(docs)][2] for [Docs.WaMDaM.org][3] 

The Water Management Data Model (WaMDaM) is an information model and a couple of supporting software ecosystem. WaMDaM tools are designed to organize, identify, and compare multiple systems water management data in a single database. 

Think of WaMDaM as a repository of water management data (blue cylinder) and a translator between numerous data sources on the left and different models on the right. WaMDaM translates two aspects of the data: the syntax (i.e., structure) and semantics (terminology). WaMDaM intends to speed the time to find, organize, and synthesize data from different data sources, and prepare data for modeling.
![](/mkdocs/Edit_MD_Files/images/Workflow.png)


[1]:/mkdocs
[2]:/docs
[3]:http://Docs.WaMDaM.org
# ODM2 GitHub Repositories and Software Ecosystem


## 1. [WaMDaM Schemas and Information Model copies][4]  

* [Entity Relationship diagrams for WaMDaM schema 1.0][5]

* [DDL scripts and copies for RDBMS: MS SQL Server, MySQL, PostgreSQL, and SQLite][6]

[4]:https://github.com/WamdamProject/WaMDaM_Information_Model
[5]:http://schema.wamdam.org/diagrams/01_WaMDaM.html
[6]:https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/database_schemas


## 2. [WaMDaM Data Loader Wizard][7]  
A Python-based Graphical User Interface to validate and load water management data mainly from an Excel Template into a SQLite WaMDaM compliant database.  
By using the Wizard, users are not expected to understand the underlying WaMDaM database of schema. Users just need to understand how to fit their data into these concepts: ObjectType, Attribute, Instance, Network, and Scenario. 

[7]:https://github.com/WamdamProject/WaMDaM_Wizard

## 3. [WaMDaM Controlled vocabulary][8]  
A Python/Django-based web application for managing the WaMDaM controlled vocabularies
* Online submittal and moderation of new terms and changes to existing terms
* Views of all existing vocabularies and terms
* Application deployed at [vocabulary.wamdam.org](http://vocabulary.wamdam.org)

[8]:https://github.com/WamdamProject/WaMDaM_ControlledVocabularies

## 4. [WaMDaM Application and use cases][9]  
Demonstrate how WaMDaM enables systematic data query and comparisons across multiple different models and datasets.
 
*   
*  

[9]:https://github.com/WamdamProject/WaMDaM_UseCases
 

## 5. [WaMDaM Publications and Presentations][10] 
List of all the presentations and publications on WaMDaM products since inspection 

[10]:https://github.com/WamdamProject/WaMDaM_Publications


## Do you have feedback on WaMDaM? Tell us what interest you 
[Quick survey](https://goo.gl/forms/SQROuovc2Cs4bmZB3)


## Licensing  
WaMDaM and materials in this GitHub repository are disturbed under a BSD 3-Clause [LICENSE](/LICENSE). 
For alternative licensing arrangements, contact Adel M. Abdallah or David E. Rosenberg directly.    
  

## Sponsors and Credit 
WaMDaM and related software development have been developed under funding from several different sources. It was primarily supported by the National Science Foundation <a href="http://www.nsf.gov/awardsearch/showAward?AWD_ID=1135482" target="_blank">CI-Water Project</a> and later from the <a href="https://www.nsf.gov/awardsearch/showAward?AWD_ID=1208732" target="_blank">iUtah Project</a>. 
Any opinions, findings, and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the National Science Foundation.    

WaMDaM has been developed at and also additionally funded by the Utah Water Research Lab at Utah State University, Logan Utah during the period of August, 2012-2017. Thanks to Dr. Steven Burian at the University of Utah, Salt Lake City Utah for hosting Adel Abdallah as a visiting scholar 2014-2017.

David Tarboton, Josué Medellín-Azuara, and Stephen Knox provided thoughtful feedback and comments on earlier designs and manuscript drafts. We thank our collaborators and our research group for their feedback. 

