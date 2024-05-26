#Job Scraper Script

##Overview

This script is designed to scrape job postings from LinkedIn based on user-provided job titles and save the extracted data to CSV files. Each job title results in a separate CSV file containing job details such as job title, company name, and job description.

##Prerequisites
Before running the script, ensure you have the following Python libraries installed:

-requests
-pandas
-beautifulsoup4
-lxml
You can install these dependencies using the following command:
pip install requests pandas beautifulsoup4 lxml
How to Use
Input the Number of Job Titles:
When prompted, enter the number of job titles you want to search for.

Input the Job Titles:
Enter each job title one by one. The script will ask for each title based on the number you provided.

Run the Script:
The script will process each job title, scrape job postings from LinkedIn, and save the data to separate CSV files named after the job title and the current date.

Example
If you want to search for two job titles, Data Scientist and Software Engineer, you would input:

plaintext
Copy code
Enter the number of job titles: 2
Enter job title 1: Data Scientist
Enter job title 2: Software Engineer
Output
For each job title, a CSV file will be created in the format {job_title}_{date}.csv. For example:

Data_Scientist_2024-05-26.csv
Software_Engineer_2024-05-26.csv
Each CSV file will contain the following columns:

job_title: The title of the job.
company_name: The name of the company offering the job.
description: The job description.
Code Description
Functions
individual_extract(url):

Fetches and parses a job posting webpage.
Extracts the job title, company name, and job description.
Returns the extracted data as a dictionary.
copytocsv(text, date_str):

Constructs a search URL for LinkedIn job postings.
Fetches and parses the search results page.
Calls individual_extract for each job posting link to get job details.
Saves the collected job details to a CSV file.
Main Script
Prompts the user to input the number of job titles and the job titles themselves.
Iterates over the list of job titles, calling copytocsv for each one.
Saves the job details to separate CSV files named after the job title and current date.
Notes
This script scrapes data from LinkedIn and is intended for educational purposes. Be mindful of LinkedIn's terms of service regarding scraping.
The script may need to be adapted if LinkedIn's page structure changes.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements
BeautifulSoup for HTML parsing.
Requests for making HTTP requests.
Pandas for data manipulation and CSV handling.
Feel free to contribute and improve this script!
