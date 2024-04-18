# Extract and Load from External API to Lakehouse using Data Pipelines (Microsoft Fabric)


## Problem Statement

Design a system to retrieve data from an external API and seamlessly integrate it into a lakehouse architecture using data pipelines, specifically leveraging Microsoft Fabric technology and Establish a structured file folder system to organize data files and implement automated processes for extracting data files and storing them in a Microsoft Fabric lakehouse environment.

### Datasource
     Public API:
     https://api.publicapis.org/entries

### Requirement
     Need Power BI pro account with enable Microsoft Fabric services (Trial)
     
![0 Requirement](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/6fe44b57-f555-42ff-8bcd-635ff885dda0)





### Steps followed 

- Step 1: Create a data pipeline.

![1 PL Create Pipeline](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/a89ad563-87fe-4e1e-b8d4-987784699c54)


- Step 2: Go to 'Copy Data' and add 'Add to Canvas'

![2 PL Add to Canvas](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/15cf449d-e47c-4c2b-9306-20c1cf0b1f30)


- Step 3: Configure all required fields

  (a) General - Name, Description

  ![3 PL Configure General](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/62e8137c-4952-457e-8548-f8191ec416ee)


  (b) Source
  - Data Store Type (External) ,
  ![4 1 PL Configure Source](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/f70759d1-9670-4267-a489-b9931a9f9fd4)
  
  - Create new connection; Go to 'Generic Protocol -> REST (generic protocol)
  ![4 2 PL Configure Source add new source](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/f8181ce7-07d9-4623-bb65-0f0b9c9e7551)

  - Add Connection String (Base API URL)
  ![4 3 PL configure new source](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/a0f6e606-dc8c-4631-8f00-16b7bfa3c619)

  
  (c) Destination 
  - Data Store Type (Workspace)
  - Choose Lakehouse (Lakehouse or Warehouse)
  - Root Folder - File (because we need to data store in JSON file format)
  ![5 1 Configure Destination](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/3c2437ce-9453-4d8a-97d7-300bdb71bde3)
  - File Path - Create Dynamic file path name
  ![5 2 Configure Destination add dynamic file path 1](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/4bf79eef-805e-4557-bd1d-457b7302866f)

  - File Format - JSON (Select required file format)
  ![5 3 PL Configure Destination dynamic File Path 2](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/16ad4a93-eb94-497b-9498-f835fd33668c)


- Step 4: Validate The Pipeline
- Step 5: Run the Pipeline
- Step 6: Observe Output - All the Activitie have captured in output and show the status pf each activity is success or failed, if activity is failed then click on little icon to show the error.
- Step 7: Go to Lakehouse path which are mentioned in destination and check the JSON files stored in proper folder structured and check the data preview, If data preview not supported then your file format name was not in proper format with extension like 'filename.json'.
