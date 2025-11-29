# Maldivian Nakaiy Calander Dataset
Dataset on the ancient Maldivian Nakaiy calendar system, extracted from Hassan Ahmed Maniku's 1989 book.

## Description
This dataset contains information on the ancient Maldivian Nakaiy system, a traditional calendar based on lunar mansions (asterisms) used for determining seasons, auspicious times, fishing, and agriculture. It divides the year into two monsoons: Hulhangu (South-West, 18 Nakaiy) and Iruvai (North-East, 9 Nakaiy). Each Nakaiy includes details like start/end dates, names/meanings in multiple languages (Divehi, Arabic, Sinhala), presiding divinities/regents, wind directions, speeds, rainfall, and sunshine hours.

The data was extracted and compiled from the book "NAKAIY" by Hassan Ahmed Maniku. This system has roots in ancient Indian (Indus Valley) and Sinhala traditions, as discussed in the book.

## Data Source and Credits
- **Original Source:** "NAKAIY" by Hassan Ahmed Maniku, published by the Department of Information and Broadcasting, Republic of Maldives, March 19, 1989 (Vanavaru No. 2). ISBN: 99915-78-01-X.
- **Extraction:** Data transcribed from the book's tables and text by [Ajmal Shaheed/ajmals]. All credit for the content goes to the author. This dataset is shared for educational and research purposes under fair use.



## Dataset Structure
The main file is `maldivian_nakaiy_calendar.tsv` with the following columns:

- **Nakaiy**: Name of the lunar mansion (e.g., Assidha).
- **Season**: Hulhangu or Iruvai.
- **Season sequence no**
- **Start Date**: Approximate Gregorian start date (e.g., 8 April).
- **End Date**: Approximate Gregorian end date (e.g., 21 April).
- **Hindu Lunar Mansion (Name & Meaning)**: e.g., Asvini ("the two horsemen").
- **Arab Lunar Mansion (Name & Meaning)**: e.g., Ash-Sharatan ("the two tokens").
- **Sinhala Name**: e.g., Asvidha.
- **Presiding Divinity/Regent**: e.g., Acvins.
- **Wind Direction**: e.g., West.
- **Wind Speed (km/hr)**: e.g., 12.96.
- **Rainfall (m)**: e.g., 46.6.
- **Sunshine (hrs)**: e.g., 1116.
- **Figure/Symbol**
- **Asterism/Constellation**
- **Notes (Activities, Sayings, Status)**



Sample rows:

| Nakaiy   | Season   | Start Date | End Date | Hindu Lunar Mansion (Name & Meaning) | Arab Lunar Mansion (Name & Meaning) | Sinhala Name | Presiding Divinity/Regent | Wind Direction       | Wind Speed (km/hr) | Rainfall (m) | Sunshine (hrs) |
|----------|----------|------------|----------|--------------------------------------|-------------------------------------|--------------|---------------------------|----------------------|--------------------|--------------|----------------|
| Assidha | Hulhangu | 8 April   | 21 April | Asvini ("the two horsemen")         | Ash-Sharatan ("the two tokens")    | Asvidha     | Acvins                   | West                | 12.96             | 46.6        | 1116          |
| Burunu  | Hulhangu | 22 April  | 5 May    | Bharani ("bearer away")             | Al-Butain ("little belly")         | Berana      | Yama                     | Not settled, generally West | 18.52             | 66.9        | 115           |
| ...     | ...      | ...       | ...      | ...                                 | ...                                | ...         | ...                      | ...                 | ...               | ...         | ...           |

- **Rows:** 27 (one per Nakaiy, covering the full year).
- **Notes:** Dates are approximate and based on historical observations; they may vary by year due to lunar cycles. Wind/rain/sun data appears to be averaged or observed values from the book.

## Usage
- **Load in Python (Pandas):**
  ```python
  import pandas as pd
  df = pd.read_csv('maldivian_nakaiy_calendar.tsv')
  print(df.head())

- **Load in R (readr)**
  ```R
  library(readr)
  df <- read_csv("maldivian_nakaiy_calendar.tsv")
  head(df)
