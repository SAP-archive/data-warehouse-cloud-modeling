# Create <i>Employees</i> View

1. Navigate to the Repository Explorer
2. Click on <b><i>Create - Graphical View</i></b> Button to create a new view
  <br><br>![](/exercises/ex1/images/create_in_repository_explorer.png)<br><br>
3. Drag and drop the table <b><i>T_EMPLOYEES</i></b> into the canvas
  <br><br>![](../images/employee_view_02.png)
4. Select the Output Node in the canvas and configure the following properties:
    - Business Name: <b>V_EMPLOYEES</b>
    - Technical Name: <b>V_EMPLOYEES</b>
    - Semantic Usage: <b>Dimension</b>
    - Expose for Consumption: <b>ON</b>
    <br><br>![](../images/create_employee_dimension_03.png)

5. Click on the <b>Hierarchy</b> button 
  <br><br>![](../images/create_employee_dimension_04.png)
6. Add a new <b>Parent Child Hieararchy</b> (aka Internal Hierarchy)
  <br><br>![](../images/create_employee_dimension_05.png)
7. Adjust the following properties:
    - Business Name: <b>Employee Hierarchy</b>
    - Technical Name: <b>EMP_HIER</b>
    - Parent Column: <b>MANAGERID</b>
    - Child Column: <b>EMPLOYEEID</b>
  <br><br>![](../images/create_employee_dimension_06.png)
8. Select the Output Node in the canvas and click on <b>Data Preview</b> from the context menu
    <br><br>![](../images/create_employee_dimension_10.png)
9. Click on <b><i>deploy</i></b> button to deploy the view
  <br><br>![](../images/create_employee_dimension_08.png)







