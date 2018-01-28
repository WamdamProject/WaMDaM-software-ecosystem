## WaMDaM Data Loader Wizard  

We designed a Python 2.7-based data loader (WaMDaM Wizard) to auto-read input data from an Excel Workbook template into a physical WaMDaM SQLite database instance on the user’s local machine. We chose Excel as a generic input data medium because it is commonly used by modelers and widely used across computer operating systems. The Wizard validates entries to comply with the database, maps primary and foreign keys, and implements software business rules. We elected to use SQLite (https://www.sqlite.org/index.html) because it is free, open-source, and server-less to satisfy open-source design (Feature #8). We also used the SQLite Manager Add-ons to Mozilla Firefox 56 (https://addons.mozilla.org/en-US/firefox/addon/sqlite-manager/) as an open-source user interface to visualize and execute queries against WaMDaM database tables. 

The WaMDaM Wizard has three demo data utilities to help users prepare time series data, seasonal data, and shapefile for input to WaMDaM. The Wizard can import data directly from WaterOneFlow CUAHSI web-services and WaterML files by the U.S. Bureau of Reclamation (USBOR) Water Information System web service https://water.usbr.gov/. The Wizard can also provide users with automated detailed and summary comparisons of network topology, metadata, and data values between scenarios in the same network. See instructions to use WaMDaM on Windows at http://docs.wamdam.org/Getting_started/Steps/


For info on the Wizard architecture, please visit the GitHub repo here.
https://github.com/WamdamProject/WaMDaM_Wizard#wamdam_wizard-architecture

![](/DesignDocumentation/images/Wizard_Architecture.jpg)
