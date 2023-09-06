# Epoch Timestamp Converter

This program is designed to identify and convert epoch timestamps in microseconds to human-readable date-time formats within CSV files. It intelligently analyzes the first 10 rows of the file to determine which columns likely contain epoch timestamps and then processes the entire file to make the conversions.

## Features

- **Automatic Detection**: The program automatically detects which columns contain epoch timestamps, eliminating the need for user input on column names.
- **Optimized for Large Files**: By initially sampling only a subset of rows, the program remains efficient even with large CSV files containing millions of rows.
- **Flexible Timestamp Range**: The program recognizes epoch timestamps ranging from 13 to 17 digits, making it adaptable to various timestamp formats.

## Usage

1. Modify the `input_path` variable in the `main` function to point to your CSV file:
   \```python
   input_path = 'path_to_input_file.csv'
   \```

2. Run the script. The converted file will be saved in the same directory as the input file with "_converted" appended to its name.

## Dependencies

- Python 3.x
- pandas

To install the required libraries, use:

```
pip install pandas
```

## Code Structure

- `epoch_to_human_readable`: Converts an epoch timestamp in microseconds to a human-readable date-time string.
- `is_likely_epoch_microseconds`: Determines if a 

