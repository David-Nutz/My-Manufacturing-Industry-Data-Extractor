# The Manufacturing-Industry-Data-Extractor

An ETL pipeline designed to help users analyze and monitor economic developments across sectors of the German manufacturing industry. Two Python functions automate data extraction, cleaning, transformation, and storage, providing reliable, analysis-ready data so users can focus directly on their analysis.

## General Description

Whether a user works in the manufacturing of metalworking machinery or automotive parts and wants to quickly access reliable historical data on their own industry's turnover, sales markets, and employment trends to compare their company's performance with the industry average, or whether a company or investor is considering investments in a specific sector of the manufacturing industry and needs a data-driven basis for decision-making.

The functions are also designed for consulting companies specializing in the manufacturing industry that want to analyze both overall economic developments and the market structure of different manufacturing sectors.

For all these users, my functions provide a straightforward way to access relevant data, automate much of the data preparation process, and move directly to the analysis!

## Project Structure

README: Project description.

Industry-Codes.pdf: Contains a list of manufacturing sectors and their WZ codes. The WZ code is used by the functions to extract data regarding the selected sector.

Presentation.pptx: The presentation of my project.

Functions.ipynb: The heart and soul of this project. This notebook contains the two functions that extract data from the GENESIS database, a description of the requirements, the information users have to provide to the functions, and how they work.

## Database

The data used is extracted from two tables provided by the Federal Statistical Office of Germany. The following tables form the foundation:

Table 42111-0026 – Monthly data: Contains monthly data on employment and turnover by economic sector. The original columns include the reporting period, industry classification, statistical indicator, and value. The data covers topics such as total turnover, domestic and foreign turnover, employment, and the number of reporting units.

Table 48121-0003 – Annual data: Contains annual business statistics by economic sector and company size. The data covers the number of enterprises, turnover, persons employed, gross investment in tangible fixed assets, and gross value added.

For the functions to work, you have to enter the WZ code, not the sector name. You can find a list of the available sectors in the PDF provided in the repository. This list is based on the code list provided by GENESIS. Please keep in mind that codes may change or be deleted by the Federal Statistical Office. Always check after each function run whether the data was stored successfully.

## Technologies Used

Data Extraction & Cleaning: VS Code (Pandas)

ETL Pipeline Construction: VS Code (requests, getpass, sqlalchemy)

Data Storage: MySQL Workbench and BigQuery

Dashboard Construction: Data Studio, based on BigQuery queries.

Presentation: Google Slides
