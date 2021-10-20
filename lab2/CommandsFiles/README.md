# CommandFiles
Is containing scirpt to process OriginalData.

Scope of this script is to clear OriginalData from any unnecessary things and modify it to make it clear and transparent.

Script modify OriginalData in following ways:
1. For every line from weather.txt file:
    - Separate line to code (`ID`, `year`, `month`, `variable name`) and rest of line.
    - Split code to `ID`, `date` and `variable name`.
    - Clear rest of line from unnecessary whitespaces and chars like: "I", "S", "O", "D", "B".
    - Split rest of line into list of `temperatures` for every day.
    - Replace NaN values with -9999 in list of temperatures.
    - Create record using data in following order: `ID`, `date`, `variable name`, `list of temperatures`.
    - Store record in record list.
2. Prepare columns names for DataFrame.
3. Create "data" DataFrame using column names and record from record list.
4. Create "tidy_data" DataFrame by melting "data" DataFrame.
5. Clean record with NaNs from "tidy_data" DataFrame.
6. Update column Date by adding day to date.
7. Create "tidy_data_2" DataFrame by pivoting "tidy_data" DataFrame.
8. Save "tidy_data_2" to TidyData.csv in AnalysedData file.

Requirements:
- pandas
- numpy

To run the script you need to open it in Jupyter Notebook and run all cells.
