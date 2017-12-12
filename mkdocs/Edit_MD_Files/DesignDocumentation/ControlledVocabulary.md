# Controlled Vocabulary tables

The three key controlled vocabulary that are needed to basic data quries are:  
CV_AttributeName, CV_InstanceName, and CV_ObjectType


## CV_AggregationStatistic	
A term for describing the statistical action used to calculate over recorded time series values within a time interval. For example, 100 cfs of delivery target to a demand site is a "cumulative" aggregation statistic calculated over a time interval like a month.


## CV_AttributeDataType	
A term for describing the supported types of data that an attribute in WaMDaM can take based on logical and physical groupings like numeric, text, time stamped values, and parried categorical values. For example, numeric values, descriptor value, electronic files, time series, and multi attribute series.


## CV_AttributeName	
A Term describing the name of quantitate or qualitative property of a water system component (e.g., reservoir).

## CV_DescriptorValues	
A term for describing descriptive values (characters as numeric or strings) for an attribute. The descriptor values can be shared across attributes of systems components like land use "Grass_Pasture" or irrigation type "Flood", or site code as "10000010"


## CV_DualValueMeaning  
A Term describing the specific meaning of Boolean data values (True, False)for an attribute.

## CV_ElectronicFileFormat	
A term for describing the supported physical format of files loaded into WaMDaM as values to attributes(e.g., csv, jpg, NETCDF).

## CV_ElevationDatum	
A term for describing vertical datums. Vertical datums are used in WaMDaM to specify the origin for elevations associated with node instance in networks.

## CV_InstanceName	
A term for describing the name of a specific node or link system component in a specific location which can related synonymous native instance terms (e.g., Hyrum = Hrm & Hyrum Reservoir).

## CV_MethodType	 
A term for describing types of Methods associated with recording or generating data values to attributes. Example method types are like "expert opinion", "field procedure", "model simulation".

## CV_ObjectType	 
A term for describing a built or natural water system component .

## CV_ObjectTypology	
A term for describing the category of an Object Type as either: Node, link, network.

## CV_SeasonName	
A term for describing a categorical value that may correspond to numeric values of an attribute. The CategoricalValue represents steps in time (e.g., Winter, Summer, March, April) or space (e.g., categorical levels of reservoir levels (e.g., inactive, conservation, flood)

## CV_SpatialReference	
A term for describing a geographic reference to all the node instances that belong to the same Master Network.

## CV_Units	
A term for describing the name of the Unit of data value of an attribute.


# Application
A Python/Django web application and REST API for managing the WaMDaM Controlled Vocabularies. This repository contains the source code for the master controlled vocabulary registry for the Water Management Data Model (WaMDaM).  
The configuration and deployment of the original repository have been significantly changed to be much simplified and automated using Ansible and Docker. A developer now can configure and deploy the app many times if they wish much easier than before.     

The production Controlled Vocabulary website for WaMDaM (which uses this code) can be accessed at: http://vocabulary.wamdam.org/
This online moderated registry aims to promote consistent terminology (i.e., Controlled Vocabularies-(CVs)) to describe water system components and their attributes across datasets, models, and users, while still retaining the native terms. Registering your model's native terms against these CVs will allow you to relate, query, and compare all of your water management data within a single database. 


