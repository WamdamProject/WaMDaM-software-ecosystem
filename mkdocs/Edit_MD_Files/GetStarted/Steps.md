# Getting Started  

Follow these eight steps in order to install WaMDaM Wizard, populate your data into WaMDaM SQLite database, and implement use cases. 

## 1. Download and Install the WaMDaM Wizard V 1.02
WaMDaM Wizard is a desktop data loader from a spreadsheet template to a SQLite database. The SQLite database is created based on the WaMDaM data model. 
Download the software for Windows 7 or 10 64 bit from the table below. You also can find out all the [WaMDaM_Wizard releases][1] on GitHub.
[1]:https://github.com/WamdamProject/WaMDaM_Wizard/releases

<!-- Place this tag in your head or just before your close body tag. -->
<script async defer src="https://buttons.github.io/buttons.js"></script>


|Choose one|  <i class="fa fa-windows fa-3x" style="color: black"></i>        |Note |
|---| :---------------: |:------------- |
|Executable (.exe) [230 MB]  |<a class="github-button" href="https://github.com/WamdamProject/WaMDaM_Wizard/releases/download/v1.02/wamdam.exe" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a>| Good option if you don't have Admin access to install it|
|Installer (msi) [160 MB]   | <a class="github-button" href=" https://github.com/WamdamProject/WaMDaM_Wizard/releases/download/v1.02/WaMDaM_v1.02_UtahStateUniversity-1.02-amd64.msi" data-icon="octicon-cloud-download" data-size="large" aria-label="Download ntkme/github-buttons on GitHub">Download</a> |Lighter to donwload and probably faster to run   |
|Run from source code|<a href="https://github.com/WamdamProject/WaMDaM_Wizard"><i class="fa fa-github fa-3x"></i></a>|Good option to debug potential issues and improve it|

## 2. Launch WaMDaM Wizard

Once you installed the Wizard, double click at the Wizard's shortcut and this main window should appear.   

Navigate the top tabs and see the Wizard's capabilites to prepare data for and import it into WaMDaM, and to export data to models.    

![](/images/Wizard.PNG)

## 3. Connect to SQLite
In WaMDaM Wizard you can either create and connect to a new or existing SQLite database instance on your machine. The Wizard automatically creats a blank WaMDaM SQLite file for you based on WaMDaM data model schema. Connecting to MySQL although it should work fine, it is not supported in this version.    

## 4. Prepare your data into Excel
Follow the [instructions here][2] on how to prepare your data into WaMDaM Excel Workbook and register terms with controlled vocabulary. 

[2]: http://docs.wamdam.org/Getting_started/PrepareData/


## 5. Use the Wizard importers 
* Import from Excel workbooks your prepared in Step 4
* Importers time series data from CUAHSI
* Import reservoir related data from the US Reclamation Water Information System. *


## 6. Open the SQLite database
Download and install the [DB Browser For SQLite][3] to query the database and view its tables. 


[3]: https://sqlitebrowser.org/


Use the DB Browser For SQLite to inspect the loaded data into WaMDaM. 


## 7. Execute use case queries
Use and adapt queries from WaMDaM use cases and execute them in the SQLite Manager. 


## 8. Compare scenarios 


## 9. Query WaMDaM   
Use and adapt Python scripts to v


## 10. Export Data to Models


## 11. Publish Models to OpenAgua
