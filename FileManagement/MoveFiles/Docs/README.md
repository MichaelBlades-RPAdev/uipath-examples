Purpose

This workflow scans the Data\\Input folder, moves all .txt files to Data\\Output, and logs how many files were moved or skipped. Any file that isn't .txt stays in the input folder.



Folder Layout

Project folder and Data folder sit at the same level:



..\\Data\\Input (source files)

..\\Data\\Output (destination for .txt files)

The workflow uses these relative paths so it runs cleanly on any machine.



Variables Used



sInputFolder – holds ..\\Data\\Input

sOutputFolder – holds ..\\Data\\Output

dataFiles – array of all files found in the input folder

FilesCount – total number of files discovered

fileMoved – count of files moved to Output

fileSkipped – count of files ignored (non .txt)



Workflow Logic



Read sInputFolder and gather files into dataFiles.

Store the number of files in FilesCount.

Loop each file in dataFiles.



&nbsp;	If file extension is .txt:

&nbsp;	Build output path using sOutputFolder

&nbsp;	Move the file

&nbsp;	Increment fileMoved



&nbsp;	Else:

&nbsp;	Leave the file in Input

&nbsp;	Increment fileSkipped



At the end, log a summary showing totals.



Logging

The workflow logs:

Start and folder paths being used

Number of input files found

Each file moved or skipped

Final summary: moved vs skipped

All logs use Info level except errors during a move.



How to Run

Place a mix of .txt and other file types inside Data\\Input.

Run the main workflow from UiPath Studio.

.txt files will appear in Data\\Output; all other files remain in Data\\Input.

