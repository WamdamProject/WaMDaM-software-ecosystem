# Why WaMDaM?

## Problem
Data analysis and synthesis are foundational in developing water resources management models (Loucks et al., 2005), and the way data are organized can enable or inhibit the analysis that water managers and researchers perform (Horsburgh et al., 2008).   

Current practices to organize, manipulate and compare water resources data to develop water resources systems models are often specific to the data sources, models, and study location (Brown et al., 2015).   

Source-, model-, and study area-specific practices arise because models have different data requirements for their components, store data in different file formats, have varying spatial coverage, use inconsistent metadata to describe methods, sources, and units, and use different vocabulary to name similar system components and their attributes (Laituri and Sternlieb, 2014; Maidment, 2016; Miller et al., 2004).   

This heterogeneity hampers potential synthesis of information from multiple studies (Brown et al., 2015), and source-, model-, and study area-specific practices often require considerable effort and time to develop models (Beniston et al., 2012; CUAHSI, 2005; Draper et al., 2003; Hey et al., 2009; Leonard and Duffy, 2013; Maidment, 2008; Michener, 2006; Miller et al., 2004; Ridley and Stoker, 2001; Watkins, 2013).   

The specificity in practices often makes them not readily reusable or applicable to other datasets and modes in the domain of water management data. 


![](/images/Fig1_current_wamdam.jpg)
**Figure 1:** Schematic of a systems water management network with two scenarios


## Water Management Data Domain
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
