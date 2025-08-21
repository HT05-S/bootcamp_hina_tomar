HOMEWORK 5- DATA STORAGE

OVERVIEW-

In this project, we are organizing and storing data in a clear and consistent way. The main idea is to keep raw data (original files) separate from processed data (clean or transformed files).

FOLDER STRUCTURE-

i. data/raw/ → This folder stores all raw data files exactly as they are pulled or created.
ii. data/processed/ → This folder stores processed data in  Parquet format for faster reading and analysis.

Both folders are automatically created by the code if they do not exist.

FILE FORMATS USED-

a. CSV (.csv):

i. Used for saving raw data.
ii. Easy to read and supported everywhere.

b. Parquet (.parquet):

i. Used for processed data.
ii. Compressed and optimized for large datasets.
iii. Faster to load in Python compared to CSV.

READING AND WRITING DATA-

a. The project uses environment variables (DATA_DIR_RAW, DATA_DIR_PROCESSED) to set the paths for raw and processed folders.
b. If these environment variables are not defined, the default paths data/raw/ and data/processed/ are used.
c. The utility functions:
        * write_df(df, path) → Saves a DataFrame to either CSV or Parquet based on file extension.
        * read_df(path) → Loads a DataFrame from CSV or Parquet.
d. The functions also ensure that folders are created before saving files.
