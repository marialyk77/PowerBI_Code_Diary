# ABS function 

![ABS_Outlier Flag](https://github.com/user-attachments/assets/642c6418-5bc7-4b66-86c8-d66078a02a30)

Outlier_Flag = IF(ABS('2000 Normal Dist HDI'[Z-Score]) > 3, "Outlier", "Not Outlier")

+ The ABS function handles both positive and negative values, ensuring that any z-score greater than 3 or less than -3 is flagged as an outlier. 
+ In other words, it checks if the absolute value of the z-score is greater than 3.
+ This means it will convert any negative z-score to a positive number before checking the condition.
+ Therefore, both a z-score of -4 and 4 will satisfy this condition because ABS(-4) = 4 and ABS(4) = 4, both of which are greater than 3.
