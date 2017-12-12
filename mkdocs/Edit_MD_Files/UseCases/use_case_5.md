# Use case 5

**Identify inflow and outflow into and out of a node water system component and compare them across data sources or models**   

**Example**   
What is the inflow and outflow of Hyrum Reservoir, Utah?   

### Problem  
Learning about flow direction in water management networks can be time-consuming compared to natural hydrology networks. 

### Solution  
We use one query to identify inflow and outflow links based on a controlled node instance name “Hyrum Reservoir” that serve as a start or end nodes to them. Similarly, the same query is applied to the “Bear River Migratory Bird Refuge” at the mouth of Bear River to the Great Salt Lake. We only present results for Hyrum Reservoir for simplicity but both are available on GitHub. The query results in a table for the links that flows into or out of Hyrum Reservoir in three model scenarios in the Little Bear River Utah. We draw a schematic for each one which visually reveal similarities and differences among them (Figure 10). 

The first model in Figure 10-A (left) is built in a GenRes UDWR model that is transferred into WEAP in 2010 for the Lower Bear River to allocate water based on priority. The middle one is a WEAP model that intends to improve the WEAP 2010 model to represent more specific supply and demand connectivity, among other improvements. The third model (right) is a WASH model to allocate water to maximize habitat suitable areas while meeting demand requirements. In the Figure 10-A (left) shows that Hyrum Reservoir supplies two demand sites and is constructed on the Little Bear River. In Figure 10-B (middle), none of the two demand sites exist in the new model but there are three demand sites with different names. On the other hand, the new model scenario has two demand sites, Hyrum and Paradise Canals that return flow back into Hyrum Reservoir. Figure 10-C (right) shows an identical schematic to Figure 10-B but the WASH model uses codes to name all its node and links. Registering controlled vocabulary for each node and link instance allows relating such coded and names instances. It is important to note that WaMDaM requires each node and link instance to have a source and method that would explain what it represent like an actual site or an aggregation of sites. Such network metadata would help explain interpreting its representation and comparing it with others. Comparing these three models allows users to identify how different models have modeled water supply and demand in the same region. They can incorporate one or many of these schematics to their new models. 

WaMDaM here enabled a more readily and consistent method to search for water system components as nodes and links and compare their connectivity across sources. This connectivity aspect of is an important improvement over the existing time series data discovery tools which identifies standalone nodes. With WaMDaM, users can identify how and where water flows from and into nodes. Future software tools may help users visualize and filter the results based on model, scenario, object type and categories. 


| Use Case        | Query           | Result  |
| ------------- |:-------------:| -----:|
|NumericValues_otherTypes     | [Query][1] | [Result][2] csv |
|MultiAttributeValues    | [Query][3] | [Result][4] csv |



![](/UseCases/images/networks.png) 
**Figure 1**: Schematics of identified water system node and link components that flow in our out of Hyrum Reservoir from three models in the Lower Bear River Watershed, Utah. Arrows indicate the direction of flow. Nodes or links with the same color and shape indicate they belong to same Object Type in the same model.

### Next  
The next use case allows users to compare similarities and differences in network topology, metadata, and data values between two scenarios of any model in WaMDaM. 


[1]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/5.1FindNodeLinkInstances_Hyrum.sql
[2]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/5.1FindNodeLinkInstances_Hyrum.csv


[3]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/5.2FindNodeLinkInstances_refuge.sql
[4]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/5.2FindNodeLinkInstances_refuge.csv