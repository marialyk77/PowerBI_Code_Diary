# IN Operator 

## Weekend = IF('Calendar Lookup'[Week Day] IN {6,7}, "Weekend", "Weekday")

![IN](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/3896d652-e8a5-40d6-8ff8-144df03c812b)

+ It provides a more concise and readable way to check if a value exists within a set of values. In contrast, using logical OR (||) to achieve the same result requires explicitly listing each condition, which can be more time consuming.

## Weekend = IF('Calendar Lookup'[Week Day] = 6 || 'Calendar Lookup'[Week Day] = 7, "Weekend", "Weekday")

![OR](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/62e97bee-43f2-4e43-a766-a27cfc6f19af)

## Day Type with IN 
Day Type = IF('Calendar Lookup'[Week Day] IN {1, 2, 3, 4, 5}, "Weekday", "Weekend")

![Day Type IN](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/896adcb4-bd92-4be5-9c4d-dea29d192e5f)

## Day Type with OR 
Day Type = 
IF(
    'Calendar Lookup'[Week Day] = 1 || 
    'Calendar Lookup'[Week Day] = 2 || 
    'Calendar Lookup'[Week Day] = 3 || 
    'Calendar Lookup'[Week Day] = 4 || 
    'Calendar Lookup'[Week Day] = 5,
    "Weekday",
    "Weekend")
![Day Type OR](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/57c7b557-16d7-47a0-8e98-801bacd0300a)

+ Days are defined as follows in Back and Front end: 

![image](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/ede90efd-f3cd-4dc1-9568-e20119d47e30)

## Income Level with SWITCH and IN
Income Level = 

SWITCH(

    TRUE(),
    
    Customers[yearly_income] IN {"$110K - $130K", "$130K - $150K", "$150K +"}, "Very High",

    Customers[yearly_income] IN {"$10K - $30K", "$30K - $50K"}, "Average",
    
    "Low"
)
![Income level switch in](https://github.com/marialyk77/PowerBI_Code_Diary/assets/139682076/b29918d0-b4ba-4472-b998-4ad041b50cc3)




