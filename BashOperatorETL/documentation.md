# This project works with Bash Operators

### Basics

##### What is a script
This script is designed to process data from tollbooths (like those on highways).  It takes raw data from different sources, cleans it up, combines it, and prepares it for analysis.  Think of it as a data preparation factory.  We want to take messy, scattered data and turn it into organized, useful information.

#### What does ETL mean?
1. Extract: We take the data from different sources (like CSV files, text files, etc.). In this case, the data comes from files related to vehicle information, toll plaza details, and payment information
2. Transform: We clean and modify the data. This might involve changing the format, correcting errors, or combining data from different sources. Here, we're extracting specific information, combining them, and changing the vehicle type to uppercase.
3. Load: We load the transformed data into a usable format (like a CSV file) where it can be used for reporting, analysis, or other purposes.

### How does this script work?
The script uses a tool called Apache Airflow. Airflow helps automate and schedule complex data processes like ETL.

# Steps inside the process
1. Unzip Data: The script starts by unpacking (unzipping) the raw data files, which are initially bundled together in a compressed file. Think of it like opening a package containing all the ingredients for a recipe.

2. Extract Data: The script then extracts specific information from different data files:
From the vehicle data, it extracts the Row ID, Timestamp, Vehicle Number, and Vehicle Type. - 
From the toll plaza data, it extracts the Number of Axles, Toll Plaza ID, and Toll Plaza Code. -
From the payment data, it extracts the Payment Code and Vehicle Code. - 
It's like picking out the important ingredients from each package. -

3. Combine Data: The script combines all the extracted information into a single file. This file now contains all the relevant data about each vehicle that passed through the tollbooth, including payment details and toll plaza information.  It's like combining all the prepared ingredients into a single dish.

4. Transform Data: The script transforms the Vehicle Type to uppercase. This is a simple data-cleaning step.  It's like putting a label on the dish.

5. Save Data: Finally, the script saves the transformed data into a new file, ready for use. This is like putting the finished dish on the table.

