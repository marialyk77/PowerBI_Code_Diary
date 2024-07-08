# Total Orders = DISTINCTCOUNT('YourTableName'[Order Number])

![carbon (2)](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/e38e5ec5-c52a-42cc-ae6e-620a3f1e7c7e)


* The Total Orders refers to the Volume of orders, not the quantity that customers bought. .

For this measure the emphasis is on [Order Number] column.


Ex:

![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/ae587aff-f06b-45bc-8628-4e7b7d05c3d6)

Total Orders = DISTINCTCOUNT('Sales Data'[Order Number])

Result = 3 , because there are three distinct orders (Order Numbers 1, 2, and 3).



* Less common code: Total Orders = COUNTROWS('Sales Data') 

1. It is going to count all rows!
2.  Generally not appropriate for counting distinct orders if the table contains multiple rows per order (e.g., one row for each line item in an order). As it is going to sum all the Line items as a different order, while the belong to the same order. 



![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/e5ee3718-49e5-4747-bb5a-41c0e9633370)


COUNTROWS('Sales Data'): This will return 5, because there are five rows in total in the 'Sales Data' table, which sums all line items.

