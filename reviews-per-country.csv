# Code KY Wine Sales Activity
import pandas as pd

# Define the file path
file_path = 'data/winemag-data-130k-v2.csv.zip'

# Read the dataset
df = pd.read_csv(file_path, compression='zip')

# Create a summary of the data for each unique country
summary = df.groupby('country').agg({
    'points': ['count', 'mean']
}).reset_index()

# Rename columns for clarity
summary.columns = ['Country', 'Number of Reviews', 'Average Points']

# Display the summary
print("Summary:")
print(summary)

# Write the summary data to a new file
output_file_path = 'data/reviews-per-country.csv'
summary.to_csv(output_file_path, index=False)

print(f"\nSummary data written to: {output_file_path}")