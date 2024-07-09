# Switch Function and Variables 

+ Assuming we want to categorize Shipment Durations based on the Order Priority.

## Duration Category 

DurationCategory = 

VAR ExpectedTime =

    SWITCH(
    
        [Order Priority],
        
        "C", 1,
        
        "H", 2,
        
        "M", 7,
        
        "L", 10,
        
        BLANK()
    
    )
    
VAR DurationCategory = 

    SWITCH(
    
        TRUE(),
        
        [Shipment Duration] <= ExpectedTime, "On Time",
        
        [Shipment Duration] <= ExpectedTime + 5, "Up to 5 days late",
        
        [Shipment Duration] <= ExpectedTime + 10, "Up to 10 days late",
        
        [Shipment Duration] <= ExpectedTime + 20, "Up to 20 days late",
        
        [Shipment Duration] <= ExpectedTime + 30, "Up to 30 days late",
        
        [Shipment Duration] > ExpectedTime + 30, "Over 30 days late",
        
        "Unknown"
    )
RETURN DurationCategory

// or to concatenate: 

RETURN [Order Priority] & " : " & DurationCategory

![Duration Category](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/0814075d-bdac-4ad0-8d4f-08db676f785f)

