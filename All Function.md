## All Function 

+ It removes filters! 

## All Cost =   CALCULATE(SUMX('Sales', 'Sales'[Unit Cost] * 'Sales'[Units Sold]),    ALL('Sales'))

![All Cost](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/7d9ec6c5-4ac8-44de-9802-b60773a815e2)

* Suppose you have a report that allows users to filter sales data by region, date, or product category. While filtered visuals will show the cost for the selected criteria, the All Cost measure will always display the total cost of all sales, providing a constant reference point.


## All Orders = CALCULATE([Total Orders], ALL( 'Sales Data'))
