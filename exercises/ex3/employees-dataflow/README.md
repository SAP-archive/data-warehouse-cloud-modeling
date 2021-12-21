# Create <i>Employees </i> Data Flow

1. Navigate to the Repository Explorer
2. Click on **Create - Data Flow** button to create a new view
  <br><br>![](../images/empoloyee_dataflow_01.png)
3. Click on **Details** button and configure the following properties:
  - Business Name: **DF_COSTCENTER**
  - Technical Name: **DF_COSTCENTER**
  <br><br>![](../images/cost_center_dataflow_02.png)

<br><br>![](../images/cost_center_dataflow_03.png)
<br><br>![](../images/cost_center_dataflow_04.png)
<br><br>![](../images/cost_center_dataflow_05.png)
<br><br>![](../images/cost_center_dataflow_06.png)
<br><br>![](../images/cost_center_dataflow_07.png)
<br><br>![](../images/cost_center_dataflow_08.png)
<br><br>![](../images/cost_center_dataflow_09.png)
<br><br>![](../images/cost_center_dataflow_10.png)



    #####################################################
    # Provide the function body for data transformation #
    #####################################################
    data["COMP_COSTCTR"] = (data["COMPANYCODE"].astype(str) +  data["COSTCENTER"])   
    return data


<br><br>![](../images/cost_center_dataflow_11.png)
<br><br>![](../images/cost_center_dataflow_12.png)
<br><br>![](../images/cost_center_dataflow_13.png)
<br><br>![](../images/cost_center_dataflow_14.png)
<br><br>![](../images/cost_center_dataflow_15.png)
<br><br>![](../images/cost_center_dataflow_16.png)
<br><br>![](../images/cost_center_dataflow_17.png)
<br><br>![](../images/cost_center_dataflow_18.png)
<br><br>![](../images/cost_center_dataflow_19.png)



