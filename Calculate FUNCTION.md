# Calculate function

## Total Weekday Trips =  CALCULATE(COUNTROWS(TABLE NAME), TABLE NAME [WeekdayOrWeekend] = "Weekday")

## Total Weekend Trips = CALCULATE( COUNTROWS(TABLE NAME), TABLE NAME [WeekdayOrWeekend] = "Weekend")

* CALCULATE: modifies the context in which the data is evaluated.


## Average Ride of Length for a specific group:

Average of Ride Length for casual = CALCULATE( AVERAGE('TRIPDATA'[Ride Length]), 'TRIPDATA'[Type of Customer] IN { "casual" })

Average of Ride Length for member = CALCULATE(AVERAGE('TRIPDATA'[Ride Length]),'TRIPDATA'[Type of Customer] IN { "member" })





