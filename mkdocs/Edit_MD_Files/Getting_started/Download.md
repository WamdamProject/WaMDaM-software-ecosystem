# Download

WaMDaM Wizard is a desktop data loader from a spreadsheet template to a SQLite database. The SQLite database is created based on the WaMDaM data model. 


## 1. Download the WaMDaM Excel Workbook     
Templates for Input Data to prepare your data into it. Each dataset into one workbook

<i class="fa fa-file-excel-o fa-5x"></i>


 

<a class="github-button" href="
https://github.com/WamdamProject/WaMDaM_UseCases/raw/master/UseCases_files/0WorkbookTemplates/InputData_Template/WaMDaM_InputData_template.xlsm" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a>

<!-- Place this tag in your head or just before your close body tag. -->
<script async defer src="https://buttons.github.io/buttons.js"></script>



## 2. Download the Wizard GUI   

|Choose one|  <i class="fa fa-windows fa-3x" style="color: black"></i>        |  <i class="fa fa-apple fa-3x" style="color: black"></i>           | <i class="fa fa-linux fa-3x" style="color: black"></i>  |
|---| :-------------: |:-------------:| :-----:|
|Executable (.exe)|<a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/releases/download/v1.0_beta/wamdam.exe" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a>|<a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/releases/download/v1.0_beta/wamdam.exe" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a> |
|Installer (msi)     | <a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/releases/download/v1.0_beta/wamdam.exe" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a> | <a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/releases/download/v1.0_beta/wamdam.exe" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a> ||
|Run from source code|||<a href="https://github.com/amabdallah/wamdam_wizard"><i class="fa fa-github fa-2x"></i></a>|



![](/images/Wizard.PNG)


## Steps to use WaMDaM
![](/Getting_started/images/Use_WaMDaM.jpg)


## Wizard info for developers 
* Here is the schema that the Wizard works within: [WaMDaM Schema](https://wamdamproject.github.io/WaMDaM_Information_Model/diagrams/01_WaMDaM.html). 

* The Wizard is built using Python 2.7 and the [wxPython](https://www.wxpython.org/) GUI library with the help of [wxFormBuilder](https://github.com/wxFormBuilder/wxFormBuilder).  
 


## Why WaMDaM Wizard?   
The WaMDaM Wizard is an open-source, cross-platform, Python-based graphical user software to interact with WaMDaM database. By using the Wizard, users are not expected to understand the underlying WaMDaM database of schema. Users just need to understand how to fit their data into these concepts: ObjectType, Attribute, Instance, Network, and Scenario. 
The Wizard mainly allows users to automatically:    

* **1.** Read, validate, and load data from a spreadsheet template in SQLite  

* **2.** Use data preparation tools to help manipulate and transform users data to fit into the spreadsheet template. 
 
* **3.** Import data directly from supported web-services (e.g., time series data from CUAHSI)  

* **4.** Use pre-defined functions to query and compare scenario data from multiple datasets loaded in WaMDaM   

* **5.** Export data loaded into WaMDaM to multiple supported models (in-progress)  



