# Divide Function

+ Ideal to perform divisions, when you want to avoid errors occur by dividing by zero.
+ If the denominator is zero or blank, instead of causing an error, DIVIDE returns an alternative result (if specified) or BLANK().
## SafetyDivision = DIVIDE(10, 0, "Division by zero error")


## Week-day/end % Difference = DIVIDE([Total Weekday Trips] - [Total Weekend Trips], [Total Weekend Trips]) * 100

![Week Day Weekend % Difference](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/385eba4d-cad4-4030-8cf7-155ad6f8f986)


## % Late Shipment= DIVIDE( CALCULATE( COUNTROWS(Sales), Sales[On TimeShipment] = "Late"),COUNTROWS(Sales),0) * 100

![% Late Shipment](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/335898c2-385c-4cac-80c9-63640527dd45)


## % On Time Shipment = DIVIDE( CALCULATE( COUNTROWS(Sales), Sales[On TimeShipment] = "On Time" ), COUNTROWS(Sales),0)*100

![% On Time Shipment](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/58f5c1cd-a9ee-4dfd-b762-ec6c6576d10a)


