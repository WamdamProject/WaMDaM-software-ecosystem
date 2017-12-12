# Physical Model Implementation

## Implementation  
We selected the physical data types (e.g., integer, character, binary) for the fields of tables and we imposed physical constraints on each field (e.g., value cannot be null) by following the physical data types convention in ODM2 (Horsburgh et al., 2016).    

We saved the ER diagram of the logical model of WaMDaM in DbWrench in an Extensible Markup Language (XML) format file. Then we adapted an existing script in Python 2.7 used in (Horsburgh et al., 2016; Tony Castronova, 2015) to forward engineer the XML ER diagram into the Data Definition Language (DDL) which is a set of create statements for tables for four RDBMS implementations: PostgreSQL, MySQL, Microsoft SQL Server, and SQLite.   

The DDL scripts, physical data model implementations for the four RDBMS, and details about the used physical data types and constraints are described in the GitHub repository. The differences between these databases are marginal and mostly related to physical data types that are native to each database and minor syntax differences.  
   
## Copies of WaMDaM Dbs 
 Script to create blank WaMDaM databases OR copies of each database to restore   
1. [Microsoft SQL Server](https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/schemas/MS_SQL_Server)    
2. [MySQL](https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/schemas/MySQL)  
3. [PostgreSQL](https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/schemas/PostgreSQL)  
4. [SQLite](https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/schemas/SQLite)  

## Working with SQLite    
Users can choose to work with any of these WaMDaM databases. We elected to use [SQLite][1] and populate it with data to demonstrate the use cases and benefits of WaMDaM to the water resources community as discussed in the next section. SQLite is free, open-source, and server-less. We also used the [SQLite Manager Add-ons][2] to Mozilla Firefox as an open-source user interface to visualize and interact with WaMDaM tables. 


[1]: https://www.sqlite.org/index.html
[2]: https://addons.mozilla.org/en-US/firefox/addon/sqlite-manager