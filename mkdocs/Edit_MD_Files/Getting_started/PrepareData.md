# Prepare your data


## Download the WaMDaM Workbook     
Templates for Input Data to prepare your data into it. Each dataset into one workbook

<!-- Place this tag in your head or just before your close body tag. -->
<script async defer src="https://buttons.github.io/buttons.js"></script>


|Donwlaod|  <i class="fa fa-file-excel-o fa-2x"></i>       |Use it for |
|---| :---------------: |:------------- |
|WaMDaM Workbook Template  |<a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/blob/master/WorkbookTemplates/InputData_Template/WaMDaM_InputData_template.xlsm?raw=true" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a>| Generic template for any data source to WaMDaM|
|Prepre shapefile template   | <a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/blob/master/WorkbookTemplates/Prepare_transform_data_templates/Shapefile.xlsx?raw=true" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a> |Transform the shapefile columns into WaMDaM sheets |
|Prepare time series template| <a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/blob/master/WorkbookTemplates/Prepare_transform_data_templates/Prepare_Pivot_TimeSeries_data.xlsx?raw=true" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a>|Transform time series data into WaMDaM sheets|
|Prepare seasonal data template| <a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/blob/master/WorkbookTemplates/Prepare_transform_data_templates/AllSeaosnalData_templates.xlsx?raw=true" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a>|Transform seasonal data into WaMDaM sheets|


## Why Excel?
We chose Excel as a generic input data medium with a custom Excel workbook that has 17 sheets with fixed column headers for the main tables of input data in WaMDaM. Each dataset is prepared to a single workbook one-at-a-time. The sheets are related with each other through dropdown lists to help users for example to relate metadata elements to the attributes and data values

The Wizard maps all the bridge tables’ complex relationships and users do not need to know anything about primary or foreign keys.

## Preprare data order
**First**: Load the controlled vocabulary or leave them blank.    
Controlled vocabulary are available in the template workbook and users can update them in a button on the workbook’s homepage sheet. The button calls the online registry application user interface and updates the list of vocabularies in the sheet. Then the CVs are available as dropdown lists in each sheet where they apply.  

**Second**: Define metadata that will be used for the Attributes and Instances.   

**Third**: Define the data structure of Object Types and Attributes. 
      
**Fourth**: Add the master network, scenario, and nodes and links. 
 
**Fifth**: Load data values to each attribute of each Instance. 

## Simple case 
Users have to populate at least six sheets for any dataset and they can populate more as the complexity of the dataset increases. In a simple case, the three sheets of Organizations&People, Sources&Methods, Networks&Scenarios can be populated with only two rows each. 
 

