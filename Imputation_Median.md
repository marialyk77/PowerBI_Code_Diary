# Simultaneous Replacement of Zero Values with Median Across Multiple Columns

This imputation process calculates the median of values across multiple columns for each row and replaces any 0 values in these columns with the computed median. 

This approach applies the transformation to all specified columns simultaneously. 

**Step 1: Calculate Median for Each Row**

    = Table.AddColumn(

    #"Replaced Value, nulls, 0", 
    
    "Median", 
    
    each List.Median({
    
        [Column1], [Column2], [Column3], [Column4], [Column5], [Column6], 
        
        [Column7], [Column8], [Column9], [Column10], [Column11], [Column12], 
        
        [Column13], [Column14], [Column15], [Column16], [Column17], [Column18], 
        
        [Column19], [Column20], [Column21]
    }), 
    
    type number
    
)

Adds a new column named Median containing the median of values from the specified columns for each row.

Utilizes the List.Median function to compute the median value for the listed columns.

**Step 2: Replace 0 Values with Median Across Multiple Columns**

= Table.TransformColumns(

    #"Inserted Median",
    
    List.Transform(
    
        {"Column1", "Column2", "Column3", "Column4", "Column5", "Column6",
        
         "Column7", "Column8", "Column9", "Column10", "Column11", "Column12", 
         
         "Column13", "Column14", "Column15", "Column16", "Column17", "Column18", 
         
         "Column19", "Column20", "Column21"},
         
        (columnName) => {columnName, each if _ = 0 then [Median] else _, type number}
        
    )
    
)

The cose uses: **Table.TransformColumns** and **List.Transform** functions to iterate over each specified column and apply the transformation in a single step.

Within the  **List.Transform** there is a lambda function: **(columnName) => {columnName, each if _ = 0 then [Median] else _, type number}**

![image](https://github.com/user-attachments/assets/7573476e-3390-4ecc-8d52-5df31b7acd89)

**List.Transform** is a function used to apply a transformation to each item in a list. The lambda function specifies what transformation should be applied. 

**columnName:** Represents each column name from the list {"Column1", "Column2", ..., "Column21"}.

**each if _** = 0 then [Median] else _: Defines how each value in the column should be transformed.

**_:** Represents each individual value in the column.

**if _** = 0 then [Median] else _: Replaces 0 with the median value, otherwise keeps the original value.

**type number**: Ensures the column retains the number type after transformation.

