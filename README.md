uipath-examples



This repository contains a set of small, focused UiPath workflows that demonstrate core automation patterns. Each example is self-contained, uses clean folder structure, and includes a short README describing the purpose of the workflow and how it runs.



The goal is to show clear, practical UiPath capability — not large production robots — but compact examples that reflect real automation work.



Repository Structure

uipath-examples/

&nbsp; ExcelAutomation/

&nbsp; FileManagement/

&nbsp; EmailProcessing/        (planned)

&nbsp; JSONProcessing/         (planned)

&nbsp; APIAutomation/          (planned)

&nbsp; QueueWorkflows/         (planned)

&nbsp; PDFandOCR/              (planned)

&nbsp; LoggingAndErrorHandling/ (planned)





Each category contains one or more example projects in this structure:



ExampleName/

&nbsp; Project/      UiPath project files

&nbsp; Data/         Input data (if required)

&nbsp; Docs/         README and notes



Current Examples

ExcelAutomation / ReadWriteExcel

Reads an input spreadsheet, filters rows based on simple rules, and writes two output files:

a cleaned version containing all valid rows

an excluded file containing rows that did not meet the criteria

Uses basic workbook activities with clear logging.



FileManagement / MoveFiles

Scans a folder, identifies .txt files, and moves them to an output folder.

Logs each operation, counts processed files, and demonstrates a simple file-handling pattern.

Style and Conventions

Clean, modern activity usage

Consistent variable naming (e.g., dtInput, sInputFolder, iFileCount)

Logging added to each significant step

Minimal dependencies and no external orchestrator setup

Designed to run locally for demonstration purposes



Planned Additions

Future examples will cover:

Reading and processing email (IMAP/POP3)

Working with JSON data

Calling REST APIs

Queue item patterns

PDF extraction and OCR

Centralized logging and error-handling patterns

Each will follow the same structure and documentation style.



Purpose



This repo is meant to give a clear picture of UiPath fundamentals:

data extraction, file handling, simple transformations, logging, and basic workflow design.

It is intentionally small, readable, and easy to expand.

