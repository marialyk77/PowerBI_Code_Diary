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

+ Switch  is used to evaluate multiple conditions sequentially and return a value when the condition is met.
+ But, the Switch  evaluates equality (=) rather than comparison operators like <, >, <=, and >= directly.
+ True : The True acts as a placeholder and allows the use of comparison operators. 
