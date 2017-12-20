# Getting Started  

Follow these eight steps in order to install WaMDaM Wizard, populate your data into WaMDaM SQLite database, and implement use cases. 

## 1. Install WaMDaM Wizard 
WaMDaM Wizard is a desktop data loader from a spreadsheet template to a SQLite database. The SQLite database is created based on the WaMDaM data model. 
Download the software for Windows 7 or 10 64 bit from the table below. You also can find out all the [WaMDaM_Wizard releases][1] on GitHub.
[1]:https://github.com/WamdamProject/WaMDaM_Wizard/releases

<!-- Place this tag in your head or just before your close body tag. -->
<script async defer src="https://buttons.github.io/buttons.js"></script>


|Choose one|  <i class="fa fa-windows fa-3x" style="color: black"></i>        |Note |
|---| :---------------: |:------------- |
|Executable (.exe) [230 MB]  |<a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/releases/download/v0.2-beta/wamdam.exe" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a>| Good option if you don't have Admin access to install it|
|Installer (msi) [27 MB]   | <a class="github-button" https://github.com/WamdamProject/WaMDaM_Wizard/releases/download/v0.2-beta/WaMDaM_Main_Setup-1.0.0-amd64.msi" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a> |Lighter to donwload and probably faster to run   |
|Run from source code|<a href="https://github.com/WamdamProject/WaMDaM_Wizard"><i class="fa fa-github fa-3x"></i></a>|Good option to debug potential issues and improve it|


Once you installed the Wizard, double click at the Wizard's shortcut and this main window should appear.  

![](/images/Wizard.PNG)

## 2. Connect to SQLite
In WaMDaM Wizard you can either create and connect to a new or existing SQLite database instance on your machine. The Wizard automatically creats a blank WaMDaM SQLite file for you based on WaMDaM data model schema.   

## 3. Prepare your data into Excel
Follow the [instructions here][2] on how to prepare your data into WaMDaM Excel Workbook and register terms with controlled vocabulary. 

[2]: http://docs.wamdam.org/Getting_started/PrepareData/


## 4. Use the Wizard importers 
* Import from Excel workbooks your prepared in Step 3
* Importers time series data from CUAHSI
* Import reservoir related data from the US Reclamation Water Information System. 


## 5. Open the SQLite database
Use the SQLite Manager to inspect the loaded data into WaMDaM. If you dont have it, download and install the Mozilla Firefox SQLite Manager Add-on and use it to open the SQLite database file. 
Follow these [steps][3] here.    

[3]:http://docs.wamdam.org/UseCases/Download/


## 6. Execute use case queries
Use and adapt queries from WaMDaM use cases and execute them in the SQLite Manager. 


## 7. Compare scenarios 


## 8. Visualize query results   
Use and adapt Python scripts to v
