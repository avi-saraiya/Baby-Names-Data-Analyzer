# Baby Names Data Analyzer
The bn script is a Bash program that allows users to find the rank of a baby name for a given year and gender based on U.S. Social Security Administration data. 
It supports the years between 1880 and 2022 and works with three genders: Female (F), Male (M), and Both (B).
## Features

- Validates the input format for the year, gender, and name.
- Finds the rank of a name among male and female baby names.
- Provides helpful error messages when inputs are invalid.
- Supports searching for names across both genders.

## Requirements

- Bash (Unix/Linux environment).
- Data files in the format yobYYYY.txt (where YYYY is the year, e.g., yob2022.txt), which can be downloaded from the U.S. Social Security Administration website.

## Installation
1. Clone this repository to your local machine<br>

2. Make sure the yobYYYY.txt files (for the years you're interested in) are in the same directory as the script or adjust the script to point to the correct location of the files.<br>

3. Make the script executable<br>

## Usage

![image](https://github.com/user-attachments/assets/d527785d-d354-4fc1-a612-417bf4c063ac)

## Arguments
* <b>YEAR:</b> A four-digit year between 1880 and 2022 (inclusive).
* <b>GENDER:</b> The gender for which you want the rankings:
* <b>F</b> for female
* <b>M</b> for male
* <b>B</b> for both genders
* <b>NAMES:</b> A list of names separated by whitespace. The script will print the ranking of each name among the given gender in the specified year.

## Error Handling
* <b>Invalid Year Format:</b> The year must be a four-digit number.
* <b>Invalid Gender Argument:</b> The gender must be one of M, F, or B.
* <b>Name Formatting:</b> Names must only contain alphabetic characters (A-Z, a-z).
* <b>Missing Year Data:</b> If data for the specified year doesn't exist, the script will notify you

## How It Works
1. The script first validates the year and gender inputs.
2. It checks if the year data file exists (e.g., yob2022.txt).
3. It checks the validity of each name entered by the user.
4. It retrieves the rankings from the corresponding year file and gender-specific data.
5. It prints out the rank of each name along with the total count of names for that gender.

## Script Structure
### Functions
* <b>valid_year_format:</b> Validates that the input year is a valid four-digit number.
* <b>valid_gender:</b> Validates that the gender is one of "F", "M", or "B".
* <b>convert_gender_case:</b> Converts gender to uppercase if provided in lowercase.
* <b>year_file_exists:</b> Checks if the "yob" file exists for the provided year.
* <b>valid_name:</b> Validates that the name contains only alphabetic characters.
* <b>total_gender_names_f:</b> Finds the total number of female names in the year file.
* <b>total_gender_names_m:</b> Finds the total number of male names in the year file.
* <b>rank_f:</b> Retrieves the rank of a female name.
* <b>rank_m:</b> Retrieves the rank of a male name.

## License
This script is open source. You are free to use, modify, and distribute it under the MIT License.
