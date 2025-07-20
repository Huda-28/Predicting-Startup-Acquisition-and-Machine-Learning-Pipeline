# Predicting-Startup-Acquisition-and-Machine-Learning-Pipeline
The objective of this project is to predict the outcome of startups based on their historical data. Startups could fall into one of the following categories:

Operating: The company is still functioning and generating revenue.

IPO: The company went public through an Initial Public Offering.

Acquired: The company was acquired by a larger company.

Closed: The company shut down or went bankrupt.

This problem will be tackled using a Supervised Machine Learning approach, and interns will build an end-to-end machine learning pipeline to train and evaluate the model. Interns will also get exposure to different types of classification models, feature engineering, data preprocessing, and deployment of the final model.

# Dataset 
https://drive.google.com/file/d/14kVJ6IC-OmZP5THZ5ayl2ck8R8vllM05/view?usp=drive_link

Crunchbase Data: Crunchbase contains a wealth of information on startups, their funding rounds, acquisitions, IPOs, and much more.

You can use the Crunchbase API or download a dataset from the provided link on GitHub that has information about the company name, industry, funding, founding year, number of employees, and other metrics related to a startup's success.

# Cleaned dataset
https://drive.google.com/file/d/1sE9qyBC36GLrRm7g1h53uUMwdFa1qZy-/view?usp=sharing

🗂️ Step 1: Understand the Dataset Structure
Refer to the variable dictionary to understand the purpose of each column. Identify essential columns (e.g., name, status, funding_total_usd) and columns that are metadata or redundant (e.g., Unnamed: 0.1, logo_width, created_at).

🧹 Step 2: Drop Unnecessary Columns
Remove columns that do not contribute to the analysis or are duplicates, such as:

Extra index columns (Unnamed: 0.1)

Metadata fields (created_by, created_at, updated_at)

Irrelevant media fields (logo_url, logo_width, logo_height)

Detailed text fields that are too long or repetitive for now (overview, permalink)

⚠️ Step 3: Handle Missing Values
a. Critical Columns

Remove records where key fields like name or status are missing, as these are required for identifying and categorizing startups.

b. Descriptive and Location Fields

Fill missing descriptions (description, short_description) with a placeholder such as “Not Provided.”
Replace missing values in geographical fields (country_code, state_code, city, region) with “Unknown.”

c. Dates

Ensure all date-related fields (e.g., founded_at, first_funding_at, last_milestone_at) are correctly converted to date format. Mark any invalid or missing dates clearly.

🛠️ Step 4: Correct Data Types
Ensure all numeric fields such as funding_total_usd, investment_rounds, ROI are stored as numbers (integers or decimals).

Make sure categorical and text-based fields like status, category_code, and city are stored as text strings.

Date fields should be stored in a proper date/time format.

🧭 Step 5: Geographical Coordinates
Check the lat and lng columns (latitude and longitude) for validity. Remove or flag any invalid coordinates. If missing, leave them as null unless they can be retrieved from external sources.

💾 Step 6: Save the Cleaned Data
Once all cleaning steps are complete, save the cleaned dataset to a new file. This dataset will be used for modeling and visualization in upcoming weeks.
