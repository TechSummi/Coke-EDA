# Coke-EDA
EDA_23 : Price variance for same Material,Plant and different Vendor.
Files used : EKKO,EKPO,LFA1 master data .
Step 1 - Load and process EKKO and EKPO data .
Step 2 - Removed whitespaces and converted the columns to desired datatypes.
Step 3 - Performed the first left merge on EKPO and EKKO as db1. left_on Purchasing Document , right_on Purchasing Document .
Step 4 - Applied the check prefix on Purchasing Document column i.e. value starts with ’42’ or ’45’ .
Step 5 - Sort the merged data frame db1 by Material, Plant, Vendor, and Created on columns. Step 6 - In Net Price and Per column , replaced the (‘,’) with (‘’) and converted to the desired
datatype .
Step 7 - Calculated the Net Order Price per Unit by Dividing "Net Price" to "Per".
Step 8 - Renamed the column Created on to PO Created on and covered to the date time format .
Step 9 - Applied groupby to the Material and Plant column on the basis of Net Order Price per Unit .
Step 10 - Create a new column with the previous PO price for the same Material and Plant but different vendor .
Step 11 - Compare the current PO price with the previous PO price , stored the sorted data into new data frame i.e. db1_sorted .
Step 12 - Made groups for the same Material and Plant but different Vendor . Step 13 - Created a group number column in the original data frame db1_sorted .
Step 14 - Iterate through each unique group and Filter the data frame for the current group . Step 15 - Calculated the price variation percentage , to check if the "PO Created on" date
difference between the current transaction and the last transaction is less than 90 days .
Step 16 - Identified the anomalies if the price variation % is more than 10% and gives the output.
