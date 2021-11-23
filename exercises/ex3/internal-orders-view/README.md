 # Create Internal Orders View

1. Navigate to the Repository Explorer
2. Click on <b><i>Create - Graphical View</i></b> Button to create a new view
  <br><br>![](../images/internal_orders_view_00.png)<br><br>
3. Drag and drop the table **_CSV_InternalOrders_** into the canvas.
  <br><br>![](../images/internal_orders_view_01.png)

4. Select the Output Node in the canvas and configure the following properties:
  - Business Name: <b>V_INTERNAL_ORDERS</b>
  - Technical Name: <b>V_INTERNAL_ORDERS</b>
  - Semantic Usage: <b>Analytical Dataset</b>
  - Expose for Consumption: <b>ON</b>
  <br><br>![](../images/internal_orders_view_02.png)
5. Select the *Output Node* and change the following columns to **Measure**:
  - **GROSSAMOUNT**
  - **NETAMOUNT**
  - **TAXAMOUNT**
  - **QUANTITY**
  <br><br>![](../images/internal_orders_view_03.png)

6. Select the **_CSV_InternalOrders_ Node** and add a new **Projection Node** from the context menu
  <br><br>![](../images/internal_orders_view_04.png)


7. Select the _Projection Node_ and change the name of the column **CREATEDAT** 
  <br><br>![](../images/internal_orders_view_05.png)
  
8. Set the new name to **CREATE_DATE**
  <br><br>![](../images/internal_orders_view_06.png)
  
9. Select the _Output Node_ and add a new **Association**
 <br><br>![](../images/internal_orders_association_01.png)

10. Search and select the view **V_VENDOR_PRODUCTS**
 <br><br>![](../images/internal_orders_association_02.png)

11. Map the column **V_VENDOR_PRODUCTS.PRODUCTID** with the column **V_INTERNAL_ORDERS.PRODUCTID**
 <br><br>![](../images/internal_orders_association_03.png)

12. Select the _Output Node_ and add a new **Association**
 <br><br>![](../images/internal_orders_association_04.png)

13. Search and select the view **V_EMPLOYEES**
 <br><br>![](../images/internal_orders_association_05.png)

14. Map the column **V_EMPLOYEES.EMPLOYEEID** with the column **V_INTERNAL_ORDERS.EMPLOYEEID**
 <br><br>![](../images/internal_orders_association_06.png)

15. Select the _Output Node_ and add a new **Association**
 <br><br>![](../images/internal_orders_association_07.png)

16. Search and select the view **SAP.TIME.VIEW_DIMENSION_DAY (Time Dimension - Day)**
 <br><br>![](../images/internal_orders_association_08.png)

17. Map the column **V_INTERNAL_ORDERS.CREATE_DATE** with the column **SAP.TIME.VIEW_DIMENSION_DAY.DATE_SQL**
  <br><br>![](../images/internal_orders_association_09.png)

18. Click on the **Deploy** button to deploy the view.
  <br><br>![](../images/internal_orders_view_07.png)
  <br><br>![](../images/internal_orders_view_08.png)


  




  
