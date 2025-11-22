Purpose
This workflow reads an Excel file from the Data folder, removes incomplete rows, and writes two output files: one containing valid rows and one containing excluded rows. It uses a simple “clean vs exclude” split to demonstrate how to filter and manage DataTables in UiPath.

Folder Layout
The Project and Data folders sit at the same level:

..\Data\InputData.xlsx – source data
..\Data\CleanedOutputData.xlsx – cleaned rows
..\Data\ExcludedOutputData.xlsx – removed or incomplete rows

Using relative paths keeps the example portable and GitHub-friendly.

Variables Used
These variable names may differ slightly depending on your workflow, but the typical set includes:

dtbInput – DataTable holding the raw Excel data
dtbCleaned – DataTable holding valid rows
dtbExcluded – DataTable holding invalid or incomplete rows


Workflow Logic

Read InputData.xlsx into dtbInput using Workbook activities.
Filter out rows where required fields (for example “Name” and “Amount”) are empty. These become dtbExcluded.
Keep rows with valid data. These become dtbCleaned.
Write dtbCleaned to OutputData.xlsx.
Write dtbExcluded to ExcludedOutput.xlsx.
Log the number of input, cleaned, and excluded rows.

What Counts as “Valid Data”
A row is considered valid if the required columns are not empty. In this example:

Name must not be empty
Amount must not be empty

Any row missing one or both fields is excluded and written separately.

Logging
The workflow logs:
When processing begins
How many rows were read
How many rows were kept
How many rows were excluded
Confirmation that both output files were created
All logs use Info level to keep output clean and consistent.

How to Run
Place your input file in the Data folder as InputData.xlsx.
Run the main workflow from UiPath Studio.
After execution:

CleanedOutputData.xlsx contains rows with complete data
ExcludedOutputData.xlsx contains incomplete rows you may want to review or fix