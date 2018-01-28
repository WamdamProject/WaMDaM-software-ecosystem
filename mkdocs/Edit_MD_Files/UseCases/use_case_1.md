# Use case 1
**What data are available to develop a model in a particular watershed?**   

### Problem
Building a water resources model to solve water management and planning problems requires acquiring input data that describe the system. In existing practices, once a modeler selects a model and identifies its required types of input data, they manually search for datasets that contain relevant data. Then a modeler manually maps out the term for each attribute in their model with equivalent attributes in other datasets to math them.  

### Solution
This use case shows how a modeler can use WaMDaM extensible Objects, Attributes, and controlled vocabularies to more readily and consistently identify available data from the 13 loaded datasets for WEAP and WASH models. Users can use identified data to expand existing WEAP and WASH model instances in the Lower Bear River Watershed Utah (light red in Figure 4) to the entire Watershed (darker red in Figure 4).  

First, provide the model name (e.g., Dataset name is WEAP) and a min and max longitudes and latitudes of the study area (e.g., Box that includes Bear River Watershed). Second, execute the use case script that uses the registered controlled vocabularies to search for equivalent Attributes that have data values in all the datasets within the provided boundary. The script also identifies the list of Object Types and Attributes required by the model but do not have available data in WaMDaM database.  

For the two models in this use case, the WEAP model has 11 Object Types with 127 Attributes whiles the WASH model has three Object Types with 54 attributes. Using the Reservoir controlled term as a mediator between and the 13 datasets returns all the local native terms: Dam from the US Dams dataset and Reservoir Node from the BRSDM model instance. Similarly, the controlled attribute Volume returns Max_STOR from US Major Dam’s dataset, STORG_ACFT and Capacity from Utah Dams dataset, and Max Storage Capacity from the BRSDM model instance. 


![](/UseCases/images/UseCase1.jpg)
**Figure 1:** Example conceptual mapping showing how the use of controlled vocabulary can help retrieve different available native attributes in datasets for reservoirs in the WEAP model instance. 


In the query results, WaMDaM shows that five datasets can provide data for 22 attributes in the Bear River WEAP model and there are still 105 attributes that are needed to expand the WEAP model (Table 1). The five datasets are: US Dams Dataset, BRSDM model instance, Utah Dams Dataset, WaDE, and Idaho Flows dataset. Users can also select Categories to narrow their search for available data. For example, searching only for attributes in the Physical and Operational categories and excluding the Water Quality and Cost categories focuses on 65 attributes required in WEAP which reduces the search for the actually needed data in a model instance. The use case also shows that the five data sources can provide for six attributes in the Bear River WASH model while 48 more attributes are still needed. The WASH model uses many ecologic parameters that do not have data values among the datasets in WaMDaM. 
 

**Table 1:** Summary of data availability to expand WEAP and WASH models in the Bear River Watershed. Full list is available the use cases online page   

| Availability        | WEAP           | WASH  |
| ------------- |:-------------:| :-----:|
|      | count of unique attributes | count of unique attributes |
| Required      | 127     |   54 |
| Available  | 105      |    6 |
| No data for them | 43      |    48 |



**SQL queries for the WEAP Model**   

| Question        | Query           | Result  |
| ------------- |:-------------:| -----:|
| Identify model data requirements     | [script][1] | [Result][9] |
| Which attributes have available data     | [script][2]      |   [Result][10] |
| Where the data is available in datasets | [script][3]      |    [Result][11] |
| What additional data are needed | [script][4]      |    [Result][12] |


**SQL queries for the WASH Model**  

| Question        | Query           | Result  |
| ------------- |:-------------:| -----:|
| Identify model data requirements     | [script][5] | [Result][13] |
| Which attributes have available data     | [script][6]      |   [Result][14] |
| Where the data is available in datasets | [script][7]      |    [Result][15] |
| What additional data are needed | [script][8]      |    [Result][16] |



### Significance
This use case demonstrates how WaMDaM provides a more readily automated and consistent method to identify available (or unavailable) data in multiple datasets that are required by models in a study area. Note that the value of data in WaMDaM increases as far as identifying it for other models, as users add coordinates and register it with controlled vocabulary.  


### Next
This first step searched for input data to models. Next, users can further query specific nodes and attributes like streamflow, demand, reservoir storage, natural and built infrastructure connectivity with the reservoir and prepare it as input to their model as shown in the next use cases


[1]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/1.01Identify_WEAPmodel_requirements.sql
[2]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/1.111WHICHAvailableDataForModel_WEAP.sql
[3]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/1.112WHEREAvailableDataForModel_WEAP.sql
[4]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/1.21AdditionalDataForModel_WEAP.sql
[5]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/1.02Identify_WASHmodel_requirements.sql
[6]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/1.121WHICHAvailableDataForModel_WASH.sql
[7]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/1.122WHEREAvailableDataForModel_WASH.sql
[8]: https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/1.22AdditionalDataForModel_WASH.sql


[9]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/1.01Identify_WEAPmodel_requirements.csv
[10]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/1.111WHICHAvailableDataForModel_WEAP.csv
[11]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/1.112WHEREAvailableDataForModel_WEAP.csv
[12]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/1.21AdditionalDataForModel_WEAP.csv

[13]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/1.02Identify_WASHmodel_requirements.csv
[14]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/1.121WHICHAvailableDataForModel_WASH.csv
[15]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/1.122WHEREAvailableDataForModel_WASH.csv
[16]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/1.21AdditionalDataForModel_WEAP.csv

