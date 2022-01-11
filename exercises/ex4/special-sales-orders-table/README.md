
<br><br>![](../images/special_sales_orders_01.png)



```
	create column table T_SPECIAL_ORDER(
		INTERNALORDERID int primary key, 
		CREATE_DAT date, 
		COMPANYCODE varchar(4),
		COSTCENTER varchar(6),
		PRODUCTID varchar(9),
		QUANTITY int,
		NETAMOUNT decimal(38,19),
		CURRENCY varchar(3),
		COMPANYCODE_COSTCENTER varchar(10)
	)
```

<br><br>![](../images/open_sql_09.png)
<br><br>![](../images/open_sql_10.png)

```
insert into T_SPECIAL_ORDER values(	
	800000001, '2021-01-01', '9004', 'C01004', 
	'SPECIAL', 1, 400, 'EUR', '9004C01004' 
)
```

<br><br>![](../images/open_sql_11.png)

```
select * from T_SPECIAL_ORDER
```
<br><br>![](../images/open_sql_12.png)
<br><br>![](../images/open_sql_13.png)
