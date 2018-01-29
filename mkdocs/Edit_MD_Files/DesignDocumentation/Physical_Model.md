# Physical Model Implementation

## Implementation  
We implemented the logical data model schema represented in XML into four physical Relational Database Management Systems (RDBMS: PostgreSQL, MySQL, Microsoft SQL Server, and SQLite) to demonstrate that WaMDaM is independent of the RDBMS and increase value to users. First, we selected a physical data type for each field in the logical model entities (e.g., integer, character, binary) and we imposed physical constraints on each field (e.g., value cannot be null) by following the physical data types convention in ODM2 (Horsburgh et al., 2016). 

Second, we adapted an existing Python 2.7 script [ODM2-build_schemas](https://github.com/ODM2/ODM2/tree/master/src/build_schemas
) to forward engineer the logical model XML schema format into the Data Definition Language (DDL) which is a set of create statements for WaMDaM tables for each of the four RDBMS. Finally, we executed the DDL script within each RDBMS to create a physical blank WaMDaM database that users can then load with data.

The adapted script and a GUI to use it for other desings will be posted here
https://github.com/WamdamProject/WaMDaM_DDL_generator_Wizard

   
## Copies of WaMDaM Dbs 
 Script to create blank WaMDaM databases OR copies of each database to restore   
1. [Microsoft SQL Server](https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/database_schemas/MS_SQL_Server)    
2. [MySQL](https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/database_schemas/MySQL)  
3. [PostgreSQL](https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/database_schemas/PostgreSQL)  
4. [SQLite](https://github.com/WamdamProject/WaMDaM_Information_Model/tree/master/database_schemas/SQLite)  



[1]: https://www.sqlite.org/index.html
[2]: https://addons.mozilla.org/en-US/firefox/addon/sqlite-manager