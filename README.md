Groundwater Level Data API and Concatenation of Data

This repository contains scripts to fetch groundwater level data from an API (DEFRA hydrology data explorer, URL: http://environment.data.gov.uk/hydrology) process it, and combine the results into a single dataset. The data is collected from two types of borehole measurements:

Dipped Boreholes: For manually dipped measurements.

Logged Boreholes: For automatically logged measurements.

Contents

WISKI_API_Code_for_Dipped.ipynb: Script to fetch and process data from dipped boreholes.

WISKI_API_Code_for_Logged.ipynb: Script to fetch and process data from logged boreholes.

Concatenation_of_CSV_outputs.ipynb: Script to concatenate the outputs of the two previous scripts into a single dataset.

Scripts

1. WISKI_API_Code_for_Dipped.ipynb

This script retrieves historical groundwater level data for dipped boreholes from the API and saves it into individual CSV files based on their associated keywords. It also combines all data into a master CSV file.

Key Features:

Fetches data using a list of WISKI IDs and keywords.
Writes data to individual CSV files and a master CSV file.
Handles different date formats with a custom parsing function.

2. WISKI_API_Code_for_Logged.ipynb

This script performs a similar function to WISKI_API_Code_for_Dipped.ipynb but for logged boreholes. It saves data into individual CSV files and a master CSV file, combining all fetched data.

Key Features:

Fetches data for logged boreholes using predefined WISKI IDs and keywords.
Writes data to individual CSV files and a master CSV file.

3. Concatenation_of_CSV_outputs.ipynb

This script reads all CSV files created by the previous scripts, parses dates, and concatenates the data into a single DataFrame. It saves the combined data into a new CSV file called ultimate.csv.

Key Features:

Reads all CSV files in the directory.
Parses dates using multiple date formats.
Combines all data into a single CSV file.

To use:

First, run WISKI_API_Code_for_Dipped.ipynb to fetch and process dipped borehole data.
Then, run WISKI_API_Code_for_Logged.ipynb for logged borehole data.
Finally, execute Concatenation_of_CSV_outputs.ipynb to combine all CSV files into a single dataset.

File Outputs:

combined_groundwaterlevels.csv: Contains combined data from dipped and logged boreholes.
ultimate.csv: Final concatenated dataset from all CSV files.

Notes

Make sure to adjust the API endpoints and parameters (for example site names and WISKI IDs, or timeframes of required data) in the scripts according to your data needs.
You may need to handle API rate limits or authentication depending on the API's requirements (See DEFRA Hydrology Data Explorer API guidance).


Contact
For questions or feedback, please open an issue on the GitHub repository.

