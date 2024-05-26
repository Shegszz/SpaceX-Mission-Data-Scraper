# SpaceX Mission Data Scraping and Analysis

## Objective
The goal of this project was to scrape mission data from the SpaceX website, specifically focusing on launch dates, mission names, and detailed mission headlines. The extracted data was then cleaned and organized into a structured format suitable for analysis.

## Workflow

### 1. Web Scraping SpaceX Launch Data
- *HTML Content Fetching*: Utilized the requests library to fetch the HTML content of the SpaceX launches page.
- *Data Parsing*: Employed BeautifulSoup to parse the HTML and extract relevant mission information, such as launch dates, mission names, and article links.
### 2. Extracting Mission Headlines
- *Detailed Mission Access*: For each mission, accessed the detailed mission page using the extracted link.
- *Headline Extraction*: Parsed the detailed mission page to find the first two <p> elements within a specific div, collecting the text content to form the mission headline.

### 3. Cleaning the Extracted Headlines
- *DataFrame Conversion*: Converted the extracted data into a pandas DataFrame.
- *String Cleaning*: Applied string cleaning operations to remove unwanted characters from the mission headlines, ensuring the text was clean and readable.

### 4. Saving and Displaying the Data
- *CSV Export*: Saved the cleaned data into a CSV file for future use.
- *Data Verification*: Displayed the DataFrame to verify the cleaning process.

## Challenges Faced

### HTML Structure Variability
Different pages had slight variations in their HTML structure, making it difficult to find the first two <p> elements within a specific div common to all the launch links extracted. Also, collecting the text content to form the mission headline proved tasking, a counter was initiated with the help of Chat-GPT to get the needed contents.

### Data Cleaning
Extracted data often contained unwanted characters due to the JSON-like structure from which it was parsed. Cleaning these characters required careful string manipulation to ensure no useful data was lost.

### Efficiency
Iterating over multiple pages and fetching content from each link required optimizations to ensure the process was both fast and reliable. The extraction of the mission headlines took 7minutes to run.
SpaceX limited the number of mission data extracted to only 136 missions(August 29, 2019 - November 26, 2022) out of over 300 mission launches(August 29, 2019 - present) on the website.

## Skills Demonstrated
This project demonstrates proficiency in web scraping, data extraction, and cleaning using Python, showcasing skills that are valuable for data-driven roles. The organized workflow and comprehensive comments make the code easy to understand and maintain.
