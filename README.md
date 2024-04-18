# Extract and Load from External API to Lakehouse using Data Pipelines (Microsoft Fabric)


## Problem Statement

Design a system to retrieve data from an external API and seamlessly integrate it into a lakehouse architecture using data pipelines, specifically leveraging Microsoft Fabric technology and Establish a structured file folder system to organize data files and implement automated processes for extracting data files and storing them in a Microsoft Fabric lakehouse environment.

### Datasource
     Public API:
     https://api.publicapis.org/entries

### Requirement
     Need Power BI pro account with enable Microsoft Fabric services (Trial)


### Steps followed 

- Step 1: Create a data pipeline.

- Step 2: Go to 'Copy Data' and add 'Add to Canvas'

- Step 3: Configure all required fields

  (a) General - Name, Description
  
  (b) Source - Data Store Type (External) ,
  - Create new connection; Go to 'Generic Protocol -> REST (generic protocol)
  - Add Connection String (Base API URL)
  (c) Destination - Data Store Type (Workspace)
  - Choose Lakehouse (Lakehouse or Warehouse)
  - Root Folder - File (because we need to data store in JSON file format)
  - File Path - Create Dynamic file path name
  - File Format - JSON (Select required file format)

- Step 4: Validate The Pipeline
- Step 5: Run the Pipeline
- Step 6: Observe Output - All the Activitie have captured in output and show the status pf each activity is success or failed, if activity is failed then click on little icon to show the error.
- Step 7: Go to Lakehouse path which are mentioned in destination and check the JSON files stored in proper folder structured and check the data preview, If data preview not supported then your file format name was not in proper format with extension like 'filename.json'.
