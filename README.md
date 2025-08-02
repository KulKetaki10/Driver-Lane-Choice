Workflow for Automated Lane Choice Identification

1. Requirement Analysis:
•	Reviewed the assignment objectives to confirm the goal: automate identification of lane choices (Inside or Outside) for each driver at the choose cone during restarts.
•	Confirmed the requirement to analyze the top 16 drivers for every restart, capturing both running order and lane selection.
•	Assessed the completeness of the provided Excel data and identified that, if any critical information was missing or unclear, was verified using the SMT portal, which serves as the official source for NASCAR timing and scoring data.
2. Data Review and Cleaning:
•	Examined the provided Excel files and relevant worksheets for necessary data fields, such as lap numbers, driver running order, car numbers, and choose distances.
•	Verified the accuracy and completeness of this data by cross-referencing with SMT outputs when there were discrepancies or missing information.
•	Standardized column headers, resolved inconsistencies, and removed invalid rows.
•	Ensured all numerical data types were correct and constructed a clean DataFrame for analysis.
3. Identifying Restarts and Mapping Data:
•	Determined the restart laps by analyzing caution periods in the data.
•	Used the lap immediately prior to each restart to extract the running order, ensuring the top 16 drivers were selected for lane choice analysis.
•	If there was any uncertainty or missing information regarding restart timing or order, reference SMT data for validation and accuracy.
4. Lane Choice Logic Implementation:
•	Applied the lane choice criteria using the “Choose Distance (ft)” data: classifying drivers as “Outside” if their distance from the outside wall was 0–14 feet, and as “Inside” if it was 14 feet or more.

 
Statistic	Value
Min	3.8
25%	6.5
Median	7.6
75%	14.0
Max	432.7
Mean	15.9
Observations from the histogram and stats:
Most values are under 20 ft — in fact, 75% are under 14 ft.
Thant is why I chose 14 as the threshold value

•	Incorporated exception handling for missing or ambiguous values.
5. Automated Excel Sheet Population:
•	Developed code to automatically populate the "Pocono Choose Results" Excel sheet with the processed lane choice data for each restart.
•	Ensured the results were written in the required format, with clear separation for each restart and correct placement of driver names, running order, and lane choices as specified by the template.
•	This was achieved using Python.
6. Streamlit Application Development:
•	Built a Streamlit web app to streamline the process and provide an interactive interface for users.
•	Provided options for adjusting thresholds, exploring interactive charts, and exporting processed results.







