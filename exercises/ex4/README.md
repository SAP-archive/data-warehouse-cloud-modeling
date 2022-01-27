# Exercise 4 - Sales Orders Extension

In this exercise, you're going to bring more data into the system and consolidate them with the Sales Orders.
The classic way to ingest data is to **setup a connection with the data source** and afterwards to pull the data in.
However, SAP Data Warehouse Cloud offers some more options in addition to that, which covers different scenarios and needs. We are going to look into the various options during the exercise.

![](./images/data_ingestion.png)

### Pulling data via Connection
This is the classic and standard way to ingest data in SAP Data Warehouse Cloud. For that you setup a connection to the source system and then just pull the data in. SAP Data Warehouse Cloud comes here with various connectors and adaptors to SAP and Non-SAP sources. There is also an option to install your own connector in order to access a specific source. Once the connection is set, you can **read the data** from the source system in two different modes: 
- **Data Federation (remote data access)**: keep the data in the sources and access them remotely. This approach will lower the cost of operations, since you will not consume any additional disc space. However, please be aware of potential performance penalties and security.   
- **Data Replication**: copy and transfer the data physically into SAP Data Warehouse Cloud. This approach will utilize the underlying disc space in SAP data warehouse cloud. You will benefit from the performance since the data are stored in the local persistence. In the SAP Data Warehouse Cloud the underlying persistence is the SAP HANA Cloud.

### Pushing data to Open SQL Schema
The _Pushing Data_ approach is similar to _Pulling data_ approach. The main difference is the trigger point, who initiates the data load process. 
While in the Pulling Data scenario the initiator is SAP Data Wareshouse Cloud itself, whereas in the Pushing Data scenario, the initiator is an external client which **writes the data** into a dedicated persistence of SAP Data Warehouse Cloud: the _Open SQL Schema_.  

The configuration of an Open SQL Schema comes along with a database user with access rights to read and write into SAP HANA Cloud database. 
By using the database user credential, you can access the schema with e.g. SAP HANA Database Explorer (which comes along with the SAP Data Warehouse Cloud delivery) or SAP Data Intelligence. With that you can execute standard SQL statements (DDL + DML), and integrate the artefacts later in the modeling.

Here are some other examples, how you can utilize the Open SQL Schema for different use cases:
- [SAP Data Intelligence Cloud – File Upsert into SAP Data Warehouse Cloud](https://blogs.sap.com/2021/12/23/sap-data-intelligence-cloud-file-upsert-into-sap-data-warehouse-cloud/)
- [HOW TO use the SAP Business Technology Platform to extend SAP Marketing Cloud with Predictive Scores](https://blogs.sap.com/2022/01/11/how-to-use-the-sap-business-technology-platform-to-extend-sap-marketing-cloud-with-predictive-scores/)
- https://sapdemostore.com/sap/bc/ui5_ui5/sap/yunifiedstore/index.html#/scenario/0000017447


And last but not least, you can use any 3rd party client (e.g. DBeaver) or ETL tool of your choice to push data to the system.

### Sharing data from Spaces
In general, in SAP Data Warehouse Cloud you can use _Spaces_ to isolate resources such as CPU, disc spaces, users and data by grouping them logically to the business needs.
However, Spaces can also be used to share dedicated data and models to other spaces and make them available there. The shared data and models can be used, as if they were in the same space you are working. Hence, it is possible to reuse existing data and models from other spaces without the need of shifting and synchronizing data forth and back. A typical scenario is a central space for master data. The benefit is a much lower development effort and TCO. 

### Downloading data from Data Market Place
The latest feature in SAP Data Warehouse Cloud is the Data Market Place, where SAP partners and customers can offer data and models for download / purchase. For instance, that could be tailor made content for a specific industry or a market dataset which you require for your business scenario. The data market place allows you and others to exchange and monetize datasets, which can be easily integrated with your models in SAP Data Warehouse Cloud.
For more information on SAP Data Warehouse Cloud please checkout also the following blog:
https://blogs.sap.com/2021/12/13/sap-data-warehouse-cloud-data-marketplace-an-overview/

In the following exercise we will cover all of these options and enrich the existing Sales Order model:


[<h2>Exercise 4 - Sales Orders Extension</h2>](exercises/ex4/)
- **Exercise 4.1 - Get data from Open SQL Schema**
   - [Exercise 4.1.1 - Create Database Access User and Open SQL Schema](/exercises/ex4/open-sql-schema)
      - Database Access User
      - Open SQL Schema 
   - [Exercise 4.1.2 - Create a local Sales Order Table](/exercises/ex4/special-sales-orders-table)   
      - Database Explorer  
   - [Exercise 4.1.3 - Adjust the Sales Order View](/exercises/ex4/sales-orders-union)
      - Union Node   
   - [Exercise 4.1.4 - Use 3rd party database client](/exercises/ex4/3rd-party-db-client) :construction::construction::construction:
- **Exercise 4.2 - Get data from Data Market Place** 
   - [Exercise 4.2.1 - Download Sample Data from the Data Market Place](/exercises/ex4/data-market-place-sample-data-download)
      - Data Market Place
   - [Exercise 4.2.2 - Create Sample Data View](/exercises/ex4/data-market-place-sample-data-view)
   - [Exercise 4.2.3 - Update Sales Orders View with Sample data](/exercises/ex4/data-market-place-update-sales-view)
- **Exercise 4.3 - Get data from Shared Spaces** 
   - [Exercise 4.3.1 - Create Master Data Space](/exercises/ex4/master-data-space)
   - [Exercise 4.3.2 - Upload Region CSV File](/exercises/ex4/region-data-upload)
   - [Exercise 4.3.3 - Create Sales Organization View](/exercises/ex4/sales-organization-view)
   - [Exercise 4.3.4 - Share Sales Organization View](/exercises/ex4/sales-organization-view-share)
      - Cross Space Sharing 
   - [Exercise 4.3.5 - Adjust Sales Order View](/exercises/ex4/sales-orders-sales-organization)
