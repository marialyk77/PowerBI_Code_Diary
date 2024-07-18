# Length 

Text.Length([hdicode])


![image](https://github.com/user-attachments/assets/475e2edd-445b-4c98-8260-0ac32cd617f9)

+ Where I Needed It:
+ I was attempting to create a conditional column to update categories to a more readable format. However, every row's output was "other," even though my typing seemed correct at first glance.
![what is wrong](https://github.com/user-attachments/assets/525ceb4c-fd98-474d-8de9-6bdcd283c35f)

+ How I Used It:
  
By utilizing the Text.Length([hdicode]) function on the source column, I discovered that the issue was due to unintentionally adding extra white spaces when typing the categories into the Conditional column dialog box.

+ Conclusion:
  
This experience taught me that adding unintended extra spaces can cause Power BI to not recognize the categories as identical, even if the spelling is correct, leading to incorrect conditional outcomes.

+ Correct Result:

![image](https://github.com/user-attachments/assets/45194b89-4b42-493e-921b-80400f747ae8)
