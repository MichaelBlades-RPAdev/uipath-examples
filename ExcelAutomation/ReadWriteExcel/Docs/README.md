\# Read, Clean, and Split Excel Rows



This example demonstrates a complete Excel data-processing pattern in UiPath:



\- Read raw data from an input Excel file  

\- Clean the data by removing incomplete rows  

\- Split the data into two outputs  

&nbsp; - \*\*OutputData.xlsx\*\* → valid rows  

&nbsp; - \*\*ExcludedOutput.xlsx\*\* → rejected/incomplete rows  



This is a common structure used in Accounts Payable, data validation, and ETL-style workflows.



---



\## Folder structure



```text

ExcelAutomation/

&nbsp; ReadWriteExcel/

&nbsp;   Project/          

&nbsp;   Data/             

&nbsp;     InputData.xlsx

&nbsp;     CleanedOutputData.xlsx

&nbsp;     ExcludedOutputData.xlsx

&nbsp;   Docs/

&nbsp;     README.md

