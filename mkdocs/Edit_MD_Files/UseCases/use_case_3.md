# Use case 3
**Identify and compare demand data for a site as reported in many sources**   

**Example** 
What is the total agriculture water use or demand in Cache County, Utah?   

### Problem  
Identifying water use and demand data is probably the most difficult task in populating models with data. Likely in part because the source of data is specific to each study area compared to water supply data that are often available from national or regional sources like USGS and BOR. In Appendix B, we identify nine issues that users need to consider while working with and importing demand data into WaMDaM. They provide a better context to the results of the use case.  

### Solution   
In the use case query, we aggregated and converted demand values to answer the use case question of how much water demand for agriculture in a geo-spatial boundary for Cache County in Utah, controlled attribute name “flow”, and instance category of “Agriculture”. We aggregated the data within the county for each data source and converted the units to acre-feet (Figure 8). The Figure shows data from four different sources: WEAP and WASH models, and the Water Data Exchange database (WaDE) by the Western States Water Council (http://www.westernstateswater.org/wade/). The comparison here intends to show how WaMDaM enables querying all of them together and what each data source has data for. Users then can make an informed decision to choose the aggregation level or site specific demand data to their own model. Users also could possibly incorporate the total values for two equivalent estimates (two top curves) to test a model sensitivity to different demands.   


We note that the number of available demand sites within the area is not necessarily an indicator of the demand volume per year but here it may indicate whether the reported value is aggregated from many or comes from one site. In Figure 8, one comparison point is that three models often represent demand as constant through years while the WaDE as new data source, can improve these models by considering variable demand. A second point is that data sources either have data for all the country area like in the WEAP Model 2017 and WaDE. Or they may cover part of the area like in the WASH and WEAP 2010 models based on the locations of the sites in the County compared to the WEAP 2017 model. The first two top curves in Figure 7 are comparable to each other as they cover the whole county in Utah and they have attributes of diverted or delivered water compared to consumptive water as in the third curve (from top) for WaDE. Obviously, the low values of the bottom two curves indicate that both WASH and WEAP 2010 models represent part of Cache County’s demand as their study area and sites do not include all the county.  

Table 1: Key different conceptual terms for demand available in models and data sources
![](/UseCases/images/DemandTerms.png) 


All these differences are context specific and require knowledge of them before making comparisons which still make it challenging to correctly interpret data values and compare them. WaMDaM begins to enable such comparisons by organizing all the data sources into one database with mapping of terms through controlled vocabulary. We do not foresee WaMDaM to fully automate how the data is aggregated or grouped in this use case or others. There could be assumptions embedded in how the data is represented and grouped. WaMDaM however documents metadata which could help users more accurately interpret data values. 

| Use Case        | Query           | Result  |
| ------------- |:-------------:| -----:|
|IdentifyDemandSites     | [Query][3] | [Result][4] csv |
| Identify Demand Sites Seasonal Values     | [Query][5] | [Result][6] csv |
| Identify DemandSites Time Series Values     | [Query][7] | [Result][8] csv |
| Water Rights     | [Query][9] | [Result][10] csv |


| Use Case figure       | Python Script   | Interactive figure  |
| ------------|:----------:| -----:|
|Figure a     | [script][1] | [Figure][2]  |



![](/UseCases/images/UseCase3.png) 
Figure 1: Differences in aggregated water demand for Cache County Utah across WEAP and WASH models and the WaDE web-service. Native attribute terms are in quotes. The curves are color coded from dark to light blue to indicate higher to lower overall demand volumes

In addition to demand data, the query also can return water rights data from the WaDE data source under the controlled Object Type “Demand Site” and attribute name of “Flow”. For example, the “WATER RESEARCH LAB. UTAH STATE UNIVERSITY” has two water rights. One of them is 84 AF/Year and 146 cfs for the beneficiary use descriptor value of “Power”. So WaMDaM organizes descriptive and numeric data for water rights.

### Next  
After identifying supply and demand data, the next use case identifies data that describe water infrastructure like reservoir bathymetry curves.      

[1]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/6Figures_Python/3.3dentifyDemandSites_TimeSeriesValues.py
[2]:http://htmlpreview.github.io/?https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/7Figures_HTML/3.3dentifyDemandSites_TimeSeriesValues.html

[3]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/3.1IdentifyDemandSites.sql
[4]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/3.1IdentifyDemandSites.csv

[5]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/3.2dentifyDemandSites_SeasonalValues.sql
[6]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/3.2dentifyDemandSites_SeasonalValues.csv

[7]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/3.3dentifyDemandSites_TimeSeriesValues.sql
[8]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/3.3dentifyDemandSites_TimeSeriesValues.csv


[9]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/3.4WaterRights.sql
[10]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/3.4WaterRights.csv




