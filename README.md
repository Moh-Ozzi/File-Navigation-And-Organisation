📂 File Inventory Generator

This script recursively scans a folder and its subdirectories to generate a detailed inventory of all files it contains.

It is designed for scenarios involving large, nested file systems, such as shared drives with thousands of mixed file types (e.g., .las, .segy, .shp, .csv, .pdf, .png, etc.).

🔍 Features

Counts files grouped by extension/type

Lists each file's:

Name

Size (in KB)

Extension

Full path

Outputs results as a clean, structured CSV report

🛠️ Use Case

Originally developed to analyze and organize a large collection of oil and gas data files stored in a shared drive. Useful for any scenario requiring an automated scan and summary of unstructured file systems.

🐍 Requirements
Python 3.6+

pandas

Install dependencies (if needed):
```pip install pandas```

▶️ Usage
Replace the directory variable in the script with the path to the folder you want to scan:
```directory = "your_folder_path_here"```

This will generate a file_report.csv file containing all the details.

