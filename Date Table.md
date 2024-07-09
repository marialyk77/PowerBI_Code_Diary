## Date Table 

DateTable =

ADDCOLUMNS(

    CALENDAR(
    
        MIN(railway[Date of Purchase]),
        
        MAX(railway[Date of Purchase])
    ),
    
    "Year", YEAR([Date]),
    
    "Month Number", MONTH([Date]),
    
    "Month Name", FORMAT([Date], "MMM"),
    
    "Quarter", QUARTER([Date]),
    
    "Weekday", WEEKDAY([Date], 2),
    
    "Start of Month", DATE(YEAR([Date]), MONTH([Date]), 1),
    
    "Start of Week", [Date] - WEEKDAY([Date], 2) + 1
)

