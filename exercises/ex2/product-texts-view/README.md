# Create <i>Product Texts</i> View
In this exercise you will learn, how to create and configure Views of type <i>Text</i>.
>**Text View**: In SAP Data Warehouse Cloud Text Views typically interplay together with Dimension Views, and enable the support of multiple languages for textual columns. 
> With Text Views users are able to view the master data on the reports and stories in their preferred language. The column which determines the language should comply with ISO 639-1 (https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes), e.g. <b>en, de, fr</b>. Please note: for SAP ABAP systems, the one digit language will be automatically mapped against the ISO codes and will work out of the box, too!

## Exercise
1. Navigate to the Repository Explorer
2. Click on <b><i>Create - Graphical View</i></b> Button to create a new view
  <br><br>![](/exercises/ex1/images/create_in_repository_explorer.png)<br><br>
3. Drag and drop the table <b><i>CSV_ProductTexts</i></b> into the canvas
  <br><br>![](../images/create_product_texts_01.png)
4. Select the Output Node in the canvas and configure the following properties:
    - Business Name: <b>V_PRODUCT_TEXTS</b>
    - Technical Name: <b>V_PRODUCT_TEXTS</b>
    - Semantic Usage: <b>Text</b>
    - Expose for Consumption: <b>ON</b>
    <br><br>![](../images/create_product_texts_02.png)
 5. Set the <b>primary keys</b> to:
    - <b>PRODUCTID</b>
    - <b>LANGUAGE</b> 
    <br>![](../images/create_product_texts_03.png)
    <br>![](../images/create_product_texts_04.png)
 6. Click on <b><i>Edit Attributes</i></b> 
    <br><br>![](../images/create_product_texts_05.png)<br><br>
 7. Adjust the attributes properties as the following:
    - <b>LANGUAGE</b>: set the semantic usage to <b>Language</b>
    - <b>MEDIUM_DESCR</b>: set the semantic usage to <b>Text</b>
    - <b>PRODUCTID</b>: set label to <b>MEDIUM_DESCR</b>  
    <br>![](../images/create_product_texts_06.png)
 8. Select the Output node in the canvas, and click on <b>Data Preview</b> from the context menu to display the data of the view. 
    <br><br>![](../images/create_product_texts_07.png)
 9. Click on <b><i>deploy</i></b> button to deploy the view
  <br><br>![](../images/create_product_texts_08.png)
