# Use case 2

**What differences are there across datasets in the data values of properties of a water system component?** 

### Problem  
Once modelers have identified the data available for a modeling study, next they need to determine which datasets and values to use in their model. Modelers often use many data management methods to query, manipulate, and join different water management data types (e.g., time series, multi-column arrays) to analyze and prepare them for systems models. Modelers also manually search for descriptive metadata stored separately in many files like PDF documents or HTML pages.   

### Solution   
This use case shows how a modeler can use WaMDaM’s multiple data types, controlled vocabularies, conditional queries, and metadata design features to both query and compare values across datasets.
 We query and compare results for 1) time series and seasonal streamflow below Stewart Dam, Idaho, 2) water use in Cache Valley, Utah, 3) storage elevation curves for Hyrum Reservoir in Utah, and 4) dam height, hydropower purpose, and number of generators for Flaming Gorge and Shasta Reservoirs.  

### Use Case 2.1  
**What differences are there across datasets in flow data values below Stewart Dam in Idaho?**   

Use Case 1 identified four flow datasets available for the site below Stewart Dam in Idaho. These datasets were identified using the controlled node instance name “USGS 10046500 BEAR RIVER BL STEWART DAM NR MONTPELIER, ID” and the controlled attribute name “Flow”. The datasets are maintained by USGS, Utah Division of Water Resources (UDWR), Idaho Department of Water Resources (IDWR), and the Bear River Commission (Figure 5-A). We use the time series metadata: attribute unit, year type, aggregation statistic, and aggregation interval unit to aggregate and convert all the time series datasets into a comparable cumulative monthly flow in acre-feet in calendar years. The field Year Type (Section 4.2) allowed us to correctly shift years to the same calendar year that started January 1.  

**SQL scripts and results**   

| Use Case        | Query           | Result (csv) |
| ------------- |:-------------:| -----:|
| Identify TimeSeries Seasonal Dual data      | [Query][1] | [Result][4]  |
| Identify aggregate TimeSeries Values      | [Query][2] | [Result][5]  |
| Identify Seasonal Values | [Query][3] | [Result][6]  |

**Python 2.7 script to plot figures of use case**  
To run the Python script, you need to be connected to the Internet. The script reads its data from the csv files hosted on GitHub.


