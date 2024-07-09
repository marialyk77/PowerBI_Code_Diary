# Switch FUNCTION 

## Purchase Time Bucket =

  SWITCH(

    TRUE(),
    
    TABLE NAME[Purchase Hour] >= 0 && TABLE NAME[Purchase Hour] < 6, "Night",
    
    TABLE NAME[Purchase Hour] >= 6 && TABLE NAME[Purchase Hour] < 12, "Morning",
    
    TABLE NAME[Purchase Hour] >= 12 && TABLE NAME[Purchase Hour] < 18, "Afternoon",
    
    TABLE NAME[Purchase Hour] >= 18 && TABLE NAME[Purchase Hour] < 24, "Evening"
    
)


##  Age Group =
  
SWITCH(

  TRUE(),
    
  'Table'[Age] < 18, "Child",
    
  'Table'[Age] >= 18 && 'Table'[Age] < 65, "Adult",
    
  'Table'[Age] >= 65, "Senior"
    
)


## Month Number 
Month Number = 

SWITCH(

    'Calendar Lookup'[Month Name], 
    
    "January", "1",
    
    "February", "2",
    
    "March", "3",
    
    "April", "4",
    
    "May", "5",
    
    "June", "6",
    
    "July", "7",
    
    "August", "8",
    
    "September", "9",
    
    "October", "10",
    
    "November","11",
    
    "December", "12",
    
    "Other")
    


+ Switch  is used to evaluate multiple conditions sequentially and return a value when the condition is met.
+ But, the Switch  evaluates equality (=) rather than comparison operators like <, >, <=, and >= directly.
+ True : The True acts as a placeholder and allows the use of comparison operators. 
