# Compare Scenarios

This utility compares two scenarios of a model within the same Master Network loaded into a WaMDaM SQLite database. It exports the results into an Excel Workbook template.   

The Workbook reports differences and similarities in four spreadsheets: ChangeInTopology, ChangeInMetadata_Topology, ChangeInMetadata_Attributes, and ChangeInDataValues 


## Steps:
### 1. Download the ScenariosComparion Template

<!-- Place this tag in your head or just before your close body tag. -->
<script async defer src="https://buttons.github.io/buttons.js"></script>


|Download|  <i class="fa fa-file-excel-o fa-2x"></i>       |Use it for |
|---| :---------------: |:------------- |
|ScenariosComparion Template  |<a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/blob/master/WorkbookTemplates/Compare_scenarios_result/CompareScenario_empty.xlsx?raw=true" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a>| Generic template to export scenario comparisons results|

### 2. Launch WaMDaM Wizard, If not already connected, connect to the SQLite database with loaded data. 

### 3. Click at the Query WaMDaM tab, then click at "Compare Scenarios of a Network button". Choose the Model name, Network name and scenarios for comparison. Finally provide the downloaded Workbook template to export results.

![](/Getting_started/images/CompareScenarios.PNG)




