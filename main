import os
import pandas as pd

def scan_folder(directory):
    file_counts = {}
    file_details = []

    for root, _, files in os.walk(directory):
        for file in files:
            file_path = os.path.join(root, file)
            file_extension = os.path.splitext(file)[-1].lower()  # Get file extension
            file_size_kb = round(os.path.getsize(file_path) / 1024, 2)  # File size in KB
            
            # Count files by type
            file_counts[file_extension] = file_counts.get(file_extension, 0) + 1
            
            # Store file details
            file_details.append([file, file_size_kb, file_extension, file_path])

    return file_counts, file_details

# Set the directory to scan
directory = "shared_drive_path_here"

# Run the scan
file_counts, file_details = scan_folder(directory)

# Convert file details to a Pandas DataFrame and save as CSV
df = pd.DataFrame(file_details, columns=["File Name", "Size (KB)", "File Type", "Full Path"])
df.to_csv("file_report.csv", index=False)
