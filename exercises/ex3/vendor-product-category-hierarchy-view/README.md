# Create Vendor Product Category Hierarchy View

1. Navigate to the Repository Explorer
2. Click on <b><i>Create - Graphical View</i></b> Button to create a new view
  <br><br>![](/exercises/ex1/images/create_in_repository_explorer.png)<br><br>
3. Drag and drop the table <b><i>CSV_VendorProductCategoryHierarchy</i></b> into the canvas
  <br><br>![](/exercises/ex4/images/create_vendor_product_category_hierarchy_01.png)
4. Select the Output Node in the canvas and configure the following properties:
    - Business Name: <b>V_VENDOR_PRODUCT_CATEGORY_HIERARCHY</b>
    - Technical Name: <b>V_VENDOR_PRODUCT_CATEGORY_HIER</b>
    - Semantic Usage: <b>Hierarchy</b>
    - Parent: <b>PARENTCATEGORY</b>
    - Child: <b>PRODUCTCATEGORY</b>
    - Expose for Consumption: <b>ON</b>
    <br><br>![](/exercises/ex4/images/create_vendor_product_category_hierarchy_02.png)
 4. Click on <b><i>deploy</i></b> button to deploy the view
  <br><br>![](/exercises/ex4/images/create_vendor_product_category_hierarchy_03.png)
