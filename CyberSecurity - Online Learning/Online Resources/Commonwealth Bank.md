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

Task 1
Steps I have taken:
1. On splunk home page  I went to add data
2. I uploaded converted from `XLSX` to `CSV` format file which consisted of fraudulent activates in data spreadsheet. ( this helped splunk upload data without artifacts)
3. Change timestamps from auto to current and select source type to csv
4. Saved the file to fraud_dectection1.csv
5. Click on start searching

command used  to find task 1 to count:
```
sourcetype="fraud_dectection1.csv" | top age
```

command used to find task 2 to count by category:
```
sourcetype="fraud_detection1.csv" fraud="1"  | stats count values(fraud) by category```
```

command used to find task 3 to count by category using two fields:
```
sourcetype="fraud_dectection1.csv" fraud="1" gender="M'"  | stats count values(fraud) by category
```
command used to find task 4 :
```
sourcetype="fraud_detection1.csv" fraud="1" | stats count by age merchant | sort - count | head 1
```

```

sourcetype="fraud_detection1.csv" fraud="1"
| stats count by age merchant
| sort - merchant count
| streamstats count as row_number by merchant
| where row_number <= 5
| chart count over merchant by age
```

![[how to create charts.png]]


Summary:
- I learnt a little bit about Splunk
- Learn commands to create graphs
- Imported data to Splunk
- Created different graphs to produce well detailed dashboard
- Exported dashboard to report
In short: I analysed data and created Splunk dashboard with all the information. 

# Task 2
*Identify the type of cyber attack that occurred based on the incident details.*
*Outline the next steps to be taken as a cyber security analyst, including containment, resolution, and recovery measures.*
*Provide a list of actions to contain, resolve, and recover from the incident.*
*Describe post-incident activities and measures to prevent similar incidents in the future.*\

## Scenario

As a member of the cyber security division, your team must handle this incident and the team lead has assigned the issue to you. Below is the timeline of events:

- 10:30 a.m. – The IT Service Desk receives a report from one of your colleagues at the bank that they have received an email from HR telling all employees to update their timesheets in the company’s support portal so the timesheets can be approved on time by their line managers against the next pay day. The colleague clicked the link in the email that opened what looked like the portal. However, following the employee's input of the user credentials, an unfamiliar error page appeared like the one below.

![](https://cdn.theforage.com/vinternships/companyassets/2sNmYuurxgpFYawco/y2NzZJASdgERdYR4S/1674571919466/Google%20error.png)

- 2:00 p.m. – Eight more reports of emails similar to the one reported earlier are received by the IT Service Desk. Upon further investigation, it was found that 62 colleagues across the Risk Department received the same email over the course of two days.  The emails directed the users to a fake website to steal their usernames and passwords and download a harmful program.
- 3:50 p.m. – The IT Service Desk receives calls and emails from more colleagues that the file-shares are not opening and they receive an error when trying to open a Word document they have always been able to open.


### Steps
In addition to the background information above, study the links in the Resources to learn how to provide solutions to the following questions. Answer the questions in the text input below.

_**Hint:** From the links below, you should look for types of cyber security attacks and the steps to take after an incident._

1. What kind of attack has happened and why do you think so?
2. As a cyber security analyst, what are the next steps to take? List all that apply.
3. How would you contain, resolve and recover from this incident? List all answers that apply.
4. What activities should be performed post-incident?

_Please note that the scenario described in this module is fictional and was created just for your virtual experience._

1. [Top 10 Common types of Cybersecurity Attacks (infocyte.com)](https://www.datto.com/blog/cybersecurity-101-intro-to-the-top-10-common-types-of-cybersecurity-attacks)
2. [11 Types of Phishing + Real-Life Examples (pandasecurity.com)](https://www.pandasecurity.com/en/mediacenter/tips/types-of-phishing/)
3. [8 Critical steps to take after a ransomware attack: Ransomware response guide for businesses - Emsisoft | Security Blog](https://blog.emsisoft.com/en/36921/8-critical-steps-to-take-after-a-ransomware-attack-ransomware-response-guide-for-businesses/)
4. [Battling Ransomware: How to Respond to a Ransomware Incident (forbes.com)](https://www.forbes.com/sites/forbestechcouncil/2018/12/27/battling-ransomware-how-to-respond-to-a-ransomware-incident/?sh=b464b4864dc6)
5. [Frequently Asked Questions - Ransomware | Information Security Office (berkeley.edu)](https://security.berkeley.edu/faq/ransomware/)
6. [What to do before and after a cybersecurity breach? | american.edu](https://www.american.edu/kogod/research/cybergov/upload/what-to-do.pdf)

Report:
The cyber attack was carried out through a  spear phishing email that spread to other accounts, combined with malware that propagated via a link. The reason behind this is that spear phishing emails are typically sent to many targeted accounts. They use strong social engineering techniques to trick users into believing they are from legitimate sources. In this scenario, the phishing email used the company "timesheet" (very directed) and the excuse that they needed to be filled out to trick users into clicking the link, which then directed them to a website to steal their passwords. Once the link was clicked, it also downloaded malware that made it impossible to use file shares and Word documents.

