# customer360
Hadoop based Customer 360 Demo

# Design

## Design Flow 

Data Ingestion -> Data Pre-processing (Cleansing, Enrichment) -> Data Processing (Co-relation, Aggregation, Transformation etc) -> Predictive Analytics -> Visualization 

## Tools used

* Data - Sample data is used from the data generators 
* Data Ingestion - NiFi on the edge node ingests the data from local disk and pushed to HDFS
* Pre-Processing - Data from External 'Raw' tables is moved to the 'Staging' area 
* Processing - Data is correlated based on fields that can be used to join the data set. Data is pushed into Solr
* Visualization - Silk AKA BananaUI 

## Datasets 

* Customer - ID, Name, Address, Gender, Age, Customer Since, social media handle
* Social Media - handle, message, timestamp, 
* Clickstream - standard 
* Transactions - timestamp, product id, amount etc; 
* Chat History - timestamp, customer service rep id, chat blob

# Goal for MVP 
There could be future enhancement to this demo but in initial version, we should set the foundation with at least 2-3 datasets, some hive processing, at least 1 model and at least 1 index in Solr. 
