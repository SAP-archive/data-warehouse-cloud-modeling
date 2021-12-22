# Create Internal Orders Story in SAP Analytics Cloud

1. In SAP Analytics Cloud navigate to **Stories** to add a new **Canvas**
  <br><br>![](../images/internal_orders_story_01.png)
2. Click on **Add Data**
  <br><br>![](../images/internal_orders_story_02.png)
3. Click on **new Data Source**  
  <br><br>![](../images/internal_orders_story_03.png)
4. Select from the _Connect to Live Data_ section the connection to **SAP Data Warehouse Cloud**
  <br><br>![](../images/internal_orders_story_04.png)

5. Add a **new Table** to the canvas
  <br><br>![](../images/internal_orders_story_05.png)
  
6. Select **V_INTERNAL_ORDERS** as the data source
  <br><br>![](../images/internal_orders_story_06.png)
  
7. Since the model _V_INTERNAL_ORDERS_ contains an _Input Parameter_, a Prompt Dialog will show up. Please enter **EUR** as currency for the parameter **IP_TARGET_CURRENCY**.
  <br><br>![](../images/internal_orders_story_07.png)

8. **Filter** the measures from the **Columns** section 
  <br><br>![](../images/internal_orders_story_08.png)

9. Select the measure **NETAMOUNT_TG** 
  <br><br>![](../images/internal_orders_story_09.png)
  <br><br>![](../images/internal_orders_story_09b.png)

10. Add the column **EMPLOYEEID** into the **Rows** section
  <br><br>![](../images/internal_orders_story_10.png)

11. **Expand the Employee Hierarchy** and check result as the following
  <br><br>![](../images/internal_orders_story_13.png)
  
12. Add a **new Table** into the canvas
  <br><br>![](../images/internal_orders_story_14.png)
  

13. **Filter** the measures from the **Columns** section 
  <br><br>![](../images/internal_orders_story_15.png)
  
14. Select the measure **NETAMOUNT_TG** 
  <br><br>![](../images/internal_orders_story_16.png)
  <br>![](../images/internal_orders_story_16b.png)

15. Add the column **PRODUCTID** into the **Rows** section
  <br><br>![](../images/internal_orders_story_17.png)

16. **Expand the Vendor Product Category Hierarchy** and check result as the following
  <br><br>![](../images/internal_orders_story_18.png)

16. Click on **Data** from the toolbar
  <br><br>![](../images/internal_orders_story_19.png)

17. Click on **Add New Data**
  <br><br>![](../images/internal_orders_story_20.png)

17. Click on _Data from a data source_.
  <br><br>![](../images/internal_orders_story_21.png)

18. Select _SAP Data Warehouse Cloud_ as a source.
  <br><br>![](../images/internal_orders_story_22.png)

19. Select the configured connection.
  <br><br>![](../images/internal_orders_story_23.png)

20. Select your working space.
  <br><br>![](../images/internal_orders_story_24.png)
  
21. Select the model **V_MY_INTERNAL_ORDERS**
  <br><br>![](../images/internal_orders_story_25.png)
  
22. Return to the story by clicking on the _Story_ button from the toolbar.
  <br><br>![](../images/internal_orders_story_26.png)
  
23. Add a new _Table_.
  <br><br>![](../images/internal_orders_story_27.png)

24. Make sure that the new data source **V_MY_INTERNAL_ORDERS** is selected.
  <br><br>![](../images/internal_orders_story_28.png)

25. Add the column **COMPANYCODE** in the section _Rows_.
  In the table, you should be able to see records for the company code **9004** only.
  <br><br>![](../images/internal_orders_story_29.png)

26. Click _Save_ to save the story.
  <br><br>![](../images/internal_orders_story_30.png)

27. Enter the story name **S_INTERNAL_ORDERS**
  <br><br>![](../images/internal_orders_story_31.png)

28. The end result should look like the following:
  <br><br>![](../images/internal_orders_story_32.png)
