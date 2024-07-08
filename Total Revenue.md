# Total Revenue 

## Total Revenue = SUM(Railway[Price])
![Total Revenue _ SUM](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/690d1b38-2137-4f4d-81bb-33cc25237624)


* Use SUM for straightforward summation of a single column.
  
## Total Revenue = SUMX('YourTableName', 'YourTableName'[Quantity] * 'YourTableName'[Unit Price])

![Total Revenue__SUMX](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/6567b1c1-559f-49d4-ae1e-8fa0be7b95dd)

* SUMX is an iterator function. This means it performs row-by-row calculations across a table and then aggregates the results.It multiplies Quantity and Unit Price for each row and then summing these values across the entire table.
In other words, SUMX starts at the first row of 'YourTableName'. It evaluates the expression 'YourTableName'[Quantity] * 'YourTableName'[Unit Price] for that row. Moves to the next row and repeats the evaluation.


![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/09a02cbe-875b-44c0-b3eb-22e15c7c8440)


![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/323f2cdd-0d74-48bb-b617-b96377d9666f)

## Total Revenue = SUMX( 'Sales Data','Sales Data'[OrderQuantity] * RELATED('Product Lookup'[ProductPrice]))

![Total Revenue_SUMX_Related](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/9907f9a6-e0e8-4024-9b27-f04ca31e3730)

* No need for merging tables and columns and creating Redundant Data, you can easily use the Related function to fetch the Price column from the lookup table. 


## Total Revenue CC= SUM('YourTableName'[Revenue])
* In general, better to avoid having many Calculated Columns. Ideally, better to delete the column Revenue and replace it with a Measure.

  ![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/c6346e46-4250-4aba-b85d-567578cf5f51)




