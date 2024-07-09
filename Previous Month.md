# Previous Month 

## Previous Month Revenue = CALCULATE([Total Revenue], DATEADD('Calendar Lookup'[Date], -1, MONTH))

![Previous Month Revenue](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/621fcc18-d54d-4bad-b9a0-b80e206b9418)

+ -1, MONTH: refers to the number of intervals in the past. Here we look at 1 month before! 

## Previous Months Returns = CALCULATE([Total Returns], DATEADD('Calendar Lookup'[Date], -1, MONTH))

![Previous Months Returns](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/dc792853-5ea3-4da1-9589-d8701eda8d2b)

## Previous Months Orders = CALCULATE([Total Returns], DATEADD('Calendar Lookup'[Date], -1, MONTH))

![Previous Months Orders](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/fab3587a-0a74-4d6f-944f-d75fcfb32591)

## Previous Month Profit = CALCULATE( [Total Profit], DATEADD( 'Calendar Lookup'[Date], -1, MONTH))

![Previous Month Profit](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/fcebf924-d3a7-459d-b99e-c439c42a6505)

