
## Total Returns = COUNTA('Returns Data'[ProductKey])

The concept of Total Returns refers to the volume of Returns/ the transactions for Returns.

-------- A customer decides to return 2 items. That makes Total Returns = 1 


COUNTA:

Use when: You need to count all non-blank values in a column, regardless of type.

What it counts: All non-blank values (numeric, text, logical, etc.). Suitable when you want to count how many return records exist based on the presence of a ProductKey. 

 // COUNT:

Use when: You need to count numeric values in a column.

What it counts: All non-blank numeric values.

In Practice:

COUNTA('Returns Data'[ProductKey]) counts how many return records are associated with a product, regardless of the return quantity.

COUNT('Returns Data'[ReturnQuantity]) : Appropriate when you are interested in counting instances where a return quantity is recorded.

If we se the COUNTROWS, it will count the BLANKS! 
## Total Returns = COUNTROWS('Returns Data')

![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/3d9338cf-26c1-4a59-8c44-cee383571be4)

