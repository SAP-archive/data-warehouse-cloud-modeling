
<br><br>![](../images/special_sales_orders_01.png)
<br><br>![](../images/special_sales_orders_02.png)
<br><br>![](../images/special_sales_orders_03.png)



```
create column table T_SPECIAL_SALES_ORDERS(
	SALESORDERID bigint, 
	SALESITEM bigint,
	CREATEDAT date, 
	PARTNERID bigint,
	PRODUCTID varchar(5000),
	QUANTITY int,
	NETAMOUNT decimal(38,19),
	GROSSAMOUNT decimal(38,19),
	TAXAMOUNT decimal(38,19),
	CURRENCY varchar(5000),
	PRIMARY KEY (SALESORDERID, SALESITEM)
)
```
<br><br>![](../images/special_sales_orders_04.png)
<br><br>![](../images/special_sales_orders_05.png)

```
insert into T_SPECIAL_SALES_ORDERS values(	
	700000001, '10','2021-01-01', '100000014', 'HB-1173', '5', '3333', '3777', '444', 'USD'
)
```
<br><br>![](../images/special_sales_orders_06.png)


<br><br>![](../images/special_sales_orders_07.png)

```
select * from T_SPECIAL_SALES_ORDERS
```
<br><br>![](../images/special_sales_orders_08.png)


