# Why WaMDaM?

## Problem
Water resources modelers and researchers seek to solve integrated water management problems in an area of interest. Current practices to identify and analyze input data for water resources systems models are often dataset specific, stored in different formats, described using different vocabularies, require time-intensive, manual data manipulations, and cannot be reused despite the fact that basic data elements are similar across models

**None of the existing data management methods can help modelers answer these these questions for data query, comparison, and model building activities:** 

1.	What data are available to develop a model in a study area?
2.	How do data values for properties of system components differ across datasets? 
3.	What differences are there across datasets in connectivity of natural and built infrastructure components in a particular area? 
4.	What differences are there in network topology, metadata, and input data between two scenarios of a model instance?


![](/images/Fig1_current_wamdam.jpg)
**Figure 1:** Schematic of a systems water management network with two scenarios


## What are the Water Management Data?
The water management data domain fundamentally includes natural and built water system components like water supply, infrastructure, and demand sites, represented through nodes and links (Brown et al., 2015; Loucks et al., 2005; Rosenberg and Madani, 2014).    

The domain also includes using multiple data types that represent quantitative and qualitative attributes of the system components like time series, seasonal parameters, and multi variable arrays. Example attribute data types are, time series of inflow and outflow of reservoirs, multi variable series of reservoir storage and surface area that change with elevation, and monthly seasonal reservoir evaporation across years. 

![](/images/wmd.png)
**Figure 2:** systems water management data


## Solution
**What can you do with WaMDaM not possible before?** 

WaMDaM is an effort to standardize how we organize water management data which supports eight features altogether that partially exist in prior methods to enable users to: 

1. Support different water resources systems components that are used in water management models like hydrology, infrastructure, and demand sites as reusable modules or sets of systems components.   
2. Represent connectivity and interactions between components in space through networks of nodes and links as used in systems modeling. 
3. Support scenarios that track topologic changes in networks, metadata and data values. 
4. Support multiple data types that are used in systems modeling like time series and multidimensional arrays.  
5. Uses consistent contextual metadata to unambiguously interpret data values.
6. Uses controlled vocabulary to relate inconsistent terms across data sources and models.  
7. Enables conditional data queries to access and compare subsets of data and metadata 
8. Developed in an open-source software environment.  