| Use Case figure       | Python Script   | Interactive figure  |
| ------------|:----------:| -----:|
|Figure a     | [script][7] | [Figure][11]  |
|Figure b     | [script][8] | [Figure][12]  |


 
The resulting traces span 92 years from 1923-2015 and show most datasets are identical except for a few discrepancies in 1996 and 1999 [Figure 1-B](/UseCases/use_case_2/#figure-1). Metadata shows that the PacifiCorp power company collected streamgage data before and after USGS record. PacifiCorp shares raw data (not available to us) with each state that states then interpolates values if data is missing. The IDWR flagged deviated data values for potential errors while the UDWR interpolated missing values. This data discrepancy underscores the importance of comparisons and using source, method, and organizations, and time series contextual metadata to convert and interpret data values for each flow data and help users choose a time series for this site like the UDWR dataset with the longest record. 
 
#### Figure 1  

![](/UseCases/images/UseCase2.1-a.png) 
**Figure 1:** Compiled time series data of flow below Stewart Dam, Idaho reported by different agencies over time. [A] 1923 to 2015 and [B] a six-year window that highlights similarities and discrepancies among sources.   
 
Flow data in water management datasets also exist in derived seasonal form and modelers may use them as input to models. The same query also returned seasonal data from a fifth source, the BRSDM model, which has three scenarios for monthly flow (dry, normal, and wet) for the same Stewart Dam site [Figure 2-A](/UseCases/use_case_2/#figure-2). The BRSDM model respectively reported average flows for June as 666, 2,506, and 17,181 acre-ft/month for dry, normal, and wet years. The model materials did not document how seasonal monthly values were derived. But by comparing results to June flow values in the longest UDWR time series record (1923 to 2015) we estimated  the dry and wetter flow scenarios have 48% and 3% probabilities of exceedance [Figure 2-B](/UseCases/use_case_2/#figure-2). These results can help define more representative flow values for models with seasonal-based analysis. 
 
 
**Python 2.7 script to plot figures of use case**   
To run the Python script, you need to be connected to the internet. The script reads its data from the csv files hosted on GitHub.  

| Use Case figure       | Python Script   | Interactive figure  |
| ------------|:----------:| -----:|
|Figure A     | [script][9] | [Figure A][13]  |
|Figure B     | [script][10] | [Figure B][14] |

 
#### Figure 2  
![](/UseCases/images/UseCase2.1-b.png) 
**Figure 2:** [A] Average monthly flow data at Below Stewart Dam site (same site in Figures 1). Color coded from light to dark blue for dry, normal, and wet year scenarios. [B] A cumulative distribution of the all June flow data in the Utah UDWR dataset to evaluate how well the dry and wet years represent the historic record peak flows. 
 


[1]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.1/1_IdentifyTimeSeriesSeasonal_Dual.sql

[2]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.1/2_Identify_aggregate_TimeSeriesValues.sql

[3]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.1/3_Identify_SeasonalValues.sql

[4]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/2.1IdentifyTimeSeriesSeasonal.csv

[5]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/2.2Identify_aggregate_TimeSeriesValues.csv

[6]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/2.3Identify_SeasonalValues.csv

[7]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/6Figures_Python/2.2Identify_aggregate_TimeSeriesValues.py
[8]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/6Figures_Python/2.2bIdentify_aggregate_TimeSeriesValues.py
[9]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/6Figures_Python/2.3Identify_SeasonalValues.py
[10]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/6Figures_Python/2.4_plotcdf.py


[11]:http://htmlpreview.github.io/?https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/7Figures_HTML/2.2Identify_aggregate_TimeSeriesValues.html
[12]:http://htmlpreview.github.io/?https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/7Figures_HTML/2.2bIdentify_aggregate_TimeSeriesValues.html
[13]:http://htmlpreview.github.io/?https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/7Figures_HTML/2.3Identify_SeasonalValues.html
[14]:http://htmlpreview.github.io/?https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/7Figures_HTML/2.4_plotcdf.html


## Use Case 2.2  
**What differences are there across datasets in water use in Cache County Utah?**  

Modelers often require data for agriculture and other water uses, which might be derived or estimated, not measured like discharge in rivers. We use controlled vocabulary, metadata, and multiple data types features to enable querying, aggregating, and comparing all the datasets for agriculture water use in Cache County in the Lower Bear River, Utah. The query used “diverted flow” controlled term and returns four time series and seasonal water use values with different estimate methods from three datasets: the WEAP and WASH model instances and the WaDE data source [Figure 3](/UseCases/use_case_2/#figure-3). Using “depleted flow” controlled term returns a fifth time series form the WaDE source (dashed line in Figure 3). We used the source and method descriptions for attributes, node instances, and scenarios to identify how the datasets represent water use in spatial or time extents. Data either represent i) the entire county area annually in one node as diverted or depleted water like the WaDE dataset (two curves), ii) the entire county seasonally across 11 demand sites (WEAP Model 2017), iii) part of the county monthly in one or five sites as in the WEAP 2010 and WASH 2017 models, respectively. Users can query many agriculture water use estimates in multiple datasets and use values that match their models required data for the entire county or part of it, monthly or annually, and for diverted or depleted flow. 

In addition to demand data, the query also can return water rights data from the WaDE data source under the controlled Object Type “Demand Site” and attribute name of “Flow”. For example, the “WATER RESEARCH LAB. UTAH STATE UNIVERSITY” has two water rights. One of them is 84 AF/Year and 146 cfs for the beneficiary use descriptor value of “Power”. So WaMDaM organizes descriptive and numeric data for water rights.


| Use Case        | Query           | Result (csv)  |
| ------------- |:-------------:| -----:|
| IdentifyDemandSites     | [Query][31] | [Result][41]  |
| Identify Demand Sites Seasonal Values     | [Query][51] | [Result][61]  |
| Identify DemandSites Time Series Values     | [Query][71] | [Result][81]  |
| Water Rights     | [Query][91] | [Result][101]  |


| Use Case figure       | Python Script   | Interactive figure  |
| ------------|:----------:| -----:|
|Figure a     | [script][111] | [Figure][211]  |

#### Figure 3  

![](/UseCases/images/UseCase2.2.png) 
**Figure 3:** Aggregated water demand for Cache County Utah across WEAP and WASH models and the WaDE dataset. Color-coded from light to dark blue for low to high water use. Native attribute terms are in quotes 


[111]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/6Figures_Python/UseCase2.2_dentifyDemandSites_TimeSeriesValues.py

[211]:http://htmlpreview.github.io/?https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/7Figures_HTML/UseCase2.2_identifyDemandSites_TimeSeriesValues.html

[31]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.2/1_IdentifyDemandSites.sql

[41]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/3.1IdentifyDemandSites.csv

[51]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.2/2_IdentifyDemandSites_SeasonalValues.sql

[61]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/3.2dentifyDemandSites_SeasonalValues.csv

[71]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.2/3_IdentifyDemandSites_TimeSeriesValues.sql

[81]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/3.3dentifyDemandSites_TimeSeriesValues.csv


[91]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.2/4_WaterRights.sql

[101]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/3.4WaterRights.csv



## Use Case 2.3    
**What differences are there across datasets in volume and elevation curves of a reservoir?**    

Molders also search for data describing multi-attribute series such as reservoir bathymetry (elevation versus storage) to represent the physical capacity of reservoirs in their models. Here, we use the controlled instance name of Hyrum Reservoir and controlled attribute names Volume and Elevation to identify five volume-elevation curves for Hyrum Reservoir from three datasets: USBOR, Utah Dams, and WEAP model datasets. The USBOR Water Info dataset has two time series of storage and elevation, which have the same daily time step from January 2010 to May 2017. We plotted both series to empirically derive a storage and elevation curve for this dataset (Figure 8). 



| Use Case        | Query (SQL)          | Result (csv)  |
| ------------- |:-------------:| -----:|
|NumericValues_otherTypes     | [Query][300] | [Result][400]  |
|MultiAttributeValues    | [Query][500] | [Result][600]  |
|MergeTimeSeriesValues     | [Query][700] | [Result][800]  |
|NumericValues_Metadata   | [Query][900] | [Result][1000]  |
|MultipleTimeSeriesColumnsSameTimeStamp   | [Query][1100] | [Result][1200]  |



| Use Case figure       | Python Script   | Interactive figure  |
| ------------|:----------:| -----:|
|Figure     | [script][10000] | [Figure][2000]  |




Metadata indicate the five curves originate from two sources: the Utah Dams dataset and USBOR who owns the dam. The WEAP model instance used older curves from the UDWR while Utah Dams and USBOR datasets used USBOR source. Next, we discuss the following three comparison insights, which are related to semantics, range of data, and its date of measurement. 
Looking more closely at the [Figure 4](/UseCases/use_case_2/#figure-4) results, first, there is a systematic displacement in volume and elevation between the upper red and lower brown sets of curves. The upper red curves indicate “live storage” which does not account for “dead storage”, while the lower brown curves reflect “total storage”. The USBOR reported dead storage as 3012 acre-feet at the elevation of 4629.6 feet. We verified this interpretation by subtracting or adding dead storage below the elevation of 4629.6 feet, which reproduced similar lower or upper curves. In the WEAP and WASH models, dead storage is termed “Top of Inactive” and MinCap.   

Second, the Figure 8 curves cover different ranges of volume and elevation. The BOR Water Info Sys. (2017) derived curve represents operational ranges of elevation and storage. The Utah Dams (2016) curve and its equivalent BOR Reservoirs Dataset (2006) curve both represent the full bathymetry range. The identical WEAP model curves have a physical range that extend longer up to 70,000 acre-feet volume and 4,750 feet elevation (not shown). Metadata suggest that this extension could have represented a future scenario that raised the dam height.   

Third, the methods metadata show there have been two different bathymetry surveys in 1935 and 2016, which are reflected in the BOR Reservoirs Dataset (2006) and USU WEAP Model 2017 curves (both for total storage). The BOR Reservoirs Dataset (2006) curve has less total storage than the other identical curves in the WEAP model instances that use the 1935 survey. Total storage decreased by 1,179 acre-feet which is 6% of the original storage due to decrease in both the dead and live storage potential. The percentage of dead storage to total storage is relatively high, about 17% in this small reservoir and misrepresenting the total or live storage could affect modeling results.   

WaMDaM used the features of CVs, metadata, and multiple data types to readily identify and compare multi-attribute bathymetry curves across datasets that had different semantics, measurement periods, and extrapolated versus measured methods. The comparison helps identify differences in the datasets, improve our contextual understanding of reported data values, and help to select the appropriate curve for modeling. Modelers can follow this data analysis exercise to correctly represent the bathymetry curve for other reservoirs in their models and account for dead and live storage. 


#### Figure 4  

![](/UseCases/images/UseCase2.3.png) 
**Figure 4**: Five volume-elevation curves for Hyrum Reservoir, Utah. Red and brown color-coded curves lighter to darker indicate larger volume at the same elevation. Blue shadings indicate Dead, Live, and Total storage zones for the 2006 BOR survey.


[10000]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/6Figures_Python/UseCase2.3_HyrumReservoir_Curves.py

[2000]:http://htmlpreview.github.io/?https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/7Figures_HTML/UseCase2.3_HyrumReservoir_Curves.html


[300]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.3/1_NumericValues_otherTypes.sql

[400]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/4.1NumericValues_otherTypes.csv


[500]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.3/4_MultiAttributeValues.sql

[600]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/4.2MultiAttributeValues.csv


[700]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.3/3_MergeTimeSeriesValues.sql

[800]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/4.3MergeTimeSeriesValues.csv


[900]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.3/2_NumericValues_Metadata.sql

[1000]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/4.4NumericValues_Metadata.csv


[1100]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.3/3_MultipleTimeSeriesColumnsSameTimeStamp.sql

[1200]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/4.5MultipleTimeSeriesColumnsSameTimeStamp.csv


[1300]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/4.6MultipleDescriptorValues_HydroPower.sql
[1400]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/5Results_CSV/4.6MultipleDescriptorValues_HydroPower.csv


## Use Case 2.4    
**What differences are there across datasets in dam heights, installed hydropower capacity, and number of generators for two reservoirs?**    

Modelers may search for attributes with numeric and descriptive values to correctly understand and represent the functions of water systems like modeling hydropower in dams. In this case, we use the controlled Instances of Shasta Reservoir, California and Flaming Gorge Reservoir, Utah to identify, compare, and relate their dam heights, installed hydropower capacity, and number of generators across both the US Dams and the National Hydropower Datasets (Table 1). The dam for Shasta Reservoir is 100 feet higher, has four more installed generators, and five times the installed generation capacity as Flaming Gorge Reservoir. 


| Use Case        | Query           | Result  |
| ------------- |:-------------:| -----:|
|HydroPower_UT_USDams  					| [Query][123456] |  |
|CompareShastaFlamingGorge  | [Query][123457] |   |
|HydroPowerPlants_UT  | [Query][123458] |   |
|HydroPower_CA_USDams  | [Query][123459] |   |


The Hydropower Dataset should be used to update the US Dams dataset to include Hydropower as a purpose for reservoirs like Hyrum and Jordanelle in Utah that have capacities of 0.5 and 13 Megawatts. The US Dams Dataset has only nine reservoirs in Utah and 127 in California with a Hydropower purpose while the Hydropower dataset has 73 in Utah and 413 plants in California. We used the WaMDaM features of controlled vocabularies of Instance name and multiple data types in descriptor values: “Hydropower”, “UT”, “CA” to enable comparisons across two datasets in both Utah and California.


**Table 1**: Companion between two major US dams’ height and hydropower from two datasets 
![](/UseCases/images/UseCase2.4.png) 



[123456]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.4/1_HydroPower_UT_USDams.sql

[123457]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.4/2_CompareShastaFlamingGorge.sql

[123458]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.4/3_HydroPowerPlants_UT.sql


[123459]:https://github.com/WamdamProject/WaMDaM_UseCases/blob/master/UseCases_files/4Queries_SQL/UseCase2/UseCase2.4/4_HydroPower_CA_USDams.sql

