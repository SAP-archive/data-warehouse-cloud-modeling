# Modeling in SAP Data Warehouse Cloud
## Description



This repository aims to onboard new users into Modeling in SAP Data Warehouse Cloud in the most practical manner. For that you will build a real working data model, which will embrace specific features and functions. During the journey there will be additional tips and explanations on various modeling concepts.

<!-- <div><video controls src="/images/TestVideo.mp4" muted="false"></video></div> -->

## Overview

<!-- <img align="right" src="/images/santran.png"> -->
<b>"Learning by Doing"</b> is the main principle of this tutorial. Discover and understand the features and modeling concepts by putting your hands on the SAP Data Warehouse Cloud application and build a fully functioning data model yourself. 

The exercises are meant to be built in this particular order starting from basic concepts and diving step by step into deeper advanced features while progressing with the exercises. The exercises are also based on each other. Hence, they prerequisite each other.

The tutorial comes along with a sample dataset (CSV files), so that only a minimalistic system setup is required, without any complex source system connection and data ingestion processing activities (Off course, it is still highly recommended to get yourself familiar with those features, especially when you run SAP Data Warehouse Cloud in a full enterprise and productive manner). For this tutorial working with the prepared sample datasets serves the purpose.

In general, you should be aware that SAP Data Warehouse constantly updates and delivers new features. That means, that some of the described features might be outdated and look differently than from your latest version (for that please check regularly the "What's New" website and the SAP Roadmaps in the links section below). 

That being said, I hope this tutorial will give you a solid understanding and insights into the fundamental modeling principles of SAP Data Warehouse Cloud on which you can build upon in the future.

And now enjoy the tutorial ;)<br> 




San Tran<br>
Product Manager, SAP

p.s. many thanks to Amogh Kulkarni who provided the sample datasets for the exercises.

## Pre-requisites
### SAP Data Warehouse Cloud

<img align="right" src="/images/FreeDWCTrial_2.png">

Before you can start with the exercises, please make sure to get a running SAP Data Warehouse Cloud tenant with the latest updates.
For that you can apply for a **30-Days free Trial Tenant** under the following link:
- https://www.sap.com/products/data-warehouse-cloud/trial.html
- https://saphanajourney.com/data-warehouse-cloud/trial/

