# Create Calculation Node with Currency Conversion

1. Navigate to the Repository Explorer
2. Search and open the view **V_INTERNAL_ORDERS** Button to create a new view
  <br><br>![](../images/internal_orders_currency_conversion_01.png)<br><br>
3. Select the source node <b>CSV_InternalOrders</b> and add a new Calculation Node from the context menu.
<br><br>![](../images/internal_orders_currency_conversion_02.png)

4. Select the Calculation Node and add a new <b>Calculated Column</b>.
<br><br>![](../images/internal_orders_currency_conversion_03.png)

5. Configure the Calculated Column as the following:
    - Business Name: <b>TARGET_CURRENCY</b>
    - Technical Name: <b>TARGET_CURRENCY</b>
    - Data Type: <b>Double</b>
    - Length: <b>3</b>
    - Expression: <b>'EUR'</b>
    <br><br>![](../images/internal_orders_currency_conversion_04.png)

6. Select the Calculation Node and add another <b>Calculated Column</b>.
  <br><br>![](../images/internal_orders_currency_conversion_03.png)

7. Configure the Calculated Column as the following:
  - Business Name: <b>NETAMOUNT_TG</b>
  - Technical Name: <b>NETAMOUNT_TG</b>
  - Data Type: <b>Double</b>
  - Length: <b>3</b>
  - Expression: 
  
    ```javascript
    CONVERT_CURRENCY(
      "AMOUNT" => "NETAMOUNT", 
      "SOURCE_UNIT" => "CURRENCY", 
      "TARGET_UNIT" => 'EUR', 
      "CONVERSION_TYPE" => 'M', 
      "REFERENCE_DATE" => CURRENT_DATE, 
      "CLIENT" => '002', "SCHEMA" => 'ZST_WORKSHOP', 
      "ERROR_HANDLING" => 'set_to_null', 
      "STEPS" => 'shift,convert,round', 
      "PRECISIONS_TABLE" => 'V_TCURX', 
      "CONFIGURATION_TABLE" => 'V_TCURV', 
      "PREFACTORS_TABLE" => 'V_TCURF', 
      "RATES_TABLE" => 'V_TCURR',
      "NOTATION_TABLE" => 'V_TCURN')
    ```
    
  >🎓 **CONVERT_CURRENCY() Function**: More information about the SAP HANA Function and the configuration of the parameters can be found under the [SAP Help site](https://help.sap.com/viewer/7c78579ce9b14a669c1f3295b0d8ca16/Cloud/en-US/d22d746ed2951014bb7fb0114ffdaf96.html). 


  <br>![](../images/internal_orders_currency_conversion_05.png)
      
    
8. Select the Calculation Node and click on <b>Data Preview</b> from the context menu.
    - Validate the values in <b>NETAMOUNT_TG</b> and <b>TARGET_CURRENCY</b>
    - Compare the values between <b>NETAMOUNT</b> and <b>NETAMOUNT_TG</b>
      <br><br>![](../images/internal_orders_currency_conversion_06.png)

9. Select the _Output Node_ and set the column **NETAMOUNT_TG** as a Measure
  <br><br>![](../images/internal_orders_currency_conversion_07.png)

10. Click on <b><i>deploy</i></b> button to deploy the view
<br><br>![](../images/internal_orders_currency_conversion_08.png)
