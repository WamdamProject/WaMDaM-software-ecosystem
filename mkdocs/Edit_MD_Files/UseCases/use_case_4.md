# Use case 4
**What differences are there in network topology, metadata, and input data between two scenarios of a model instance?**  
 
### Problem   
Modelers use scenarios to simulate how potential management alternatives can affect the system performance in their defined metrics. Modelers often seek to verify and communicate differences for changes they introduce to network topology, metadata, and data values between scenarios. However, when a model or a dataset does not natively support scenario comparisons, modelers have to manually compare the input values. This comparison is challenging for models with a large number of attributes such as WEAP. 

### Solution  
This use case employs the scenario and parsimony design features to track changes among scenarios and efficiently store data. To perform scenario comparisons in data loaded to WaMDaM, the Wizard has a comparison function that requires users to select a Model, a Master Network, and two Scenarios. Then a Wizard script queries the ScenarioMappings table and identifies the data that is shared among and unique to each Scenario. Results are exported to an Excel workbook. 

The WEAP 2010 and 2016 scenarios share about 9% of the network instances, 1% metadata, and 5 % data values (Table 6). Similarity, the BRSDM model scenarios of dry, normal, and wet have identical network and metadata, share about 80% of data values with 10% unique values to each scenario (details not presented for simplicity). The larger percentage of shared elements among the BRSDM model scenarios means a correspondingly larger savings in database storage (records in the Mappings, Instances, Connections, and DataValuesMapper tables) than the WEAP model scenarios.


Table 1: Comparison summary of unique and shared network topology, metadata and data values between two WEAP Bear River Watershed model scenarios
![](/UseCases/images/UseCase4.png) 

### SQL scripts

The SQL scripts to compare scenarios exist here 
https://github.com/WamdamProject/WaMDaM_Wizard/blob/master/src_1.0/controller/wamdamAPI/GetComapreScenarios.py

An older version of the scripts exist on a private repo. I need to update them and move them here 
https://github.com/amabdallah/Wizard/tree/Dev/SQL_Queries
