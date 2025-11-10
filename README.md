<p align="center">
 <img width="100%" src="./images/market-maverick-logo.png " align="center" alt="Project banner" />
 <h1 align="center">Online Retail Transaction Analysis</h1>
 <p align="center">Analysing data and producing PowerBI dashboard visualisations</p>
</p>

<p align="center">
  <br/>
  <a href="https://www.python.org/" title="Python official website">
    <img alt="Python Logo" height="30px" src="./images/python-logo.png" />
  </a>
  <a href="https://pandas.pydata.org/" title="Pandas official wesbite">
    <img alt="Pandas Logo" height="30px" src="./images/pandas-logo.png" />
  </a>
   <a href="https://matplotlib.org/stable/" title="Matplotlib offical website">
    <img alt="Matplotlib Logo" height="30px" src="./images/matplotlib-logo.png" />
  </a>
  <a href="https://seaborn.pydata.org/" title="Seaborn offical website">
    <img alt="Seaborn Logo" height="30px" src="./images/seaborn-logo.png" />
  </a>
  <a href="https://www.microsoft.com/en-us/power-platform/products/power-bi" title="PowerBI offical website">
    <img alt="PowerBI Logo" height="30px" src="./images/powerbi-logo.png" />
  </a>
  <a href="https://www.kaggle.com/" title="Kaggle offical website">
    <img alt="Kaggle Logo" height="30px" src="./images/kaggle-logo.png" />
  </a>
  <br />
</p>

<p align="center">
  <a href="https://github.com/users/BethW83/projects/3">Project Board</a>
  &nbsp;&nbsp;-&nbsp;&nbsp;
  <a href="./jupyter_notebooks/data_clean_EDA.ipynb">Data Cleanup & EDA</a>
  &nbsp;&nbsp;-&nbsp;&nbsp;
  <a href="#conclusions">Conclusions</a>
  <br/><br/><br/>
</p>

<details>
<summary>Table of contents (Click to show)</summary>

