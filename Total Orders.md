# Total Orders = DISTINCTCOUNT('YourTableName'[Order Number])

The Total Orders is the Volume of orders.

For this measure the emphasis is on [Order Number] column.

With total orders we count the number of orders not the quantity that customers bought. 

Ex: If a Customer made one order and bought 3 items. Total Orders is 1! And Total Quantity is 3!

![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/729894ff-9347-47f2-8c3c-61db57fbc2da)



# Less common code: Total Orders = COUNTROWS('Sales Data') 

-- is going to count all rows!
-- Generally not appropriate for counting distinct orders if the table contains multiple rows per order (e.g., one row for each line item in an order).
-- The COUNTROWS function would count the line items even though in the same order.



![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/bddfeba8-5b88-4ad5-84d2-e99416476842)

DISTINCTCOUNT('Sales Data'[Order Number]): This will return 3, because there are three distinct orders (Order Numbers 1, 2, and 3).

COUNTROWS('Sales Data'): This will return 5, because there are five rows in total in the 'Sales Data' table, which includes all line items.

