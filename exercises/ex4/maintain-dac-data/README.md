# Maintain Data for a Data Access Control

In this exercise we will maintain data of a **Data Access Control** and grant your user access to specific data of the view **_V_MY_INTERNAL_ORDERS_**. 
This you will do by editing and inserting new entries directly into the Data Access Control table **_T_DAC_DATA_**.
Of course, you could also upload CSV file, which contains the access values for all users.

>For more information please see the [SAP Help site](https://help.sap.com/viewer/c8a54ee704e94e15926551293243fd1d/cloud/en-US/a032e51c730147c7a1fcac125b4cfe14.html).

## Maintain allowed value in _T_DAC_DATA_
In the first step you define a local table, which contains the allowed value for a user.

1. Navigate to the Repository Explorer
2. Search and open the table _**T_DAC_DATA**_ 
  <br><br>![](../images/maintain_dac_01.png)

 
3. Click on the **Open Data Editor** button to enter the editing mode of the table:
  <br><br>![](../images/create_dac_table_02.png)
4. Click on the **Add** button to create a new record with the following values:
   ALLOWED_VALUE | USER_EMAIL | USER_ID
   ---|---|---
   9004 | _your user email_ | _your user id_  
   
   <br><br>![](../images/maintain_dac_03.png)

5. Click on the **Save** button to insert the records into the table.
  <br><br>![](../images/maintain_dac_04.png)
  

## Data Preview in View V_MY_INTERNAL_ORDERS 
6. Navigate to the Repository Explorer
7. Search and open the view _**V_MY_INTERNAL_ORDERS**_ 
   <br><br>![](../images/maintain_dac_05.png)
8. Select on the _Output_ Node the Data Preview from the context menu. As a result you should be able to see only data for **Company Code 9004**, which is maintained in the table **T_DAC_DATA**
   <br><br>![](../images/maintain_dac_06.png)
