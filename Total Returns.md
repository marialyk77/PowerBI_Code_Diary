
## Total Returns = COUNTA('Returns Data'[ProductKey])
![carbon (1)](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/19b31ed2-c761-4aa8-b3bb-85f2f9f4b537)



The concept of Total Returns refers to the number of return transactions rather than the quantity of products returned. It measures how many times a customer initiates a return, regardless of the number of items returned in each transaction.

-------- A customer decides to return 2 items in one go. That makes Total Returns = 1 

* COUNTA: 

DAX: COUNTA('Returns Data'[ProductKey])

Use when: You need to count all Non-Blank rows in a column. COUNTA counts the number of records regardless of data type. They can be numeric, text, dates, etc. 
Example: To identify how many return transactions occurred based on the ProductKey column.

* As of the COUNT:
 
DAX: COUNT('Returns Data'[ReturnQuantity]) 

Use when: It is also counting all Non- Blank numeric values in a column. And it is also going to identify how many transactions occured but not on the Product Key column if that contains text values. Because, it is appropriate when the column contains only NUMERIC DATA.

Example: To identify how many return transactions occurred based on the Return Quantity column.

## Conclusion: 

![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/a8ba51dc-e509-4857-aa1c-8f98331f0688)

** COUNTA('Returns Data'[Product Key]): Counts all non-blank values in the Product Key column.

Result: 4 (because there are 4 non - blank text values : A12, A13 ,A14, A15)
 
**COUNT('Returns Data'[Return Quantity]) : Counts only the numeric, non-blank values in the Return Quantity column.

Result: 4 (because there are 4 non-blank numeric values: 2, 6, null, 20, 12)

### And for further food of thought: 

Quantity Returned = SUM('Returns Data'[Return Quantity])

Result: 40 (because it sums up and tells how many products were returned) 


+ As of the COUNTROWS: 

If you have a column with BLANKS and for some reason you need to count them, then use the COUNTROWS:  

DAX ## Total Returns = COUNTROWS('Returns Data')

![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/97076e5e-be0f-498e-abf5-bc2f8d7feab4)

Total Returns = COUNTROWS('Returns Data') 

     Result = 5 , because it counts the Null ROWS! 

Total Returns = COUNTA('Returns Data'[Product Key]) 

     Result = 4 , because the Null Rows are not considered. 

Total Returns = COUNT('Returns Data'[Return Quantity]) 

     Result = 4 , because the Null Rows are not considered. 



