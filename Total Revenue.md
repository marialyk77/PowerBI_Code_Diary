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

