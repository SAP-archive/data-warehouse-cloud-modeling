# Create Sales Story in SAP Analytics Cloud

1. In SAP Analytics Cloud navigate to **Stories** to add a new **Canvas**
  <br><br>![](../images/create_sales_story_01.png)

2. Click on **Add Data** button
 <br><br>![](../images/create_sales_story_02.png)

3. Click on **Data from a Data Source** 
  <br><br>![](../images/create_sales_story_03.png)

4. Click on **Connect to Live Data** and select your *SAP Data Warehouse Cloud* instance
  <br><br>![](../images/create_sales_story_04.png)

5. Select your Space, e.g. **ZST_WORKSHOP**
  <br><br>![](../images/create_sales_story_05.png)

6. Select the model **V_SALES_ORDERS**
  <br><br>![](../images/create_sales_story_06.png)

7. Add the object **Table** into the canvas
  <br><br>![](../images/create_sales_story_07.png)
  
8. Select the *table* object and make sure that the measure **GROSSAMOUNT** is by default in the **Filters** section 
9. Add new **Measures/Dimensions** into the **Rows**
  <br><br>![](../images/create_sales_story_08.png)
 
10. Select the column **PRODUCTID**
  <br><br>![](../images/create_sales_story_09.png)

### Display ID and Description

11. For the column **PRODUCTID** set the display option to **ID and Description**.
  <br><br>![](../images/create_sales_story_10.png)

### Save the Story
12. Click on the **Save** button on the toolbar.
  <br><br>![](../images/create_sales_story_11.png)

13. As the name for the story, please enter **S_SALES**.
  <br><br>![](../images/create_sales_story_12.png)

### Change the Data Access Language 
14. Select the **Profile Settings**.
<br><br>![](../images/create_sales_story_13.png)

15. Change the **User Preferences** as the follwoing and click on **Save** button to confirm:
  - Data Access Language: **Deutsch** (German)
  <br><br>![](../images/create_sales_story_14.png)

16. Please check the description language of **PRODUCTID RC-1055** has been changed its language to German with description *Rennsemmel*.  
  <br><br>![](../images/create_sales_story_15.png)

### Level Based Hierarchy
17. Add a new **Table** into the canvas.
  <br><br>![](../images/create_sales_story_20.png)

18. Add new **Measures/Dimensions** into the **Rows** section
  <br><br>![](../images/create_sales_story_21.png)

19. Select the column **PARTNERID**.
  <br><br>![](../images/create_sales_story_22.png)

20. Expand the **Hierarchy** on the table. Please validate the the hieararhcy is organized by **REGION**, **COUNTRY**, **CITY**.
  <br><br>![](../images/create_sales_story_23.png)

### Time Series
21. Add a new **Chart** into the canvas.
  <br><br>![](../images/create_sales_story_30.png)
  
22. Add a new **Measure** into the chart.  
  <br><br>![](../images/create_sales_story_31.png)
  
23. Select the column **GROSSAMOUNT**.  
  <br><br>![](../images/create_sales_story_32.png)
  
24. Add new **DIMENSION** into the dimensions section.  
  <br><br>![](../images/create_sales_story_33.png)
  
25. Select the column **CREAT_DATE**.  
  <br><br>![](../images/create_sales_story_34.png)
  
26. Click on the **Hierarchy** button on the chart and set the level to **Level 2**.  
  <br><br>![](../images/create_sales_story_35.png)

27. In the Filters section add a new **Range Filter** for **CREATE_DATE** 
  <br><br>![](../images/create_sales_story_35a.png)

28. Set the the **Look Back** property to **3**.
  <br><br>![](../images/create_sales_story_35b.png)
  
29. Open the context menu of the chart, and click on **Compare To - Previous Year**.
  <br><br>![](../images/create_sales_story_36.png)

30. A new variance calculation will be added to the chart, which you can always change from the **Variance section**.
  <br><br>![](../images/create_sales_story_36a.png)

### Geo Spatial
28. Add a new **Geo Map** into the canvas.
  <br><br>![](../images/create_sales_story_40.png)
  
29. Add a new **Layer** into the Geo Map.
  <br><br>![](../images/create_sales_story_41.png)
  
30. Set Layer Type to **Bubble Layer** and add a new **Location* Dimension*
  <br><br>![](../images/create_sales_story_42.png)
  
31. Select the column **Location**. 
  <br><br>![](../images/create_sales_story_43.png)
  
32. Add a new **Measure** for **Bubble Size**.  
  <br><br>![](../images/create_sales_story_44.png)
  
33. Select the column **GROSSAMOUNT**.  
  <br>![](../images/create_sales_story_45.png)
  
34. Add a new **Measure** for **Bubble Color**.  
  <br><br>![](../images/create_sales_story_46.png)
  
35. Select the column **QUANTITY**.   
  <br>![](../images/create_sales_story_47.png)

### Save the Story 

36. Click on **Save** button to save the story **S_SALES**.
  <br><br>![](../images/create_sales_story_48.png)