- [Dataset Content](#dataset-content)
- [Business Requirements](#business-requirements)
- [Hypothesis](#hypothesis)
- [Project Plan](#project-plan)
- [The rationale to map the business requirements to the Data Visualisations](#the-rationale-to-map-the-business-requirements-to-the-data-visualisations)
- [Analysis techniques used](#analysis-techniques-used)
- [Ethical considerations](#ethical-considerations)
- [Unfixed Bugs](#unfixed-bugs)
- [Development Roadmap](#development-roadmap)
- [Conclusions](#conclusions)
- [Main Data Analysis Libraries](#main-data-analysis-libraries)
- [Credits](#credits)
  - [Content](#content)
  - [Media](#media)
- [Acknowledgements](#acknowledgements)

</details>

<p>

</p>

<details>
<summary>How to use this repo (Click to show)</summary>

**Make sure you have:**

- Python installed, this project used V3.12,
- VS Code latest

**Inside VS Code:**

Open Extensions (Ctrl+Shift+X or ⇧⌘X on macOS)
Install these extensions if you don't have them:

- Python extension (by Microsoft in the Extensions Marketplace)
- Jupyter extension (also by Microsoft)

**From the terminal:**

Open the folder in a terminal where you want the project to be saved

#### Run git clone:

```
git clone https://github.com/BethW83/Group-Project-1-Retail.git
```

#### Navigate in to the new folder:

```
cd Group-Project-1-Retail
```

#### Setup a virtual enviroment:

Create a virtual enviroment for the project.

Linux / Mac:

```
python3 -m venv .venv
source .venv/bin/activate
```

Windows CMD:

```
python3 -m venv .venv
.venv\Scripts\activate
```

Windows PowerShell:

```
python3 -m venv .venv
.\.venv\Scripts\Activate.ps1
```

#### Install the dependancies:

This will install all the dependancies needed for the project in to the virtual enviroment if it is setup, rather than globally

```
pip install -r requirements.txt
```

#### Select the Kernel

There is a drop down at the top of the notebooks to select your kernal that will run the Python.
If you setup a virtual enviroment then make sure you pick the venv one.

---

</details>

<p>
<br/>
</p>

**Online Retail Transaction Analysis** is a comprehensive data analysis tool to provide insights through interactive dashboards: to analyse customer behaviour, optimise pricing and marketing strategies and identify popular products.

Team Members:
- Beth Williams
- Pete Smith
- Tom Burgess


# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

## Dataset Content

The dataset contains information on customer transactions made through an online retail platform. It includes the following columns:

- `InvoiceNo:` - Transaction number
- `StockCode:` - Product number
- `Description:` - Product name
- `Quantity:` - Quantity sold (negative for cancelled orders)
- `InvoiceDate:` - Date and time of transaction
- `UnitPrice:` - Price of one unit of the item
- `CustomerID:` - Unique customer identifier
- `Country:` - Customer location

## Business Requirements

- TODO: Describe your business requirements

## Hypothesis

- TODO: General Sales trends/Descriptive Stats: Tom
- Majority of the orders are made at lunch time
- Majority of the orders are made by UK customers
- Customers make return and make multiple orders
- TODO: Products: Beth: The top 10 products provide the most revenue


## Project Plan

- TODO
-   Mention that Saturdays are missing. Perhaps the company providing the online transactions did not want to provide the Saturday data as this is their busiest day and competitors would be most interested in this?

-   Second December, data goes up until 08/12/2011. Add date slicers in Power BI rather than deleting data. 

-   Outline the high-level steps taken for the analysis.
-   How was the data managed throughout the collection, processing, analysis and interpretation steps?
-   Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations

-   List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used

1. Methods Used:

   - Descriptive statistics (`.describe()`, `.info()` etc.)

   - Segmentation (used bins for day parts)

   - Visual analytics (`Matplotlib`, `Seaborn`, `Power BI`)

2. Limitations & Alternatives:

   - Limited data points availble in the csv, especially with the product data, it only had product code and description which limited how we could report on products.
   - There was no data for Saturdays.
   - There was no cost price so we couldn't report on margins etc.

3. Structure Justification:

   - Data cleanup and transform notebook as the first part.
   - Created a shared published Source Data in star diagram format.
   - Created a Power BI dashboard visualisation file for each team member, pulling from the single shared source data.

4. Use of Generative AI:

   - AI supported: GitHub copilot extention was installed and so did speed up some repetative tasks.


## Ethical considerations

-   The Customer ID was anonymised. 
-   The data is available publicly on Kaggle and (Tom insert link here)

-   Were there any data privacy, bias or fairness issues with the data?
-   How did you overcome any legal or societal issues?

## Dashboard Design

After the data cleanup, we exported five CSV files via Python to be imported in to Power BI which are setup as a star data structure:

<p align="center">
<img src="./images/spider_diagram.png" alt="Spider diagram of data structure" width="50%" />
</p>

In the `/visualisations` folder we created four Power BI Desktop files:

- `SharedDataset.pbix` - This is the file that imports the CSV files. As all team members folder location is different on their local development, we import the CSV files from this GitHub repository raw links using the Web import rather than the File import. This allows all team members to open and edit the file without modifying each time. All extra columns and measures were added to this file, then the data published to our shared Power BI workspace. The other three files then directly connect to this published dataset, so there is a single source of truth for the data that we all shared. We could then individually work on the following dashboard files separetly without conflicts, while still publishing the dashboards to the same shared workspace.
- `1-Descriptive-Statistics-and-Trend-Analysis.pbix` - This is the visualisations for the sales and descriptive statistics dashboard.
- `2-Customer-Segmentation-and-Purchase-Behaviour.pbix` - This is the visualisations for the cusotmer behaviour dashboard.
- `3-Product-Analysis.pbix` - This is the visualisations for the product dashboard.


**DAX Measures and Columns**

We added a number of different measures to the SharedDataset Power BI file that we used in different visualisations:

- Average Order Value - total sales divided by the number of orders:
```
Average Order Value = 
DIVIDE([Total Sales], DISTINCTCOUNT(FactSales[InvoiceNo]))
```
- Avg Days Between Purchases - Average of the days between purchases measure
```
Avg Days Between Purchases = 
AVERAGE(FactSales[Days Between Purchases])
```
- Avg Sales per Hour per Transaction - Sales per hour measure divided by the number of orders
```
Avg Sales per Hour per Transaction = 
DIVIDE(
    [Sales per Hour],
    DISTINCTCOUNT(FactSales[InvoiceNo])
)
```
- Days Between Purchases - column added that is the number of days between the invoice date and the previous purchase date:
```
Days Between Purchases = 
DATEDIFF([Previous Purchase Date], FactSales[InvoiceDate_date], DAY)
```
- Days Since Last Purchase - number of days since last purchase, counted up until the end of the data set (as the data is over a decade old, not capping at the end of the data set resulted in very large numbers for all records):
```
Days Since Last Purchase = 
VAR LastPurchaseDate =
    CALCULATE(
        MAX(FactSales[InvoiceDate_date]),
        ALLEXCEPT(FactSales, DimCustomer[anon_customer])
    )

VAR DataEndDate =
    CALCULATE(
        MAX(FactSales[InvoiceDate_date]),
        ALL(FactSales)
    )

RETURN
DATEDIFF(LastPurchaseDate, DataEndDate, DAY)
```
- Frequency per Customer - The number of orders for a cusomter:
```
Frequency Per Customer = 
CALCULATE(
    DISTINCTCOUNT(FactSales[InvoiceNo]),
    ALLEXCEPT(DimCustomer, DimCustomer[anon_customer])
)
```
- Previous Purchase Date - get the most recent order date before this order:
```
Previous Purchase Date = 
VAR CurrentCustomer = FactSales[anon_customer]
VAR CurrentDate = FactSales[InvoiceDate_date]
RETURN
CALCULATE(
    MAX(FactSales[InvoiceDate_date]),
    FILTER(
        FactSales,
        FactSales[anon_customer] = CurrentCustomer &&
        FactSales[InvoiceDate_date] < CurrentDate
    )
)
```
- Quantity per Hour - as all day part bins vary in size, we divide by the bin size to give a per hour value so they can be compared:
```
Quantity per Hour = 
DIVIDE(
    SUM(FactSales[Quantity]),
    MAX(DimDayPart[HoursInBin])
)
```
- Sales per Hour - Same as above but for the sales per hour:
```
Sales per Hour = 
DIVIDE(
    SUM(FactSales[TotalTransacrtionValue]),
    MAX(DimDayPart[HoursInBin])
)
```
- Spend per Customer - total cost per customer:
```
Spend per customer = 
CALCULATE(
    SUM(FactSales[TotalTransacrtionValue]),
    ALLEXCEPT(DimCustomer, DimCustomer[anon_customer])
)
```
- Total Cusotmers - number of distinct cusotmers:
```
Total Customers = 
DISTINCTCOUNT(FactSales[anon_customer])
```
- Total Quantity - Sum of the quanitity value:
```
Total Quantity = 
SUM(FactSales[Quantity])
```
- Total Sales - Sum of the total transaction value:
```
Total Sales = 
SUM(FactSales[TotalTransacrtionValue])
```

Once imported, it looked like:
![Power BI Relashionship Diagram](./images/power-bi-relashionship-diagram.png)

### **1 Descriptive Statistics and Trend Analysis**

TODO: Add here!

### **2 Customer Segmentation and Purchase Behaviour**

- [Interactive dashboard link](https://app.powerbi.com/links/sx0ue_oPtW?ctid=c233c072-135b-431d-af59-35e05babf941&pbi_source=linkShare) - This links only available to Code Institute users, and isn't publically shareable.

- [Link to a PDF of the dashboard](./visualisations/pdfs/2-Customer-Segmentation-and-Purchase-Behaviour.pdf)

- <a href="https://screen.studio/share/1OGghJFI" target="_blank" rel="noopener noreferrer">Dashboard Walkthrough Video</a>

**When are customers purchasing page:**

![When are customers purchasing page](./images/2-Customer-Segmentation-and-Purchase-Behaviour-when-are-customers-purchasing.png)

**Customer orders page:**

![Customer orders page](./images/2-Customer-Segmentation-and-Purchase-Behaviour-customer-orders.png)

**Where are customers based page:**

![Where are customers based page](./images/2-Customer-Segmentation-and-Purchase-Behaviour-customer-locations.png)


### **3 Product Analysis**

TODO: Add here!

## Conclusions

-
-

## Unfixed Bugs

-   Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.


## Development Roadmap

- Power BI stores absolute file paths when importing CSV files which makes it challenging when we all have different enviorments and both PC and MAC. We overcame this by making a single source dataset, connected it via the Web import instead of the File import, using the GitHub raw file links for the CSV files, and then made a single source data Power BI file, published the datset, and then conected oue own copies of a Power BI desktop file to the remote dataset. This enabled all team memebers to work on dashboards separetly but still publish them to the same shared workspace.
- The main map visualisation options in Power BI were not enabled for our organisation, so we used the Azure map visualisation option instead for mapping.
- Initially the order of the day parts in the visualisations were not in the correct order, showing lunch, then evening and then morning. We over came this by ading an extra sort column to the day part table and sorting the daypart field by this new order column.
- We had a few issues with Git getting out of sync and not allowing a team member to switch branch or merge from main. We overcame this as a team, sharing screens and helping each other through the process.

-   (if we need something else here, include updating the requirements.txt file?)
-   What challenges did you face, and what strategies were used to overcome these challenges?
-   What new skills or tools do you plan to learn next based on your project experience?
-   Did you recognise gaps in your knowledge, and how did you address them?
-   If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Main Data Analysis Libraries

- `Pandas` - For cleaning the data and EDA.
- `Seaborn` - For visualising the data in the Jupyter Notebook.
- `Matplotlib` - For formatting the Seaborn charts and adding titles and labels.
- `Power BI` - For creating the interactive dashobards.

## Credits

-   Code Institute https://learn.codeinstitute.net/
-   GitHub https://github.com/Code-Institute-Org/data-analytics-template and https://github.com/5pence/sept-2025-da and https://github.com/mbriscoe/MatplotlibDemo
-   Copilot in VSCode to help with generating code and formatting
-   Chatgpt for general coding queries and fixing some errors
-   Kaggle data https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset/data


### Content

-   The text for the Home page was taken from Wikipedia Article A
-   Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
-   The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

-   The photos used on the home and sign-up page are from This Open-Source site
-   The images used for the gallery page were taken from this other open-source site

## Acknowledgements

-   Thank you to our tutor Emma Lamont and data coaches Spencer Bariball and Mark Briscoe for their ongoing help and support. Thank you also to our fellow bootcampers for their ongoing help and support.
