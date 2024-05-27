You're part of cybersecurity team and you have been asked to produce dashboard to indetify fraudulent activities.

**About the dataset**  
Data was collected and structured by the Fraud team. This dataset consists of payments from various customers made in different periods and amounts. The feature columns include:

- **Step:** This feature represents the month from the start of the simulation. The steps represent four months that the simulation ran virtually.
    - 0: May
    - 1: June
    - 2: July
    - 3: August
- **Customer:** Customer ID
- **Age:** Categorised age
    - 0.0: <= 18
    - 1.0: 19 - 25
    - 2.0: 26 - 35
    - 3.0: 36 - 45
    - 4.0: 46 - 55
    - 5.0: 56 - 65
- **Gender:** Gender of the customer
    - F: Female
    - M: Male
- **PostcodeOrigin:** The postcode of origin/source.
- **Merchant:** The merchant's ID. 
- **Category:** Category of the purchase. 
- **Amount:** Amount of the purchase.
- **Fraud:** Target variable that shows if the transaction is fraudulent - 1 or non-fraudulent - 0.

First task:
1. Download the 60-day free trial of Splunk Enterprise. (The link is provided in the Resources section below.)
2. Install Splunk Enterprise on your computer.
3. Using the **“prepared_data”** file in the Resources section, import this file into Splunk. 
4. Study the file using the “Interesting Fields” section in Splunk. This tells you about the data you’re using.
5. Create a dashboard to include the following charts/tables:
    1. *Count by Category, Fraudulent transactions, Age and Merchant.*
    2. *Fraud detected by Age, Category, Step (month) and Gender.*
    3. *Which gender performed the most fraudulent activities and in what category?*
    4. *Which age group performed the most fraudulent activities and to what merchant?*
6. Export the dashboard as a PDF and upload it below as your submission for this task.


examples:
To get “Fraud detected by category”, type
```
sourcetype="practicesplunk.csv" fraud="1" | stats count values(fraud) by category
```
 To get “Gender with the most fraudulent activity by category”, type
```
sourcetype="practicesplunk.csv" fraud="1" gender="F'" | stats count values(fraud) by category
```

First problem:
Data set given is in xlsx which is excel format and the one needed is csv to process data through splunk. There is massive feature difference and splunk will struggle to process file type csv.


Steps I have taken:
1. On splunk home page  I went to add data
2. I uploaded converted from `XLSX` to `CSV` format file which consisted of fraudulent activates in data spreadsheet. ( this helped splunk upload data without artifacts)
3. Change timestamps from auto to current and select source type to csv
4. Saved the file to fraud_dectection1.csv
5. Click on start searching
6. Created first dashboard by most in category with this command `sourcetype="fraud_detection.csv" | top category`
7. 



