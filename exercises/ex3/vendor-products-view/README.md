# Create <i>Vendor Products</i> View

1. Navigate to the Repository Explorer
2. Click on <b><i>Create - Graphical View</i></b> Button to create a new view
  <br><br>![](/exercises/ex1/images/create_in_repository_explorer.png)<br><br>
3. Drag and drop the table <b><i>CSV_VendorProducts</i></b> into the canvas
  <br><br>![](/exercises/ex4/images/create_vendor_product_dimension_01.png)
4. Select the Output Node in the canvas and configure the following properties:
    - Business Name: <b>V_VENDOR_PRODUCTS</b>
    - Technical Name: <b>V_VENDOR_PRODUCTS</b>
    - Semantic Usage: <b>Dimension</b>
    - Expose for Consumption: <b>ON</b>
    <br><br>![](/exercises/ex4/images/create_vendor_product_dimension_02.png)
 5. Navigate to the <i>Attributes</i> section and click on <b>edit</b> button
    <br><br>![](/exercises/ex4/images/create_vendor_product_dimension_12.png)
 6. Adjust the following attribute properties:
    - <b>LONG DESCR</b>: set the semantic type to <b>TEXT</b>
    - <b>PRODUCT ID</b>: set the label to <b>LONG_DESCR</b>
    <br><br>![](/exercises/ex4/images/create_vendor_product_dimension_13.png)
 7. Close the Attribute Properties dialog
 8. Select the Output Node in the canvas and click on <b>Data Preview</b> from the context menu
   <br><br>![](/exercises/ex4/images/create_vendor_product_dimension_03.png)
 9. Click on <b><i>deploy</i></b> button to deploy the view
  <br><br>![](/exercises/ex4/images/create_vendor_product_dimension_04.png)







