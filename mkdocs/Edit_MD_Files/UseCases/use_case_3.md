# Use case 3

**How does connectivity of natural and built infrastructure components compare in a particular area across datasets?**   


### Problem  
After identifying data values that describe water systems components, researchers must determine how water supply, demand, and other system components are connected to correctly represent components in models. 

### Solution  
This use case employs the features of controlled vocabularies and the connectivity of nodes and links through networks to help modelers search for water system components and their connectivity across datasets. For example, what links flow into and out of Hyrum Reservoir in the Little Bear River Utah? 


Results show that Hyrum Reservoir supplies two demand sites in the WEAP 2010 model and three different demand sites in the USU WEAP 2017 and WASH models (Figure 1). The latter two models also return flow back into Hyrum Reservoir from Hyrum and Paradise Canals. The WASH model has the same schematic as the USU WEAP 2017 model but uses different labels for its nodes and links (Figure 1-C). Identifying and comparing connectivity between supply and demand sites across datasets can assist molders to more accurately incorporate simplified representations of supply and demand relationships like the WEAP 2010 model or more detailed representations like WEAP 2017 and WASH models into their water allocation models.

WaMDaM here enabled a more readily and consistent method to search for water system components as nodes and links and compare their connectivity across sources. This connectivity aspect of is an important improvement over the existing time series data discovery tools which identifies standalone nodes. With WaMDaM, users can identify how and where water flows from and into nodes. Future software tools may help users visualize and filter the results based on model, scenario, object type and categories. 


| Use Case        | Query           | Result  |
| ------------- |:-------------:| -----:|
|Hyrum Reservoir, Utah     | [Query][1] | [Result][4] csv |
|Bear River Migratory Bird Refuge, Utah    | [Query][2] | [Result][4] csv |
|Shasta Reservoir, California    | [Query][3] | [Result][6] csv |



![](/UseCases/images/networks.png) 
**Figure 1**: Schematics of water system node and link components that flow in or out of Hyrum Reservoir for three models in the Lower Bear River Watershed, Utah. Arrows indicate directions of flow. Nodes or links with the same color and shape belong to same controlled Object Type across models.

### Next  
The next use case allows users to compare similarities and differences in network topology, metadata, and data values between two scenarios of any model in WaMDaM. 


[1]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase3/1_FindNodeLinkInstances_Hyrum.sql
[2]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase3/2_FindNodeLinkInstances_refuge.sql

[3]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase3/3_FindNodeLinkInstances_Shasta.sql
[4]: