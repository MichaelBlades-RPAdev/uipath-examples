\# Read, Clean, and Split Excel Rows



This example demonstrates a complete, production-style Excel processing pattern in UiPath:



\- Read structured data from an input Excel file

\- Validate and clean the rows

\- Split results into \*\*valid\*\* and \*\*invalid\*\* datasets

\- Export both to separate output files for auditing and review



This workflow is intentionally simple but follows real-world RPA design conventions.



---



\## Folder Structure



```text

ReadWriteExcel/

\&nbsp; Project/                 UiPath project (Main.xaml)

\&nbsp; Data/                    Sample input and generated output

\&nbsp;   InputData.xlsx

\&nbsp;   CleanedOutputData.xlsx

\&nbsp;   ExcludedOutputData.xlsx

\&nbsp; Docs/

\&nbsp;   README.md              (this file)




