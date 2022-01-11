
1. Navigate to the _Space Management_
2. Navigate to the _Database Access_ section
3. Select your created database user and click on _Open Database Explorer_  
	<br><br>![](../images/special_sales_orders_01.png)
4. Enter the user credentials and check the parameter _Save Password (saved in SAP HANA secure store)
	<br><br>![](../images/special_sales_orders_02.png)

5. Right click on the database _catalog_ and click on _Open SQL Console_ from the context menu.

	<br><br>![](../images/special_sales_orders_03.png)


6. Enter the following SQL DDL statement to create a database table for the special sales. 
	```
	create column table T_SPECIAL_SALES_ORDERS(
		SALESORDERID bigint, 
		SALESORDERITEM bigint,
		CREATEDAT date, 
		PARTNERID bigint,
		PRODUCTID varchar(5000),
		QUANTITY int,
		NETAMOUNT decimal(38,19),
		GROSSAMOUNT decimal(38,19),
		TAXAMOUNT decimal(38,19),
		CURRENCY varchar(5000),
		PRIMARY KEY (SALESORDERID, SALESORDERITEM)
	)
	```
7. Run the SQL statement. 
	<br><br>![](../images/special_sales_orders_04.png)
	
8. Open a new SQL console from the context menue
	<br><br>![](../images/special_sales_orders_05.png)

9. Enter the following SQL DML statement to insert data into the sales table
	```
	insert into T_SPECIAL_SALES_ORDERS values(	
		700000001, '10','2021-01-01', '100000014', 'HB-1173', '5', '3333', '3777', '444', 'USD'
	)
	```
10. Run the SQL statement
	<br><br>![](../images/special_sales_orders_06.png)

11. Open a new SQL console from the context menue
	<br><br>![](../images/special_sales_orders_07.png)

12. Enter the following SQL SELECT statement 
	```
	select * from T_SPECIAL_SALES_ORDERS
	```
	
13. Run the SQL statement to view the content of the table
	<br><br>![](../images/special_sales_orders_08.png)