Please note that the trial version does not provide all available features. Especially the more advanced exercises (e.g. Dataflow) can only be applied with full SAP DWC licence only. For more detailed information about the trial limiation and restriction, please refer to SAP note [3007887](https://launchpad.support.sap.com/#/notes/3007887).



### SAP Analytics Cloud
Optionally you will need also a running SAP Analytics Cloud (SAC), which is required to build the Stories, Dashboards and Visualization on top of the SAP Data Warehouse Models.
In case you are not interested, you can skip the exercises with the SAC part. However, it is highly recommended to walk through these exercises as well, to see how the individual features are consumed from the client side. For that, you can request an SAC trial tenant from the following link:
- https://www.sap.com/products/cloud-analytics/trial.html

Furthermore, I would like to refer to SAP Analytics Designer Developer Handbook inluding lots of Best Practices: 
https://blogs.sap.com/2021/08/25/introduction-to-analytics-designer-developer-handbook/

# Table of Content
[<h2>Exercise 1 - Upload Sample Data</h2>](/exercises/ex1/) 
- [**Exercise 1.1 - Download BIKE SALES Sample Data**](/exercises/ex1/download-sample-data)
- [**Exercise 1.2 - Upload BIKE SALES Sample Data**](/exercises/ex1/upload-bike-sales)
   - Upload CSV Files 
- [**Exercise 1.3 - Upload Currency Conversion Sample Data (TCUR)**](/exercises/ex1/upload-tcur)
   - Data Wrangling    
    
[<h2>Exercise 2 - Sales Orders</h2>](exercises/ex2/)  
- [**Exercise 2.1 - Create Business Partners View**](/exercises/ex2/business-partners-view)
   - Dimension View
   - ID + Text Semantic
   - Join Node  
   - Projection Node
   - Level Based Hierarchy 
   - Data Preview
   - View Deployment
   - [Exercise 2.1.1 - Configure Geospatial Data (Latitude, Longitude)](/exercises/ex2/business-partners-geospatial)
- [**Exercise 2.2 - Create Products View**](/exercises/ex2/products-view)
   - [Exercise 2.2.1 - Create Product Texts View](/exercises/ex2/product-texts-view)
   - [Exercise 2.2.2 - Create Text Association](/exercises/ex2/product-texts-association)
- [**Exercise 2.3 - Generate Time Tables and Views**](/exercises/ex0/time-tables-views)
- [**Exercise 2.4 - Create Sales Orders View**](/exercises/ex2/sales-orders-view)
   - Analytical Dataset View
   - Filter Node
   - Associations
   - Measures
   - Replace Table
- [**Exercise 2.5 - Create Sales Story in SAP Analytics Cloud**](/exercises/ex2/sales-story)
   - ID + Description (Text)
   - Level Based Hierarchy
   - Time Series
   - Variance on Previous and Current Period
   - Range Filter
   - Geo Spatial - Bubble Layer


[<h2>Exercise 3 - Internal Orders</h2>](exercises/ex3/)  
- [**Exercise 3.1 - Create Employee Data Flow**](/exercises/ex3/employees-dataflow) :star:
   - Data Flow
- [**Exercise 3.2 - Create Employee View**](/exercises/ex3/employees-view)
   - Parent Child Hierarchy (Internal)
- [**Exercise 3.3 - Create Vendor Product Category Hierarchy View**](/exercises/ex3/vendor-product-category-hierarchy-view)
   - Parent Child Hierarchy (External), Standalone Hierarchy  
- [**Exercise 3.4 - Create Vendor Products View**](/exercises/ex3/vendor-products-view)
   - [Exercise 3.3.1 - Create Hierarchy Association](/exercises/ex3/vendor-products-hierarchy-association)
      - Hierarchy Association 
- [**Exercise 3.5 - Create Internal Orders View**](/exercises/ex3/internal-orders-view)
   - [Exercise 3.5.1 - Wrap Currency Tables as Views](/exercises/ex3/currency-wrapper-view) 
   - [Exercise 3.5.2 - Apply Currency Conversion](/exercises/ex3/internal-orders-currency-conversion) :star:
      - Calculation Node 
   - [Exercise 3.5.3 - Input Parameters](/exercises/ex3/internal-orders-input-parameter)
- [**Exercise 3.6 - Create My Orders View**](/exercises/ex3/my-orders-view)
   - [Exercise 3.6.1 - Create Company Code Data Access Control](/exercises/ex3/data-access-control)
      - Data Access Control  
   - [Exercise 3.6.2 - Use Data Access Control](/exercises/ex3/my-orders-dac)
   - [Exercise 3.6.3 - Maintain Data for a Data Access Control](/exercises/ex3/maintain-dac-data)
   - [Exercise 3.6.4 - SAC Story Filter](/exercises/ex3/my-orders-sac-story-filter)
- [**Exercise 3.7 - Create Internal Orders Story in SAP Analytics Cloud**](/exercises/ex3/internal-orders-story) :star:



[<h2>Exercise 4 - Getting more data</h2>](exercises/ex4/):construction::construction::construction:
-  [**Exercise 4.1 - Extend Sales Order View**](/exercises/ex4/open-sql-schema)
   - [Exercise 4.2.1 - Create Database Access User and Open SQL Schema](/exercises/ex4/open-sql-schema)
      - Database Access User
      - Open SQL Schema 
   - [Exercise 4.2.2 - Create Sales Order Table](/exercises/ex4/special-sales-orders-table)   
      - Database Explorer  
   - [Exercise 4.2.3 - Adjust the Sales Order View](/exercises/ex4/sales-orders-union)
      - Union Node 
  
- [**Exercise 4.1 - Pulling data via Connections**](/exercises/ex4/connection) :construction::construction::construction:
- [**Exercise 4.2 - Pushing data via Database Access User**](/exercises/ex4/open-sql-schema)
   - Database Access User
   - Open SQL Schema  
   - [Exercise 4.2.1 - Create Special Sales Orders Table](/exercises/ex4/special-sales-orders-table)
      - Database Explorer 
   - [Exercise 4.2.2 - Extend Sales Orders View](/exercises/ex4/sales-orders-union)
      - Union Node
   - [Exercise 4.2.3 - Use 3rd party database client](/exercises/ex4/3rd-party-db-client)
- [**Exercise 4.3 - Sharing data between Spaces**](/exercises/ex4/connection) :construction::construction::construction:
   - Create a Master Data Space
   - [Exercise 4.3.2 - Create Cost Center Dataflow](/exercises/ex4/costcenter-dataflow)
   - [Exercise 4.3.3 - Cost Center View](/exercises/ex4/costcenter-view) 
   - Share Cost Center View to other Spaces 
- [**Exercise 4.4 - Download data from Data Market Place**](/exercises/ex4/data-market-place) :construction::construction::construction:





[<h2>Exercises in Pipeline</h2>](exercises/ex4/):construction::construction::construction:
> **Lessons**: Time Dependency
- [**Exercise 5.1 - Create Special Orders Table**](/exercises/ex4/special-orders-table)
   - Open SQL Schema
   - HANA Database Explorer
- [**Exercise 5.2 - Extend Internal Orders View**](/exercises/ex4/internal-special-orders-view)
   - Union Node
- Exercise - Create Entity Relationship Model (ERM) - :construction::construction::construction:
   - Associations
   - Text Associations
   - Hierarchy Associations
- Create Cost Center Hierarchy View - :construction::construction::construction:
  - Time Dependency :construction::construction::construction:
- [SQL Internal Orders] - :construction::construction::construction:
  - SQL View :construction::construction::construction:
  - Scripted View :construction::construction::construction:
  - Window Functions :construction::construction::construction:
- Excercise 4.5:  :construction::construction::construction:     
  - Cross Space Sharing :construction::construction::construction:
- Excercise 4.6 View Persistence :construction::construction::construction:
   
### Business Layer :construction::construction::construction:
- [Exercise 7 - Sales Pipeline]
    - [Exercise 7.1 - Create Business Entity]
    - [Exercise 7.2 - Create Consumption Model]
    - [Exercise 7.3 - Create a Cube / Query]
- [Exercise 7 - Sales Quota]
    - [Exercise 7.1 - Create Business Entity]
    - [Exercise 7.2 - Create Consumption Model]
    - [Exercise 7.3 - Create a Cube / Query]
- [Exercise 3 - Second Exercise Description]
    - [Exercise 2.1 - Exercise 2 Sub Exercise 1 Description](exercises/ex2#exercise-21-sub-exercise-1-description)
    - [Exercise 2.2 - Exercise 2 Sub Exercise 2 Description](exercises/ex2#exercise-22-sub-exercise-2-description)
    - 
### SAP Data Warehouse Fundamentals
- [Repository Explorer] - :construction::construction::construction:
- [Data Source Browser] - :construction::construction::construction:
- [Space Management] - :construction::construction::construction:
- [Time Tables and Views Configurator](exercises/ex0/time-tables-views)
- [Currency Conversion Configurator] - :construction::construction::construction:
- [Fiscal Calendar Configurator] - :construction::construction::construction:
- [Modeling Entities] - :construction::construction::construction:
- [Data Lineage] - :construction::construction::construction:
- [Versioning](/exercises/ex0/versioning) - :construction::construction::construction:
- [Change Management](exercises/ex0/change-management) - :construction::construction::construction:
- [View Persistence](/exercises/ex0/change-management) - :construction::construction::construction:


## How to obtain support
[Create an issue](https://github.com/SAP-samples/data-warehouse-cloud-modeling/issues) in this repository if you find a bug or have questions about the content.
For additional support, [ask a question in SAP Community](https://answers.sap.com/questions/ask.html).

## Links
- **SAP Data Warehouse Cloud**
     - SAP Data Warehouse Cloud in [SAP Roadmaps](https://roadmaps.sap.com/board?PRODUCT=73555000100800002141&range=FIRST-CURRENT)
     - Latest and greatest features of SAP Data Warehouse Cloud are presented regularly in [What's New](https://jam4.sapjam.com/blogs/show/JytsjzYpI9LproZNYpdkhG)
     - SAP Help Site of SAP Data Warehouse Cloud: https://help.sap.com/viewer/product/SAP_DATA_WAREHOUSE_CLOUD/cloud/en-US
- **SAP Analyics Cloud**
     - SAP Analytics Cloud Getting Started: https://community.sap.com/topics/cloud-analytics/getting-started  
     - SAP Analytics Designer Developer Handbook: https://blogs.sap.com/2021/08/25/introduction-to-analytics-designer-developer-handbook/
- **SAP Data Intelligence**
     -  SAP Data Intelligence Tutorials: https://blogs.sap.com/2021/02/04/sap-data-intelligence-hands-on-video-tutorials/

## License
Copyright (c) 2021 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.

[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/data-warehouse-cloud-modeling)](https://api.reuse.software/info/github.com/SAP-samples/data-warehouse-cloud-modeling)

![visitor badge](https://visitor-badge.glitch.me/badge?page_id=d031182.visitor-badge&left_color=blue&right_color=lightblue&left_text=visitors)


