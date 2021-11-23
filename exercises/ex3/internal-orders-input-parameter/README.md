# Create Input Parameters

1. Navigate to the Repository Explorer
2. Search and open the view **V_INTERNAL_ORDERS** Button to create a new view
  <br><br>![](../images/internal_orders_input_parameter_01.png)<br><br>
3. Select the _Output Node_ and click on the **Edit** button in the _Input Parameter_ section.
  <br><br>![](../images/internal_orders_input_parameter_02.png)
4. Add a new Input Parameter with the following properties:
    - Business Name: **IP_TARGET_CURRENCY**
    - Technical Name: **IP_TARGET_CURRENCY**
    - Data Type: **String**
    - Length: **3**
    
    <br>![](../images/internal_orders_input_parameter_03.png)

5. Select the _Calculation Node_ and edit the column **NETAMOUNT_TG**
  <br><br>![](../images/internal_orders_input_parameter_04.png)

6. In the _Calculation Expression_ replace in the _CONVERT_CURRENCY()_ function the 'EUR' with the input parameter **:IP_TARGET_CURRENCY**
  <br><br>![](../images/internal_orders_input_parameter_05.png)

7. Select again the _Calculation Node_ and edit the column **TARGET_CURRENCY**
  <br><br>![](../images/internal_orders_input_parameter_06.png)

8. In the _Calculation Expression_ replace in the constant value 'EUR' with the input parameter **:IP_TARGET_CURRENCY**
  <br><br>![](../images/internal_orders_input_parameter_07.png)

9. Select the _Calculation Node _ and click on the **Data Preview** button from the context menu
  <br><br>![](../images/internal_orders_input_parameter_08.png)

10. In the _Input Parameter_ prompt enter the currency **AUD** (Australian Dollar)
  <br><br>![](../images/internal_orders_input_parameter_09.png)

11. Click on **OK** button to confirm. Please check the values on the columns **NETAMOUNT_TG** and **TARGET_CURRENCY**:
  <br><br>![](../images/internal_orders_input_parameter_10.png)

