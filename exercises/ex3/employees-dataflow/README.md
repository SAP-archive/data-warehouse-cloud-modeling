# Create <i>Employees </i> Data Flow

1. Navigate to the Repository Explorer
2. Click on **Create - Data Flow** button to create a new view
  <br><br>![](../images/employee_dataflow_01.png)
3. Click on **Details** button and configure the following properties:
  - Business Name: **DF_EMPLOYEES**
  - Technical Name: **DF_EMPLOYEES**
  <br><br>![](../images/employee_dataflow_02.png)

4. Drag and Drop the table **CSV_EMPLOYEES** into the canvas and set the type to **_Source_**. 
  <br><br>![](../images/employee_dataflow_03.png)

5. Add a new _Script_ Operator from the menu. The name is defaulted to **Script 1**.
  <br><br>![](../images/employee_dataflow_04.png)

6. Select the source operator **CSV_EMPLOYEES** and add a new _Link_ to the operator **Script 1**.
  <br><br>![](../images/employee_dataflow_05.png)
  <br><br>![](../images/employee_dataflow_06.png)

7. Select the operator **Script 1** and create a new column from the menu.
  <br><br>![](../images/employee_dataflow_07.png)

8. Maintain the following fields:
  - Name: **FULL_NAME**
  - Data Type: **string**
  - Length: **30**
  <br><br>![](../images/employee_dataflow_08.png)
  and click on _Save_ button.
  
  
<br><br>![](../images/employee_dataflow_09.png)
<br><br>![](../images/employee_dataflow_10.png)



    #####################################################
    # Provide the function body for data transformation #
    #####################################################
    data["COMP_COSTCTR"] = (data["COMPANYCODE"].astype(str) +  data["COSTCENTER"])   
    return data


<br><br>![](../images/employee_dataflow_11.png)
<br><br>![](../images/employee_dataflow_12.png)
<br><br>![](../images/employee_dataflow_13.png)
<br><br>![](../images/employee_dataflow_14.png)
<br><br>![](../images/employee_dataflow_15.png)
<br><br>![](../images/employee_dataflow_16.png)
<br><br>![](../images/employee_dataflow_17.png)
<br><br>![](../images/employee_dataflow_18.png)
<br><br>![](../images/employee_dataflow_19.png)



